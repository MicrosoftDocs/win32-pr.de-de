---
title: DownloadCollection.id
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Die ID-Eigenschaft ruft die ID der Download Auflistung ab.
ms.assetid: b5b17f22-913c-4055-8958-e3efac819b2b
keywords:
- DownloadCollection.ID Windows Media Player
topic_type:
- apiref
api_name:
- DownloadCollection.id
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9edcca4f56c485951ca907ae228dfec7a958b308
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362158"
---
# <a name="downloadcollectionid"></a><span data-ttu-id="5318f-106">DownloadCollection.id</span><span class="sxs-lookup"><span data-stu-id="5318f-106">DownloadCollection.id</span></span>

> [!Note]  
> <span data-ttu-id="5318f-107">In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores</span><span class="sxs-lookup"><span data-stu-id="5318f-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="5318f-108">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5318f-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="5318f-109">Die **ID** -Eigenschaft ruft die ID der Download Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="5318f-109">The **id** property retrieves the ID of the download collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5318f-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="5318f-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).id
      
```

## <a name="possible-values"></a><span data-ttu-id="5318f-111">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="5318f-111">Possible Values</span></span>

<span data-ttu-id="5318f-112">Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="5318f-112">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="5318f-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5318f-113">Remarks</span></span>

<span data-ttu-id="5318f-114">Wenn der Download-Manager eine neue Download Sammlung erstellt, wird der Sammlung eine ID-Nummer zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="5318f-114">When the Download Manager creates a new download collection, it assigns the collection an ID number.</span></span> <span data-ttu-id="5318f-115">ID-Nummern werden zwischen Windows Media Player-Sitzungen und Betriebssystem Sitzungen beibehalten.</span><span class="sxs-lookup"><span data-stu-id="5318f-115">ID numbers persist between Windows Media Player sessions and operating system sessions.</span></span>

<span data-ttu-id="5318f-116">Die ID-Nummern sind nicht eindeutig.</span><span class="sxs-lookup"><span data-stu-id="5318f-116">ID numbers are not unique.</span></span> <span data-ttu-id="5318f-117">Es sind jedoch genügend ID-Nummern im 32-Bit-Wert verfügbar, dass es äußerst unwahrscheinlich ist, dass eine vorhandene ID jemals durch eine neue ID überschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="5318f-117">However, there are enough ID numbers available in the 32-bit value that it is extremely unlikely that an existing ID number will ever be overwritten by a new one.</span></span>

## <a name="requirements"></a><span data-ttu-id="5318f-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5318f-118">Requirements</span></span>



| <span data-ttu-id="5318f-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5318f-119">Requirement</span></span> | <span data-ttu-id="5318f-120">Wert</span><span class="sxs-lookup"><span data-stu-id="5318f-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5318f-121">Version</span><span class="sxs-lookup"><span data-stu-id="5318f-121">Version</span></span><br/> | <span data-ttu-id="5318f-122">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="5318f-122">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="5318f-123">DLL</span><span class="sxs-lookup"><span data-stu-id="5318f-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="5318f-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5318f-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5318f-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5318f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5318f-126">**Download Collection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="5318f-126">**DownloadCollection Object**</span></span>](downloadcollection-object.md)
</dt> </dl>

 

 





