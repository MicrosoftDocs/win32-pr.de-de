---
description: Behandlung von Cookies in WinHTTP
ms.assetid: ef0f0847-05f6-4477-8e48-e0bea66314ab
title: Behandlung von Cookies in WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e3b596225dc3c741ab9ed0139a63e343e7afb3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349725"
---
# <a name="cookie-handling-in-winhttp"></a>Behandlung von Cookies in WinHTTP

HTTP-Sitzungsdaten werden zwischen dem Client und dem Server im Cookie-Header der Anforderung oder der Antwort übermittelt. Der Server sendet Cookies im Set-Cookie-Header der Antwort an den Client, und die WinHTTP-API sendet das Server Cookie erneut an den Server im Cookieheader der Anforderung. Die in RFC 2109 (http State Management-Mechanismus) beschriebenen Spezifikationen zur Behandlung von Cookies werden standardmäßig in WinHTTP implementiert. Die aktuellen Spezifikationen für die Behandlung von Cookies, die in RFC 2964 beschrieben werden, werden von WinHTTP nicht unterstützt.

WinHTTP Ruft das Cookie von der Server Set-Cookie Kopfzeile ab und speichert es pro Sitzung in einem Cache. Dieses Cookie wird bei nachfolgenden Anforderungen in derselben WinHTTP-Sitzung erneut gesendet, in der das Ziel mit der Quelle des Cookies übereinstimmt. Die WinHTTP-API generiert den Anforderungs Cookie-Header für jeden Abschnitt in der Anforderung erneut.

In der folgenden Liste werden verschiedene Optionen beschrieben, die WinHTTP-Client Anwendungen zum Verarbeiten von Cookies verwenden können:

-   Automatische Cookiebehandlung: mit WinHTTP werden Cookies automatisch verarbeitet, und die Client Anwendung führt keine benutzerdefinierte Cookiebehandlung aus.
-   Deaktivieren der automatischen Cookiebehandlung: die Automatische Cookiebehandlung in der WinHTTP-API ist deaktiviert, und es werden keine Cookies gesendet.
-   Manuelles angeben aller Cookies – die Automatische Cookiebehandlung ist deaktiviert, und die Client Anwendung fügt alle Cookie-Header für jede Anforderung in der Sitzung hinzu bzw. entfernt Sie.
-   Manuelle und automatische Cookie-Behandlung: kombinieren Sie die automatische und manuelle Behandlung von Cookies.

## <a name="disabling-automatic-cookie-handling"></a>Deaktivieren der automatischen Behandlung von Cookies

