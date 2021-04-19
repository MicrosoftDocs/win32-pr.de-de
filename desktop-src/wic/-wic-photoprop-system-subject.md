---
description: Die fotometadatenrichtlinie für die System. Subject-Eigenschaft.
ms.assetid: 5ab7c74b-8a5e-4329-8a49-291470d406cc
title: System. Subject Photo Metadata-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceabbab95a52a1155db949dbc60b4525dd5f9d73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364118"
---
# <a name="systemsubject-photo-metadata-policy"></a>System. Subject Photo Metadata-Richtlinie

Die fotometadatenrichtlinie für die [System. Subject](../properties/props-system-subject.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Betreff

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Eingabe-PROPVARIANT-Typ

Entweder VT \_ LPWSTR oder VT \_ LPWSTR

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                     | Datenträger Format    |
|-------|--------------------------|----------------|
| 1     | /App1/IFD/{ushort = 40095} | Unicode- \_ Bytes |
| 2     | /App1/IFD/{ushort = 270}   | ascii          |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                     | Datenträger Format    |
|-------|--------------------------|----------------|
| 1     | /App1/IFD/{ushort = 40095} | Unicode- \_ Bytes |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                     |
|-------|--------------------------|
| 1     | /App1/IFD/{ushort = 40095} |
| 2     | /App1/IFD/{ushort = 270}   |



 

### <a name="tiff-policy"></a>TIFF-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                | Datenträger Format    |
|-------|---------------------|----------------|
| 1     | /IFD/{ushort = 40095} | Unicode- \_ Bytes |
| 2     | /IFD/{ushort = 270}   | ascii          |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                | Datenträger Format    |
|-------|---------------------|----------------|
| 1     | /IFD/{ushort = 40095} | Unicode- \_ Bytes |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                |
|-------|---------------------|
| 1     | /IFD/{ushort = 40095} |
| 2     | /IFD/{ushort = 270}   |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Subject](../properties/props-system-subject.md)
</dt> </dl>

 

 
