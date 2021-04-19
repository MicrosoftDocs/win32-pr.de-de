---
description: Die fotometadatenrichtlinie für die System. GPS. destlatitude-Eigenschaft.
ms.assetid: 05284291-977d-49b8-ad92-365f68384960
title: System. GPS. destlatitude-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192db0f8efc868e9457e86d283d9967e4692c95b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351063"
---
# <a name="systemgpsdestlatitude-photo-metadata-policy"></a>System. GPS. destlatitude-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. GPS. destlatitude](../properties/props-system-gps-destlatitude.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey \_ GPS \_ destlatitude

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ Vector \| VT \_ R8

### <a name="input-propvariant-type"></a>Eingabe-PROPVARIANT-Typ

VT \_ Vector \| VT \_ R8

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Dieser Wert wird von "System. GPS. destlatitudenenumerator" und "System. GPS. destlatitudebug" generiert. Sie kann nicht direkt geschrieben werden. Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 20} |             |
| 2     | /XMP/EXIF: gpsdestlatitude |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 20} |             |
| 2     | /XMP/EXIF: gpsdestlatitude |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                      |
|-------|---------------------------|
| 1     | /App1/IFD/GPS/{ushort = 20} |
| 2     | /XMP/EXIF: gpsdestlatitude |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 20}          |             |
| 2     | /IFD/XMP/EXIF: gpsdestlatitude |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 20}          |             |
| 2     | /IFD/XMP/EXIF: gpsdestlatitude |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /IFD/GPS/{ushort = 20}          |
| 2     | /IFD/XMP/EXIF: gpsdestlatitude |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. GPS. destlatitude](../properties/props-system-gps-destlatitude.md)
</dt> </dl>

 

 
