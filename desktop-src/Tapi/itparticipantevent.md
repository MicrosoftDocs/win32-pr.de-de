---
description: Die itparticipvorgänger Vent-Schnittstelle enthält Methoden, mit denen die Beschreibung der Teilnehmer Ereignisse abgerufen wird.
ms.assetid: 1199ec91-ee06-4e6c-8d8f-1585a3da3db0
title: Itparticipvorgänger Vent-Schnittstelle (confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ac6e2b43a528bc041a71962e84b4e1be62152a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355909"
---
# <a name="itparticipantevent-interface"></a>Itparticipvorgänger Vent-Schnittstelle

\[**Itparticipvorgänger Vent** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **itparticipvorgänger Vent** -Schnittstelle enthält Methoden, mit denen die Beschreibung der Teilnehmer Ereignisse abgerufen wird. Wenn die Implementierung der [**ittapieventnotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) -Methode der Anwendung ein [**TAPI- \_ Ereignis**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) angibt, das gleich " **te \_ private**" ist, ist der " *Peer* Event"-Parameter der Methode ein **IDispatch** -Zeiger für die **itparticipvorgänger Vent** -Schnittstelle. Die Methoden dieser Schnittstelle können zum Abrufen von Informationen über eine geänderte Teilnehmer Änderung verwendet werden.

> [!Note]  
> Sie müssen die Ereignis [**\_ Filter-Methode ittapi::p UT**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) und eine Ereignis Filtermaske mit dem privaten Ereignis **te \_** festlegen, um den Empfang von Teilnehmer Ereignissen zu ermöglichen. Wenn Sie **ittapi::p UT \_ EventFilter** nicht anrufen, empfängt Ihre Anwendung keine Ereignisse. Weitere Informationen finden Sie in der Übersicht über [Ereignisse](events.md) .

 

## <a name="members"></a>Member

Die **itparticipvorgänger Vent** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Itparticipvorgänger Vent** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **itparticipvorgänger Vent** -Schnittstelle verfügt über diese Methoden.



| Methode                                                         | BESCHREIBUNG                                                                                                                                     |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get- \_ Ereignis**](itparticipantevent-get-event.md)             | Ruft den [**Teilnehmer \_ Ereignis**](participant-event.md) Deskriptor des Ereignisses ab.<br/>                                                    |
| [**\_Teilnehmer erhalten**](itparticipantevent-get-participant.md) | Ruft einen Zeiger auf ein Array von [**itteilnehmer**](itparticipant.md) -Schnittstellen ab, die die am Ereignis beteiligten Teilnehmer darstellen.<br/> |
| [**\_substream erhalten**](itparticipantevent-get-substream.md)     | Ruft einen Zeiger auf ein Array von [**itsubstream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) -Schnittstellen ab, die die untergeordneten Datenströme darstellen.<br/>       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>"Confpriv. h"</dt> </dl> |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itteilnehmer**](itparticipant.md)
</dt> <dt>

[**Itsubstream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> <dt>

[**Itcallinfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[**Teilnehmer \_ Ereignis**](participant-event.md)
</dt> <dt>

[**Ittapieventnotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)
</dt> <dt>

[**TAPI- \_ Ereignis**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event)
</dt> <dt>

[Code Ausschnitt für das Registrieren von Ereignissen](register-events.md)
</dt> </dl>

 

