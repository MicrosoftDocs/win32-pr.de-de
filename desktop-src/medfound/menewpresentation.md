---
description: Wird von einer Medienquelle ausgelöst, die Topologien über die SCHNITTSTELLE "ARRANGEMediaSourceTopologyProvider" bereitstellt, z. B. die Sequencerquelle. Die Quelle löst das -Ereignis aus, wenn es über eine neue Präsentation verfügt. Die Mediensitzung leitet dieses Ereignis an die Anwendung weiter.
ms.assetid: c669b2c9-5ece-4045-b691-8a71bbf491e1
title: MENewPresentation-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa2adec5b3dbb8544e537bdcc8f5c724130175b3167f9c51dc005112fdbd9a0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119228880"
---
# <a name="menewpresentation-event"></a>MENewPresentation-Ereignis

Wird von einer Medienquelle ausgelöst, die Topologien über die [**SCHNITTSTELLE "ARRANGEMediaSourceTopologyProvider"**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) bereitstellt, z. B. die Sequencerquelle. Die Quelle löst das -Ereignis aus, wenn es über eine neue Präsentation verfügt. Die Mediensitzung leitet dieses Ereignis an die Anwendung weiter.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind:



| VARTYPE                | BESCHREIBUNG                                                                                                                                                             |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| VT \_ UNKNOWN<br/> | Zeiger auf die [**INTERFACESPresentationDescriptor-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) des Präsentationsdeskriptors für die neue Präsentation.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Die Anwendung kann die Topologie, die dem Präsentationsdeskriptor entspricht, abrufen, indem [**SIE AUFMEDIASourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) für die Medienquelle aufrufen. Die Anwendung kann dann die neue Topologie in der Mediensitzung in die Warteschlange stellen, indem [**SIE DIESMEDIASESSION::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (include Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation Ereignisse](media-foundation-events.md)
</dt> <dt>

[Sequencer-Quelle](sequencer-source.md)
</dt> </dl>

 

 




