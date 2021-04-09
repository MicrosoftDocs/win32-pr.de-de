---
title: BITS Compact Server
description: Der Background Intelligent Transfer Service (Bits) Compact Server ist ein eigenständiger HTTP/HTTPS-Dateiserver, der die Möglichkeit bietet, eine begrenzte Anzahl von großen Dateien asynchron zwischen Computern zu übertragen.
ms.assetid: ab4cf901-6d93-433c-b1b2-ffa54d10725c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b40e2840c24e15379fac11a5a12ed76c225e7be5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858370"
---
# <a name="bits-compact-server"></a><span data-ttu-id="e0c20-103">BITS Compact Server</span><span class="sxs-lookup"><span data-stu-id="e0c20-103">BITS Compact Server</span></span>

<span data-ttu-id="e0c20-104">Der Background Intelligent Transfer Service (Bits) Compact Server ist ein eigenständiger HTTP/HTTPS-Dateiserver, der die Möglichkeit bietet, eine begrenzte Anzahl von großen Dateien asynchron zwischen Computern zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="e0c20-104">The Background Intelligent Transfer Service (BITS) Compact Server is a stand-alone HTTP/HTTPS file server that provides the ability to transfer a limited number of large files asynchronously between computers.</span></span> <span data-ttu-id="e0c20-105">Der Compact Server wird als NT-Dienst erstellt und verwendet HTTP.SYS.</span><span class="sxs-lookup"><span data-stu-id="e0c20-105">The Compact Server is built as an NT Service and uses HTTP.SYS.</span></span>

<span data-ttu-id="e0c20-106">Der BITS Compact-Server ist für die Verwendung durch Kunden von Unternehmen und Kleinunternehmen unter folgenden Bedingungen bestimmt:</span><span class="sxs-lookup"><span data-stu-id="e0c20-106">The BITS Compact Server is intended for use by enterprise and small business customers under the following conditions:</span></span>

-   <span data-ttu-id="e0c20-107">Die erwartete Verwendung beträgt maximal 25 URL-Gruppen, und jede URL-Gruppe unterstützt drei gleichzeitige Dateiübertragungen.</span><span class="sxs-lookup"><span data-stu-id="e0c20-107">The anticipated usage is a maximum of 25 URL groups, and each URL group supports 3 simultaneous file transfers.</span></span>
-   <span data-ttu-id="e0c20-108">Dateiübertragungen erfolgen zwischen Computern in derselben Domäne oder in sich gegenseitig vertrauenswürdigen Domänen.</span><span class="sxs-lookup"><span data-stu-id="e0c20-108">File transfers occur between computers in the same domain or mutually trusted domains.</span></span>
-   <span data-ttu-id="e0c20-109">Dateiübertragungen sind nicht für Clients mit Internet Zugriff vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="e0c20-109">File transfers are not intended for Internet-facing clients.</span></span>

## <a name="installing-the-bits-compact-server"></a><span data-ttu-id="e0c20-110">Installieren des BITS Compact-Servers</span><span class="sxs-lookup"><span data-stu-id="e0c20-110">Installing the BITS Compact Server</span></span>

<span data-ttu-id="e0c20-111">Der BITS Compact-Server ist eine optionale Serverkomponente.</span><span class="sxs-lookup"><span data-stu-id="e0c20-111">The BITS Compact Server is an optional server component.</span></span> <span data-ttu-id="e0c20-112">Sie können eine der folgenden Optionen verwenden, um den BITS Compact-Server zu installieren:</span><span class="sxs-lookup"><span data-stu-id="e0c20-112">You can use one of the following options to install the BITS Compact Server:</span></span>

-   <span data-ttu-id="e0c20-113">Server-Manager</span><span class="sxs-lookup"><span data-stu-id="e0c20-113">Server Manager</span></span>

-   <span data-ttu-id="e0c20-114">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="e0c20-114">Windows PowerShell</span></span>

-   <span data-ttu-id="e0c20-115">Paket-Manager</span><span class="sxs-lookup"><span data-stu-id="e0c20-115">Package Manager</span></span>

