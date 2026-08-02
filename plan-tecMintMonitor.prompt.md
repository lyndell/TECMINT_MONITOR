Plan for fixing the monitor script:

1. Update the script to avoid unsupported hostname flags on macOS/BSD by using portable fallbacks such as hostname -f, hostname -I, ifconfig, or uname -n.
2. Guard the RAM/SWAP section so it only runs the free command when available, otherwise report that memory usage is unavailable on the current platform.
3. Keep the rest of the script behavior intact while preserving the existing output format as much as possible.
4. Verify the script by running it and confirming that the hostname/free errors no longer appear.
