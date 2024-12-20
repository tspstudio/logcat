# Logcat - a simple, lightweight logging library
Logcat is simple logging library written in Rust
## Usage
```rust
use logcat::logger::Logger;
fn main() {
	// Creating logging class
	let mut logger = Logger::new(String::from("output/log/filename.txt"));
	// Logging
	logger.info(String::from("This is info!"));
	logger.warning(String::from("This is warning!"));
	logger.error(String::from("This is error!"));
	logger.custom(String::from("CUSTOM"), String::from("This is custom log!"));
	logger.export(); // Will export all logs with timestamp.
	logger.critical(String::from("This is critical error! Program will export logs and exit with code -1!"));
}

```
Output:
```
[INFO] 14:42:29 >> This is info!
[WARNING] 14:42:29 >> This is warning!
[ERROR] 14:42:29 >> This is error!
[CUSTOM] 14:42:29 >> This is custom log!
[INFO] 14:42:29 >> Log exported successfully!
[CRITICAL ERROR] 14:42:29 >> This is critical error! Program will exit with code -1!
[INFO] 14:42:29 >> Log exported successfully!
```
Log file:
```
# Log generated by Logcat v0.0.1
# Exported at 14:42:29

[INFO] 14:42:29 >> This is info!
[WARNING] 14:42:29 >> This is warning!
[ERROR] 14:42:29 >> This is error!
[CUSTOM] 14:42:29 >> This is custom log!
[INFO] 14:42:29 >> Log exported successfully!
[CRITICAL ERROR] 14:42:29 >> This is critical error! Program will exit with code -1!
```

[GitHub](https://github.com/tspstudio/logcat)