---
title: Bearbeiten der Windows 95-Registrierung
description: Sie können regedit verwenden, um die Windows 95-Registrierung zu bearbeiten und einen NSP zu bestimmen.
ms.assetid: 109daf4a-722f-4a25-a778-72360ee07ad9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c622ea44a5e365ca631d6d4db34af8e939ea6487
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856772"
---
# <a name="editing-the-windows-95-registry"></a><span data-ttu-id="c8df1-103">Bearbeiten der Windows 95-Registrierung</span><span class="sxs-lookup"><span data-stu-id="c8df1-103">Editing the Windows 95 Registry</span></span>

<span data-ttu-id="c8df1-104">Sie können regedit verwenden, um die Windows 95-Registrierung zu bearbeiten und einen NSP zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="c8df1-104">You can use REGEDIT to edit the Windows 95 registry to designate an NSP.</span></span>

<span data-ttu-id="c8df1-105">**So bestimmen Sie einen Microsoft Locator Name Service Provider für Windows 95**</span><span class="sxs-lookup"><span data-stu-id="c8df1-105">**To designate a Microsoft Locator name service provider for Windows 95**</span></span>

1.  <span data-ttu-id="c8df1-106">Select</span><span class="sxs-lookup"><span data-stu-id="c8df1-106">Select</span></span>

    <span data-ttu-id="c8df1-107">**HKEY \_ Software für den lokalen \_ Computer** \\  \\ **Microsoft** \\ **RPC**</span><span class="sxs-lookup"><span data-stu-id="c8df1-107">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Rpc**</span></span>

2.  <span data-ttu-id="c8df1-108">Erstellen Sie einen neuen Schlüssel mit dem Namen</span><span class="sxs-lookup"><span data-stu-id="c8df1-108">Create a new key called</span></span>

    <span data-ttu-id="c8df1-109">**NameService**</span><span class="sxs-lookup"><span data-stu-id="c8df1-109">**NameService**</span></span>

3.  <span data-ttu-id="c8df1-110">Wenn Sie den **Nameservice** -Schlüssel ausgewählt haben, erstellen Sie die neuen **StringValue** -Namen, und ändern Sie Sie so, dass Sie Daten enthalten, wie in der folgenden Tabelle</span><span class="sxs-lookup"><span data-stu-id="c8df1-110">With the **NameService** key selected, create the new **StringValue** names and modify them to contain data as shown in the following table.</span></span>

    

    | <span data-ttu-id="c8df1-111">Name</span><span class="sxs-lookup"><span data-stu-id="c8df1-111">Name</span></span>                     | <span data-ttu-id="c8df1-112">Daten</span><span class="sxs-lookup"><span data-stu-id="c8df1-112">Data</span></span>                                                                        |
    |--------------------------|-----------------------------------------------------------------------------|
    | <span data-ttu-id="c8df1-113">**Defaultsyntax**</span><span class="sxs-lookup"><span data-stu-id="c8df1-113">**DefaultSyntax**</span></span>        | <span data-ttu-id="c8df1-114">3</span><span class="sxs-lookup"><span data-stu-id="c8df1-114">3</span></span><br/>                                                                |
    | <span data-ttu-id="c8df1-115">**Protokoll**</span><span class="sxs-lookup"><span data-stu-id="c8df1-115">**Protocol**</span></span>             | <span data-ttu-id="c8df1-116">ncacn \_ NP</span><span class="sxs-lookup"><span data-stu-id="c8df1-116">ncacn\_np</span></span><br/>                                                        |
    | <span data-ttu-id="c8df1-117">**Endpunkt**</span><span class="sxs-lookup"><span data-stu-id="c8df1-117">**Endpoint**</span></span>             | <span data-ttu-id="c8df1-118">\\\\pipelocator</span><span class="sxs-lookup"><span data-stu-id="c8df1-118">\\pipe\\locator</span></span><br/>                                                  |
    | <span data-ttu-id="c8df1-119">**NetworkAddress**</span><span class="sxs-lookup"><span data-stu-id="c8df1-119">**NetworkAddress**</span></span>       | <span data-ttu-id="c8df1-120">MyServer (wobei MyServer der Name des Windows NT-Computers ist)</span><span class="sxs-lookup"><span data-stu-id="c8df1-120">myserver (where myserver is the name of the Windows NT computer)</span></span><br/> |
    | <span data-ttu-id="c8df1-121">**Servernetworkaddress**</span><span class="sxs-lookup"><span data-stu-id="c8df1-121">**ServerNetworkAddress**</span></span> | <span data-ttu-id="c8df1-122">MyServer</span><span class="sxs-lookup"><span data-stu-id="c8df1-122">myserver</span></span><br/>                                                         |

    

     

