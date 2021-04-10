---
description: Die fotometadatenrichtlinie für die System. Photo. relatedsound File-Eigenschaft.
ms.assetid: 3b212d90-7ae2-4b7c-b77a-2017490aca40
title: System. Photo. relatedsound File-fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07a29adb71f572868f21b1b8427e71b09616b24c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960363"
---
# <a name="systemphotorelatedsoundfile-photo-metadata-policy"></a>System. Photo. relatedsound File-fotometadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Photo. relatedsound File](../properties/props-system-photo-relatedsoundfile.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Foto \_ relatedsound file

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ LPWSTR

### <a name="input-type"></a>Eingabetyp

Eine Zeichenfolge.

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 40964} | ascii       |
| 2     | /XMP/EXIF: relatedsoundfile    | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 40964} | ascii       |
| 2     | /XMP/EXIF: relatedsoundfile    | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 40964} |
| 2     | /XMP/EXIF: relatedsoundfile    |



 

### <a name="tiff-policy"></a>TIFF-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                           | Datenträger Format |
|-------|--------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 40964}       | ascii       |
| 2     | /IFD/XMP/EXIF: relatedsoundfile | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                           | Datenträger Format |
|-------|--------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 40964}       | ascii       |
| 2     | /IFD/XMP/EXIF: relatedsoundfile | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                           |
|-------|--------------------------------|
| 1     | /IFD/EXIF/{ushort = 40964}       |
| 2     | /IFD/XMP/EXIF: relatedsoundfile |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Photo. relatedsound file](../properties/props-system-photo-relatedsoundfile.md)
</dt> </dl>

 

 