<span data-ttu-id="e0c20-116">**So installieren Sie den BITS Compact-Server mithilfe von Server-Manager**</span><span class="sxs-lookup"><span data-stu-id="e0c20-116">**To install the BITS Compact Server by using Server Manager**</span></span>

1.  <span data-ttu-id="e0c20-117">Klicken Sie im Abschnitt " **featurezusammenfassung** " des **Server-Manager** auf **Features hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="e0c20-117">In the **Features Summary** section of the **Server Manager**, click **Add Features**.</span></span>
2.  <span data-ttu-id="e0c20-118">Wählen Sie im Assistenten zum Hinzufügen von Features **Background Intelligent Transfer Service (Bits)** und **Compact Server** aus.</span><span class="sxs-lookup"><span data-stu-id="e0c20-118">In the Add Features Wizard, select **Background Intelligent Transfer Service (BITS)** and **Compact Server**.</span></span>
3.  <span data-ttu-id="e0c20-119">Befolgen Sie die Anweisungen des Assistenten, einschließlich der Installation der erforderlichen Software, falls angegeben.</span><span class="sxs-lookup"><span data-stu-id="e0c20-119">Follow the wizard instructions, including installing the required software if indicated.</span></span>

<span data-ttu-id="e0c20-120">Weitere Informationen finden Sie in der **Server-Manager** -Online Hilfe.</span><span class="sxs-lookup"><span data-stu-id="e0c20-120">For more information, see the **Server Manager** online help.</span></span>

<span data-ttu-id="e0c20-121">**So installieren Sie den BITS Compact-Server mithilfe von Windows PowerShell**</span><span class="sxs-lookup"><span data-stu-id="e0c20-121">**To install the BITS Compact Server by using Windows PowerShell**</span></span>

1.  <span data-ttu-id="e0c20-122">Geben Sie an einer Windows PowerShell-Eingabeaufforderung den folgenden Befehl ein: **Import-Module Server Manager**.</span><span class="sxs-lookup"><span data-stu-id="e0c20-122">In a Windows PowerShell command prompt, type the following command: **Import-Module ServerManager**.</span></span> <span data-ttu-id="e0c20-123">Drücken Sie dann die Eingabetaste.</span><span class="sxs-lookup"><span data-stu-id="e0c20-123">Then press Enter.</span></span>
2.  <span data-ttu-id="e0c20-124">Geben Sie den folgenden Befehl ein: **Add-Windows Feature BITS-Compact-Server**.</span><span class="sxs-lookup"><span data-stu-id="e0c20-124">Type the following command: **Add-WindowsFeature BITS-Compact-Server**.</span></span> <span data-ttu-id="e0c20-125">Drücken Sie dann die Eingabetaste.</span><span class="sxs-lookup"><span data-stu-id="e0c20-125">Then press Enter.</span></span>

<span data-ttu-id="e0c20-126">Im folgenden textbasierten Beispiel wird die Installation des BITS Compact-Servers mithilfe von Windows PowerShell-Cmdlets veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="e0c20-126">The following text-based example demonstrates installing the BITS Compact Server using Windows PowerShell cmdlets.</span></span>

``` syntax
PS C:\> Import-Module ServerManager
PS C:\> Add-WindowsFeature BITS-Compact-Server

Success Restart Needed Exit Code Feature Result
------- -------------- --------- --------------
True    No             Success   {Compact Server}


PS C:\>
```

<span data-ttu-id="e0c20-127">Weitere Informationen zur Verwendung von Cmdlets finden Sie in der [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) -Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="e0c20-127">For information about using cmdlets, see the [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) documentation.</span></span>

