PORTNAME=	xlibre-xf86-video-ati
PORTVERSION=	19.1.0
CATEGORIES=	x11-drivers

MAINTAINER=	b-aazbsd@proton.me
COMMENT=	XLibre ati display driver

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/COPYING

# No Radeon kernel driver on non-x86.
ONLY_FOR_ARCHS=		aarch64 amd64 i386 powerpc64 powerpc64le
ONLY_FOR_ARCHS_REASON=	KMS is required and currently only available on x86/arm64/powerpc64

LIB_DEPENDS=	libpciaccess.so:devel/libpciaccess \
		libdrm_radeon.so:graphics/libdrm

GH_TAGNAME=	d0ddf97
USES=		gl xlibre xlibre-cat:driver
USE_GL=		gl
USE_XORG=	pciaccess

GNU_CONFIGURE_MANPREFIX=${PREFIX}/share
CONFIGURE_ARGS+=--disable-udev

.include <bsd.port.mk>
