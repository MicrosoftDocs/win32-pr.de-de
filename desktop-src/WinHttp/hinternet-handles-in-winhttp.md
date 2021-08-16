---
description: Microsoft Windows HTTP Services (WinHTTP) verwendet Handles, um die Einstellungen und Informationen nachzuverfolgen, die bei Verwendung des HTTP-Protokolls erforderlich sind.
ms.assetid: 0bd82860-1347-40c8-ae77-c4d865c109be
title: HINTERNET-Handles in WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a76f925d11646ed2fe5b5d3732fe8972d979cdc6383a4d47e955c0e60a1390e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563270"
---
# <a name="hinternet-handles-in-winhttp"></a>HINTERNET-Handles in WinHTTP

Microsoft Windows HTTP Services (WinHTTP) verwendet Handles, um die Einstellungen und Informationen nachzuverfolgen, die bei Verwendung des HTTP-Protokolls erforderlich sind. Jedes Handle verwaltet Informationen zu einer HTTP-Sitzung, einer Verbindung mit einem HTTP-Server oder einer bestimmten Ressource. In diesem Thema werden die verschiedenen Typen von Handles, die Benennungskonventionen für diese Handles und ihre hierarchische Struktur beschrieben.

-   [Informationen zu HINTERNET-Handles](#about-hinternet-handles)
-   [Benennungshandles](#naming-handles)
-   [Handlehierarchie](#handle-hierarchy)
-   [Erläuterung der Handlehierarchie](#explanation-of-the-handle-hierarchy)

## <a name="about-hinternet-handles"></a>Informationen zu HINTERNET-Handles

Die von WinHTTP erstellten und verwendeten Handles werden **als HINTERNET-Handles** bezeichnet. Die WinHTTP-Funktionen geben **HINTERNET-Handles** zurück, die nicht mit anderen Handles austauschbar sind, sodass sie nicht mit Funktionen wie [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) oder [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle)verwendet werden können. Auf ähnliche Weise können andere Handles nicht mit WinHTTP-Funktionen verwendet werden. Beispielsweise kann ein von [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) zurückgegebenes Handle nicht an [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)übergeben werden. Diese **HINTERNET-Handles** können nicht geschlossen werden, während ein API-Aufruf mit dem Handle ausgeführt wird. Um eine Racebedingung zu vermeiden, sollten Anwendungen das Handle schützen und verhindern, dass es geschlossen wird, solange der API-Aufruf ausgeführt wird.

Microsoft Win32 Internet-Funktionen (WinInet) verwenden auch **HINTERNET-Handles.** Die in WinInet-Funktionen verwendeten Handles können jedoch nicht mit den Handles ausgetauscht werden, die in WinHTTP-Funktionen verwendet werden. Weitere Informationen zu WinInet finden Sie unter [Informationen zu WinINet.](/windows/desktop/WinInet/about-wininet)

Die [**WinHttpCloseHandle-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle) schließt WinHTTP **HINTERNET-Handles.**

## <a name="naming-handles"></a>Benennungshandles

In der gesamten WinHTTP-Dokumentation zeigen Beschreibungen der Funktionen in der Anwendungsprogrammierschnittstelle (APPLICATION Programming Interface, API) und Beispielcode die Erstellung und Verwendung verschiedener **Hinternet-Handles.** Um die verschiedenen verfügbaren Handles nachzuverfolgen, ist die Benennung dieser Handles konsistent. In der folgenden Tabelle sind die konventionsgemäß verwendeten Bezeichner in der Dokumentation aufgeführt.



| Handletyp       | Handle zum Erstellen einer Funktion                                                                                                          | Bezeichner |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------|------------|
| Generisches Handle    | [**WinHttpOpen,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)oder [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) | hInternet  |
| Sitzungshandle    | [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)                                                                                                | hSession   |
| Verbindungshandle | [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)                                                                                          | hConnect   |
| Anforderungshandle    | [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)                                                                                  | hRequest   |



 

## <a name="handle-hierarchy"></a>Handlehierarchie

Die **HINTERNET-Handles** werden in einer Hierarchie verwaltet. Das von [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) zurückgegebene Handle ist das **HINTERNET-Handle** der Sitzung. Durch den Aufruf von **WinHttpOpen** werden die WinHTTP-Funktionen initialisiert und ein Sitzungskontext gestartet, der Benutzerinformationen und -einstellungen während der gesamten Lebensdauer des Sitzungshandle verwaltet. [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) gibt einen HTTP- oder HTTPS-Zielserver an und erstellt ein HINTERNET-Verbindungshandle.  Standardmäßig erbt das Verbindungshandle die Einstellungen für das Sitzungshandle. Jeder Ressource, die mit einem Aufruf von [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) angegeben wird, wird ein HINTERNET-Anforderungshandle zugewiesen. 

Das folgende Diagramm veranschaulicht die Hierarchie der **HINTERNET-Handles.** Jedes Feld im Diagramm stellt eine WinHTTP-Funktion dar, die ein **HINTERNET-Handle** zurückgibt.

![Funktionen, die Handles erstellen](images/art-winhttp2.png)

Nach dem Schließen eines Handles muss die Anwendung darauf vorbereitet sein, Rückrufbenachrichtigungen für das Handle zu empfangen, bis der endgültige **WINHTTP \_ CALLBACK \_ STATUS HANDLE \_ \_ CLOSED-Wert** zurückgegeben wird, um anzugeben, dass das Handle vollständig geschlossen ist.

Ein Sitzungshandle wird als übergeordnetes Element eines Verbindungshandle bezeichnet, das zum Erstellen verwendet wird. Ebenso werden sowohl das Verbindungshandle als auch das übergeordnete Sitzungshandle als übergeordnetes Element jedes Anforderungshandle bezeichnet, das vom Verbindungshandle erstellt wird.

Wenn ein übergeordnetes Handle geschlossen wird, werden alle untergeordneten Elemente indirekt ungültig, auch wenn sie nicht selbst geschlossen werden. Nachfolgende Anforderungen, die sie verwenden, schlagen mit dem Fehler **FEHLER \_ UNGÜLTIGES \_ HANDLE** fehl. Ausstehende asynchrone Anforderungen können nicht ordnungsgemäß abgeschlossen werden.

Das folgende Diagramm zeigt die Funktionen, die das von [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)erstellte **HINTERNET-Handle** verwenden. Die schattierten Felder stellen WinHTTP-Funktionen dar, die Handles erstellen, und die einfachen Felder zeigen die Funktionen an, die diese **HINTERNET-Handles** verwenden. Das Diagramm ist auch so organisiert, dass die Reihenfolge angezeigt wird, in der WinHTTP-Funktionen normalerweise aufgerufen werden.

![Funktionen, die Handles erstellen](images/art-winhttp2.png)

## <a name="explanation-of-the-handle-hierarchy"></a>Erläuterung der Handlehierarchie

Zunächst wird ein Sitzungshandle mit [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)erstellt. [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) erfordert das Sitzungshandle als ersten Parameter und gibt ein Verbindungshandle für einen angegebenen Server zurück. Ein Anforderungshandle wird von [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)erstellt, das das von [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)erstellte Verbindungshandle verwendet. Wenn die Anwendung der Anforderung zusätzliche Header hinzufügst oder die Anwendung Anmeldeinformationen für die Authentifizierung festlegen muss, können [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) und [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) mit diesem Anforderungshandle aufgerufen werden. Die Anforderung wird von [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)gesendet, die das Anforderungshandle verwendet. Nach dem Senden der Anforderung können zusätzliche Daten mit [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)an den Server gesendet werden, oder die Anwendung kann direkt zu [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) springen, um anzugeben, dass keine weiteren Informationen an den Server gesendet werden. An diesem Punkt kann das Anforderungshandle abhängig vom Zweck der Anwendung verwendet werden, um [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders), [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)oder eine Ressource mit [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) und [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)abzurufen.

 

 
