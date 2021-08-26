---
description: Eine decoderdefinierte GUID, die das Metadatenformat für räumliche Audiodaten identifiziert und downstream-Komponenten des Metadatenobjekttyps benachrichtigt, die vom Decoder ausgegeben werden.
ms.assetid: 9714A2C7-25A1-4735-A0AC-22329ECBBC46
title: MF_MT_SPATIAL_AUDIO_OBJECT_METADATA_FORMAT_ID -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b43751655f2a583d50c8de3fe108babcaa08d11d78df552b6ddf1f10e413be8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955500"
---
# <a name="mf_mt_spatial_audio_object_metadata_format_id-attribute"></a>MF \_ MT SPATIAL AUDIO OBJECT METADATA FORMAT \_ \_ \_ \_ \_ \_ ID-Attribut

Eine decoderdefinierte GUID, die das Metadatenformat für räumliche Audiodaten identifiziert und downstream-Komponenten des Metadatenobjekttyps benachrichtigt, die vom Decoder ausgegeben werden.

## <a name="data-type"></a>Datentyp

**GUID**

## <a name="remarks"></a>Hinweise

Das Metadatenblob im angegebenen Format wird mithilfe der [**ISpatialAudioMetadataWriter-Schnittstelle**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) geschrieben und mithilfe der [**ISpatialAudioMetadataReader-Schnittstelle**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) gelesen. Das Metadatenblob ist für die Media Foundation und Komponenten nicht transparent. Das -Attribut wird auf den Räumlichen Audiomedientyp angewendet. Wenn eine Downstreamkomponente das von der GUID angegebene Metadatenformat nicht unterstützt, sollte die Komponente den Eingabemedientyp ablehnen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10 Desktop-Apps, Version 1703 \[\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                          |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 
