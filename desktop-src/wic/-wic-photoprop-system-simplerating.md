---
description: Die fotometadatenrichtlinie für die System. simplerating-Eigenschaft.
ms.assetid: d932a251-f238-4582-a1c4-cf4855f26fb3
title: System. simplerating Photo Metadata Policy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63b91e41a0684c8e395992683e0a1d4fe43306a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050292"
---
# <a name="systemsimplerating-photo-metadata-policy"></a>System. simplerating Photo Metadata Policy

Die fotometadatenrichtlinie für die [System. simplerating](../properties/props-system-simplerating.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ simplerating

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ UI4

### <a name="input-propvariant-type"></a>Eingabe-PROPVARIANT-Typ

Kann "VT \_ UI1", "VT \_ UI2" oder "VT UI4" lauten \_ . Der ganzzahlige Wert kann zwischen 0 und 5 liegen.

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                     | Datenträger Format |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/{ushort = 18246} | ushort      |
| 2     | /XMP/XMP: Bewertung          | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                     | Datenträger Format |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/{ushort = 18246} | ushort      |
| 2     | /XMP/XMP: Bewertung          | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                     |
|-------|--------------------------|
| 1     | /App1/IFD/{ushort = 18246} |
| 2     | /XMP/XMP: Bewertung          |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                | Datenträger Format |
|-------|---------------------|-------------|
| 1     | /IFD/{ushort = 18246} | ushort      |
| 2     | /IFD/XMP/XMP: Bewertung | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                | Datenträger Format |
|-------|---------------------|-------------|
| 1     | /IFD/{ushort = 18246} | ushort      |
| 2     | /IFD/XMP/XMP: Bewertung | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                |
|-------|---------------------|
| 1     | /IFD/{ushort = 18246} |
| 2     | /IFD/XMP/XMP: Bewertung |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. simplerating](../properties/props-system-simplerating.md)
</dt> </dl>

 

 
