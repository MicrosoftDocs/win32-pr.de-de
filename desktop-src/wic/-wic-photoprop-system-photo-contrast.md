---
description: Die fotometadatenrichtlinie für die System. Photo. Contrast-Eigenschaft.
ms.assetid: c5e2589d-507c-4b92-9ada-7d64e7c45dd8
title: System. Photo. Contrast Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d6ed34854b525e9eaac2ff5ac7339a75ad10e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530263"
---
# <a name="systemphotocontrast-photo-metadata-policy"></a>System. Photo. Contrast Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Photo. Contrast](../properties/props-system-photo-contrast.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Kontrast zum pkey- \_ Foto \_

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ UI4

### <a name="input-type"></a>Eingabetyp

UShort

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 41992} | ushort      |
| 2     | /XMP/EXIF: Kontrast            | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 41992} | ushort      |
| 2     | /XMP/EXIF: Kontrast            | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 41992} |
| 2     | /XMP/EXIF: Kontrast            |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                     | Datenträger Format |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 41992} | ushort      |
| 2     | /IFD/XMP/EXIF: Kontrast   | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                     | Datenträger Format |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 41992} | ushort      |
| 2     | /IFD/XMP/EXIF: Kontrast   | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                     |
|-------|--------------------------|
| 1     | /IFD/EXIF/{ushort = 41992} |
| 2     | /IFD/XMP/EXIF: Kontrast   |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Photo. Kontrast](../properties/props-system-photo-contrast.md)
</dt> </dl>

 

 
