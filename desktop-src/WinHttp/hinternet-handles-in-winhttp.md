---
description: Microsoft Windows HTTP Services (WinHTTP) verwendet Handles, um die Einstellungen und Informationen nachverfolgung zu erhalten, die bei Verwendung des HTTP-Protokolls erforderlich sind.
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

Microsoft Windows HTTP Services (WinHTTP) verwendet Handles, um die Einstellungen und Informationen nachverfolgung zu erhalten, die bei Verwendung des HTTP-Protokolls erforderlich sind. Jedes Handle verwaltet Informationen, die für eine HTTP-Sitzung, eine Verbindung mit einem HTTP-Server oder eine bestimmte Ressource relevant sind. In diesem Thema werden die verschiedenen Typen von Handles, die Namenskonventionen für diese Handles und ihre hierarchische Struktur beschrieben.

-   [Informationen zu HINTERNET-Handles](#about-hinternet-handles)
-   [Benennungshandles](#naming-handles)
-   [Handlehierarchie](#handle-hierarchy)
-   [Erläuterung der Handlehierarchie](#explanation-of-the-handle-hierarchy)

## <a name="about-hinternet-handles"></a>Informationen zu HINTERNET-Handles

Die von WinHTTP erstellten und verwendeten Handles werden als **HINTERNET-Handles** bezeichnet. Die WinHTTP-Funktionen geben **HINTERNET-Handles** zurück, die nicht mit anderen Handles austauschbar sind, sodass sie nicht mit Funktionen wie [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) oder [**CloseHandle verwendet werden können.**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) Auf ähnliche Weise können andere Handles nicht mit WinHTTP-Funktionen verwendet werden. Beispielsweise kann ein von [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) zurückgegebenes Handle nicht an [**WinHttpReadData übergeben werden.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) Diese **HINTERNET-Handles** können nicht geschlossen werden, während ein API-Aufruf mit dem Handle in Bearbeitung ist. Um eine Racebedingung zu vermeiden, sollten Anwendungen das Handle schützen und verhindern, dass es geschlossen wird, solange der API-Aufruf läuft.

WinInet-Funktionen (Microsoft Win32 Internet) verwenden ebenfalls **HINTERNET-Handles.** Die in WinInet-Funktionen verwendeten Handles können jedoch nicht mit den Handles in WinHTTP-Funktionen ausgetauscht werden. Weitere Informationen zu WinInet finden Sie unter [Informationen zu WinINet.](/windows/desktop/WinInet/about-wininet)

Die [**WinHttpCloseHandle-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle) schließt WinHTTP **HINTERNET-Handles.**

## <a name="naming-handles"></a>Benennungshandles

In der gesamten WinHTTP-Dokumentation zeigen Beschreibungen von Funktionen in der Anwendungsprogrammierschnittstelle (API) und Beispielcode die Erstellung und Verwendung verschiedener Typen von **HINTERNET-Handles.** Um die verschiedenen verfügbaren Handles zu verfolgen, ist die Benennung dieser Handles konsistent. In der folgenden Tabelle sind die bezeichner aufgeführt, die von der Konvention in der Dokumentation verwendet werden.



| Handletyp       | Funktion, die handle erstellt                                                                                                          | Bezeichner |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------|------------|
| Generisches Handle    | [**WinHttpOpen,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)oder [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) | hInternet  |
| Sitzungshand handle    | [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)                                                                                                | hSession   |
| Verbindungshand handle | [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)                                                                                          | hConnect   |
| Anforderungshand handle    | [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)                                                                                  | hRequest   |



 

## <a name="handle-hierarchy"></a>Handlehierarchie

Die **HINTERNET-Handles** werden in einer Hierarchie verwaltet. Das von [**WinHttpOpen zurückgegebene Handle ist**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) das **HINTERNET-Handle der** Sitzung. Durch **aufrufen von WinHttpOpen** werden die WinHTTP-Funktionen initialisiert und ein Sitzungskontext begonnen, der Benutzerinformationen und -einstellungen während der gesamten Lebensdauer des Sitzungshandpunkts verwaltet. [**WinHttpConnect gibt**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) einen HTTP- oder HTTPS-Zielserver an und erstellt ein **HINTERNET-Verbindungshand** handle. Standardmäßig erbt das Verbindungshand handle die Einstellungen für das Sitzungshand handle. Jeder Ressource, die mit einem Aufruf von [**WinHttpOpenRequest angegeben**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) wird, wird ein **HINTERNET-Handle** für Anforderungen zugewiesen.

Das folgende Diagramm veranschaulicht die Hierarchie der **HINTERNET-Handles.** Jedes Feld im Diagramm stellt eine WinHTTP-Funktion dar, die ein **HINTERNET-Handle** zurückgibt.

![Funktionen, die Handles erstellen](images/art-winhttp2.png)

Nach dem Schließen eines Handles muss die Anwendung darauf vorbereitet sein, Rückrufbenachrichtigungen für das Handle zu empfangen, bis der endgültige **WERT VON WINHTTP \_ CALLBACK STATUS HANDLE \_ \_ \_ CLOSED** zurückgegeben wird, um anzugeben, dass das Handle vollständig geschlossen ist.

Ein Sitzungshand handle wird als übergeordnetes Element jedes Verbindungshandpunkts, das zum Erstellen verwendet wurde, verwendet. ebenso werden sowohl das Verbindungshandy als auch das übergeordnete Sitzungshandl als übergeordnetes Element eines anforderungshandl bezeichnet, das vom Verbindungshandl erstellt wird.

Wenn ein übergeordnetes Handle geschlossen wird, werden alle übergeordneten Handle indirekt ungültig gemacht, auch wenn sie nicht selbst geschlossen wurden, und bei nachfolgenden Anforderungen, die sie verwenden, tritt der Fehler **ERROR \_ INVALID HANDLE \_ auf.** Ausstehende asynchrone Anforderungen können nicht zuverlässig abgeschlossen werden.

Das folgende Diagramm zeigt die Funktionen, die das **hinternet-Handle** verwenden, das von [**WinHttpOpenRequest erstellt wurde.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) Die schattierten Felder stellen WinHTTP-Funktionen dar, die Handles erstellen, und die einfachen Felder zeigen die Funktionen, die diese **HINTERNET-Handles** verwenden. Das Diagramm ist auch so organisiert, dass die Reihenfolge angezeigt wird, in der WinHTTP-Funktionen normalerweise aufgerufen werden.

![Funktionen, die Handles erstellen](images/art-winhttp2.png)

## <a name="explanation-of-the-handle-hierarchy"></a>Erläuterung der Handlehierarchie

Zunächst wird mit [**WinHttpOpen ein Sitzungshand handle erstellt.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) erfordert das Sitzungshand handle als ersten Parameter und gibt ein Verbindungshand handle für einen angegebenen Server zurück. Ein Anforderungshand handle wird von [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)erstellt, das das von [**WinHttpConnect erstellte Verbindungshand handle verwendet.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) Wenn die Anwendung der Anforderung zusätzliche Header hinzufüge, oder wenn die Anwendung Anmeldeinformationen für die Authentifizierung festlegen muss, können [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) und [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) mit diesem Anforderungshandle aufgerufen werden. Die Anforderung wird von [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)gesendet, die das Anforderungshand handle verwendet. Nach dem Senden der Anforderung können zusätzliche Daten mit [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)an den Server gesendet werden, oder die Anwendung kann direkt zu [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) springen, um anzugeben, dass keine weiteren Informationen an den Server gesendet werden. An diesem Punkt kann je nach Zweck der Anwendung das Anforderungshandles verwendet werden, um [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders), [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)oder eine Ressource mit [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) und [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)abzurufen.

 

 