<span data-ttu-id="e0c20-128">Weitere Informationen zum Cmdlet "Import-Module" finden Sie unter " [Import-Module](/previous-versions//dd347701(v=technet.10)) " in der Microsoft TechNet-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="e0c20-128">For more information about the Import-Module cmdlet, see [Import-Module](/previous-versions//dd347701(v=technet.10)) in the Microsoft TechNet Library.</span></span> <span data-ttu-id="e0c20-129">Um Hilfe in der Befehlszeile zu erhalten, geben **Sie Get-Help Import-Module** ein.</span><span class="sxs-lookup"><span data-stu-id="e0c20-129">For help at the command line, type **get-help import-module**.</span></span>

<span data-ttu-id="e0c20-130">Weitere Informationen zum Cmdlet "Add-WindowsFeature" finden [Sie unter Add-Windows Feature](/previous-versions//dd347701(v=technet.10)) in der Microsoft TechNet-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="e0c20-130">For more information about the Add-WindowsFeature cmdlet, see [Add-WindowsFeature](/previous-versions//dd347701(v=technet.10)) in the Microsoft TechNet Library.</span></span> <span data-ttu-id="e0c20-131">Um Hilfe in der Befehlszeile zu erhalten, geben **Sie Get-Help Add-Windows Feature** ein.</span><span class="sxs-lookup"><span data-stu-id="e0c20-131">For help at the command line, type **get-help Add-WindowsFeature**.</span></span>

<span data-ttu-id="e0c20-132">**So installieren Sie den BITS Compact-Server mithilfe des Paket-Managers**</span><span class="sxs-lookup"><span data-stu-id="e0c20-132">**To install the BITS Compact Server by using Package Manager**</span></span>

-   <span data-ttu-id="e0c20-133">Geben Sie den folgenden Befehl ein: **PkgMgr.exe/IU: lightweightserver**.</span><span class="sxs-lookup"><span data-stu-id="e0c20-133">Enter the following command: **PkgMgr.exe /iu:LightweightServer**.</span></span>

> [!Note]  
> <span data-ttu-id="e0c20-134">Die Einstellungen gehen verloren, wenn der Compact Server-Dienst neu gestartet wird oder wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="e0c20-134">The settings are lost if the Compact Server service is restarted or if the computer is rebooted.</span></span>

 

## <a name="bits-compact-server-remote-management"></a><span data-ttu-id="e0c20-135">BITS Compact Server-Remote Verwaltung</span><span class="sxs-lookup"><span data-stu-id="e0c20-135">BITS Compact Server Remote Management</span></span>

<span data-ttu-id="e0c20-136">Der BITS Compact-Server mit Bits-Remote Verwaltung ermöglicht sicherere Remote Dateiübertragungen.</span><span class="sxs-lookup"><span data-stu-id="e0c20-136">The BITS Compact Server with BITS Remote Management enables more secure remote file transfers.</span></span> <span data-ttu-id="e0c20-137">Die Bits-Remote Verwaltung verwendet einen Windows-Verwaltungsinstrumentation (WMI)-Anbieter, um einem Systemadministrator oder einer Controller Anwendung das Remote Erstellen von Bits-Übertragungs Aufträgen auf den Clients und das Veröffentlichen von Dateien für das Hosting auf dem BITS Compact-Server zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="e0c20-137">BITS Remote Management uses a Windows Management Instrumentation (WMI) provider to let a system administrator or a controller application remotely create BITS transfer jobs on the clients and to publish files for hosting on the BITS Compact Server.</span></span> <span data-ttu-id="e0c20-138">Der Bits-Anbieter kann auch verwendet werden, um einer Anwendung die Remote Verwendung des BITS-Clients in Verbindung mit dem BITS Compact-Server zu ermöglichen, um Dateien von einem Remote Computer auf einen anderen Remote Computer zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="e0c20-138">The BITS provider can also be used to enable an application to remotely use the BITS client in conjunction with the BITS Compact Server to transfer files from one remote computer to another remote computer.</span></span>

<span data-ttu-id="e0c20-139">Weitere Informationen finden Sie in der Dokumentation zum [Bits-Anbieter](/previous-versions/windows/desktop/bitsprov/bits-provider) .</span><span class="sxs-lookup"><span data-stu-id="e0c20-139">For more information, see the [BITS provider](/previous-versions/windows/desktop/bitsprov/bits-provider) documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0c20-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e0c20-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0c20-141">Bits-Anbieter</span><span class="sxs-lookup"><span data-stu-id="e0c20-141">BITS provider</span></span>](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> </dl>

 

 