Zum Deaktivieren der Cookiebehandlung Ruft die WinHTTP-Client Anwendung die [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) -Funktion auf, wobei der Parameter *dwOption* auf WinHTTP \_ \_ -Option deaktivierte \_ Funktion und der *lpBuffer* -Parameter auf WinHTTP- \_ Deaktivierte Cookies festgelegt ist \_ . Der *HINTERNET* -Parameter kann entweder ein Sitzungs handle oder ein Anforderungs Handle sein. Wenn die Cookie-Verarbeitung für ein Anforderungs handle deaktiviert ist, das eine vorherige Anforderung gesendet hat, sollte der Client vorhandene Anforderungs Cookie-Header manuell mit der [**winhttpadressquestheaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) -Funktion entfernen, bevor die nächste Anforderung gesendet wird. Weitere Informationen finden Sie unter [Entfernen von Cookie-Headern](#removing-cookie-headers).

**Hinweis**  Die Client Anwendung muss alle Cookies in der Sitzung festlegen, nachdem der automatische Modus deaktiviert wurde.

## <a name="manually-specifying-all-cookies"></a>Manuelles angeben aller Cookies

Wenn die Automatische Cookiebehandlung deaktiviert ist, kann die WinHTTP-Client Anwendung alle Cookies manuell angeben. Um das Cookie manuell festzulegen, ruft die Anwendung [**winhttpadressquestheaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) auf und gibt den Cookie-Header im *pwszheaders* -Parameter an. Die Client Anwendung sollte vor dem erneuten Senden der Anforderung alle Cookie-Header löschen.

Die Client Anwendung sollte auch den Cookie-Header ändern, wenn die Anforderung umgeleitet wurde. Um das Cookie für umgeleitete Anforderungen zu ändern, gibt der Client eine Rückruffunktion mit [**winhttpsetstatus Callback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback) an, die auf den Umleitungs Rückruf Fall antwortet. Der Rückruf Handler sollte das Cookie, das zuvor in der Anforderung gesendet wurde, durch Aufrufen von [**winhttpadressquestheaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)löschen. Weitere Informationen zum Entfernen von Cookie-Headern finden Sie unter [Entfernen von Cookie-Headern](#removing-cookie-headers).

## <a name="manual-and-automatic-cookie-handling"></a>Manuelle und automatische Behandlung von Cookies

WinHTTP-Client Anwendungen können den automatischen WinHTTP-Cookie-Behandlungs Mechanismus mit manueller Behandlung von Cookies kombinieren. Die Anwendung fügt dem automatisch generierten Cookieheader benutzerdefinierte Cookies hinzu, bevor die Anforderung mit der [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) -Funktion gesendet wird. Das benutzerdefinierte Cookie sollte der erste Cookie-Header in der Anforderung für die WinHTTP-API sein, um das Cookie ordnungsgemäß zwischenzuspeichern. Die Client Anwendung sollte auch Cookies entfernen, die für vorherige Anforderungen gesendet wurden, bevor eine Anforderung für dasselbe Anforderungs handle erneut gesendet wird. Weitere Informationen finden Sie unter Entfernen von Cookie-Headern.

Cookies, die einer Anforderung vor dem Aufruf von [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) hinzugefügt werden, sind in allen WinHTTP-Anforderungen enthalten, die im Auftrag der nächsten **WinHttpSendRequest** -und [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) -Aufrufe gesendet werden. Die Client Anwendung muss möglicherweise den Cookie-Header löschen, wenn die Anforderung umgeleitet wurde. Um das Cookie für umgeleitete Anforderungen zu löschen, gibt der Client eine Rückruffunktion mit [**winhttpsetstatus Callback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback) an, die auf den Umleitungs Rückruf Fall antwortet. Der Rückruf Handler sollte das Cookie, das zuvor in der Anforderung gesendet wurde, durch Aufrufen von [**winhttpadressquestheaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)löschen. Die Rückruffunktion legt möglicherweise keine neuen benutzerdefinierten Cookies für den Umleitungs Rückruf fest. Der Client muss auf den Abschluss von **WinHttpReceiveResponse** warten, bevor neue Cookies für den nächsten **WinHttpSendRequest** -Befehl hinzugefügt werden.

## <a name="removing-cookie-headers"></a>Entfernen der Cookie-Header

Die WinHTTP-Client Anwendung muss möglicherweise das vorhandene Anforderungs Cookie löschen, bevor eine Anforderung erneut gesendet wird, um zu verhindern, dass Cookies, die für vorherige Anforderungen gesendet wurden, bei der aktuellen Anforderung erneut gesendet werden. Weitere Informationen finden Sie in der folgenden Notiz. Beachten Sie auch, dass Cookies nicht gelöscht werden müssen, bevor die erste Anforderung für das Anforderungs handle gesendet wird. Der Client kann vorhandene Cookies löschen, indem er [**winhttpadressquestheaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) mit einem leeren Cookieheader im *pwszheaders* -Parameter und das \_ \_ \_ im Parameter " *dwmodifier* " festgelegte Flag "WinHTTP-adressflag ersetzen" aufruft. Im folgenden Codebeispiel wird gezeigt, wie der Cookie-Header für die Anforderung gelöscht wird.

``` syntax
WinHttpAddRequestHeaders( hRequest, 
                          L"Cookie:", 
                          -1, 
                          WINHTTP_ADDREQ_FLAG_REPLACE);
```

Die WinHTTP-API verfügt über unterschiedliche Verhalten beim Verhalten von Cookies für Versionen des Betriebssystems vor Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 mit Service Pack 1 (SP1).

* * Windows XP mit SP2 und höher und Windows Server 2003 mit SP1 und höher: * *

Die WinHTTP-API löscht alle Cookies, die für vorherige Anforderungen für das Anforderungs handle gesendet wurden. Der Client kann vor jedem WinHttpSendRequest-Rückruf manuell neue Cookie-Header hinzufügen. Wenn die Funktion zur automatischen Behandlung von Cookies der WinHTTP-API nicht deaktiviert wurde, fügt die WinHTTP-API den neuen Cookie-Header an (oder fügt einen neuen Cookie-Header hinzu, wenn die Client Anwendung keinen manuell hinzugefügt hat) mit dem Cookie vom Server.

* * Windows XP mit SP2 und Windows Server 2003 mit SP1: * *

Die WinHTTP-API löscht den Anforderungs Cookie-Header nicht, nachdem [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) abgeschlossen wurde. In früheren Anforderungen gesendete Cookies werden bei nachfolgenden Aufrufen von " [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)" erneut gesendet. Die WinHTTP-Client Anwendung sollte vor dem erneuten Senden einer Anforderung für das Anforderungs handle vorhandene Cookies-Header löschen.

 

 



