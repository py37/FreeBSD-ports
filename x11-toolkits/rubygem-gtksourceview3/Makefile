# $FreeBSD$

PORTNAME=	gtksourceview3
PORTVERSION=	3.3.0
CATEGORIES=	x11-toolkits rubygems
MASTER_SITES=	RG

MAINTAINER=	ruby@FreeBSD.org
COMMENT=	Ruby/GtkSourceView3 is a Ruby binding of gtksourceview-3.x

LICENSE=	LGPL21+

BUILD_DEPENDS=	rubygem-rake>=0:devel/rubygem-rake
RUN_DEPENDS=	rubygem-gobject-introspection>=${PORTVERSION}:devel/rubygem-gobject-introspection \
		rubygem-gtk3>=${PORTVERSION}:x11-toolkits/rubygem-gtk3

USES=		gem gnome
USE_GNOME=	gtksourceview3
USE_RUBY=	yes

NO_ARCH=	yes

.include <bsd.port.mk>
