---
description: Enthält den Index eines Eintrags und seine Taginformationen in einer Shimdatenbank.
ms.assetid: 2ff58e01-cc47-4612-a3bc-a87ccb343bd2
title: TagID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e7d8b8a25633d3505936d105b0eef7ed38746ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958253"
---
# <a name="tagid"></a><span data-ttu-id="5c91d-103">TagID</span><span class="sxs-lookup"><span data-stu-id="5c91d-103">TAGID</span></span>

<span data-ttu-id="5c91d-104">Enthält den Index eines Eintrags und seine Taginformationen in einer Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="5c91d-104">Contains the index of an entry and its TAG information in a shim database.</span></span>


```C++
typedef DWORD TAGID;
```



## <a name="remarks"></a><span data-ttu-id="5c91d-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c91d-105">Remarks</span></span>

<span data-ttu-id="5c91d-106">Eine **TagID** ist für eine Datenbank spezifisch.</span><span class="sxs-lookup"><span data-stu-id="5c91d-106">A **TAGID** is specific to a database.</span></span> <span data-ttu-id="5c91d-107">Dabei kann es sich um einen ganzzahligen Wert handeln, der den Index darstellt, oder um einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="5c91d-107">It can be an integer value that represents the index, or one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="5c91d-108"><span id="TAGID_NULL__0_"></span><span id="tagid_null__0_"></span>TagID \_ NULL (0)</span><span class="sxs-lookup"><span data-stu-id="5c91d-108"><span id="TAGID_NULL__0_"></span><span id="tagid_null__0_"></span>TAGID\_NULL (0)</span></span>
</dt> <dd>

<span data-ttu-id="5c91d-109">Die **TagID** ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5c91d-109">The **TAGID** does not exist.</span></span> <span data-ttu-id="5c91d-110">Dieser Wert wird von einer Funktion zurückgegeben, wenn keine gültige **TagID** zurückgegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="5c91d-110">This value is returned from a function when it cannot return a valid **TAGID**.</span></span>

</dd> <dt>

<span data-ttu-id="5c91d-111"><span id="TAGID_ROOT__0_"></span><span id="tagid_root__0_"></span>TagID-Stamm \_ (0)</span><span class="sxs-lookup"><span data-stu-id="5c91d-111"><span id="TAGID_ROOT__0_"></span><span id="tagid_root__0_"></span>TAGID\_ROOT (0)</span></span>
</dt> <dd>

<span data-ttu-id="5c91d-112">Gibt ein Stamm Listen-Tag an, das als übergeordnetes Element zum Abrufen einer untergeordneten **TagID** verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5c91d-112">Indicates a root list TAG that can be used as a parent to obtain a child **TAGID**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5c91d-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c91d-113">Requirements</span></span>



| <span data-ttu-id="5c91d-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5c91d-114">Requirement</span></span> | <span data-ttu-id="5c91d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="5c91d-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5c91d-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5c91d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5c91d-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c91d-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5c91d-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5c91d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5c91d-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c91d-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5c91d-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c91d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c91d-121">**Tag**</span><span class="sxs-lookup"><span data-stu-id="5c91d-121">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="5c91d-122">Tagtypen</span><span class="sxs-lookup"><span data-stu-id="5c91d-122">TAG Types</span></span>](tag-types.md)
</dt> <dt>

[<span data-ttu-id="5c91d-123">**Tagref**</span><span class="sxs-lookup"><span data-stu-id="5c91d-123">**TAGREF**</span></span>](tagref.md)
</dt> </dl>

 

 




