---
description: Die fotometadatenrichtlinie für die System. Comment-Eigenschaft.
ms.assetid: 02a6ac18-ad69-4880-a267-8330d648c0d9
title: System. Comment-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9d7526e05a72b073ac32bd8286a621b33ee62a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348598"
---
# <a name="systemcomment-photo-metadata-policy"></a>System. Comment-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Comment](../properties/props-system-comment.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Kommentar

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Eingabe-PROPVARIANT-Typ

VT \_ LPWSTR oder VT \_ LPSTR

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                                | Datenträger Format    |
|-------|-------------------------------------|----------------|
| 1     | /App1/IFD/{ushort = 40092}            | Unicode- \_ Bytes |
| 2     | /App1/IFD/{ushort = 37510}            | Unicode        |
| 3     | /XMP/ <xmpalt> EXIF: UserComment | Unicode        |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                     | Datenträger Format    |
|-------|--------------------------|----------------|
| 1     | /App1/IFD/{ushort = 40092} | Unicode- \_ Bytes |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /App1/IFD/{ushort = 40092}      |
| 2     | /App1/IFD/EXIF/{ushort = 37510} |
| 3     | /XMP/EXIF: UserComment         |



 

### <a name="tiff-policy"></a>TIFF-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                                    | Datenträger Format    |
|-------|-----------------------------------------|----------------|
| 1     | /IFD/{ushort = 40092}                     | Unicode- \_ Bytes |
| 2     | /IFD/{ushort = 37510}                     | Unicode        |
| 3     | /IFD/XMP/ <xmpalt> EXIF: UserComment | Unicode        |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                | Datenträger Format    |
|-------|---------------------|----------------|
| 1     | /IFD/{ushort = 40092} | Unicode- \_ Bytes |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                      |
|-------|---------------------------|
| 1     | /IFD/{ushort = 40092}       |
| 2     | /IFD/{ushort = 37510}       |
| 3     | /IFD/XMP/EXIF: UserComment |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Comment](../properties/props-system-comment.md)
</dt> </dl>

 

 
