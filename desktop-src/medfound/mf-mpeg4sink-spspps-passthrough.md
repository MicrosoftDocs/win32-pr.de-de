---
description: Gibt an, ob die MPEG-4-Dateisenke NALUs (Sequence Parameter Set) und Picture Parameter Set (PPS) herausfiltert.
ms.assetid: B2574BE5-6334-4ED2-A008-86326CDC13B8
title: MF_MPEG4SINK_SPSPPS_PASSTHROUGH-Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b939302999fc7e095abbc97aed5910976972c860440a2c865248949e0f052aa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104626"
---
# <a name="mf_mpeg4sink_spspps_passthrough-attribute"></a>MF \_ MPEG4SINK \_ SPSPPS \_ PASSTHROUGH-Attribut

Gibt an, ob die [**MPEG-4-Dateisenke**](mpeg-4-file-sink.md) NALUs (Sequence Parameter Set) und Picture Parameter Set (PPS) herausfiltert.

## <a name="data-type"></a>Datentyp

**BOOL** als **UINT32** gespeichert

## <a name="applies-to"></a>Gilt für:

[**WFMEDIASink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)

## <a name="remarks"></a>Hinweise

Die [**MPEG-4-Dateisenke**](mpeg-4-file-sink.md) schreibt die SPS- und PPS-Parameter in das Beispielbeschreibungsfeld der MP4-Datei. Standardmäßig werden die SPS- und PPS-NALUs aus dem Videostream heraus gefiltert. Um dieses Verhalten zu überschreiben, legen Sie das MF \_ MPEG4SINK \_ SPSPPS \_ PASSTHROUGH-Attribut auf **TRUE** fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 \|Desktop-Apps UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 \|Desktop-Apps UWP-Apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




