Sample instructions:

	# Build data. This sample is for a small sandbox.
	./generate_data.sh 2 && \
		./load_data.sh 2 dfossouo-1.dfossouo.root.hwx.site:2181:/hbase

	# Edit testhosts to specify the hosts that will run JMeter.
	# Assumes passwordless SSH access.

	# Setup the test environment.
	./build_driver.sh && \
		./setup_testenv.sh

	# Install numpy and scipy
	yum install -y numpy scipy

	# Switch into the directory for running tests
	cd runner
	# Run various styles of queries providing the JMX "scenario"
	./RunPointStyle.sh jmeter_tests/Point_NoJoin_NoGroup_Pri1.jmx
