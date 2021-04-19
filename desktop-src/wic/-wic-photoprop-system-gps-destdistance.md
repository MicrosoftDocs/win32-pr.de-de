---
description: Die fotometadatenrichtlinie für die System. GPS. destdistance-Eigenschaft.
ms.assetid: 1bd72acb-f462-454d-aec2-72d5b4517de3
title: System. GPS. destdistance-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecc71c89ae6270f5babf08637f54baaf2cb57aae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363573"
---
# <a name="systemgpsdestdistance-photo-metadata-policy"></a>System. GPS. destdistance-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. GPS. destdistance](../properties/props-system-gps-destdistance.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey \_ GPS \_ destdistance

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ R8

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Dieser Wert wird von System. GPS. destdistancenenumerator und System. GPS. destdistancenenner generiert. Sie kann nicht direkt geschrieben werden. Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 26} |             |
| 2     | /XMP/EXIF: gpsdestdistance |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 26} |             |
| 2     | /XMP/EXIF: gpsdestdistance |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                      |
|-------|---------------------------|
| 1     | /App1/IFD/GPS/{ushort = 26} |
| 2     | /XMP/EXIF: gpsdestdistance |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 26}          |             |
| 2     | /IFD/XMP/EXIF: gpsdestdistance |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 26}          |             |
| 2     | /IFD/XMP/EXIF: gpsdestdistance |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /IFD/GPS/{ushort = 26}          |
| 2     | /IFD/XMP/EXIF: gpsdestdistance |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. GPS. destdistance](../properties/props-system-gps-destdistance.md)
</dt> </dl>

 

 
