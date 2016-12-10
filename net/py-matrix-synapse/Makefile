# Created by: Brendan Molloy <brendan+freebsd@bbqsrc.net>
# $FreeBSD: head/net/py-matrix-synapse/Makefile 412348 2016-04-01 14:17:44Z mat $

PORTNAME=	matrix-synapse
DISTVERSIONPREFIX=	v
DISTVERSION=	0.18.4
PORTREVISION=	1
CATEGORIES=	net python
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	joe@sigwinch.uk
COMMENT=	Matrix protocol reference homeserver

LICENSE=	APACHE20
LICENSE_FILE=	${WRKSRC}/LICENSE

RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}frozendict>=0.4:devel/py-frozendict \
		${PYTHON_PKGNAMEPREFIX}unpaddedbase64>=1.0.1:devel/py-unpaddedbase64 \
		${PYTHON_PKGNAMEPREFIX}canonicaljson>=1.0.0:devel/py-canonicaljson \
		${PYTHON_PKGNAMEPREFIX}signedjson>=1.0.0:security/py-signedjson \
		${PYTHON_PKGNAMEPREFIX}pynacl>=0.3.0:security/py-pynacl \
		${PYTHON_PKGNAMEPREFIX}service_identity>=1.0.0:security/py-service_identity \
		${PYTHON_PKGNAMEPREFIX}openssl>=0.14:security/py-openssl \
		${PYTHON_PKGNAMEPREFIX}yaml>0:devel/py-yaml \
		${PYTHON_PKGNAMEPREFIX}pyasn1>0:devel/py-pyasn1 \
		${PYTHON_PKGNAMEPREFIX}daemonize>0:devel/py-daemonize \
		${PYTHON_PKGNAMEPREFIX}bcrypt>0:security/py-bcrypt \
		${PYTHON_PKGNAMEPREFIX}pillow>0:graphics/py-pillow \
		${PYTHON_PKGNAMEPREFIX}pydenticon>0:devel/py-pydenticon \
		${PYTHON_PKGNAMEPREFIX}ujson>0:devel/py-ujson \
		${PYTHON_PKGNAMEPREFIX}blist>0:devel/py-blist \
		${PYTHON_PKGNAMEPREFIX}pysaml2>0:security/py-pysaml2 \
		${PYTHON_PKGNAMEPREFIX}pymacaroons-pynacl>0:security/py-pymacaroons-pynacl \
		${PYTHON_PKGNAMEPREFIX}simplejson>dd0:devel/py-simplejson \
		${PYTHON_PKGNAMEPREFIX}sqlite3>0:databases/py-sqlite3 \
		${PYTHON_PKGNAMEPREFIX}matrix-angular-sdk>0:devel/py-matrix-angular-sdk \
		${PYTHON_PKGNAMEPREFIX}msgpack-python>=0.3.0:devel/py-msgpack-python \
		${PYTHON_PKGNAMEPREFIX}matrix-angular-sdk>0:devel/py-matrix-angular-sdk \
		${PYTHON_PKGNAMEPREFIX}netaddr>=0.7.18:net/py-netaddr \
		${PYTHON_PKGNAMEPREFIX}Jinja2>=2.8:devel/py-Jinja2 \
		${PYTHON_PKGNAMEPREFIX}bleach>=1.4.2:www/py-bleach \
		${PYTHON_PKGNAMEPREFIX}ldap3>=1.0:net/py-ldap3 \
		${PYTHON_PKGNAMEPREFIX}psutil>=2.0:sysutils/py-psutil
TEST_DEPENDS=	${PYTHON_PKGNAMEPREFIX}virtualenv>0:devel/py-virtualenv \
		${PYTHON_PKGNAMEPREFIX}tox>0:devel/py-tox

USES=		python:2.7 twisted:conch,names,web
USE_GITHUB=	yes
USE_PYTHON=	autoplist distutils

GH_ACCOUNT=	matrix-org
GH_PROJECT=	synapse

NO_ARCH=	yes

do-test:
	# -epy27 added to skip running python packaging and other dist tests
	@(cd ${WRKSRC} && ${PYTHON_CMD} ${PYDISTUTILS_SETUP} ${TEST_TARGET} \
		-a "-epy27")

.include <bsd.port.mk>
