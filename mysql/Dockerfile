FROM mysql:8.0

# # 1. Create system user
# RUN adduser -r expense

# # 2. Environment variables for MySQL
ENV MYSQL_ROOT_PASSWORD=ExpenseApp@1 \
    MYSQL_USER=expense \
    MYSQL_PASSWORD=ExpenseApp@1 \
    MYSQL_DATABASE=transactions

# # 3. Give ownership of MySQL directories
# RUN mkdir -p /var/lib/mysql /var/run/mysqld \
#     && chown -R expense:expense /var/lib/mysql /var/run/mysqld

# # 4. Copy initialization scripts
COPY scripts/*.sql /docker-entrypoint-initdb.d/

# # 5. Switch to expense user
# USER expense

# # 6. Use the same MySQL entrypoint
# ENTRYPOINT ["docker-entrypoint.sh"]

# # 7. Default command to start MySQL
# CMD ["mysqld"]
