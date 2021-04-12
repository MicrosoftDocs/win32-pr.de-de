---
title: HINTERNET-Handles
description: Dieser Abschnitt enthält Informationen zu den Handles, die von den WinInet-Funktionen und der Hierarchie verwendet werden, in der Sie funktionieren.
ms.assetid: 8a9788ed-eb25-42cb-b912-8dffa3df1850
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba70d2fadbd0d8393685fec2075ebf0dc4aa11c2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473948"
---
# <a name="hinternet-handles"></a>HINTERNET-Handles

Dieser Abschnitt enthält Informationen zu den Handles, die von den WinInet-Funktionen und der Hierarchie verwendet werden, in der Sie funktionieren.

-   [Informationen zu hinternethandles](#about-hinternet-handles)
-   [Handle der Hierarchie](#handle-hierarchy)
-   [FTP-Hierarchie](#ftp-hierarchy)
-   [HTTP-Hierarchie](#http-hierarchy)

## <a name="about-hinternet-handles"></a>Informationen zu hinternethandles

Die Handles, die von den WinInet-Funktionen erstellt und verwendet werden, sind vom Typ **HINTERNET**. Die WinInet-Funktionen geben **HINTERNET** Handles zurück, die nicht mit anderen Handlertypen austauschbar sind. Daher können Sie nicht mit Funktionen wie "read [**File**](/windows/desktop/api/fileapi/nf-fileapi-readfile) " oder " [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle)" verwendet werden. Ebenso können andere handle-Typen nicht mit den WinInet-Funktionen verwendet werden. So kann z. b. ein von " [**kreatefile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) " zurückgegebener Handle nicht an " [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)" übergeben werden.

Die [**internetclosehandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) -Funktion schließt Handles vom Typ **HINTERNET**. Beachten Sie, dass Handle-Werte schnell wieder verwendet werden. Wenn ein Handle geschlossen und ein neues Handle sofort generiert wird, besteht die Möglichkeit, dass das neue Handle denselben Wert hat wie das Handle, das gerade geschlossen wurde.

## <a name="handle-hierarchy"></a>Handle der Hierarchie

Die **HINTERNET** -Handles werden in einer Struktur Hierarchie verwaltet. Das von der [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) -Funktion zurückgegebene Handle ist der Stamm Knoten. Handles, die von der [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) -Funktion zurückgegeben werden, belegen die nächste Ebene. Handles, die von den Funktionen [**ftpopeinfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)und [**httpopanrequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) zurückgegeben werden, sind die Blattknoten.

**Windows XP und Windows Server 2003 R2 und früher:** Handles, die von, [**gopheropenfile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)und [**gopherfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) zurückgegeben werden, sind ebenfalls Blattknoten.

Im folgenden Diagramm wird die Hierarchie der **hinternethandles** veranschaulicht. Jedes Feld im Diagramm stellt eine Funktion dar, die ein **HINTERNET** -handle zurückgibt.

![Funktionen zum Erstellen von Handles](images/ax-wnt01.png)

Auf der obersten Ebene befindet sich die [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) -Funktion, die das Stamm Handle erstellt. Die nächste Ebene enthält die Funktionen [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) und [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) . Die Funktionen, die das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) zurückgegebene Handle verwenden, bilden die letzte Ebene.

Das folgende Diagramm zeigt die Funktionen, die von dem von [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)erstellten handle abhängig sind. Die schattierten Felder stellen Funktionen dar, die **hinternethandles** zurückgeben, während die einfachen Felder Funktionen darstellen, die das **hinternethandle** verwenden, das von der zugeordneten Funktion erstellt wurde.

![Funktionen, die das InternetOpenURL-Handle verwenden](images/ax-wnt02.png)

Die Funktionen [**internetquerydataavailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)und [**internetsetfilepointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) verwenden das **hinternethandle** , das von [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)erstellt wurde.

## <a name="ftp-hierarchy"></a>FTP-Hierarchie

Das folgende Diagramm zeigt die FTP-Funktionen, die vom von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)zurückgegebenen FTP-Sitzungs handle abhängig sind. Die schattierten Felder stellen Funktionen dar, die **hinternethandles** zurückgeben, während die einfachen Felder Funktionen darstellen, die das **hinternethandle** verwenden, das von der Funktion erstellt wurde, von der Sie abhängig sind.

![Funktionen, die das FTP-Sitzungs Handle verwenden](images/ax-wnt06.png)

Die Funktionen [**ftpkreatedirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya), [**ftpdeletefile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea), [**ftpgetcurrentdirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya), [**ftpgetfile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**ftpputfile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**ftprewvedirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya), [**ftprenamefile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)und [**ftpsetcurrentdirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) verwenden alle das **HINTERNET** handle, das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)erstellt wurde.

Das folgende Diagramm zeigt die zwei FTP-Funktionen, die Handles und die von ihnen abhängigen Funktionen zurückgeben. Die schattierten Felder stellen Funktionen dar, die **hinternethandles** zurückgeben, während die einfachen Felder Funktionen darstellen, die das **hinternethandle** verwenden, das von der Funktion erstellt wurde, von der Sie abhängig sind.

![Funktionen, die das Handle von ftpopen und ftpfindfirstfile verwenden](images/ax-wnt03.png)

Die [**internetfindnextfile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) -Funktion ist von dem Handle abhängig, das von [**ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)erstellt wurde, während für [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) und [**internetwrite tefile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) das von [**ftpopenfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)erstellte Handle verwendet wird.

## <a name="http-hierarchy"></a>HTTP-Hierarchie

Das folgende Diagramm zeigt die Beziehungen der Funktionen, die für das HTTP-Protokoll verwendet werden. Die schattierten Felder stellen Funktionen dar, die **hinternethandles** zurückgeben, während die einfachen Felder Funktionen darstellen, die das **hinternethandle** verwenden, das von der Funktion erstellt wurde, von der Sie abhängig sind.

![Funktionen, die das Handle aus httpopanrequest verwenden](images/ax-wnt05.png)

Die Funktionen [**httpadressquestheaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa), [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa), [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta), [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa)und [**internetterrordlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) sind von dem Handle abhängig, das von [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)erstellt wurde.

Das folgende Diagramm zeigt die Funktionen, die das **hinternethandle** verwenden, das von [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) erstellt wurde, nachdem es von [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)gesendet wurde. Die schattierten Felder stellen Funktionen dar, die **hinternethandles** zurückgeben, während die einfachen Felder Funktionen darstellen, die das **hinternethandle** verwenden, das von der Funktion erstellt wurde, von der Sie abhängig sind.

![Funktionen, die das Handle nach HttpSendRequest verwenden](images/ax-wnt07.png)

Nachdem [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) das von [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)zurückgegebene Handle verwendet hat, kann es von [**internetquerydataavailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)und [**internetsetfilepointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer)verwendet werden.

![Funktionen, die das Handle nach HttpSendRequestEx verwenden](images/ax-wnt08.png)

Nachdem [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa) das von [**httpoptenrequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)zurückgegebene Handle verwendet hat, kann das Handle von [**httpdrequest**](/windows/desktop/api/Wininet/nf-wininet-httpendrequesta), [**internetreadfileex**](/windows/desktop/api/Wininet/nf-wininet-internetreadfileexa)und [**internetwrite File**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)verwendet werden. Nachdem [**httpdrequest**](/windows/desktop/api/Wininet/nf-wininet-httpendrequesta) aufgerufen wurde, kann das Handle von " [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)", " [**internetsetfilepointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer)" und " [**internetquerydataavailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)" verwendet werden.

> [!Note]  
> WinInet unterstützt keine Server Implementierungen. Außerdem sollte Sie nicht von einem Dienst verwendet werden. Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 