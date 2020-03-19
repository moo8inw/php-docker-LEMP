// Ref Url : https://medium.com/@teamteam/%E0%B8%95%E0%B8%B4%E0%B8%94%E0%B8%95%E0%B8%B1%E0%B9%89%E0%B8%87-wordpress-%E0%B8%9A%E0%B8%99-docker-lemp-stack-b61623ca28e3
// Run docker Compose
1. docker-compose up -d

// ให้ สิทธ์ PHP (user id ของ www-data ใน docker image php:7.0-fpm-alpine คือ 82)
2. chown -R 82:82 www/