---
description: Die fotometadatenrichtlinie für die System. GPS. altituderef-Eigenschaft.
ms.assetid: abbb2441-25ca-484b-a744-620ff2794221
title: System. GPS. altituderef-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db600d218d72014c49fd3f0a8b5eb11dd4c467d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355374"
---
# <a name="systemgpsaltituderef-photo-metadata-policy"></a>System. GPS. altituderef-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. GPS. altituderef](../properties/props-system-gps-altituderef.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey \_ GPS \_ altituderef

### <a name="description"></a>BESCHREIBUNG

Gibt die als Bezugs Höhe verwendete Höhe an. Der Wert 0 gibt an, dass die Höhe oberhalb der sebene liegt. Der Wert 1 gibt eine Höhe unterhalb der sebene an.

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ UI1

### <a name="input-type"></a>Eingabetyp

Hobby.

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policies"></a>JPEG-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                     | Datenträger Format |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 5} | byte        |
| 2     | /XMP/EXIF: gpsaltituderef | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                     | Datenträger Format |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 5} | byte        |
| 2     | /XMP/EXIF: gpsaltituderef | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                     |
|-------|--------------------------|
| 1     | /App1/IFD/GPS/{ushort = 5} |
| 2     | /XMP/EXIF: gpsaltituderef |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                         | Datenträger Format |
|-------|------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 5}          | byte        |
| 2     | /IFD/XMP/EXIF: gpsaltituderef | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                         | Datenträger Format |
|-------|------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 5}          | byte        |
| 2     | /IFD/XMP/EXIF: gpsaltituderef | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                         |
|-------|------------------------------|
| 1     | /IFD/GPS/{ushort = 5}          |
| 2     | /IFD/XMP/EXIF: gpsaltituderef |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. GPS. altituderef](../properties/props-system-gps-altituderef.md)
</dt> </dl>

 

 
