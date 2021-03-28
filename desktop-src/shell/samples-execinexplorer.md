---
description: Veranschaulicht, wie die ShellExecute-Funktion aus dem Windows-Explorer-Prozess aufgerufen wird.
title: In Explorer ausführen (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: D307B22A-E4A3-4215-B28E-F48A721260A1
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7a511f7ccc7edd218edd405de163501afd530f46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979849"
---
# <a name="execute-in-explorer-sample"></a><span data-ttu-id="d0697-103">In Explorer ausführen (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="d0697-103">Execute In Explorer Sample</span></span>

<span data-ttu-id="d0697-104">Veranschaulicht, wie die [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) -Funktion aus dem Windows-Explorer-Prozess aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d0697-104">Demonstrates how to call the [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) function from the Windows Explorer process.</span></span> <span data-ttu-id="d0697-105">Dies ist nützlich, wenn ein Prozess ohne erhöhte Rechte von einem Prozess mit erhöhten Rechten gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="d0697-105">This is useful when launching an unelevated process from an elevated process.</span></span>

<span data-ttu-id="d0697-106">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="d0697-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="d0697-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d0697-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="d0697-108">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="d0697-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="d0697-109">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="d0697-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="d0697-110">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="d0697-110">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="d0697-111">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="d0697-111">Requirements</span></span>



| <span data-ttu-id="d0697-112">Produkt</span><span class="sxs-lookup"><span data-stu-id="d0697-112">Product</span></span>                                | <span data-ttu-id="d0697-113">Minimale Produkt Version</span><span class="sxs-lookup"><span data-stu-id="d0697-113">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="d0697-114">Windows</span><span class="sxs-lookup"><span data-stu-id="d0697-114">Windows</span></span>                                | <span data-ttu-id="d0697-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d0697-115">Windows Vista</span></span>           |
| <span data-ttu-id="d0697-116">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="d0697-116">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="d0697-117">7.0</span><span class="sxs-lookup"><span data-stu-id="d0697-117">7.0</span></span>                     |



 

<span data-ttu-id="d0697-118">Weitere Anforderungen finden Sie in der im Beispiel enthaltenen Infodatei.</span><span class="sxs-lookup"><span data-stu-id="d0697-118">For additional requirements, see the Readme file included with the sample.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="d0697-119">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="d0697-119">Downloading the Sample</span></span>

| <span data-ttu-id="d0697-120">Standort</span><span class="sxs-lookup"><span data-stu-id="d0697-120">Location</span></span>      | <span data-ttu-id="d0697-121">Pfad-URL</span><span class="sxs-lookup"><span data-stu-id="d0697-121">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0697-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="d0697-122">GitHub</span></span>  | [<span data-ttu-id="d0697-123">Execinexplorer-Beispiel</span><span class="sxs-lookup"><span data-stu-id="d0697-123">ExecInExplorer sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/ExecInExplorer) |

## <a name="building-the-sample"></a><span data-ttu-id="d0697-124">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="d0697-124">Building the Sample</span></span>

<span data-ttu-id="d0697-125">Anweisungen zum Erstellen des Beispiels finden Sie in der im Beispiel enthaltenen Infodatei.</span><span class="sxs-lookup"><span data-stu-id="d0697-125">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="d0697-126">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="d0697-126">Running the Sample</span></span>

<span data-ttu-id="d0697-127">Anweisungen zum Erstellen des Beispiels finden Sie in der im Beispiel enthaltenen Infodatei.</span><span class="sxs-lookup"><span data-stu-id="d0697-127">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

 

 



