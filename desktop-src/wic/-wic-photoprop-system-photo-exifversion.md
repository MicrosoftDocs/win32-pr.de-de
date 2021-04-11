---
description: Die fotometadatenrichtlinie für die System. Photo. EXIF Version-Eigenschaft.
ms.assetid: 0f9c5ea8-918f-4101-8492-3f408145a73e
title: System. Photo. exibversion-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eb823db41cb54a06fba235df5be4bb4acd55ea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217828"
---
# <a name="systemphotoexifversion-photo-metadata-policy"></a>System. Photo. exibversion-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Photo. EXIF Version](../properties/props-system-photo-exifversion.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Foto- \_ EXIF-Version

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



| Auftrag | Pfad                          | Datenträger Format   |
|-------|-------------------------------|---------------|
| 1     | /App1/IFD/EXIF/{ushort = 36864} | EXIF- \_ Version |
| 2     | /XMP/EXIF: EXIF-Version         | Unicode       |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                          | Datenträger Format   |
|-------|-------------------------------|---------------|
| 1     | /App1/IFD/EXIF/{ushort = 36864} | EXIF- \_ Version |
| 2     | /XMP/EXIF: EXIF-Version         | Unicode       |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 36864} |
| 2     | /XMP/EXIF: EXIF-Version         |



 

### <a name="tiff-policy"></a>TIFF-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                      | Datenträger Format   |
|-------|---------------------------|---------------|
| 1     | /IFD/EXIF/{ushort = 36864}  | EXIF- \_ Version |
| 2     | /IFD/XMP/EXIF: EXIF-Version | Unicode       |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                      | Datenträger Format   |
|-------|---------------------------|---------------|
| 1     | /IFD/EXIF/{ushort = 36864}  | EXIF- \_ Version |
| 2     | /IFD/XMP/EXIF: EXIF-Version | Unicode       |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                      |
|-------|---------------------------|
| 1     | /IFD/EXIF/{ushort = 36864}  |
| 2     | /IFD/XMP/EXIF: EXIF-Version |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Photo. EXIF Version](../properties/props-system-photo-exifversion.md)
</dt> </dl>

 

 
