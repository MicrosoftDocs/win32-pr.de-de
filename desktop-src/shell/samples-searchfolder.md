---
description: Veranschaulicht, wie mit dem shellprogrammierungs Modell eine Suche mit Abfrage Einschränkungen erstellt wird.
title: Suchordner (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: DF3432AB-39DF-44c6-9A08-4630408D6B9B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c86a29c4a7d01fad3b91db20035cb84751e0b78a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216986"
---
# <a name="search-folder-sample"></a><span data-ttu-id="84dec-103">Suchordner (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="84dec-103">Search Folder Sample</span></span>

<span data-ttu-id="84dec-104">Veranschaulicht, wie mit dem shellprogrammierungs Modell eine Suche mit Abfrage Einschränkungen erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="84dec-104">Demonstrates how to create a search with query constraints using the Shell programming model.</span></span>

<span data-ttu-id="84dec-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="84dec-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="84dec-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="84dec-106">Description</span></span>](#description)
-   [<span data-ttu-id="84dec-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="84dec-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="84dec-108">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="84dec-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="84dec-109">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="84dec-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="84dec-110">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="84dec-110">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="84dec-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="84dec-111">Description</span></span>

<span data-ttu-id="84dec-112">In diesem Beispiel wird gezeigt, wie eine eingeschränkte Suche mithilfe der [**isearchfolderitemfactory**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) -Schnittstelle erstellt wird, um ein Ordner shellelement (einen Container) zu erstellen, das die Abfrage darstellt.</span><span class="sxs-lookup"><span data-stu-id="84dec-112">This sample shows how to create a constrained search by using the [**ISearchFolderItemFactory**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) interface to construct a folder Shell item (a container) that represents the query.</span></span> <span data-ttu-id="84dec-113">Die Ergebnisse werden mithilfe des Dialog Felds zum Öffnen von Dateien angezeigt.</span><span class="sxs-lookup"><span data-stu-id="84dec-113">The results are displayed using the file open dialog.</span></span>

## <a name="requirements"></a><span data-ttu-id="84dec-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="84dec-114">Requirements</span></span>



| <span data-ttu-id="84dec-115">Produkt</span><span class="sxs-lookup"><span data-stu-id="84dec-115">Product</span></span>                                | <span data-ttu-id="84dec-116">Minimale Produkt Version</span><span class="sxs-lookup"><span data-stu-id="84dec-116">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="84dec-117">Windows</span><span class="sxs-lookup"><span data-stu-id="84dec-117">Windows</span></span>                                | <span data-ttu-id="84dec-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="84dec-118">Windows Vista</span></span>           |
| <span data-ttu-id="84dec-119">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="84dec-119">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="84dec-120">7.0</span><span class="sxs-lookup"><span data-stu-id="84dec-120">7.0</span></span>                     |



 

<span data-ttu-id="84dec-121">Weitere Anforderungen finden Sie in der im Beispiel enthaltenen Infodatei.</span><span class="sxs-lookup"><span data-stu-id="84dec-121">For additional requirements, see the Readme file included with the sample.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="84dec-122">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="84dec-122">Downloading the Sample</span></span>

| <span data-ttu-id="84dec-123">Standort</span><span class="sxs-lookup"><span data-stu-id="84dec-123">Location</span></span>      | <span data-ttu-id="84dec-124">Pfad-URL</span><span class="sxs-lookup"><span data-stu-id="84dec-124">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84dec-125">GitHub</span><span class="sxs-lookup"><span data-stu-id="84dec-125">GitHub</span></span>  | [<span data-ttu-id="84dec-126">Beispiel für SearchFolder</span><span class="sxs-lookup"><span data-stu-id="84dec-126">SearchFolder sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/searchfolder) |

## <a name="building-the-sample"></a><span data-ttu-id="84dec-127">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="84dec-127">Building the Sample</span></span>

<span data-ttu-id="84dec-128">Anweisungen zum Erstellen des Beispiels finden Sie in der im Beispiel enthaltenen Infodatei.</span><span class="sxs-lookup"><span data-stu-id="84dec-128">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="84dec-129">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="84dec-129">Running the Sample</span></span>

<span data-ttu-id="84dec-130">Anweisungen zum Erstellen des Beispiels finden Sie in der im Beispiel enthaltenen Infodatei.</span><span class="sxs-lookup"><span data-stu-id="84dec-130">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

 

 



