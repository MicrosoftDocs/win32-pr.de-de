---
description: Zeigt, wie die IThumbnailProvider-Schnittstelle verwendet wird, um die Miniaturansicht für ein Element aus dem Windows-Miniatur Ansichts Cachesystem zu extrahieren.
title: Verwenden von Miniaturansichtenanbieter (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: B5E4145A-AF9D-4b83-923A-2DC064B66E8E
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7e0cab8db27ddfdca0db5a7a08b6329c44776fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980240"
---
# <a name="using-thumbnail-providers-sample"></a><span data-ttu-id="6d889-103">Verwenden von Miniaturansichtenanbieter (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="6d889-103">Using Thumbnail Providers Sample</span></span>

<span data-ttu-id="6d889-104">Zeigt, wie die [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) -Schnittstelle verwendet wird, um die Miniaturansicht für ein Element aus dem Windows-Miniatur Ansichts Cachesystem zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="6d889-104">Demonstrates how to use the [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) interface to extract the thumbnail for an item from the Windows thumbnail cache system.</span></span>

<span data-ttu-id="6d889-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="6d889-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="6d889-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d889-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="6d889-107">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="6d889-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="6d889-108">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="6d889-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="6d889-109">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="6d889-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="6d889-110">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="6d889-110">Requirements</span></span>



| <span data-ttu-id="6d889-111">Produkt</span><span class="sxs-lookup"><span data-stu-id="6d889-111">Product</span></span>                                | <span data-ttu-id="6d889-112">Minimale Produkt Version</span><span class="sxs-lookup"><span data-stu-id="6d889-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="6d889-113">Windows</span><span class="sxs-lookup"><span data-stu-id="6d889-113">Windows</span></span>                                | <span data-ttu-id="6d889-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6d889-114">Windows Vista</span></span>           |
| <span data-ttu-id="6d889-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="6d889-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="6d889-116">6.1</span><span class="sxs-lookup"><span data-stu-id="6d889-116">6.1</span></span>                     |



 

<span data-ttu-id="6d889-117">Weitere Anforderungen finden Sie in der im Beispiel enthaltenen Infodatei.</span><span class="sxs-lookup"><span data-stu-id="6d889-117">For additional requirements, see the Readme file included with the sample.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="6d889-118">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="6d889-118">Downloading the Sample</span></span>

| <span data-ttu-id="6d889-119">Standort</span><span class="sxs-lookup"><span data-stu-id="6d889-119">Location</span></span>      | <span data-ttu-id="6d889-120">Pfad-URL</span><span class="sxs-lookup"><span data-stu-id="6d889-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d889-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="6d889-121">GitHub</span></span>  | [<span data-ttu-id="6d889-122">Usingthumbnailproviders-Beispiel</span><span class="sxs-lookup"><span data-stu-id="6d889-122">UsingThumbnailProviders sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/UsingThumbnailProviders) |

## <a name="building-the-sample"></a><span data-ttu-id="6d889-123">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="6d889-123">Building the Sample</span></span>

<span data-ttu-id="6d889-124">Anweisungen zum Erstellen des Beispiels finden Sie in der im Beispiel enthaltenen Infodatei.</span><span class="sxs-lookup"><span data-stu-id="6d889-124">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="6d889-125">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="6d889-125">Running the Sample</span></span>

<span data-ttu-id="6d889-126">Anweisungen zum Erstellen des Beispiels finden Sie in der im Beispiel enthaltenen Infodatei.</span><span class="sxs-lookup"><span data-stu-id="6d889-126">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

 

 



