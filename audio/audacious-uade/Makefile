COMMENT=	UADE plugin for Audacious music player

VERSION=	0.12.4
DISTNAME=	audacious-uade-${VERSION}

CATEGORIES=	audio

HOMEPAGE=	https://github.com/mvtiaine/audacious-uade

# GPLv2+
PERMIT_PACKAGE=	Yes

SITES=	${HOMEPAGE}/releases/download/${VERSION}/
EXTRACT_SUFX=	.tar.bz2

RUN_DEPENDS=	audio/audacious/player
BUILD_DEPENDS+= ${RUN_DEPENDS}
SEPARATE_BUILD=	yes
USE_GMAKE=	Yes
CONFIGURE_STYLE= gnu
CONFIGURE_ARGS=	--enable-plugin-audacious=yes \
				--with-static-stdlibs=no
SUBST_VARS=	VERSION

.include <bsd.port.mk>
