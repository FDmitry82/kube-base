# kube-base

#Войти в pod
kubectl exec -it mysql-0 -n db /bin/bash

#Войти в БД
mysql -uusername_mysql -pBruCStnMT5 -Ddb_speedtest

#Создать в БазеДанных Таблицу
CREATE TABLE `speedtest_users` (
  `id` int(11) NOT NULL,
  `timestamp` timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP,
  `ip` text NOT NULL,
  `ispinfo` text,
  `extra` text,
  `ua` text NOT NULL,
  `lang` text NOT NULL,
  `dl` text,
  `ul` text,
  `ping` text,
  `jitter` text,
  `log` longtext
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

ALTER TABLE `speedtest_users`
  ADD PRIMARY KEY (`id`);

ALTER TABLE `speedtest_users`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT;COMMIT;

#Смотрим записи
SHOW TABLES;
