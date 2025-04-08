COMMENT=	UADE plugin for Audacious and DeaDBeeF

VERSION=	0.13.1
DISTNAME=	audacious-uade-${VERSION}

CATEGORIES=	audio

HOMEPAGE=	https://github.com/mvtiaine/audacious-uade

# GPLv2+
PERMIT_PACKAGE=	Yes

SITES=	${HOMEPAGE}/releases/download/${VERSION}/
EXTRACT_SUFX=	.tar.bz2

# TODO DeaDBeeF support does not work, needs separate deadbeef option for PLIST
# install audio/deadbeef for DeaDBeeF plugin support
RUN_DEPENDS=	audio/audacious/player
LIB_DEPENDS=	audio/libopenmpt \
                audio/libxmp
WANTLIB+=	openmpt xmp
BUILD_DEPENDS+= ${RUN_DEPENDS}
SEPARATE_BUILD=	yes
USE_GMAKE=	Yes
CONFIGURE_STYLE= gnu
# needed for DeaDBeeF support
#CONFIGURE_ENV=	CPPFLAGS="-isystem${PREFIX}/include"
CONFIGURE_ARGS=	--enable-players=all \
                --enable-plugin-audacious=yes \
                --enable-plugin-deadbeef=no \
                --with-static-stdlibs=no
SUBST_VARS=	VERSION

.include <bsd.port.mk>
