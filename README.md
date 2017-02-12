jinen
====

[工房じねんWebサイト](http://jinen.hokkaido.jp/)の開発環境。

Table of Contents
----
- [Features](#features)
- [Requirement](#requirement)
	- [Docker](#docker)
- [Usage](#usage)
	- [1. .env](#1-env)
	- [2. docker-compose up](#2-docker-compose-up)
	- [3. docker-compose stop](#3-docker-compose-stop)
- [Goal](#goal)
- [Misc.](#misc)

## Features
(T.B.D.)

## Requirement

### Docker
- Dockerのインストール
    - `$ brew cask install docker`
- Docker-Composeのインストール
    - `$ brew install docker-compose`

## Usage
### 1. .env
`docker/env.sample` を参考に、 `docker/.env` を作成する。

### 2. docker-compose up
`docker` ディレクトリで、 `$ docker-compose up -d` する。

### 3. docker-compose stop
開発を終了する際、 `$ docker-compose stop` する。

## Goal
- WordPress環境の自動構築
- 問い合わせフォーム内のコピー&ペースト禁止
- バックアップの最適化
- 軽快な状態の維持

## Misc.
(T.B.D.)
