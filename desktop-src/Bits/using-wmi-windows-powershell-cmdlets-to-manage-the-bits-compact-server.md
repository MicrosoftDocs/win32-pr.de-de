---
title: Verwenden von WMI-Windows PowerShell-Cmdlets zum Verwalten des BITS Compact-Servers
description: Windows PowerShell bietet einen einfachen Mechanismus zum Herstellen einer Verbindung mit Windows-Verwaltungsinstrumentation (WMI) auf einem Remote Computer und zum Verwalten des Background Intelligent Transfer Service (Bits) Compact-Servers.
ms.assetid: fe174d2f-4ca0-431e-b1b8-1893ec54147a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c3c942672c147ec5daa0caa2a370e487be80809
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948910"
---
# <a name="using-wmi-windows-powershell-cmdlets-to-manage-the-bits-compact-server"></a><span data-ttu-id="6155f-103">Verwenden von WMI-Windows PowerShell-Cmdlets zum Verwalten des BITS Compact-Servers</span><span class="sxs-lookup"><span data-stu-id="6155f-103">Using WMI Windows PowerShell Cmdlets to Manage the BITS Compact Server</span></span>

<span data-ttu-id="6155f-104">Windows PowerShell bietet einen einfachen Mechanismus zum Herstellen einer Verbindung mit Windows-Verwaltungsinstrumentation (WMI) auf einem Remote Computer und zum Verwalten des Background Intelligent Transfer Service (Bits) Compact-Servers.</span><span class="sxs-lookup"><span data-stu-id="6155f-104">Windows PowerShell provides a simple mechanism to connect to Windows Management Instrumentation (WMI) on a remote computer and manage the Background Intelligent Transfer Service (BITS) Compact Server.</span></span> <span data-ttu-id="6155f-105">Der BITS Compact-Server ist eine optionale Serverkomponente, die separat installiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="6155f-105">The BITS Compact Server is an optional server component that must be installed separately.</span></span> <span data-ttu-id="6155f-106">Informationen zum Installieren des Compact-Servers finden Sie in der Dokumentation zu [BITS Compact Server](bits-compact-server.md) .</span><span class="sxs-lookup"><span data-stu-id="6155f-106">For information about installing the Compact Server, see the [BITS Compact Server](bits-compact-server.md) documentation.</span></span>

