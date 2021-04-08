---
description: Die fotometadatenrichtlinie für die System. GPS. destlongitude-Eigenschaft.
ms.assetid: 885a522d-e1bf-43fb-a996-97e725b6cf0c
title: System. GPS. destlongitude-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72e0a4f56e49dfbb3397b96cf7fae35a6065b7aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050302"
---
# <a name="systemgpsdestlongitude-photo-metadata-policy"></a>System. GPS. destlongitude-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. GPS. destlongitude](../properties/props-system-gps-destlongitude.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey \_ GPS \_ destlängen Grade

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ Vector \| VT \_ R8

### <a name="input-propvariant-type"></a>Eingabe-PROPVARIANT-Typ

VT \_ Vector \| VT \_ R8

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Dieser Wert wird von "System. GPS. destlängs denenumerator" und "System. GPS. dest-Debug" generiert. Sie kann nicht direkt geschrieben werden. Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                       | Datenträger Format |
|-------|----------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 22}  |             |
| 2     | /XMP/EXIF: gpsdestlängen Grad |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                       | Datenträger Format |
|-------|----------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 22}  |             |
| 2     | /XMP/EXIF: gpsdestlängen Grad |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                       |
|-------|----------------------------|
| 1     | /App1/IFD/GPS/{ushort = 22}  |
| 2     | /XMP/EXIF: gpsdestlängen Grad |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                           | Datenträger Format |
|-------|--------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 22}           |             |
| 2     | /IFD/XMP/EXIF: gpsdestlängen Grad |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                           | Datenträger Format |
|-------|--------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 22}           |             |
| 2     | /IFD/XMP/EXIF: gpsdestlängen Grad |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                           |
|-------|--------------------------------|
| 1     | /IFD/GPS/{ushort = 22}           |
| 2     | /IFD/XMP/EXIF: gpsdestlängen Grad |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. GPS. destlongitude](../properties/props-system-gps-destlongitude.md)
</dt> </dl>

 

 
