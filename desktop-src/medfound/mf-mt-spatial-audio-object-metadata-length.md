---
description: Ein -Wert, der die Größe des Objekttyps räumlicher Audiometadaten in Bytes angibt, die der Decoder ausgibt.
ms.assetid: C133693D-A8D5-4520-B561-57BF11074257
title: MF_MT_SPATIAL_AUDIO_OBJECT_METADATA_LENGTH -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 784e1b210b616f4c42c2c3d410a207adc9c8c8ccaf751432cb027a7cc30cf951
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876811"
---
# <a name="mf_mt_spatial_audio_object_metadata_length-attribute"></a>MF \_ MT SPATIAL AUDIO OBJECT METADATA \_ \_ \_ \_ \_ LENGTH-Attribut

Ein -Wert, der die Größe des Objekttyps räumlicher Audiometadaten in Bytes angibt, die der Decoder ausgibt.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Das Metadatenblob mit dem angegebenen Format wird mithilfe der [**ISpatialAudioMetadataWriter-Schnittstelle**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) geschrieben und mithilfe der [**ISpatialAudioMetadataReader-Schnittstelle**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) gelesen. Das Metadatenblob ist für die Media Foundation Pipeline und die Komponenten nicht transparent. Das -Attribut wird auf den Medientyp räumlicher Audiodaten angewendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur Desktop-Apps der Version 1703 \[\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                          |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 
