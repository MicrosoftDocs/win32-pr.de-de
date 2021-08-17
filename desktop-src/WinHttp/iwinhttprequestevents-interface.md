---
description: Stellt Ereignisse für Microsoft Windows HTTP Services (WinHTTP) bereit.
ms.assetid: 0721d7f9-2e84-41a9-be52-89c8d638eb90
title: IWinHttpRequestEvents-Schnittstelle
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
ms.openlocfilehash: 42b8355de57ada064e57a129c77ba507a72028b1c38ce115e58db110f2ce976b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744348"
---
# <a name="iwinhttprequestevents-interface"></a>IWinHttpRequestEvents-Schnittstelle

Die **IWinHttpRequestEvents-Schnittstelle** stellt Ereignisse für [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md)bereit. Es werden nur Ereignismethoden verwendet.

## <a name="members"></a>Member

Die **IWinHttpRequestEvents-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWinHttpRequestEvents** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IWinHttpRequestEvents-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                           | Beschreibung                                                          |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [**OnError**](iwinhttprequestevents-onerror.md)                                 | Tritt auf, wenn in der Anwendung ein Laufzeitfehler auftritt.<br/> |
| [**OnResponseDataAvailable**](iwinhttprequestevents-onresponsedataavailable.md) | Tritt ein, wenn Daten aus der Antwort verfügbar sind.<br/>          |
| [**OnResponseFinished**](iwinhttprequestevents-onresponsefinished.md)           | Tritt ein, wenn die Antwortdaten abgeschlossen sind.<br/>                |
| [**OnResponseStart**](iwinhttprequestevents-onresponsestart.md)                 | Tritt ein, wenn die Antwortdaten empfangen werden.<br/>      |



 

## <a name="remarks"></a>Hinweise

Im folgenden Verfahren wird beschrieben, wie Sie sich für Benachrichtigungen registrieren.

1.  Rufen Sie eine [IConnectionPointContainer-Schnittstelle](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) ab, indem **Sie QueryInterface** für ein [**IWinHttpRequest-Objekt**](iwinhttprequest-interface.md) aufrufen.
2.  Rufen [Sie FindConnectionPoint](/windows/win32/api/ocidl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint) für die zurückgegebene Schnittstelle auf, und übergeben Sie **IID \_ IWinHttpRequestEvents** an *riid*.
3.  Rufen Sie [Advise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) für den zurückgegebenen Verbindungspunkt auf, und übergeben Sie einen Zeiger auf eine **IUnknown-Schnittstelle** für ein Objekt, das **IWinHttpRequestEvents** in *pUnk* implementiert.

Benachrichtigungen können beendet werden, indem [Unadvise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-unadvise) auf dem in Schritt 2 zurückgegebenen Verbindungspunkt aufgerufen wird.

Informationen zum Anzeigen von Code, der sich für COM-Benachrichtigungen registriert, finden Sie im Abschnitt Client des Artikels [COM-Verbindungspunkte.](/archive/msdn-magazine/2007/september/clr-inside-out-com-connection-points)

> [!Note]  
> Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Laufzeitanforderungen](winhttp-start-page.md) der WinHTTP-Startseite.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP, Windows 2000 Professional nur mit \[ SP3-Desktop-Apps\]<br/>            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003, Windows 2000 Server nur mit \[ SP3-Desktop-Apps\]<br/>         |
| Verteilbare Komponente<br/>          | WinHTTP 5.0 und Internet Explorer 5.01 oder höher auf Windows XP und Windows 2000.<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[WinHTTP-Versionen](winhttp-versions.md)
</dt> </dl>

 

