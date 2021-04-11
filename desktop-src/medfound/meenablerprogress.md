---
description: Signalisiert den Fortschritt eines Inhalts Wegbereiter-Objekts. Objekte, die die imfcontentenabler-Schnittstelle verfügbar machen, können dieses Ereignis ausgeben, um die Anwendung über den Fortschritt der Aktionen des Inhalts Virtualisierungsebene zählt zu benachrichtigen.
ms.assetid: ec14ba9b-cfb6-4e32-870e-2436e11c308b
title: Meenablerprogress-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58303835113408a7fe09436967286d5ff988acdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215171"
---
# <a name="meenablerprogress-event"></a>Meenablerprogress-Ereignis

Signalisiert den Fortschritt eines Inhalts Wegbereiter-Objekts. Objekte, die die [**imfcontentenabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) -Schnittstelle verfügbar machen, können dieses Ereignis ausgeben, um die Anwendung über den Fortschritt der Aktionen des Inhalts Enablers zu benachrichtigen.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE               | BESCHREIBUNG                                                               |
|-----------------------|---------------------------------------------------------------------------|
| VT \_ LPWSTR<br/> | Breit Zeichen-Zeichenfolge, die den Fortschritt beschreibt.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Um dieses Ereignis zu erhalten, Fragen Sie die [**imfcontentenabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) -Schnittstelle für die [**imfmediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) -Schnittstelle ab. Aufrufen Sie dann [**imfmediaeventgenerator:: begingetevent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), wie im Thema [Medienereignis-Generatoren](media-event-generators.md)beschrieben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMF contentenabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
</dt> <dt>

[Medienereignis Generatoren](media-event-generators.md)
</dt> <dt>

[Ereignisse Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




