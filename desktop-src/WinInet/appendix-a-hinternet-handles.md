---
title: HINTERNET-Handles
description: Dieser Abschnitt enthält Informationen zu den Handles, die von den WinINet-Funktionen verwendet werden, und zu der Hierarchie, in der sie funktionieren.
ms.assetid: 8a9788ed-eb25-42cb-b912-8dffa3df1850
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7477558887ac484ec0c3645d568bc3d91d29926af887ebadc51cf7e9523da787
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051930"
---
# <a name="hinternet-handles"></a>HINTERNET-Handles

Dieser Abschnitt enthält Informationen zu den Handles, die von den WinINet-Funktionen verwendet werden, und zu der Hierarchie, in der sie funktionieren.

-   [Informationen zu HINTERNET-Handles](#about-hinternet-handles)
-   [Handlehierarchie](#handle-hierarchy)
-   [FTP-Hierarchie](#ftp-hierarchy)
-   [HTTP-Hierarchie](#http-hierarchy)

## <a name="about-hinternet-handles"></a>Informationen zu HINTERNET-Handles

Die Handles, die von den WinINet-Funktionen erstellt und verwendet werden, sind vom Typ **HINTERNET.** Die WinINet-Funktionen geben **HINTERNET-Handles** zurück, die nicht mit anderen Handletypen austauschbar sind. Daher können sie nicht mit Funktionen wie [**ReadFile oder**](/windows/desktop/api/fileapi/nf-fileapi-readfile) [**CloseHandle verwendet werden.**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) Auf ähnliche Weise können andere Handletypen nicht mit den WinINet-Funktionen verwendet werden. Beispielsweise kann ein von [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) zurückgegebenes Handle nicht an [**InternetReadFile übergeben werden.**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)

Die [**InternetCloseHandle-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) schließt Handles des Typs **HINTERNET.** Beachten Sie, dass Handlewerte schnell wiederverwendet werden. Wenn ein Handle geschlossen wird und sofort ein neues Handle generiert wird, besteht daher eine gute Wahrscheinlichkeit, dass das neue Handle denselben Wert wie das gerade geschlossene Handle hat.

## <a name="handle-hierarchy"></a>Handlehierarchie

Die **HINTERNET-Handles** werden in einer Strukturhierarchie verwaltet. Das von der [**InternetOpen-Funktion zurückgegebene**](/windows/desktop/api/Wininet/nf-wininet-internetopena) Handle ist der Stammknoten. Von der [**InternetConnect-Funktion zurückgegebene**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) Handles belegen die nächste Ebene. Handles, die von den [**Funktionen FtpOpenFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)und [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) zurückgegeben werden, sind die Blattknoten.

**Windows XP und Windows Server 2003 R2 und früher:** Handles, die von , [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)und [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) zurückgegeben werden, sind ebenfalls Blattknoten.

Das folgende Diagramm veranschaulicht die Hierarchie der **HINTERNET-Handles.** Jedes Feld im Diagramm stellt eine Funktion dar, die ein **HINTERNET-Handle** zurückgibt.

![Funktionen, die Handles erstellen](images/ax-wnt01.png)

Auf der obersten Ebene befindet sich die [**InternetOpen-Funktion,**](/windows/desktop/api/Wininet/nf-wininet-internetopena) die das Stammhand handle erstellt. Die nächste Ebene enthält die [**Funktionen InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) und [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) Die Funktionen, die das von InternetConnect zurückgegebene Handle [**verwenden,**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) machen die letzte Ebene aus.

Das folgende Diagramm zeigt die Funktionen, die von dem von [**InternetOpenUrl erstellten Handle abhängig sind.**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) Die schattierten Felder stellen Funktionen dar, die **HINTERNET-Handles** zurückgeben, während die einfachen Felder Funktionen darstellen, die das von der zugeordneten Funktion erstellte **HINTERNET-Handle** verwenden.

![Funktionen, die das InternetOpenurl-Handle verwenden](images/ax-wnt02.png)

Die [**Funktionen InternetQueryDataAvailable,**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)und [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) verwenden das **hinternet-Handle,** das von [**InternetOpenUrl erstellt wurde.**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)

## <a name="ftp-hierarchy"></a>FTP-Hierarchie

Das folgende Diagramm zeigt die FTP-Funktionen, die von dem FTP-Sitzungshand handle abhängig sind, das von [**InternetConnect zurückgegeben wird.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) Die schattierten Felder stellen Funktionen dar, die **HINTERNET-Handles** zurückgeben, während die einfachen Felder Funktionen darstellen, die das **HINTERNET-Handle** verwenden, das von der Funktion erstellt wurde, von der sie abhängen.

![Funktionen, die das FTP-Sitzungshand handle verwenden](images/ax-wnt06.png)

Die [**Funktionen FtpCreateDirectory,**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) [**FtpDeleteFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) [**FtpGetCurrentDirectory,**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) [**FtpGetFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) [**FtpPutFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) [**FtpRemoveDirectory,**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya) [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)und [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) verwenden alle das **hinternet-Handle,** das von InternetConnect erstellt [**wurde.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)

Das folgende Diagramm zeigt die beiden FTP-Funktionen, die Handles zurückgeben, und die Funktionen, die davon abhängig sind. Die schattierten Felder stellen Funktionen dar, die **HINTERNET-Handles** zurückgeben, während die einfachen Felder Funktionen darstellen, die das **HINTERNET-Handle** verwenden, das von der Funktion erstellt wurde, von der sie abhängen.

![Funktionen, die das Handle aus ftpopen und ftpfindfirstfile verwenden](images/ax-wnt03.png)

Die [**InternetFindNextFile-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) ist von dem von [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)erstellten Handle abhängig, während [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) und [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) das von [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)erstellte Handle verwenden.

## <a name="http-hierarchy"></a>HTTP-Hierarchie

Das folgende Diagramm zeigt die Beziehungen der Funktionen, die für das HTTP-Protokoll verwendet werden. Die schattierten Felder stellen Funktionen dar, die **HINTERNET-Handles** zurückgeben, während die einfachen Felder Funktionen darstellen, die das **HINTERNET-Handle** verwenden, das von der Funktion erstellt wurde, von der sie abhängen.

![Funktionen, die das Handle von httpopenrequest verwenden](images/ax-wnt05.png)

Die [**Funktionen HttpAddRequestHeaders,**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) [**HttpQueryInfo,**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) [**HttpSendRequest,**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa)und [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) hängen von dem von [**HttpOpenRequest erstellten**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)Handle ab.

Das folgende Diagramm zeigt die Funktionen, die das **hinternet-Handle** verwenden, das von [**HttpOpenRequest erstellt wurde,**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) nachdem es von [**HttpSendRequest gesendet wurde.**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) Die schattierten Felder stellen Funktionen dar, die **HINTERNET-Handles** zurückgeben, während die einfachen Felder Funktionen darstellen, die das **HINTERNET-Handle** verwenden, das von der Funktion erstellt wurde, von der sie abhängen.

![Funktionen, die das Handle nach httpsendrequest verwenden](images/ax-wnt07.png)

Nachdem [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) das von [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)zurückgegebene Handle verwendet hat, kann es von [**InternetQueryDataAvailable,**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)und [**InternetSetFilePointer verwendet werden.**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer)

![Funktionen, die das Handle nach httpsendrequestex verwenden](images/ax-wnt08.png)

Nachdem [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa) das von [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)zurückgegebene Handle verwendet hat, kann das Handle von [**HttpEndRequest,**](/windows/desktop/api/Wininet/nf-wininet-httpendrequesta) [**InternetReadFileEx**](/windows/desktop/api/Wininet/nf-wininet-internetreadfileexa)und [**InternetWriteFile verwendet werden.**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) Nachdem [**HttpEndRequest**](/windows/desktop/api/Wininet/nf-wininet-httpendrequesta) aufgerufen wurde, kann das Handle von [**InternetReadFile,**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer)und [**InternetQueryDataAvailable verwendet werden.**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)

> [!Note]  
> WinINet unterstützt keine Serverimplementierung. Darüber hinaus sollte sie nicht von einem Dienst verwendet werden. Verwenden Sie für Serverimplementierungen oder -dienste [Microsoft Windows HTTP Services (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

 

 