1.  <span data-ttu-id="6155f-107">Stellen Sie eine Verbindung zum Bits-Anbieter her.</span><span class="sxs-lookup"><span data-stu-id="6155f-107">Connect to the BITS provider.</span></span>

    ```PowerShell
    $cred = Get-Credential
    $bcs = Get-WmiObject -Namespace "root\Microsoft\BITS" -Class "BITSCompactServerUrlGroup" `
    -List -ComputerName Server1 -Credential $cred
    ```

    

    <span data-ttu-id="6155f-108">Das [Get-Credential-](/previous-versions//dd315327(v=technet.10)) Cmdlet fordert die Anmelde Informationen des Benutzers auf, um eine Verbindung mit dem Remote Computer herzustellen, und weist die Anmelde Informationen dem $cred-Objekt zu.</span><span class="sxs-lookup"><span data-stu-id="6155f-108">The [Get-Credential](/previous-versions//dd315327(v=technet.10)) cmdlet requests the user's credentials to connect to the remote computer and assigns the credentials to the $cred object.</span></span>

    <span data-ttu-id="6155f-109">Die vom [Get-WMIObject-](/previous-versions//dd315295(v=technet.10)) Cmdlet zurückgegebenen Objekte werden der $BCS Variablen zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="6155f-109">The objects returned by the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) cmdlet are assigned to the $bcs variable.</span></span> <span data-ttu-id="6155f-110">Im vorherigen Beispiel ruft das [Get-WMIObject-](/previous-versions//dd315295(v=technet.10)) Cmdlet die [BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) -Klasse im Microsoft Bits- \\ Stamm \\ Namespace von Server1 ab.</span><span class="sxs-lookup"><span data-stu-id="6155f-110">In the preceding example, the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) cmdlet retrieves the [BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) class in the root\\Microsoft\\BITS namespace of Server1.</span></span> <span data-ttu-id="6155f-111">Statische Methoden, die von der [BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) -Klasse verfügbar gemacht werden, können für das $BCS Objekt aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="6155f-111">Static methods exposed by the [BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) class can be called on the $bcs object.</span></span> <span data-ttu-id="6155f-112">Weitere Informationen zur Bits-Remote Verwaltung finden Sie unter [Bits-Anbieter](/previous-versions/windows/desktop/bitsprov/bits-provider) -und Bits- [Anbieter Klassen]( /previous-versions//dd904507(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6155f-112">For more information about BITS remote management, see [BITS provider](/previous-versions/windows/desktop/bitsprov/bits-provider) and [BITS provider classes]( /previous-versions//dd904507(v=vs.85)).</span></span>

    > [!Note]  
    > <span data-ttu-id="6155f-113">Das Zeichen mit einem Doppel Akzent ( \` ) wird verwendet, um einen Zeilenumbruch anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6155f-113">The grave-accent character (\`) is used to indicate a line break.</span></span>

     

2.  <span data-ttu-id="6155f-114">Erstellen Sie eine URL-Gruppe auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="6155f-114">Create a URL group on the server.</span></span>

    ```PowerShell
    $URLGroup = "https://Server1:80/testurlgroup" 
    $bcs.CreateUrlGroup($URLGroup)
    ```

    

    <span data-ttu-id="6155f-115">Die https://Server1:80/testurlgroup URL-Präfix Zeichenfolge "" wird der $URLGroup Variablen zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="6155f-115">The "https://Server1:80/testurlgroup" URL prefix string is assigned to the $URLGroup variable.</span></span> <span data-ttu-id="6155f-116">Die $URLGroup Variable wird an die Methode " [kreateurlgroup](/previous-versions/windows/desktop/bitsprov/createurlgroup-bitslightweightserverurlgroup) " übergeben, die die URL-Gruppe auf Server1 erstellt.</span><span class="sxs-lookup"><span data-stu-id="6155f-116">The $URLGroup variable is passed to the [CreateUrlGroup](/previous-versions/windows/desktop/bitsprov/createurlgroup-bitslightweightserverurlgroup) method, which creates the URL group on Server1.</span></span>

    <span data-ttu-id="6155f-117">Sie können eine andere URL-Gruppe angeben.</span><span class="sxs-lookup"><span data-stu-id="6155f-117">You can specify a different URL group.</span></span> <span data-ttu-id="6155f-118">Die URL-Gruppe muss einer gültigen URL-Präfix Zeichenfolge entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6155f-118">The URL group must conform to a valid URL prefix string.</span></span> <span data-ttu-id="6155f-119">Weitere Informationen zu URL-Präfixen finden Sie unter [URLPrefix](../http/urlprefix-strings.md)-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="6155f-119">For more information about URL prefixes, see [UrlPrefix Strings](../http/urlprefix-strings.md).</span></span>

3.  <span data-ttu-id="6155f-120">Hosten Sie eine Datei in der URL-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="6155f-120">Host a file on the URL group.</span></span>

    ```PowerShell
    $bcsObj = Get-WmiObject -Namespace "root\Microsoft\BITS" -Class "BITSCompactServerUrlGroup" -filter ("UrlGroup='" + $URLGroup + "'") -ComputerName Server1 -Credential $cred
    $bcsObj.CreateURL("url.txt", "c:\\temp\\1.txt", "") -ComputerName Server1 -Credential $cred
    ```

    

    <span data-ttu-id="6155f-121">Die BITSCompactServerUrlGroup-Instanz, die vom [Get-WMIObject](/previous-versions//dd315295(v=technet.10)) -Cmdlet zurückgegeben wird, wird der $bcsObj-Variablen zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="6155f-121">The BITSCompactServerUrlGroup instance returned by the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) cmdlet is assigned to the $bcsObj variable.</span></span> <span data-ttu-id="6155f-122">Die Methode " [kreateurl](/previous-versions/windows/desktop/bitsprov/createurl-bitslightweightserverurlgroup) " wird für die $bcsObj mit dem URL-Suffix "url.txt", dem Quellpfad "c: \\ \\ Temp \\ \\1.txt" für die Datei und einer leeren Sicherheits beschreibungerzeichenfolge als Parameter aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="6155f-122">The [CreateUrl](/previous-versions/windows/desktop/bitsprov/createurl-bitslightweightserverurlgroup) method is called for the $bcsObj with the "url.txt" URL suffix, the "c:\\\\temp\\\\1.txt" source path for the file, and an empty security descriptor string as parameters.</span></span> <span data-ttu-id="6155f-123">Das Suffix "url.txt" wird dem URL-Gruppen Präfix hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6155f-123">The "url.txt" suffix is added to the URL group prefix.</span></span> <span data-ttu-id="6155f-124">Clients können die Datei von folgender Adresse herunterladen: https://Server1:80/testurlgroup/url.txt .</span><span class="sxs-lookup"><span data-stu-id="6155f-124">Clients can download the file from the following address: https://Server1:80/testurlgroup/url.txt.</span></span>

4.  <span data-ttu-id="6155f-125">Bereinigen Sie die URL und die URL-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="6155f-125">Clean up the URL and the URL group.</span></span>

    ```PowerShell
    $bcsObj.Delete()
    ```

    

    <span data-ttu-id="6155f-126">Die " **System. Object DELETE** "-Methode löscht das $bcsObj Objekt.</span><span class="sxs-lookup"><span data-stu-id="6155f-126">The **system.object Delete** method deletes the $bcsObj object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6155f-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6155f-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6155f-128">BITS Compact Server</span><span class="sxs-lookup"><span data-stu-id="6155f-128">BITS Compact Server</span></span>](./bits-compact-server.md)
</dt> <dt>

[<span data-ttu-id="6155f-129">Bits-Anbieter</span><span class="sxs-lookup"><span data-stu-id="6155f-129">BITS provider</span></span>](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> <dt>

<span data-ttu-id="6155f-130">[Bits-Anbieter Klassen]( /previous-versions//dd904507(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6155f-130">[BITS provider classes]( /previous-versions//dd904507(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="6155f-131">[Get-Credential](/previous-versions//dd315327(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="6155f-131">[Get-Credential](/previous-versions//dd315327(v=technet.10))</span></span>
</dt> <dt>

<span data-ttu-id="6155f-132">[Get-WmiObject](/previous-versions//dd315295(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="6155f-132">[Get-WmiObject](/previous-versions//dd315295(v=technet.10))</span></span>
</dt> </dl>

 

 