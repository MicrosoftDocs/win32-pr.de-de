---
description: Die fotometadatenrichtlinie für die System. ApplicationName-Eigenschaft.
ms.assetid: bf4b310a-7e63-45c5-a327-2638fb31d676
title: System. ApplicationName Photo Metadata-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e36fac2a864cabfd7c1521d72357d187a8aea50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759505"
---
# <a name="systemapplicationname-photo-metadata-policy"></a>System. ApplicationName Photo Metadata-Richtlinie

Die fotometadatenrichtlinie für die [System. ApplicationName](../properties/props-system-applicationname.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ ApplicationName

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ LPWSTR

### <a name="input-type"></a>Eingabetyp

String

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                                         | Datenträger Format |
|-------|----------------------------------------------|-------------|
|       | /App1/IFD/{ushort = 305}                       | ascii       |
|       | /app13/IRB/8bimiptc/IPTC/Originating-Programm |             |
|       | /XMP/XMP: kreatortool                         | Unicode     |
|       | /XMP/XMP: kreatortool                         | Unicode     |
|       | /XMP/TIFF: Software                           | Unicode     |
|       | /XMP/TIFF: Software                           | Unicode     |
|       | /app13/IRB/8bimiptc/IPTC/Originating-Programm |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                                         | Datenträger Format |
|-------|----------------------------------------------|-------------|
|       | /App1/IFD/{ushort = 305}                       | ascii       |
|       | /XMP/XMP: kreatortool                         | Unicode     |
|       | /XMP/XMP: kreatortool                         | Unicode     |
|       | /XMP/TIFF: Software                           | Unicode     |
|       | /XMP/TIFF: Software                           | Unicode     |
|       | /app13/IRB/8bimiptc/IPTC/Originating-Programm |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                                         |
|-------|----------------------------------------------|
|       | /App1/IFD/{ushort = 305}                       |
|       | /XMP/XMP: kreatortool                         |
|       | /XMP/XMP: kreatortool                         |
|       | /XMP/TIFF: Software                           |
|       | /XMP/TIFF: Software                           |
|       | /app13/IRB/8bimiptc/IPTC/Originating-Programm |



 

### <a name="tiff-policy"></a>TIFF-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                                       | Datenträger Format |
|-------|--------------------------------------------|-------------|
|       | /IFD/{ushort = 305}                          | ascii       |
|       | /IFD/IPTC/Originating-Programm              |             |
|       | /IFD/XMP/XMP: kreatortool                   | Unicode     |
|       | /IFD/XMP/XMP: kreatortool                   | Unicode     |
|       | /IFD/XMP/TIFF: Software                     | Unicode     |
|       | /IFD/XMP/TIFF: Software                     | Unicode     |
|       | /IFD/IPTC/Originating-Programm              |             |
|       | /IFD/IRB/8bimiptc/IPTC/Originating-Programm |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                                       | Datenträger Format |
|-------|--------------------------------------------|-------------|
|       | /IFD/{ushort = 305}                          | ascii       |
|       | /IFD/XMP/XMP: kreatortool                   | Unicode     |
|       | /IFD/XMP/XMP: kreatortool                   | Unicode     |
|       | /IFD/XMP/TIFF: Software                     | Unicode     |
|       | /IFD/XMP/TIFF: Software                     | Unicode     |
|       | /IFD/IPTC/Originating-Programm              |             |
|       | /IFD/IRB/8bimiptc/IPTC/Originating-Programm |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                                       |
|-------|--------------------------------------------|
|       | /IFD/{ushort = 305}                          |
|       | /IFD/XMP/XMP: kreatortool                   |
|       | /IFD/XMP/XMP: kreatortool                   |
|       | /IFD/XMP/TIFF: Software                     |
|       | /IFD/XMP/TIFF: Software                     |
|       | /IFD/IPTC/Originating-Programm              |
|       | /IFD/IRB/8bimiptc/IPTC/Originating-Programm |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. ApplicationName](../properties/props-system-applicationname.md)
</dt> </dl>

 

 
