---
description: Die fotometadatenrichtlinie für die System. Photo. transcodedforsync-Eigenschaft.
ms.assetid: 1869d845-6264-425a-ab3e-e0a9f942961a
title: System. Photo. transcodedforsync Photo-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5884ad469fcf7b5dffc8c4ad14f0ee5ff90cd07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867327"
---
# <a name="systemphototranscodedforsync-photo-metadata-policy"></a>System. Photo. transcodedforsync Photo-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Photo. transcodedforsync](../properties/props-system-photo-transcodedforsync.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Foto \_ transcodedforsync

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ bool

### <a name="input-type"></a>Eingabetyp

Boolesch.

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                                  | Datenträger Format  |
|-------|---------------------------------------|--------------|
| 1     | /App1/IFD/{ushort = 18248}              | bool \_ UShort |
| 2     | /XMP/MicrosoftPhoto: transcodedforsync |              |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                                  | Datenträger Format  |
|-------|---------------------------------------|--------------|
| 1     | /App1/IFD/{ushort = 18248}              | bool \_ UShort |
| 2     | /XMP/MicrosoftPhoto: transcodedforsync |              |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                                  |
|-------|---------------------------------------|
| 1     | /App1/IFD/{ushort = 18248}              |
| 2     | /XMP/microsoftphoto: transcodedforsync |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                                      | Datenträger Format  |
|-------|-------------------------------------------|--------------|
| 1     | /IFD/{ushort = 18248}                       | bool \_ UShort |
| 2     | /IFD/XMP/MicrosoftPhoto: transcodedforsync |              |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                                      | Datenträger Format  |
|-------|-------------------------------------------|--------------|
| 1     | /IFD/{ushort = 18248}                       | bool \_ UShort |
| 2     | /IFD/XMP/MicrosoftPhoto: transcodedforsync |              |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                                      |
|-------|-------------------------------------------|
| 1     | /IFD/{ushort = 18248}                       |
| 2     | /IFD/XMP/microsoftphoto: transcodedforsync |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Photo. transcodedforsync](../properties/props-system-photo-transcodedforsync.md)
</dt> </dl>

 

 
