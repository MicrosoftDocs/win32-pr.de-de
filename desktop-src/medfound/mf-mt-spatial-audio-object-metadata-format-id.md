---
description: Eine vom Decoder definierte GUID, die das räumliche audiometadatenformat identifiziert, wobei Downstreamkomponenten des metadatenobjekttyps benachrichtigt werden, die der Decoder ausgibt.
ms.assetid: 9714A2C7-25A1-4735-A0AC-22329ECBBC46
title: MF_MT_SPATIAL_AUDIO_OBJECT_METADATA_FORMAT_ID-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed16188a24b4c61facf1e325867d093b9b5cc869
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216272"
---
# <a name="mf_mt_spatial_audio_object_metadata_format_id-attribute"></a>Das \_ MF \_ MT \_ - \_ Attribut für räumliche audioobjektmetadatenformat \_ \_ \_ ID

Eine vom Decoder definierte GUID, die das räumliche audiometadatenformat identifiziert, wobei Downstreamkomponenten des metadatenobjekttyps benachrichtigt werden, die der Decoder ausgibt.

## <a name="data-type"></a>Datentyp

**GUID**

## <a name="remarks"></a>Bemerkungen

Das metadatenblob mit dem angegebenen Format wird mithilfe der [**ispatialaudiometadatawriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) -Schnittstelle geschrieben und mithilfe der [**ispatialaudiometadatareader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) -Schnittstelle gelesen. Das metadatenblob ist für die Media Foundation Pipeline und die Komponenten nicht transparent. Das-Attribut wird auf den Typ des räumlichen audiomediums angewendet. Wenn eine Downstreamkomponente das durch die GUID angegebene Metadatenformat nicht unterstützt, sollte die Komponente den Eingabe Medientyp ablehnen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1703, \[ nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                          |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 
