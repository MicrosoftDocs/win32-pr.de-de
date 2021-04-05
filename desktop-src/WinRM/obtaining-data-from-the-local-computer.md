---
title: Abrufen von Daten vom lokalen Computer
description: Obwohl Windows-Remoteverwaltung und WS-Management Protokoll explizit für die Remote Kommunikation konzipiert sind, ist das Einrichten einer Sitzung auf dem lokalen Computer der einfachste Fall.
ms.assetid: 7f08b557-bbd4-4f67-b5e5-b84e8af58657
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ccb71fd176bf3faf425ea57d06beb27788f41a62
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727408"
---
# <a name="obtaining-data-from-the-local-computer"></a><span data-ttu-id="493ab-103">Abrufen von Daten vom lokalen Computer</span><span class="sxs-lookup"><span data-stu-id="493ab-103">Obtaining Data from the Local Computer</span></span>

<span data-ttu-id="493ab-104">Obwohl Windows-Remoteverwaltung und WS-Management Protokoll explizit für die Remote Kommunikation konzipiert sind, ist das Einrichten einer Sitzung auf dem lokalen Computer der einfachste Fall.</span><span class="sxs-lookup"><span data-stu-id="493ab-104">Although Windows Remote Management and WS-Management protocol are explicitly designed for remote communication, establishing a session on the local computer is the simplest case.</span></span> <span data-ttu-id="493ab-105">Einige Skripts erfordern möglicherweise den Zugriff auf Daten auf dem lokalen Computer und auf Remote Computern.</span><span class="sxs-lookup"><span data-stu-id="493ab-105">Some scripts may require access data on the local computer as well as remote computers.</span></span>

<span data-ttu-id="493ab-106">**WinRM-Version 2,0:  **</span><span class="sxs-lookup"><span data-stu-id="493ab-106">**WinRM version 2.0:  **</span></span>

