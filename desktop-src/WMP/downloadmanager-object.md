---
title: Download Manager-Objekt
description: Download Manager-Objekt
ms.assetid: e6b07f3c-9254-41bb-9480-8167c3cd655b
keywords:
- Windows Media Player Online Stores, Download Manager-Objekt
- Online Stores, Download Manager-Objekt
- Typ 2 Online Stores, Download Manager-Objekt
- Download Manager
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f3555ee7b99c97e85ce856766bd9f670aac4229b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856347"
---
# <a name="downloadmanager-object"></a><span data-ttu-id="60cda-107">Download Manager-Objekt</span><span class="sxs-lookup"><span data-stu-id="60cda-107">DownloadManager Object</span></span>

> [!Note]  
> <span data-ttu-id="60cda-108">In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores</span><span class="sxs-lookup"><span data-stu-id="60cda-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="60cda-109">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="60cda-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="60cda-110">Das **Download Manager** -Objekt ist das Stamm Objekt für den Windows Media Player Download-Manager.</span><span class="sxs-lookup"><span data-stu-id="60cda-110">The **DownloadManager** object is the root object for the Windows Media Player Download Manager.</span></span> <span data-ttu-id="60cda-111">Sie kann von Webseiten verwendet werden, die in den Aufgabenbereichen des Online Store Service gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="60cda-111">It can be used by webpages that are hosted in online store service task panes.</span></span>

<span data-ttu-id="60cda-112">Das **Download Manager** -Objekt unterstützt die folgenden Methoden.</span><span class="sxs-lookup"><span data-stu-id="60cda-112">The **DownloadManager** object supports the following methods.</span></span>



| <span data-ttu-id="60cda-113">Methode</span><span class="sxs-lookup"><span data-stu-id="60cda-113">Method</span></span>                                                                   | <span data-ttu-id="60cda-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60cda-114">Description</span></span>                                  |
|--------------------------------------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="60cda-115">"kreatedownloadcollection"</span><span class="sxs-lookup"><span data-stu-id="60cda-115">createDownloadCollection</span></span>](downloadmanager-createdownloadcollection.md) | <span data-ttu-id="60cda-116">Erstellt eine leere Download Auflistung.</span><span class="sxs-lookup"><span data-stu-id="60cda-116">Creates an empty download collection.</span></span>        |
| [<span data-ttu-id="60cda-117">getdownloadcollection</span><span class="sxs-lookup"><span data-stu-id="60cda-117">getDownloadCollection</span></span>](downloadmanager-getdownloadcollection.md)       | <span data-ttu-id="60cda-118">Ruft die angegebene Download Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="60cda-118">Retrieves the specified download collection.</span></span> |



 

<span data-ttu-id="60cda-119">Der Zugriff auf das **Downloadmanager** -Objekt erfolgt über " **extern". Download Manager**.</span><span class="sxs-lookup"><span data-stu-id="60cda-119">The **DownloadManager** object is accessed by using **external.DownloadManager**.</span></span> <span data-ttu-id="60cda-120">Zu Veranschaulichung wird davon ausgegangen, dass dieser Wert einer Variablen mit dem Namen "Download Manager" zugewiesen wurde, die zur Identifizierung dieses Objekts in den Abschnitten der Verweis Syntax verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="60cda-120">For illustration purposes, it is assumed that this value has been assigned to a variable named "DownloadManager", which will be used to identify this object in the reference syntax sections.</span></span>

<span data-ttu-id="60cda-121">In Windows Media Player 10 oder höher sind die **Download Manager** -Eigenschaft und das-Objekt nur über Aufgabenbereiche des Online Store Service zugänglich.</span><span class="sxs-lookup"><span data-stu-id="60cda-121">In Windows Media Player 10 or later, the **DownloadManager** property and object are accessible only from online store service task panes.</span></span> <span data-ttu-id="60cda-122">Sie können den **Download Manager** nicht aus anderen Features verwenden, bei denen das **externe** Objekt verfügbar ist, z. b. HtmlView, Info Center View und Album-Informationen.</span><span class="sxs-lookup"><span data-stu-id="60cda-122">You cannot use the **DownloadManager** from other features where the **External** object is available, such as HTMLView, Info Center View, and album information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60cda-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="60cda-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60cda-124">**Referenz für Typ 2-Onlineshops**</span><span class="sxs-lookup"><span data-stu-id="60cda-124">**Reference for Type 2 Online Stores**</span></span>](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




