---
description: Die Enumeration "mxdc \_ S0 \_ Page \_ Enums" wird verwendet, um Typen von Ressourcen anzugeben, die Seiten in XPS-Dokumenten zugeordnet werden können und die von Microsoft XPS Document Converter (mxdc) an Ihre Ausgabe verarbeitet bzw. nicht verarbeitet werden können.
ms.assetid: e111d92e-5102-4b39-b311-f9ff1d1a96f1
title: MXDC_S0_PAGE_ENUMS-Enumeration (winspool. h)
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
ms.openlocfilehash: 1b4331210027f7fc23f36fb6b9d13a2c232ccbf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864959"
---
# <a name="mxdc_s0_page_enums-enumeration"></a>Mxdc \_ S0 \_ - \_ Enumeration für Seiten Enumeration

Die Enumeration " **mxdc \_ S0 \_ Page \_ Enums** " wird verwendet, um Typen von Ressourcen anzugeben, die Seiten in XPS-Dokumenten zugeordnet werden können und die von Microsoft XPS Document Converter (mxdc) an Ihre Ausgabe verarbeitet bzw. nicht verarbeitet werden können.

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

<span id="MXDC_RESOURCE_TTF"></span><span id="mxdc_resource_ttf"></span>**mxdc- \_ Ressource \_ ttf**
</dt> <dd>

TrueType-oder OpenType-Schriftart.

</dd> <dt>

<span id="MXDC_RESOURCE_JPEG"></span><span id="mxdc_resource_jpeg"></span>**mxdc- \_ Ressource \_ JPEG**
</dt> <dd>

JPEG-Bild

</dd> <dt>

<span id="MXDC_RESOURCE_PNG"></span><span id="mxdc_resource_png"></span>**mxdc- \_ Ressource \_ PNG**
</dt> <dd>

PNG-Bild

</dd> <dt>

<span id="MXDC_RESOURCE_TIFF"></span><span id="mxdc_resource_tiff"></span>**mxdc- \_ Ressource \_ TIFF**
</dt> <dd>

TIFF-Bild

</dd> <dt>

<span id="MXDC_RESOURCE_WDP"></span><span id="mxdc_resource_wdp"></span>**mxdc- \_ Ressource ( \_ WDP)**
</dt> <dd>

Bild für Windows Media-Foto.

</dd> <dt>

<span id="MXDC_RESOURCE_DICTIONARY"></span><span id="mxdc_resource_dictionary"></span>**mxdc- \_ Ressourcen \_ Wörterbuch**
</dt> <dd>

Das Remote Ressourcen Wörterbuch, das an die nicht verarbeitete Ausgabe von mxdc weitergeleitet werden soll.

</dd> <dt>

<span id="MXDC_RESOURCE_ICC_PROFILE"></span><span id="mxdc_resource_icc_profile"></span>**mxdc- \_ Ressourcen- \_ ICC- \_ Profil**
</dt> <dd>

Das ICC-Profil, das an die nicht verarbeitete Ausgabe von mxdc übermittelt werden soll.

</dd> <dt>

<span id="MXDC_RESOURCE_JPEG_THUMBNAIL"></span><span id="mxdc_resource_jpeg_thumbnail"></span>**mxdc- \_ Ressource \_ JPEG- \_ Miniaturansicht**
</dt> <dd>

JPEG-Miniaturansicht, die an die nicht verarbeitete Ausgabe von mxdc übermittelt werden soll.

</dd> <dt>

<span id="MXDC_RESOURCE_PNG_THUMBNAIL"></span><span id="mxdc_resource_png_thumbnail"></span>**mxdc- \_ Ressource \_ PNG- \_ Miniaturansicht**
</dt> <dd>

PNG-Miniaturansicht, die an die nicht verarbeitete Ausgabe von mxdc übermittelt werden soll.

</dd> <dt>

<span id="MXDC_RESOURCE_MAX"></span><span id="mxdc_resource_max"></span>**mxdc- \_ Ressource \_ Max**
</dt> <dd>

Die maximale Ressourcen Anzahl für die Überprüfung.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Enumeration wird hauptsächlich als **dwresourcetype** -Member der [**mxdc \_ XPS \_ S0PAGE \_ Resource \_ T**](mxdcxpss0pageresource.md) -Struktur verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |



 

 