<span data-ttu-id="493ab-107">Alle Vorgänge werden als Remote betrachtet, und der WinRM-Dienst muss gestartet werden, bevor ein Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="493ab-107">All operations are considered remote and the WinRM service must be started before any operation is performed.</span></span> <span data-ttu-id="493ab-108">Wenn kein Remote Ziel angegeben ist, wird standardmäßig localhost verwendet, und alle Vorgänge werden an den lokalen WinRM-Dienst gesendet.</span><span class="sxs-lookup"><span data-stu-id="493ab-108">If a remote destination is not specified, then the localhost is used by default, and all operations will be sent to the local WinRM service.</span></span> <span data-ttu-id="493ab-109">Weitere Informationen zum Starten des WinRM-Dienstanbieter finden Sie unter [Installation und Konfiguration für Windows-Remoteverwaltung](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="493ab-109">For more information about starting the WinRM service, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>

<span data-ttu-id="493ab-110">Wenn Sie den WinRM-Dienst für lokale Vorgänge verwenden, sollten die folgenden Faktoren berücksichtigt werden:</span><span class="sxs-lookup"><span data-stu-id="493ab-110">When using the WinRM service for local operations, the following factors should be considered:</span></span>

-   <span data-ttu-id="493ab-111">Die lokale WinRM-Konfiguration kann nur von Administratoren gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="493ab-111">The local WinRM configuration can only be read by administrators.</span></span>
-   <span data-ttu-id="493ab-112">Für WMI-Namespaces müssen Berechtigungen für die Remote Aktivierung festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="493ab-112">WMI namespaces must have remote enable permissions set.</span></span> <span data-ttu-id="493ab-113">Weitere Informationen finden Sie unter [Sichern einer Remote-WMI-Verbindung](../wmisdk/securing-a-remote-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="493ab-113">For more information, see [Securing a Remote WMI Connection](../wmisdk/securing-a-remote-wmi-connection.md).</span></span>
-   <span data-ttu-id="493ab-114">Wenn kein WinRM- [*Listener*](windows-remote-management-glossary.md) erstellt wird, lauscht der WinRM-Dienst auf lokale Anforderungen an Port 47001.</span><span class="sxs-lookup"><span data-stu-id="493ab-114">If a WinRM [*listener*](windows-remote-management-glossary.md) is not created, then the WinRM service listens for local requests on port 47001.</span></span>

<span data-ttu-id="493ab-115">Jedes WinRM-Skript muss gestartet werden, indem eine Sitzung oder eine Verbindung mit einem Computer hergestellt wird, indem ein [**Sitzungs**](session.md) Objekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="493ab-115">Every WinRM script must start by establishing a session or connection to a computer by creating a [**Session**](session.md) object.</span></span> <span data-ttu-id="493ab-116">Nachdem die Sitzung erstellt wurde, können Sie die **Sitzungs** Objektmethoden verwenden, z. b. [**Session. Enumerate**](session-enumerate.md) oder [**Session. aufrufen**](session-invoke.md) , um Daten abzurufen oder Methoden auszuführen.</span><span class="sxs-lookup"><span data-stu-id="493ab-116">After the session is created, you can use the **Session** object methods, such as [**Session.Enumerate**](session-enumerate.md) or [**Session.Invoke**](session-invoke.md) to obtain data or to execute methods.</span></span>

<span data-ttu-id="493ab-117">Die Erstellung einer Sitzung ähnelt in gewisser Weise dem [Herstellen einer Verbindung](/windows/desktop/WmiSdk/wmi-tasks--connecting-to-the-wmi-service) mit einem Windows-Verwaltungsinstrumentation ([WMI](/windows/desktop/WmiSdk/wmi-start-page))-Namespace.</span><span class="sxs-lookup"><span data-stu-id="493ab-117">The creation of a session is somewhat similar to [connecting](/windows/desktop/WmiSdk/wmi-tasks--connecting-to-the-wmi-service) to a Windows Management Instrumentation ([WMI](/windows/desktop/WmiSdk/wmi-start-page)) namespace.</span></span> <span data-ttu-id="493ab-118">Die Sitzung ist im Wesentlichen eine Ebene, die es Ihnen ermöglicht, Daten über [*SOAP*](windows-remote-management-glossary.md) -Nachrichten und das WS-Management Protokoll zu senden und zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="493ab-118">The session is essentially a layer that allows you to send and receive data through [*SOAP*](windows-remote-management-glossary.md) messages and the WS-Management protocol.</span></span> <span data-ttu-id="493ab-119">Weitere Informationen finden Sie unter [WS-Management-Protokoll](ws-management-protocol.md).</span><span class="sxs-lookup"><span data-stu-id="493ab-119">For more information, see [WS-Management Protocol](ws-management-protocol.md).</span></span>

<span data-ttu-id="493ab-120">Wenn Sie die [**WSMAN. CreateSession**](wsman-createsession.md) -Methode aufrufen, um ein [**Sitzungs**](session.md) Objekt zu erstellen, wird eine [*Sitzung*](windows-remote-management-glossary.md) gestartet, die eine Verbindung mit dem lokalen WinRM herstellt.</span><span class="sxs-lookup"><span data-stu-id="493ab-120">Calling the [**WSMan.CreateSession**](wsman-createsession.md) method to create a [**Session**](session.md) object will start a [*session*](windows-remote-management-glossary.md) that connects to the local WinRM.</span></span>

<span data-ttu-id="493ab-121">**So erstellen Sie eine WSMAN-Sitzung und rufen Daten ab**</span><span class="sxs-lookup"><span data-stu-id="493ab-121">**To Create a WSMan Session and Obtain Data**</span></span>

1.  <span data-ttu-id="493ab-122">Erstellen Sie ein [**WSMAN**](wsman.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="493ab-122">Create a [**WSMan**](wsman.md) object.</span></span>

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    ```

    

2.  <span data-ttu-id="493ab-123">Erstellen Sie eine Sitzung, indem Sie die [**WSMAN. CreateSession**](wsman-createsession.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="493ab-123">Create a session by calling the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="493ab-124">Diese Sitzung wird mit Ihrem Anmelde Namen und Kennwort ausgeführt und kann Daten über das lokale WinRM abrufen.</span><span class="sxs-lookup"><span data-stu-id="493ab-124">This session runs under your logon username and password and can obtain data through the local WinRM.</span></span>

    ```VB
    Set objSession = objWsman.CreateSession()
    ```

    

3.  <span data-ttu-id="493ab-125">Erstellen Sie einen Ressourcen- [*URI*](windows-remote-management-glossary.md) , um die [*Ressource*](windows-remote-management-glossary.md) zu identifizieren, die Sie verwalten möchten, oder für die Sie Daten abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="493ab-125">Create a resource [*URI*](windows-remote-management-glossary.md) to identify the [*resource*](windows-remote-management-glossary.md) you want to manage or for which you want to obtain data.</span></span> <span data-ttu-id="493ab-126">Weitere Informationen zum Formatieren eines URIs finden Sie unter [Ressourcen-URIs](resource-uris.md).</span><span class="sxs-lookup"><span data-stu-id="493ab-126">For more information about formatting a URI, see [Resource URIs](resource-uris.md).</span></span> <span data-ttu-id="493ab-127">Dieser Ressourcen-URI gilt für eine bestimmte Instanz der WMI- [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service) Klasse, den WinMgmt-Dienst.</span><span class="sxs-lookup"><span data-stu-id="493ab-127">This resource URI is for a specific instance of the WMI [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class, the Winmgmt service.</span></span> <span data-ttu-id="493ab-128">Weitere Informationen finden Sie unter [Windows-Remoteverwaltung und WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="493ab-128">For more information, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

    ```VB
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
    ```

    

4.  <span data-ttu-id="493ab-129">Ruft [**Sitzungs**](session.md) Methoden auf, die Daten mit dem Ressourcen-URI Abrufen oder aufzählen.</span><span class="sxs-lookup"><span data-stu-id="493ab-129">Call [**Session**](session.md) methods that get or enumerate data using the resource URI.</span></span> <span data-ttu-id="493ab-130">Weitere Informationen finden Sie unter [WinRM-Skript-API](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="493ab-130">For more information, see [WinRM Scripting API](winrm-scripting-api.md).</span></span>

    ```VB
    strResponse = objSession.Get(strResource)
    Wscript.Echo strResponse
    ```

    

5.  <span data-ttu-id="493ab-131">Informationen zum Abrufen oder Verwalten von Daten von einem anderen Computer oder zum Verwenden verschiedener Authentifizierungsmethoden finden Sie unter Abrufen [von Daten von einem Remote Computer](obtaining-data-from-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="493ab-131">To get or manage data from another computer or use different methods of authentication, see [Obtaining Data from a Remote Computer](obtaining-data-from-a-remote-computer.md).</span></span>

<span data-ttu-id="493ab-132">Das folgende VBScript-Codebeispiel zeigt das komplette Skript, das die jeweilige Instanz des WMI- [**Win32- \_ diensnamens**](/windows/desktop/CIMWin32Prov/win32-service) "winmgmt" abruft.</span><span class="sxs-lookup"><span data-stu-id="493ab-132">The following VBScript code example shows the complete script that obtains the specific instance of the WMI [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) named "Winmgmt".</span></span>


```VB
Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession()
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
strResponse = objSession.Get(strResource)
Wscript.Echo strResponse
```



<span data-ttu-id="493ab-133">Das folgende VBScript-Codebeispiel zeigt das komplette Skript mit der Datentransformation.</span><span class="sxs-lookup"><span data-stu-id="493ab-133">The following VBScript code example shows the complete script with the data transform.</span></span> <span data-ttu-id="493ab-134">Weitere Informationen finden Sie unter [Anzeigen der XML-Ausgabe von WinRM-Skripts](displaying-xml-output-from-winrm-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="493ab-134">For more information, see [Displaying XML Output from WinRM Scripts](displaying-xml-output-from-winrm-scripts.md).</span></span>


```VB
Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession()
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
strResponse = objSession.Get(strResource)
Set xmlFile = CreateObject("MSXml.DOMDocument")
Set xslFile = CreateObject("MSXml.DOMDocument")
xmlFile.LoadXml(strResponse)
xslFile.Load("WsmTxt.xsl")
Wscript.Echo xmlFile.TransformNode(xslFile)

```



## <a name="related-topics"></a><span data-ttu-id="493ab-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="493ab-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="493ab-136">Informationen zu Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="493ab-136">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="493ab-137">Verwenden von Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="493ab-137">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="493ab-138">Windows-Remoteverwaltung Referenz</span><span class="sxs-lookup"><span data-stu-id="493ab-138">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 