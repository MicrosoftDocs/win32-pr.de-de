---
description: Die fotometadatenrichtlinie für die System. Photo. cameramanufakturer-Eigenschaft.
ms.assetid: 6710161c-4835-4385-9d4c-566acc000925
title: System. Photo. cameramanufakturer Photo Metadata-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1d2765b6c787b7d7ad421300f1c3492669830b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364192"
---
# <a name="systemphotocameramanufacturer-photo-metadata-policy"></a>System. Photo. cameramanufakturer Photo Metadata-Richtlinie

Die fotometadatenrichtlinie für die [System. Photo. cameramanufakturer](../properties/props-system-photo-cameramanufacturer.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Foto \_ cameramanufakturer

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



| Auftrag | Pfad                   | Datenträger Format |
|-------|------------------------|-------------|
| 1     | /App1/IFD/{ushort = 271} | ascii       |
| 2     | /XMP/TIFF: Erstellen         | Unicode     |
| 3     | /XMP/TIFF: Erstellen         | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                   | Datenträger Format |
|-------|------------------------|-------------|
| 1     | /App1/IFD/{ushort = 271} | ascii       |
| 2     | /XMP/TIFF: Erstellen         | Unicode     |
| 3     | /XMP/TIFF: Erstellen         | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                   |
|-------|------------------------|
| 1     | /App1/IFD/{ushort = 271} |
| 2     | /XMP/TIFF: Erstellen         |
| 3     | /XMP/TIFF: Erstellen         |



 

### <a name="tiff-policy"></a>TIFF-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad               | Datenträger Format |
|-------|--------------------|-------------|
| 1     | /IFD/{ushort = 271}  | ascii       |
| 2     | /IFD/XMP/TIFF: Erstellen | Unicode     |
| 3     | /IFD/XMP/TIFF: Erstellen | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad               | Datenträger Format |
|-------|--------------------|-------------|
| 1     | /IFD/{ushort = 271}  | ascii       |
| 2     | /IFD/XMP/TIFF: Erstellen | Unicode     |
| 3     | /IFD/XMP/TIFF: Erstellen | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad               |
|-------|--------------------|
| 1     | /IFD/{ushort = 271}  |
| 2     | /IFD/XMP/TIFF: Erstellen |
| 3     | /IFD/XMP/TIFF: Erstellen |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Photo. cameramanufakturer](../properties/props-system-photo-cameramanufacturer.md)
</dt> </dl>

 

 