<span data-ttu-id="c8df1-123">Sie können regedit zum Bearbeiten der Windows 95-Registrierung verwenden, um einen DCE-CDs-NSP zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="c8df1-123">You can use REGEDIT to edit the Windows 95 registry to designate a DCE CDS NSP.</span></span>

<span data-ttu-id="c8df1-124">**So legen Sie einen DCE CDs Name Service Provider für Windows 95 fest**</span><span class="sxs-lookup"><span data-stu-id="c8df1-124">**To designate a DCE CDS name service provider for Windows 95**</span></span>

1.  <span data-ttu-id="c8df1-125">Select</span><span class="sxs-lookup"><span data-stu-id="c8df1-125">Select</span></span>

    <span data-ttu-id="c8df1-126">**HKEY \_ Software für den lokalen \_ Computer** \\  \\ **Microsoft** \\ **RPC**</span><span class="sxs-lookup"><span data-stu-id="c8df1-126">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Rpc**</span></span>

2.  <span data-ttu-id="c8df1-127">Erstellen Sie einen neuen Schlüssel mit dem Namen</span><span class="sxs-lookup"><span data-stu-id="c8df1-127">Create a new key called</span></span>

    <span data-ttu-id="c8df1-128">**NameService**</span><span class="sxs-lookup"><span data-stu-id="c8df1-128">**NameService**</span></span>

3.  <span data-ttu-id="c8df1-129">Wenn Sie den **Nameservice** -Schlüssel ausgewählt haben, erstellen Sie die neuen **StringValue** -Namen, und ändern Sie Sie so, dass Sie Daten enthalten, wie in der folgenden Tabelle</span><span class="sxs-lookup"><span data-stu-id="c8df1-129">With the **NameService** key selected, create the new **StringValue** names and modify them to contain data as shown in the following table.</span></span>

    

    | <span data-ttu-id="c8df1-130">Name</span><span class="sxs-lookup"><span data-stu-id="c8df1-130">Name</span></span>                     | <span data-ttu-id="c8df1-131">Daten</span><span class="sxs-lookup"><span data-stu-id="c8df1-131">Data</span></span>                                                             |
    |--------------------------|------------------------------------------------------------------|
    | <span data-ttu-id="c8df1-132">**Defaultsyntax**</span><span class="sxs-lookup"><span data-stu-id="c8df1-132">**DefaultSyntax**</span></span>        | <span data-ttu-id="c8df1-133">3</span><span class="sxs-lookup"><span data-stu-id="c8df1-133">3</span></span><br/>                                                     |
    | <span data-ttu-id="c8df1-134">**Protokoll**</span><span class="sxs-lookup"><span data-stu-id="c8df1-134">**Protocol**</span></span>             | <span data-ttu-id="c8df1-135">ncacn \_ IP \_ TCP</span><span class="sxs-lookup"><span data-stu-id="c8df1-135">ncacn\_ip\_tcp</span></span><br/>                                        |
    | <span data-ttu-id="c8df1-136">**Endpunkt**</span><span class="sxs-lookup"><span data-stu-id="c8df1-136">**Endpoint**</span></span>             | <span data-ttu-id="c8df1-137">"" (eine leere Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="c8df1-137">"" (an empty string)</span></span><br/>                                  |
    | <span data-ttu-id="c8df1-138">**NetworkAddress**</span><span class="sxs-lookup"><span data-stu-id="c8df1-138">**NetworkAddress**</span></span>       | <span data-ttu-id="c8df1-139">MyServer (der Name des Host Computers, auf dem die nsid ausgeführt wird)</span><span class="sxs-lookup"><span data-stu-id="c8df1-139">myserver (the name of the host computer running nsid)</span></span><br/> |
    | <span data-ttu-id="c8df1-140">**Servernetworkaddress**</span><span class="sxs-lookup"><span data-stu-id="c8df1-140">**ServerNetworkAddress**</span></span> | <span data-ttu-id="c8df1-141">MyServer (der Name des Host Computers, auf dem die nsid ausgeführt wird)</span><span class="sxs-lookup"><span data-stu-id="c8df1-141">myserver (the name of the host computer running nsid)</span></span><br/> |

    

     

    > [!Note]  
    > <span data-ttu-id="c8df1-142">Zum Konfigurieren der DCE-CDs als Name Service Provider muss das Produkt "DCE-Zell Verzeichnisdienst" der Digital Equipment Corporation vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="c8df1-142">You must have the Digital Equipment Corporation DCE Cell Directory Service product to configure the DCE CDS as your name service provider.</span></span> <span data-ttu-id="c8df1-143">Weitere Informationen zu DCE CDs finden Sie in der Dokumentation der Digital Equipment Corporation.</span><span class="sxs-lookup"><span data-stu-id="c8df1-143">See the documentation provided by Digital Equipment Corporation for information about DCE CDS.</span></span>

     

 

 





