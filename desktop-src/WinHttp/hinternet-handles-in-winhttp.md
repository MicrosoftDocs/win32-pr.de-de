---
description: Die Microsoft Windows HTTP-Dienste (WinHTTP) verwenden Handles, um die Einstellungen und Informationen, die bei Verwendung des HTTP-Protokolls erforderlich sind, nachzuverfolgen.
ms.assetid: 0bd82860-1347-40c8-ae77-c4d865c109be
title: HINTERNET Handles in WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf374675ad6f2114dd48e0a3ff1db50cd0dd7f9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104560724"
---
# <a name="hinternet-handles-in-winhttp"></a>HINTERNET Handles in WinHTTP

Die Microsoft Windows HTTP-Dienste (WinHTTP) verwenden Handles, um die Einstellungen und Informationen, die bei Verwendung des HTTP-Protokolls erforderlich sind, nachzuverfolgen. Jedes Handle verwaltet Informationen, die für eine HTTP-Sitzung, eine Verbindung mit einem HTTP-Server oder eine bestimmte Ressource relevant sind. In diesem Thema werden die verschiedenen Typen von Handles, die Benennungs Konventionen für diese Handles und ihre hierarchische Struktur beschrieben.

-   [Informationen zu hinternethandles](#about-hinternet-handles)
-   [Benennungs Handles](#naming-handles)
-   [Handle der Hierarchie](#handle-hierarchy)
-   [Erläuterung der Handle-Hierarchie](#explanation-of-the-handle-hierarchy)

## <a name="about-hinternet-handles"></a>Informationen zu hinternethandles

Die Handles, die von WinHTTP erstellt und verwendet werden, werden als **hinternethandles** bezeichnet. Die WinHTTP-Funktionen geben **HINTERNET** Handles zurück, die nicht mit anderen Handles austauschbar sind, sodass Sie nicht mit Funktionen wie "read [**File**](/windows/desktop/api/fileapi/nf-fileapi-readfile) " oder " [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle)" verwendet werden können. Ebenso können andere Handles nicht mit WinHTTP-Funktionen verwendet werden. So kann z. b. ein von " [**kreatefile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) " zurückgegebener Handle nicht an " [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)" übergeben werden. Diese **HINTERNET** -Handles können nicht geschlossen werden, während ein API-Befehl, der das Handle verwendet, ausgeführt wird. Um eine Racebedingung zu vermeiden, sollten Anwendungen das Handle schützen und verhindern, dass es so lange geschlossen wird, wie der API-Vorgang ausgeführt wird.

Microsoft Win32 Internet (WinInet)-Funktionen verwenden auch **HINTERNET** -Handles. Die in WinInet-Funktionen verwendeten Handles können jedoch nicht mit den in WinHTTP-Funktionen verwendeten Handles ausgetauscht werden. Weitere Informationen zu WinInet finden Sie unter [Informationen zu WinInet](/windows/desktop/WinInet/about-wininet).

Die [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle) -Funktion schließt WinHTTP- **HINTERNET** -Handles.

## <a name="naming-handles"></a>Benennungs Handles

In der gesamten WinHTTP-Dokumentation zeigen Beschreibungen von Funktionen in der Anwendungsprogrammierschnittstelle (Application Programming Interface, API) und im Beispielcode die Erstellung und Verwendung verschiedener Typen von **hinternethandles** . Um die verschiedenen Typen der verfügbaren Handles nachzuverfolgen, ist die Benennung dieser Handles einheitlich. In der folgenden Tabelle sind die in der-Dokumentation verwendeten Bezeichner aufgeführt.



| Handle-Typ       | Funktion zum Erstellen eines Handles                                                                                                          | Bezeichner |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------|------------|
| Generisches Handle    | [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen), [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)oder [**winhttpopanrequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) | HINTERNET  |
| Sitzungs handle    | [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)                                                                                                | hsession   |
| Verbindungs Handle | [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)                                                                                          | hconnect   |
| Anforderungs handle    | [**Winhttpopanrequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)                                                                                  | hrequest   |



 

## <a name="handle-hierarchy"></a>Handle der Hierarchie

Die **HINTERNET** -Handles werden in einer-Hierarchie verwaltet. Das von [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) zurückgegebene Handle ist das Sitzungs- **HINTERNET** -handle. Durch Aufrufen von **WinHttpOpen** werden die WinHTTP-Funktionen initialisiert, und es wird ein Sitzungs Kontext gestartet, der Benutzerinformationen und Einstellungen während der gesamten Lebensdauer des Sitzungs Handles beibehält. [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) gibt einen HTTP-oder HTTPS-Zielserver an und erstellt ein **HINTERNET** -Verbindungs Handle. Standardmäßig erbt das Verbindungs Handle die Einstellungen für das Sitzungs handle. Jede Ressource, die mit einem [**winhttpopanrequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) -Befehl angegeben wird, wird einem Anforderungs- **HINTERNET** -Handle zugewiesen.

Im folgenden Diagramm wird die Hierarchie der **hinternethandles** veranschaulicht. Jedes Feld im Diagramm stellt eine WinHTTP-Funktion dar, die ein **HINTERNET** -handle zurückgibt.

![Funktionen zum Erstellen von Handles](images/art-winhttp2.png)

Nach dem Schließen eines Handles muss die Anwendung auf den Empfang von Rückruf Benachrichtigungen für das Handle vorbereitet werden, bis der endgültige **WinHTTP- \_ Rückruf \_ Status " \_ \_ Closed** "-Wert behandelt wird, um anzugeben, dass das Handle vollständig geschlossen ist.

Ein Sitzungs Handle wird als übergeordnetes Element eines beliebigen Verbindungs Handles bezeichnet, das zum Erstellen verwendet wurde. Ebenso werden sowohl das Verbindungs Handle als auch das übergeordnete Sitzungs Handle als Parent eines beliebigen Anforderungs Handles bezeichnet, das zum Erstellen des Verbindungs Handles verwendet wird.

Wenn ein übergeordnetes Handle geschlossen wird, werden alle untergeordneten Elemente indirekt ungültig gemacht, auch wenn Sie nicht geschlossen sind, und nachfolgende Anforderungen, die Sie verwenden, schlagen mit dem fehlerhaften **\_ \_ handle** fehl. Es ist nicht möglich, dass ausstehende asynchrone Anforderungen ordnungsgemäß abgeschlossen werden.

Im folgenden Diagramm werden die Funktionen gezeigt, die das **hinternethandle** verwenden, das von [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)erstellt wurde. Die schattierten Felder stellen WinHTTP-Funktionen dar, die Handles erstellen, und in den einfachen Feldern werden die Funktionen angezeigt, die diese **HINTERNET** -Handles verwenden. Das Diagramm ist auch so organisiert, dass die Reihenfolge angezeigt wird, in der WinHTTP-Funktionen normalerweise aufgerufen werden.

![Funktionen zum Erstellen von Handles](images/art-winhttp2.png)

## <a name="explanation-of-the-handle-hierarchy"></a>Erläuterung der Handle-Hierarchie

Zuerst wird ein Sitzungs Handle mit [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)erstellt. [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) erfordert das Sitzungs Handle als ersten Parameter und gibt ein Verbindungs Handle für einen angegebenen Server zurück. Ein Anforderungs Handle wird von [**winhttpopanrequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)erstellt, das das von [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)erstellte Verbindungs Handle verwendet. Wenn die Anwendung zusätzliche Header zur Anforderung hinzufügen möchte oder wenn es erforderlich ist, dass die Anwendung Anmelde Informationen für die Authentifizierung festlegt, können [**winhttpadressquestheaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) und [**winhttpsetanmelde**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) Informationen mit diesem Anforderungs Handle aufgerufen werden. Die Anforderung wird von [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)gesendet, die das Anforderungs Handle verwendet. Nachdem die Anforderung gesendet wurde, können zusätzliche Daten mithilfe von [**winhttpwrite tedata**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)an den Server gesendet werden, oder die Anwendung kann direkt zu [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) überspringen, um anzugeben, dass keine weiteren Informationen an den Server gesendet werden. An diesem Punkt kann das Anforderungs handle abhängig vom Zweck der Anwendung zum Aufrufen von [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders), [**winhttpqueryauthschemas**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)oder zum Abrufen einer Ressource mit " [**winhttpquerydataavailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) " und " [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)" verwendet werden.

 

 
