# Implement-Automatic-Log-File-Deletion-in-Laravel

In order to prevent excessive storage usage and manage the size of our logs, we should implement automatic log file deletion in our Laravel application.

This can be achieved by using Laravel's built-in feature for log rotation, which automatically deletes logs older than a certain number of days.

Here is a sample code snippet that can be used in the config/logging.php file:

```
'channels' => [
    'daily' => [
        'driver' => 'daily',
        'path' => storage_path('logs/laravel.log'),
        'level' => 'debug',
        'days' => 14, // number of days to retain the log files
    ],
],
```
This configuration will ensure that log files older than 14 days will automatically be deleted.

URL:

N/A - This is an internal enhancement and does not involve any external URL.

Tasks:

 Update the config/logging.php file to include the daily driver with 14 days retention.
 Test to ensure that logs older than 14 days are being deleted correctly.
 Update the documentation to reflect these changes.
