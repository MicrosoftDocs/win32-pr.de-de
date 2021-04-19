---
description: Die iupdatecollection-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: 38420d5e-4d36-4ed7-be06-e1df903929a7
title: Iupdatecollection-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aae347885deccb52ac44513bd1138aa18995c41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348201"
---
# <a name="iupdatecollection-properties"></a><span data-ttu-id="30985-103">Iupdatecollection-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="30985-103">IUpdateCollection Properties</span></span>

<span data-ttu-id="30985-104">Die [**iupdatecollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection) -Schnittstelle definiert die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="30985-104">The [**IUpdateCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection) interface defines the following properties.</span></span>



| <span data-ttu-id="30985-105">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="30985-105">Property</span></span>                                        | <span data-ttu-id="30985-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="30985-106">Description</span></span>                                                                                                              |
|-------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="30985-107">**\_"Netwenum"**</span><span class="sxs-lookup"><span data-stu-id="30985-107">**\_NewEnum**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get__newenum) | <span data-ttu-id="30985-108">Ruft eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle ab, die zum Auflisten der Auflistung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="30985-108">Gets an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface that can be used to enumerate the collection.</span></span> |
| [<span data-ttu-id="30985-109">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="30985-109">**Count**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_count)        | <span data-ttu-id="30985-110">Ruft die Anzahl der Elemente in der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="30985-110">Gets the number of elements in the collection.</span></span>                                                                           |
| [<span data-ttu-id="30985-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="30985-111">**Item**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_item)          | <span data-ttu-id="30985-112">Ruft eine [**iupdate**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate) -Schnittstelle in einer Auflistung ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="30985-112">Gets or sets an [**IUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate) interface in a collection.</span></span>                                                    |
| [<span data-ttu-id="30985-113">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="30985-113">**ReadOnly**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_readonly)  | <span data-ttu-id="30985-114">Ruft einen booleschen Wert ab, der angibt, ob die Update-Auflistung schreibgeschützt ist.</span><span class="sxs-lookup"><span data-stu-id="30985-114">Gets a Boolean value that indicates whether the update collection is read-only.</span></span>                                          |



 

 

 
