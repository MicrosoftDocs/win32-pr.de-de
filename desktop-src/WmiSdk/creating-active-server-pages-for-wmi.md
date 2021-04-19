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
# <a name="creating-active-server-pages-for-wmi"></a><span data-ttu-id="6e255-103">Erstellen von Active Server Seiten für WMI</span><span class="sxs-lookup"><span data-stu-id="6e255-103">Creating Active Server Pages for WMI</span></span>

<span data-ttu-id="6e255-104">Microsoft Active Server Pages (ASP) können dynamische Webseiten erstellen, indem Sie sowohl Server seitige als auch Client seitige Skripts einschließen.</span><span class="sxs-lookup"><span data-stu-id="6e255-104">Microsoft Active Server Pages (ASP) can create dynamic webpages by including both server-side and client-side scripts.</span></span> <span data-ttu-id="6e255-105">ASP-Seiten können viel schneller als Client-HTML-Seiten sein, da der Großteil der Arbeit auf dem Server erfolgt.</span><span class="sxs-lookup"><span data-stu-id="6e255-105">ASP pages can be much faster than client HTML pages because most of the work is done on the server.</span></span> <span data-ttu-id="6e255-106">Sie können ASP-Seiten auch zum Anzeigen von Informationen zu Remote Computern auf anderen Computern verwenden, auf denen keine Windows-Verwaltungsinstrumentation (WMI) installiert ist.</span><span class="sxs-lookup"><span data-stu-id="6e255-106">You can also use ASP pages to display information about remote computers to other computers that do not have Windows Management Instrumentation (WMI) installed.</span></span>

<span data-ttu-id="6e255-107">Im folgenden Verfahren wird die Verwendung von WMI mit ASP beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6e255-107">The following procedure describes how to use WMI with ASP.</span></span>

<span data-ttu-id="6e255-108">**So verwenden Sie WMI mit ASP**</span><span class="sxs-lookup"><span data-stu-id="6e255-108">**To use WMI with ASP**</span></span>

1.  <span data-ttu-id="6e255-109">Schreiben Sie eine ASP-Seite (. ASP), die WMI verwendet, und platzieren Sie Sie in einem Verzeichnis, auf das der Webserver zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="6e255-109">Write an ASP page (.asp) that uses WMI, and place it in a directory accessible to your web server.</span></span>

    <span data-ttu-id="6e255-110">ASP-Skripts für WMI können mit mehreren Skriptsprachen wie VBScript entwickelt werden.</span><span class="sxs-lookup"><span data-stu-id="6e255-110">ASP scripts for WMI can be developed with several scripting languages, including VBScript.</span></span> <span data-ttu-id="6e255-111">Sie können den WMI-Skript Teil einer ASP-Seite genauso erstellen, wie Sie ein beliebiges anderes Skript erstellen, das WMI verwendet, mit einer wichtigen Einschränkung: Sie können keine asynchronen WMI-Methoden in ASP-Seiten verwenden.</span><span class="sxs-lookup"><span data-stu-id="6e255-111">You can construct the WMI script part of an ASP page exactly as you construct any other script that uses WMI, with one important restriction: you cannot use asynchronous WMI methods within ASP pages.</span></span> <span data-ttu-id="6e255-112">Beachten Sie auch, dass sich alle Aufrufe von **GetObject** oder von " **kreateobject** " im serverseitigen Code befinden müssen.</span><span class="sxs-lookup"><span data-stu-id="6e255-112">Note also that any calls to **GetObject** or **CreateObject** must be in the server-side code.</span></span> <span data-ttu-id="6e255-113">Weitere Informationen finden Sie unter [Scripting API for WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="6e255-113">For more information, see [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

2.  <span data-ttu-id="6e255-114">Richten Sie die Authentifizierungs Konfiguration für Internetinformationsdienste (IIS) ein.</span><span class="sxs-lookup"><span data-stu-id="6e255-114">Set up authentication configuration for Internet Information Services (IIS).</span></span> <span data-ttu-id="6e255-115">Weitere Informationen finden Sie unter [Konfigurieren von IIS 5 und höher für die WMI-ASP-Skript](configuring-iis-5-for-wmi-asp-scripting.md)Erstellung.</span><span class="sxs-lookup"><span data-stu-id="6e255-115">For more information, see [Configuring IIS 5 and Later for WMI ASP Scripting](configuring-iis-5-for-wmi-asp-scripting.md).</span></span>
3.  <span data-ttu-id="6e255-116">Deaktivieren Sie den anonymen Zugriff, und aktivieren Sie die integrierte Windows-Authentifizierung für die ASP-Datei.</span><span class="sxs-lookup"><span data-stu-id="6e255-116">Disable anonymous access, and enable Windows Integrated Authentication for the ASP file.</span></span> <span data-ttu-id="6e255-117">Sie können diese Einstellungen für Ihre ASP-Seite konfigurieren, indem Sie das IIS-Snap-in verwenden, das sich im Ordner **Verwaltung** der **Systemsteuerung** befindet.</span><span class="sxs-lookup"><span data-stu-id="6e255-117">You can configure these settings for your ASP page by using the IIS snap-in located in the **Administrative Tools** folder of the **Control Panel**.</span></span>

## <a name="wmi-asp-page-example"></a><span data-ttu-id="6e255-118">Beispiel für WMI-ASP-Seite</span><span class="sxs-lookup"><span data-stu-id="6e255-118">WMI ASP Page Example</span></span>

<span data-ttu-id="6e255-119">Im folgenden Beispiel wird Windows-Verwaltungsinstrumentation (WMI) in einer Active Server Seite (ASP) verwendet, um die IP-Adresse und die IP-Standard Gateway-Einstellungen für den Server anzuzeigen, von dem dieses Skript ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6e255-119">The following example uses Windows Management Instrumentation (WMI) within an Active Server Page (ASP) to display the IP address and default IP gateway settings for the server from which this script is executed.</span></span>


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



 

 



