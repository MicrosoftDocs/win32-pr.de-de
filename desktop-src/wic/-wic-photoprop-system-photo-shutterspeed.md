---
description: Die fotometadatenrichtlinie für die System. Photo. shutterspeed-Eigenschaft.
ms.assetid: f320944c-978d-4a3c-9bf8-5c5652123e29
title: System. Photo. shutterspeed Photo Metadata-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8df8c9e7fda5643fed022f67c3b6b7846e7a72f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363289"
---
# <a name="systemphotoshutterspeed-photo-metadata-policy"></a>System. Photo. shutterspeed Photo Metadata-Richtlinie

Die fotometadatenrichtlinie für die [System. Photo. shutterspeed](../properties/props-system-photo-shutterspeed.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey \_ Photo \_ shutterspeed

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ R8

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Dieser Wert wird von "System. Photo. shutterspeednumerator" und "System. Photo. shutterspeednenner" generiert. Sie kann nicht direkt geschrieben werden. Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 37377} |             |
| 2     | /XMP/EXIF: shutterspeedvalue   |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 37377} |             |
| 2     | /XMP/EXIF: shutterspeedvalue   |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 37377} |
| 2     | /XMP/EXIF: shutterspeedvalue   |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                            | Datenträger Format |
|-------|---------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37377}        |             |
| 2     | /IFD/XMP/EXIF: shutterspeedvalue |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                            | Datenträger Format |
|-------|---------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37377}        |             |
| 2     | /IFD/XMP/EXIF: shutterspeedvalue |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                            |
|-------|---------------------------------|
| 1     | /IFD/EXIF/{ushort = 37377}        |
| 2     | /IFD/XMP/EXIF: shutterspeedvalue |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Photo. shutterspeed](../properties/props-system-photo-shutterspeed.md)
</dt> </dl>

 

 
