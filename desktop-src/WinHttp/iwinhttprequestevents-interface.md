---
description: Stellt Ereignisse für Microsoft Windows HTTP-Dienste (WinHTTP) bereit.
ms.assetid: 0721d7f9-2e84-41a9-be52-89c8d638eb90
title: Iwinhttprequestevents-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequestEvents
api_type:
- COM
api_location:
- HttpRequest.idl
ms.openlocfilehash: 3cdd0bf10c0d4bd75351ddaab6e88ce7182850fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350865"
---
# <a name="iwinhttprequestevents-interface"></a>Iwinhttprequestevents-Schnittstelle

Die **iwinhttprequestevents** -Schnittstelle stellt Ereignisse für [Microsoft Windows HTTP-Dienste (WinHTTP)](about-winhttp.md)bereit. Es werden nur Ereignis Methoden verwendet.

## <a name="members"></a>Member

Die **iwinhttprequestevents** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iwinhttprequestevents** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iwinhttprequestevents** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                           | BESCHREIBUNG                                                          |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [**OnError**](iwinhttprequestevents-onerror.md)                                 | Tritt auf, wenn in der Anwendung ein Laufzeitfehler auftritt.<br/> |
| [**Onresponondataavailable**](iwinhttprequestevents-onresponsedataavailable.md) | Tritt auf, wenn Daten aus der Antwort verfügbar sind.<br/>          |
| [**Onresponendabgeschlossen**](iwinhttprequestevents-onresponsefinished.md)           | Tritt auf, wenn die Antwortdaten fertig sind.<br/>                |
| [**Onresponse-Start**](iwinhttprequestevents-onresponsestart.md)                 | Tritt auf, wenn die Antwortdaten empfangen werden.<br/>      |



 

## <a name="remarks"></a>Bemerkungen

Im folgenden Verfahren wird beschrieben, wie Sie sich für Benachrichtigungen registrieren.

1.  Rufen Sie eine [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) -Schnittstelle ab, indem Sie **QueryInterface** für ein [**iwinhttprequest**](iwinhttprequest-interface.md) -Objekt aufrufen.
2.  Rufen Sie [FindConnectionPoint](/windows/win32/api/ocidl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint) für die zurückgegebene Schnittstelle auf, und übergeben Sie **IID \_ iwinhttprequestevents** an *riid*.
3.  Rufen Sie die [Empfehlung](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) auf dem zurückgegebenen Verbindungspunkt auf, und übergeben Sie einen Zeiger auf eine **IUnknown** -Schnittstelle für ein Objekt, das **iwinhttprequestevents** zu *Punk* implementiert.

Benachrichtigungen können beendet werden, indem Sie [Unrat](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-unadvise) für den Verbindungspunkt aufrufen, der in Schritt 2 zurückgegeben wurde.

Informationen zum Anzeigen von Code, der für com-Benachrichtigungen registriert wird, finden Sie im Abschnitt Client des Artikels [com-Verbindungspunkte](/archive/msdn-magazine/2007/september/clr-inside-out-com-connection-points) .

> [!Note]  
> Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Lauf Zeitanforderungen](winhttp-start-page.md) auf der WinHTTP-Start Seite.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]<br/>            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]<br/>         |
| Verteilbare Komponente<br/>          | WinHTTP 5,0 und Internet Explorer 5,01 oder höher unter Windows XP und Windows 2000.<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwinhttprequest**](iwinhttprequest-interface.md)
</dt> <dt>

[WinHTTP-Versionen](winhttp-versions.md)
</dt> </dl>

 

