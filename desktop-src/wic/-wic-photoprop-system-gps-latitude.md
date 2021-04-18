---
description: Die fotometadatenrichtlinie für die System. GPS. Latitude-Eigenschaft.
ms.assetid: 0f8cea07-da96-4d2a-8444-6073b51e1236
title: System. GPS. Latitude-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5320869c1e8fd0d4b17bb17da455fc939bf44b9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350825"
---
# <a name="systemgpslatitude-photo-metadata-policy"></a>System. GPS. Latitude-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. GPS. Latitude](../properties/props-system-gps-latitude.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey \_ GPS- \_ Breite

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ Vector \| VT \_ R8

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Dieser Wert kann durch Schreiben in "System. GPS. latitudenumerator" und "System. GPS. latitudebug" geschrieben werden. Sie kann nicht direkt geschrieben werden. Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                     | Datenträger Format |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 2} |             |
| 2     | /XMP/EXIF: gpslatitude    |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                     | Datenträger Format |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 2} |             |
| 2     | /XMP/EXIF: gpslatitude    |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                     |
|-------|--------------------------|
| 1     | /App1/IFD/GPS/{ushort = 2} |
| 2     | /XMP/EXIF: gpslatitude    |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 2}       |             |
| 2     | /IFD/XMP/EXIF: gpslatitude |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 2}       |             |
| 2     | /IFD/XMP/EXIF: gpslatitude |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                      |
|-------|---------------------------|
| 1     | /IFD/GPS/{ushort = 2}       |
| 2     | /IFD/XMP/EXIF: gpslatitude |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. GPS. Latitude](../properties/props-system-gps-latitude.md)
</dt> </dl>

 

 
