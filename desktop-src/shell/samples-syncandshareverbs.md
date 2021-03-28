---
description: Veranschaulicht, wie ein Verb, das den 0034 &erweitert, registriert wird \# . Synchronisieren&\# 0034; und &\# 0034; Freigeben von&\# 0034; Verben in der Windows-Explorer-Befehlsleiste.
title: Synchronisieren und Freigeben von Verben
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 78267C74-7597-4b98-9DAE-89F2FD515C6B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 734d59ce7b527ad068c03be9083ca67dfca20667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980752"
---
# <a name="sync-and-share-verbs"></a><span data-ttu-id="2f028-103">Synchronisieren und Freigeben von Verben</span><span class="sxs-lookup"><span data-stu-id="2f028-103">Sync and Share Verbs</span></span>

<span data-ttu-id="2f028-104">Veranschaulicht das Registrieren eines Verbs, das die Verben "Sync" und "Share" in der Windows-Explorer-Befehlsleiste erweitert.</span><span class="sxs-lookup"><span data-stu-id="2f028-104">Demonstrates how to register a verb that extends the "Sync" and "Share" verbs in the Windows Explorer Command Bar.</span></span>

<span data-ttu-id="2f028-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="2f028-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="2f028-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f028-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="2f028-107">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="2f028-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="2f028-108">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="2f028-108">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="2f028-109">Entfernen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="2f028-109">Removing the Sample</span></span>](#removing-the-sample)

## <a name="requirements"></a><span data-ttu-id="2f028-110">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="2f028-110">Requirements</span></span>



| <span data-ttu-id="2f028-111">Produkt</span><span class="sxs-lookup"><span data-stu-id="2f028-111">Product</span></span>                                | <span data-ttu-id="2f028-112">Minimale Produkt Version</span><span class="sxs-lookup"><span data-stu-id="2f028-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="2f028-113">Windows</span><span class="sxs-lookup"><span data-stu-id="2f028-113">Windows</span></span>                                | <span data-ttu-id="2f028-114">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2f028-114">Windows 7</span></span>               |
| <span data-ttu-id="2f028-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="2f028-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="2f028-116">7.0</span><span class="sxs-lookup"><span data-stu-id="2f028-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="2f028-117">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="2f028-117">Downloading the Sample</span></span>

| <span data-ttu-id="2f028-118">Standort</span><span class="sxs-lookup"><span data-stu-id="2f028-118">Location</span></span>      | <span data-ttu-id="2f028-119">Pfad-URL</span><span class="sxs-lookup"><span data-stu-id="2f028-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f028-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="2f028-120">GitHub</span></span>  | [<span data-ttu-id="2f028-121">Syncandshareverbs-Beispiel</span><span class="sxs-lookup"><span data-stu-id="2f028-121">SyncAndShareVerbs sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/SyncAndShareVerbs) |

## <a name="running-the-sample"></a><span data-ttu-id="2f028-122">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="2f028-122">Running the Sample</span></span>

<span data-ttu-id="2f028-123">So führen Sie das Beispiel aus (Sync):</span><span class="sxs-lookup"><span data-stu-id="2f028-123">To run the sample (sync):</span></span>

1.  <span data-ttu-id="2f028-124">Navigieren Sie zu dem Verzeichnis, das die Datei enthält. `sync.reg`</span><span class="sxs-lookup"><span data-stu-id="2f028-124">Navigate to the directory that contains the `sync.reg` file</span></span>
2.  <span data-ttu-id="2f028-125">Geben Sie `sync.reg ` in der Befehlszeile ein, oder Doppelklicken Sie auf das Symbol, um `sync.reg` es zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="2f028-125">Type `sync.reg ` at the command line, or double-click the icon for `sync.reg` register it.</span></span>
3.  <span data-ttu-id="2f028-126">Öffnen Sie den Windows-Explorer, und wählen Sie eine Datei aus.</span><span class="sxs-lookup"><span data-stu-id="2f028-126">Open the Windows Explorer and select a file.</span></span>
4.  <span data-ttu-id="2f028-127">Klicken Sie in der Befehlsleiste auf die Option **Synchronisieren** , und wählen Sie eine unter Option wie **Paint** aus.</span><span class="sxs-lookup"><span data-stu-id="2f028-127">Click the **Sync** option in the Command Bar and select a suboption such as **Paint**.</span></span>

<span data-ttu-id="2f028-128">So führen Sie das Beispiel (Freigabe) aus:</span><span class="sxs-lookup"><span data-stu-id="2f028-128">To run the sample (share):</span></span>

1.  <span data-ttu-id="2f028-129">Navigieren Sie zu dem Verzeichnis, das die `share.reg` Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="2f028-129">Navigate to the directory that contains the `share.reg` file.</span></span>
2.  <span data-ttu-id="2f028-130">Geben Sie `share.reg` in der Befehlszeile ein, oder Doppelklicken Sie auf das Symbol, um `share.reg` es zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="2f028-130">Type `share.reg` at the command line, or double-click the icon for `share.reg` register it.</span></span>
3.  <span data-ttu-id="2f028-131">Öffnen Sie Windows Explorer, und wählen Sie eine Datei aus.</span><span class="sxs-lookup"><span data-stu-id="2f028-131">Open Windows Explorer and select a file.</span></span> <span data-ttu-id="2f028-132">Klicken Sie in der Befehlsleiste auf die Option **Freigeben** .</span><span class="sxs-lookup"><span data-stu-id="2f028-132">Click the **Share** option in the Command Bar.</span></span>
4.  <span data-ttu-id="2f028-133">Klicken Sie in der Befehlsleiste auf die Option **Freigeben mit** , und wählen Sie eine unter Option wie **Paint** aus.</span><span class="sxs-lookup"><span data-stu-id="2f028-133">Click the **Share with** option in the Command Bar and select a suboption such as **Paint**.</span></span>

## <a name="removing-the-sample"></a><span data-ttu-id="2f028-134">Entfernen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="2f028-134">Removing the Sample</span></span>

<span data-ttu-id="2f028-135">So entfernen Sie das Beispiel (Sync):</span><span class="sxs-lookup"><span data-stu-id="2f028-135">To remove the sample (sync):</span></span>

1.  <span data-ttu-id="2f028-136">Navigieren Sie zu dem Verzeichnis, das die Datei "uninstallsync. reg" enthält.</span><span class="sxs-lookup"><span data-stu-id="2f028-136">Navigate to the directory that contains the Uninstallsync.reg file.</span></span>
2.  <span data-ttu-id="2f028-137">Geben `uninstallsync.reg` Sie in der Befehlszeile ein, oder Doppelklicken Sie auf das Symbol für `uninstallsync.reg` .</span><span class="sxs-lookup"><span data-stu-id="2f028-137">Type `uninstallsync.reg` at the command line, or double-click the icon for `uninstallsync.reg`.</span></span>

<span data-ttu-id="2f028-138">So entfernen Sie das Beispiel (Freigabe):</span><span class="sxs-lookup"><span data-stu-id="2f028-138">To remove the sample (share):</span></span>

1.  <span data-ttu-id="2f028-139">Navigieren Sie zu dem Verzeichnis, das die Datei "uninstallshare. reg" enthält.</span><span class="sxs-lookup"><span data-stu-id="2f028-139">Navigate to the directory that contains the Uninstallshare.reg file.</span></span>
2.  <span data-ttu-id="2f028-140">Geben `uninstallshare.reg` Sie in der Befehlszeile ein, oder Doppelklicken Sie auf das Symbol für. `uninstallshare.reg.`</span><span class="sxs-lookup"><span data-stu-id="2f028-140">Type `uninstallshare.reg` at the command line, or double-click the icon for `uninstallshare.reg.`</span></span>

 

 



