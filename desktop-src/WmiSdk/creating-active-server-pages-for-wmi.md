---
description: Beschreibt das Erstellen von Microsoft Active Server Pages (ASP), die Informationen zu Remotecomputern auf Computern anzeigen, auf denen WMI nicht installiert ist.
ms.assetid: add08566-6408-43e4-9d0d-4c0851540602
ms.tgt_platform: multiple
title: Erstellen von Active Server Pages für WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee7b31a5f4874e0ae4431ac452ea604da9c154bbb78e8debb91aad7ea892fa09
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030610"
---
# <a name="creating-active-server-pages-for-wmi"></a>Erstellen von Active Server Pages für WMI

Microsoft Active Server Pages (ASP) kann dynamische Webseiten erstellen, indem sowohl serverseitige als auch clientseitige Skripts eingeschlossen werden. ASP-Seiten können viel schneller sein als HTML-Clientseiten, da der Großteil der Arbeit auf dem Server erledigt wird. Sie können ASP-Seiten auch verwenden, um Informationen zu Remotecomputern auf anderen Computern anzuzeigen, auf denen Windows Management Instrumentation (WMI) nicht installiert ist.

Das folgende Verfahren beschreibt die Verwendung von WMI mit ASP.

**So verwenden Sie WMI mit ASP**

1.  Schreiben Sie eine ASP-Seite (.asp), die WMI verwendet, und platzieren Sie sie in einem Verzeichnis, auf das Ihr Webserver zugreifen kann.

    ASP-Skripts für WMI können mit mehreren Skriptsprachen, einschließlich VBScript, entwickelt werden. Sie können den WMI-Skriptteil einer ASP-Seite genau wie jedes andere Skript erstellen, das WMI verwendet, mit einer wichtigen Einschränkung: Sie können keine asynchronen WMI-Methoden innerhalb von ASP-Seiten verwenden. Beachten Sie auch, dass alle Aufrufe von **GetObject** oder **CreateObject** im serverseitigen Code vorhanden sein müssen. Weitere Informationen finden Sie unter [Skripterstellungs-API für WMI.](scripting-api-for-wmi.md)

2.  Richten Sie die Authentifizierungskonfiguration für Internetinformationsdienste (IIS) ein. Weitere Informationen finden Sie unter [Konfigurieren von IIS 5 und höher für WMI ASP Scripting](configuring-iis-5-for-wmi-asp-scripting.md).
3.  Deaktivieren Sie den anonymen Zugriff, und aktivieren Sie Windows integrierte Authentifizierung für die ASP-Datei. Sie können diese Einstellungen für Ihre ASP-Seite konfigurieren, indem Sie das IIS-Snap-In verwenden, das sich im Ordner **Verwaltung** des **Systemsteuerung** befindet.

## <a name="wmi-asp-page-example"></a>Beispiel für eine WMI-ASP-Seite

Im folgenden Beispiel werden Windows Management Instrumentation (WMI) innerhalb einer Active Server Page (ASP) verwendet, um die IP-Adresse und die Standardeinstellungen des IP-Gateways für den Server anzuzeigen, von dem dieses Skript ausgeführt wird.


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



 

 



