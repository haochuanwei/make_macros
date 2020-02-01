TEST_MODULE_PATH=./<my_package>

clean:
	@echo "Cleaning package build files.."
	@rm -rf build
	@rm -rf dist
	@rm -rf *.egg-info
	@echo "Done."
publish:
	@echo "Publishing to PyPI.."
	@python setup.py sdist bdist_wheel
	@twine check dist/*
	@twine upload dist/*
	@echo "Done."
coverage:
	@coverage run --source=$(TEST_MODULE_PATH) -m pytest
	@coverage report -m
