---
description: Die Fotometadatenrichtlinie für die System.Photo.TranscodedForSync-Eigenschaft.
ms.assetid: 1869d845-6264-425a-ab3e-e0a9f942961a
title: System.Photo.TranscodedForSync-Fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34e78086284e1ca13b01c5e7cd188b761afe7eeba8acb5f2bca103234f80955b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964759"
---
# <a name="systemphototranscodedforsync-photo-metadata-policy"></a>System.Photo.TranscodedForSync-Fotometadatenrichtlinie

Die Fotometadatenrichtlinie für die [System.Photo.TranscodedForSync-Eigenschaft.](../properties/props-system-photo-transcodedforsync.md)

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ TranscodedForSync

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ BOOL

### <a name="input-type"></a>Eingabetyp

Boolesch.

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus unterschiedlichen Schemas werden abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                                  | Datenträgerformat  |
|-------|---------------------------------------|--------------|
| 1     | /app1/ifd/{ushort=18248}              | bool \_ ushort |
| 2     | /xmp/MicrosoftPhoto:TranscodedForSync |              |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                                  | Datenträgerformat  |
|-------|---------------------------------------|--------------|
| 1     | /app1/ifd/{ushort=18248}              | bool \_ ushort |
| 2     | /xmp/MicrosoftPhoto:TranscodedForSync |              |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                                  |
|-------|---------------------------------------|
| 1     | /app1/ifd/{ushort=18248}              |
| 2     | /xmp/microsoftphoto:transcodedforsync |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                                      | Datenträgerformat  |
|-------|-------------------------------------------|--------------|
| 1     | /ifd/{ushort=18248}                       | bool \_ ushort |
| 2     | /ifd/xmp/MicrosoftPhoto:TranscodedForSync |              |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                                      | Datenträgerformat  |
|-------|-------------------------------------------|--------------|
| 1     | /ifd/{ushort=18248}                       | bool \_ ushort |
| 2     | /ifd/xmp/MicrosoftPhoto:TranscodedForSync |              |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                                      |
|-------|-------------------------------------------|
| 1     | /ifd/{ushort=18248}                       |
| 2     | /ifd/xmp/microsoftphoto:transcodedforsync |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Photo.TranscodedForSync](../properties/props-system-photo-transcodedforsync.md)
</dt> </dl>

 

 
