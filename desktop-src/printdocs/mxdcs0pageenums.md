---
description: Die MXDC S0 PAGE ENUMS-Enumeration wird verwendet, um Ressourcentypen anzugeben, die Seiten in XPS-Dokumenten zugeordnet werden können und die vom \_ \_ Microsoft XPS Document Converter (MXDC) an die Ausgabe verarbeitet oder nicht verarbeitet übergeben werden \_ können.
ms.assetid: e111d92e-5102-4b39-b311-f9ff1d1a96f1
title: MXDC_S0_PAGE_ENUMS -Enumeration (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0_PAGE_ENUMS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 3aa6622ea65e00c1447e6042a41c998e9ab30a29d1172d43e1a1da81feb34c54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118471315"
---
# <a name="mxdc_s0_page_enums-enumeration"></a>MXDC \_ S0 \_ PAGE \_ ENUMS-Enumeration

Die **MXDC \_ S0 \_ PAGE \_ ENUMS-Enumeration** wird verwendet, um Ressourcentypen anzugeben, die Seiten in XPS-Dokumenten zugeordnet werden können und die vom Microsoft XPS Document Converter (MXDC) an die Ausgabe verarbeitet oder nicht verarbeitet übergeben werden können.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMxdcS0PageEnums { 
  MXDC_RESOURCE_TTF,
  MXDC_RESOURCE_JPEG,
  MXDC_RESOURCE_PNG,
  MXDC_RESOURCE_TIFF,
  MXDC_RESOURCE_WDP,
  MXDC_RESOURCE_DICTIONARY,
  MXDC_RESOURCE_ICC_PROFILE,
  MXDC_RESOURCE_JPEG_THUMBNAIL,
  MXDC_RESOURCE_PNG_THUMBNAIL,
  MXDC_RESOURCE_MAX
} MXDC_S0_PAGE_ENUMS;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="MXDC_RESOURCE_TTF"></span><span id="mxdc_resource_ttf"></span>**MXDC \_ RESOURCE \_ TTF**
</dt> <dd>

TrueType- oder OpenType-Schriftart.

</dd> <dt>

<span id="MXDC_RESOURCE_JPEG"></span><span id="mxdc_resource_jpeg"></span>**MXDC \_ RESOURCE \_ JPEG**
</dt> <dd>

JPEG-Bild

</dd> <dt>

<span id="MXDC_RESOURCE_PNG"></span><span id="mxdc_resource_png"></span>**MXDC \_ RESOURCE \_ PNG**
</dt> <dd>

PNG-Bild.

</dd> <dt>

<span id="MXDC_RESOURCE_TIFF"></span><span id="mxdc_resource_tiff"></span>**MXDC \_ RESOURCE \_ TIFF**
</dt> <dd>

TIFF-Image.

</dd> <dt>

<span id="MXDC_RESOURCE_WDP"></span><span id="mxdc_resource_wdp"></span>**MXDC \_ RESOURCE \_ WDP**
</dt> <dd>

Windows Medienfotobild.

</dd> <dt>

<span id="MXDC_RESOURCE_DICTIONARY"></span><span id="mxdc_resource_dictionary"></span>**MXDC \_ RESOURCE \_ DICTIONARY**
</dt> <dd>

Remoteressourcenverzeichnis, das nicht verarbeitet an die MXDC-Ausgabe übergeben werden soll.

</dd> <dt>

<span id="MXDC_RESOURCE_ICC_PROFILE"></span><span id="mxdc_resource_icc_profile"></span>**MXDC \_ \_ RESOURCEÄTSPROFIL \_**
</dt> <dd>

DAS PROFIL, das nicht verarbeitet an die MXDC-Ausgabe übergeben werden soll.

</dd> <dt>

<span id="MXDC_RESOURCE_JPEG_THUMBNAIL"></span><span id="mxdc_resource_jpeg_thumbnail"></span>**JPEG-MINIATURANSICHT \_ DER MXDC-RESSOURCE \_ \_**
</dt> <dd>

JPEG-Miniaturansicht, die nicht verarbeitet an die MXDC-Ausgabe übergeben werden soll.

</dd> <dt>

<span id="MXDC_RESOURCE_PNG_THUMBNAIL"></span><span id="mxdc_resource_png_thumbnail"></span>**PNG-MINIATURANSICHT \_ DER MXDC-RESSOURCE \_ \_**
</dt> <dd>

PNG-Miniaturansicht, die nicht verarbeitet an die MXDC-Ausgabe übergeben werden soll.

</dd> <dt>

<span id="MXDC_RESOURCE_MAX"></span><span id="mxdc_resource_max"></span>**MXDC \_ RESOURCE \_ MAX**
</dt> <dd>

Die maximale Ressourcenanzahl für die Validierung.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Enumeration wird hauptsächlich als **dwResourceType-Member** der [**MXDC \_ XPS \_ S0PAGE \_ RESOURCE \_ T-Struktur**](mxdcxpss0pageresource.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |



 

 




