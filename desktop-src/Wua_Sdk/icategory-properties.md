---
description: Die icategory-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: aa9c4dbb-5e33-47b7-ae6c-8d83010e205b
title: Icategory-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d01e5b5eac4701ebdff4c79981ee91806a18329
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372849"
---
# <a name="icategory-properties"></a><span data-ttu-id="31411-103">Icategory-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="31411-103">ICategory Properties</span></span>

<span data-ttu-id="31411-104">Die [**icategory**](/windows/desktop/api/Wuapi/nn-wuapi-icategory) -Schnittstelle definiert die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="31411-104">The [**ICategory**](/windows/desktop/api/Wuapi/nn-wuapi-icategory) interface defines the following properties.</span></span>



| <span data-ttu-id="31411-105">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="31411-105">Property</span></span>                                     | <span data-ttu-id="31411-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="31411-106">Description</span></span>                                                                                       |
|----------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="31411-107">**CategoryID**</span><span class="sxs-lookup"><span data-stu-id="31411-107">**CategoryID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-icategory-get_categoryid)   | <span data-ttu-id="31411-108">Ruft den Bezeichner der Kategorie ab.</span><span class="sxs-lookup"><span data-stu-id="31411-108">Gets the identifier of the category.</span></span>                                                              |
| [<span data-ttu-id="31411-109">**Children**</span><span class="sxs-lookup"><span data-stu-id="31411-109">**Children**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-icategory-get_children)       | <span data-ttu-id="31411-110">Ruft eine Schnittstellen Auflistung ab, die die untergeordneten Kategorien dieser Kategorie enthält.</span><span class="sxs-lookup"><span data-stu-id="31411-110">Gets an interface collection that contains the child categories of this category.</span></span>                 |
| [<span data-ttu-id="31411-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="31411-111">**Description**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-icategory-get_description) | <span data-ttu-id="31411-112">Ruft die Beschreibung der Kategorie ab.</span><span class="sxs-lookup"><span data-stu-id="31411-112">Gets the description of the category.</span></span>                                                             |
| [<span data-ttu-id="31411-113">**Image**</span><span class="sxs-lookup"><span data-stu-id="31411-113">**Image**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-icategory-get_image)             | <span data-ttu-id="31411-114">Ruft eine Schnittstelle ab, die Informationen über das Bild enthält, das der Kategorie zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="31411-114">Gets an interface that contains information about the image that is associated with the category.</span></span> |
| [<span data-ttu-id="31411-115">**Name**</span><span class="sxs-lookup"><span data-stu-id="31411-115">**Name**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-icategory-get_name)               | <span data-ttu-id="31411-116">Ruft den lokalisierten Namen der Kategorie ab.</span><span class="sxs-lookup"><span data-stu-id="31411-116">Gets the localized name of the category.</span></span>                                                          |
| [<span data-ttu-id="31411-117">**Auftrag**</span><span class="sxs-lookup"><span data-stu-id="31411-117">**Order**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-icategory-get_order)             | <span data-ttu-id="31411-118">Ruft die empfohlene Anzeigereihenfolge dieser Kategorie in den gleich geordneten Kategorien ab.</span><span class="sxs-lookup"><span data-stu-id="31411-118">Gets the recommended display order of this category among its sibling categories.</span></span>                 |
| [<span data-ttu-id="31411-119">**Parent**</span><span class="sxs-lookup"><span data-stu-id="31411-119">**Parent**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-icategory-get_parent)           | <span data-ttu-id="31411-120">Ruft eine Schnittstelle ab, die die übergeordnete Kategorie dieser Kategorie beschreibt.</span><span class="sxs-lookup"><span data-stu-id="31411-120">Gets an interface that describes the parent category of this category.</span></span>                            |
| [<span data-ttu-id="31411-121">**type**</span><span class="sxs-lookup"><span data-stu-id="31411-121">**Type**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-icategory-get_type)               | <span data-ttu-id="31411-122">Ruft den Typ der Kategorie ab.</span><span class="sxs-lookup"><span data-stu-id="31411-122">Gets the type of the category.</span></span>                                                                    |
| [<span data-ttu-id="31411-123">**Updates**</span><span class="sxs-lookup"><span data-stu-id="31411-123">**Updates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-icategory-get_updates)         | <span data-ttu-id="31411-124">Ruft eine Schnittstelle ab, die eine Auflistung von Updates enthält, die sofort zur Kategorie gehören.</span><span class="sxs-lookup"><span data-stu-id="31411-124">Gets an interface that contains a collection of updates that immediately belong to the category.</span></span>  |



 

 

 



