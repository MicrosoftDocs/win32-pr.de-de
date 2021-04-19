---
description: Die fotometadatenrichtlinie für die System. Photo. exposurebias-Eigenschaft.
ms.assetid: 00ebe037-0116-4d75-868b-d75b3e58a84d
title: System. Photo. exposurebias-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 709aa21da7cec56d36b5de643681a592873717bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360659"
---
# <a name="systemphotoexposurebias-photo-metadata-policy"></a>System. Photo. exposurebias-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Photo. exposurebias](../properties/props-system-photo-exposurebias.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Foto \_ exposurebias

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ R8

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Dieser Wert wird von "System. Photo. exposurebiasnumerator" und "System. Photo. exposurebiasnenner" generiert. Sie kann nicht direkt geschrieben werden. Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 37380} |             |
| 2     | /XMP/EXIF: ExposureBiasValue   |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 37380} |             |
| 2     | /XMP/EXIF: ExposureBiasValue   |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 37380} |
| 2     | /XMP/EXIF: ExposureBiasValue   |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                            | Datenträger Format |
|-------|---------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37380}        |             |
| 2     | /IFD/XMP/EXIF: ExposureBiasValue |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                            | Datenträger Format |
|-------|---------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37380}        |             |
| 2     | /IFD/XMP/EXIF: ExposureBiasValue |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                            |
|-------|---------------------------------|
| 1     | /IFD/EXIF/{ushort = 37380}        |
| 2     | /IFD/XMP/EXIF: ExposureBiasValue |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Photo. exposurebias](../properties/props-system-photo-exposurebias.md)
</dt> </dl>

 

 
