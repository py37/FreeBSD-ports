# Created by: vanilla@
# $FreeBSD$

PORTNAME=	gcin
PORTVERSION=	2.8.8
CATEGORIES=	chinese textproc gnome
MASTER_SITES=	http://hyperrate.com/gcin-source/
PKGNAMESUFFIX=	-qt4
EXTRACT_ONLY=	gcin-${PORTVERSION}.tar.xz

MAINTAINER=	vanilla@FreeBSD.org
COMMENT=	Traditional Chinese input utility in X

LICENSE=	LGPL21

DEPRECATED=		Qt4 has been EOL since december 2015
EXPIRATION_DATE=	2019-03-15

LIB_DEPENDS=	libgcin-im-client.so:chinese/gcin

WRKSRC=		${WRKDIR}/${PORTNAME}-${PORTVERSION}/qt4-im
USES=		gmake pkgconfig qt:4 tar:xz
USE_QT=		inputmethods qmake_build moc_build corelib gui
MAKE_ENV=	INSTALL_PROGRAM="${INSTALL_PROGRAM}" \
		MKDIR="${MKDIR}"

PLIST_FILES=	%%QT_PLUGINDIR%%/inputmethods/im-gcin.so

post-patch:
	@${REINPLACE_CMD} -e 's,%%PREFIX%%,${PREFIX},g; \
		s,%%MOC%%,${MOC},;' ${WRKSRC}/Makefile

.include <bsd.port.mk>
