---
description: Die ITParticipantEvent-Schnittstelle enthält Methoden, die die Beschreibung von Teilnehmerereignissen abrufen.
ms.assetid: 1199ec91-ee06-4e6c-8d8f-1585a3da3db0
title: ITParticipantEvent-Schnittstelle (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d4f47e57bf1698a97be6811316409e596c9dfb03181e50b5f487798463c5cb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118864460"
---
# <a name="itparticipantevent-interface"></a>ITParticipantEvent-Schnittstelle

\[**ITParticipantEvent** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **ITParticipantEvent-Schnittstelle** enthält Methoden, die die Beschreibung von Teilnehmerereignissen abrufen. Wenn die Implementierung der [**ITTAPIEventNotification::Event-Methode**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) der Anwendung ein [**\_ TAPI-EREIGNIS**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) gleich **TE \_ PRIVATE** angibt, ist der *pEvent-Parameter* der Methode ein **IDispatch-Zeiger** für die **ITParticipantEvent-Schnittstelle.** Die Methoden dieser Schnittstelle können verwendet werden, um Informationen zu einer änderung des Teilnehmers abzurufen, die aufgetreten ist.

> [!Note]  
> Sie müssen die [**ITTAPI::p ut \_ EventFilter-Methode**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) aufrufen und eine Ereignisfiltermaske festlegen, die das **TE \_ PRIVATE-Ereignis** enthält, um den Empfang von Teilnehmerereignissen zu ermöglichen. Wenn Sie **ITTAPI::p ut \_ EventFilter** nicht aufrufen, erhält Ihre Anwendung keine Ereignisse. Weitere Informationen finden Sie in der [Übersicht über](events.md) Ereignisse.

 

## <a name="members"></a>Member

Die **ITParticipantEvent-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITParticipantEvent** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ITParticipantEvent-Schnittstelle** verfügt über diese Methoden.



| Methode                                                         | BESCHREIBUNG                                                                                                                                     |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_get-Ereignis**](itparticipantevent-get-event.md)             | Ruft den [**PARTICIPANT EVENT-Deskriptor \_**](participant-event.md) des Ereignisses ab.<br/>                                                    |
| [**\_Get-Teilnehmer**](itparticipantevent-get-participant.md) | Ruft einen Zeiger auf ein Array von [**ITParticipant-Schnittstellen**](itparticipant.md) ab, die die am Ereignis beteiligten Teilnehmer darstellen.<br/> |
| [**get \_ SubStream**](itparticipantevent-get-substream.md)     | Ruft einen Zeiger auf ein Array von [**ITSubStream-Schnittstellen**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) ab, die die am Ereignis beteiligten Unterstreams darstellen.<br/>       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> <dt>

[**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[**\_TEILNEHMEREREIGNIS**](participant-event.md)
</dt> <dt>

[**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)
</dt> <dt>

[**\_TAPI-EREIGNIS**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event)
</dt> <dt>

[Registrieren des Ereigniscodeausschnitts](register-events.md)
</dt> </dl>

 

