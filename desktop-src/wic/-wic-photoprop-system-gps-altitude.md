---
description: Die fotometadatenrichtlinie für die System. GPS. Altitude-Eigenschaft.
ms.assetid: 63d59aa3-52a6-4b6f-b6ec-a1c4abcee83f
title: System. GPS. Altitude-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 003d39d135c625a01035c023b5d7dc8d890b3b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357022"
---
# <a name="systemgpsaltitude-photo-metadata-policy"></a>System. GPS. Altitude-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. GPS. Altitude](../properties/props-system-gps-altitude.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey \_ GPS- \_ Höhe

### <a name="description"></a>BESCHREIBUNG

Die Höhe wird als absoluter Wert angegeben, auf den in Meter verwiesen wird.

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ R8

### <a name="input-propvariant-type"></a>Eingabe-PROPVARIANT-Typ

VT \_ R8

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Dieser Wert kann durch Schreiben in "System. GPS. Altitude. Numerator" und "System. GPS. Altitude. Nenner" geschrieben werden. Sie kann nicht direkt geschrieben werden. Die Schreib Pfade in den folgenden Tabellen geben an, wo der Wert möglicherweise beim Generieren gespeichert wird, nicht, wenn er direkt geschrieben wird. Wenn der Wert gelesen wird, werden Werte aus unterschiedlichen Schemas abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                     | Datenträger Format |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 6} |             |
| 2     | /XMP/EXIF: gpsaltitude    |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                     | Datenträger Format |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 6} |             |
| 2     | /XMP/EXIF: gpsaltitude    |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                     |
|-------|--------------------------|
| 1     | /App1/IFD/GPS/{ushort = 6} |
| 2     | /XMP/EXIF: gpsaltitude    |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 6}       |             |
| 2     | /IFD/XMP/EXIF: gpsaltitude |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 6}       |             |
| 2     | /IFD/XMP/EXIF: gpsaltitude |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                      |     |
|-------|---------------------------|-----|
| 1     | /IFD/GPS/{ushort = 6}       |     |
| 2     | /IFD/XMP/EXIF: gpsaltitude |     |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. GPS. Altitude](../properties/props-system-gps-altitude.md)
</dt> </dl>

 

 
