---
description: In diesem Thema wird beschrieben, wie Sie Microsoft Active Server Pages (ASP) erstellen, mit denen Informationen zu Remote Computern auf Computern angezeigt werden, auf denen WMI nicht installiert ist.
ms.assetid: add08566-6408-43e4-9d0d-4c0851540602
ms.tgt_platform: multiple
title: Erstellen von Active Server Seiten für WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 52143284be54868d36b55a6dd86e0b49c82d863d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369093"
---
# <a name="creating-active-server-pages-for-wmi"></a>Erstellen von Active Server Seiten für WMI

Microsoft Active Server Pages (ASP) können dynamische Webseiten erstellen, indem Sie sowohl Server seitige als auch Client seitige Skripts einschließen. ASP-Seiten können viel schneller als Client-HTML-Seiten sein, da der Großteil der Arbeit auf dem Server erfolgt. Sie können ASP-Seiten auch zum Anzeigen von Informationen zu Remote Computern auf anderen Computern verwenden, auf denen keine Windows-Verwaltungsinstrumentation (WMI) installiert ist.

Im folgenden Verfahren wird die Verwendung von WMI mit ASP beschrieben.

**So verwenden Sie WMI mit ASP**

1.  Schreiben Sie eine ASP-Seite (. ASP), die WMI verwendet, und platzieren Sie Sie in einem Verzeichnis, auf das der Webserver zugreifen kann.

    ASP-Skripts für WMI können mit mehreren Skriptsprachen wie VBScript entwickelt werden. Sie können den WMI-Skript Teil einer ASP-Seite genauso erstellen, wie Sie ein beliebiges anderes Skript erstellen, das WMI verwendet, mit einer wichtigen Einschränkung: Sie können keine asynchronen WMI-Methoden in ASP-Seiten verwenden. Beachten Sie auch, dass sich alle Aufrufe von **GetObject** oder von " **kreateobject** " im serverseitigen Code befinden müssen. Weitere Informationen finden Sie unter [Scripting API for WMI](scripting-api-for-wmi.md).

2.  Richten Sie die Authentifizierungs Konfiguration für Internetinformationsdienste (IIS) ein. Weitere Informationen finden Sie unter [Konfigurieren von IIS 5 und höher für die WMI-ASP-Skript](configuring-iis-5-for-wmi-asp-scripting.md)Erstellung.
3.  Deaktivieren Sie den anonymen Zugriff, und aktivieren Sie die integrierte Windows-Authentifizierung für die ASP-Datei. Sie können diese Einstellungen für Ihre ASP-Seite konfigurieren, indem Sie das IIS-Snap-in verwenden, das sich im Ordner **Verwaltung** der **Systemsteuerung** befindet.

## <a name="wmi-asp-page-example"></a>Beispiel für WMI-ASP-Seite

Im folgenden Beispiel wird Windows-Verwaltungsinstrumentation (WMI) in einer Active Server Seite (ASP) verwendet, um die IP-Adresse und die IP-Standard Gateway-Einstellungen für den Server anzuzeigen, von dem dieses Skript ausgeführt wird.


```VB
<%@ LANGUAGE="VBSCRIPT"%>
<HTML>
<HEAD>
<TITLE>WMI ASP Example:
    Read Default Gateway and IP Address information </TITLE>
</HEAD>

<BODY>

<%
On Error Resume Next
set IPConfigSet = GetObject("winmgmts:" _
   & "{impersonationLevel=impersonate}!root\cimv2").ExecQuery" _
    & "("SELECT IPAddress, DefaultIPGateway "" _ 
    & " FROM Win32_NetworkAdapterConfiguration WHERE IPEnabled=TRUE")
%>

<%If Err <> 0 Then %>
    <%if err.number = -2147217405 then%>
        <p>Error 0x80041003: Access Denied: 
           Check permissions and file security for this ASP file.</p>
    <%else%>
        <p>Error description: <%=Err.description%> 
           error number <%=Err.number%></p>
    <%end if%>

<%end if %>

<%for each IPConfig in IPConfigSet%>

    <%if Not IsNull(IPConfig.IPAddress) then %>
        <%for i=LBound(IPConfig.IPAddress) 
            to UBound(IPConfig.IPAddress)%>
            <p>IP Address: <%=IPConfig.IPAddress(i)%></p>
        <%next%>
    <%end if%>
    

    <%if Not IsNull(IPConfig.DefaultIPGateway) then %>
        <%for i=LBound(IPConfig.DefaultIPGateway) 
            to UBound(IPConfig.DefaultIPGateway)%>
            <p>Default IP Gateway: 
                <%=IPConfig.DefaultIPGateway(i)%></p>
        <%next%>
    <%end if%>
<%next%>

<%If Err <> 0 Then %>
    <p>error description: <%=Err.description%> 
       error number <%=Err.number%></p>
<%end if %>

</BODY>
</HTML>
```



 

 



