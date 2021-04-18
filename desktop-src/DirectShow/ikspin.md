---
description: Die "ikspin"-Schnittstelle bietet eine Methode zum Abrufen der von einer PIN in einem kernelmodusfilter unterstützten Medien. "Ikspin" hat neben dem hier gezeigten zusätzliche Methoden, aber Sie werden für DirectShow nicht unterstützt.
ms.assetid: 14d9bef2-e8f0-49d5-bd89-69a95814cf8c
title: Ikspin-Schnittstelle (ksproxy. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPin
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 3d65e5ba5525b977ebae27da9964579614a1d653
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345401"
---
# <a name="ikspin-interface"></a><span data-ttu-id="d69e5-104">Ikspin-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d69e5-104">IKsPin interface</span></span>

<span data-ttu-id="d69e5-105">Die `IKsPin` -Schnittstelle stellt eine Methode zum Abrufen der von einer PIN in einem Kernel Modus-Filter unterstützten Medien bereit.</span><span class="sxs-lookup"><span data-stu-id="d69e5-105">The `IKsPin` interface provides a method to retrieve the mediums supported by a pin on a kernel-mode filter.</span></span> <span data-ttu-id="d69e5-106">`IKsPin` hat neben dem hier gezeigten zusätzliche Methoden, aber Sie werden für DirectShow nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d69e5-106">`IKsPin` has additional methods besides the one shown here, but they are not supported for DirectShow.</span></span>

## <a name="members"></a><span data-ttu-id="d69e5-107">Member</span><span class="sxs-lookup"><span data-stu-id="d69e5-107">Members</span></span>

<span data-ttu-id="d69e5-108">Die " **ikspin** "-Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d69e5-108">The **IKsPin** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d69e5-109">In " **ikspin** " sind auch folgende Typen von Membern aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="d69e5-109">**IKsPin** also has these types of members:</span></span>

-   [<span data-ttu-id="d69e5-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="d69e5-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d69e5-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="d69e5-111">Methods</span></span>

<span data-ttu-id="d69e5-112">Die **ikspin** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="d69e5-112">The **IKsPin** interface has these methods.</span></span>



| <span data-ttu-id="d69e5-113">Methode</span><span class="sxs-lookup"><span data-stu-id="d69e5-113">Method</span></span>                                          | <span data-ttu-id="d69e5-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d69e5-114">Description</span></span>                                          |
|:------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="d69e5-115">**Ksquerymediums**</span><span class="sxs-lookup"><span data-stu-id="d69e5-115">**KsQueryMediums**</span></span>](ikspin-ksquerymediums.md) | <span data-ttu-id="d69e5-116">Ruft die von einer PIN unterstützten Medien ab.</span><span class="sxs-lookup"><span data-stu-id="d69e5-116">Retrieves the mediums supported by a pin.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d69e5-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d69e5-117">Remarks</span></span>

<span data-ttu-id="d69e5-118">Sie müssen "KS. h" vor "ksproxy. h" einschließen.</span><span class="sxs-lookup"><span data-stu-id="d69e5-118">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="d69e5-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d69e5-119">Requirements</span></span>



| <span data-ttu-id="d69e5-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d69e5-120">Requirement</span></span> | <span data-ttu-id="d69e5-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d69e5-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d69e5-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d69e5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d69e5-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d69e5-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d69e5-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d69e5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d69e5-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d69e5-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d69e5-126">Header</span><span class="sxs-lookup"><span data-stu-id="d69e5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d69e5-127"><dt>Ksproxy. h</dt></span><span class="sxs-lookup"><span data-stu-id="d69e5-127"><dt>Ksproxy.h</dt></span></span> </dl>    |
| <span data-ttu-id="d69e5-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d69e5-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="d69e5-129"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="d69e5-129"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
