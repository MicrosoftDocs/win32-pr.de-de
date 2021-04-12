---
description: Enthält den Index eines Eintrags und seine Taginformationen in einer Shimdatenbank.
ms.assetid: e7d83dca-13a5-4396-b50b-0d068209c03c
title: Tagref
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8631811f101850b68bdbad1097c19b9a41737bd2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523152"
---
# <a name="tagref"></a><span data-ttu-id="15d68-103">Tagref</span><span class="sxs-lookup"><span data-stu-id="15d68-103">TAGREF</span></span>

<span data-ttu-id="15d68-104">Enthält den Index eines Eintrags und seine Taginformationen in einer Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="15d68-104">Contains the index of an entry and its TAG information in a shim database.</span></span>


```C++
typedef DWORD TAGREF;
```



## <a name="remarks"></a><span data-ttu-id="15d68-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15d68-105">Remarks</span></span>

<span data-ttu-id="15d68-106">Eine **tagref** ist für eine Shimdatenbank spezifisch und über mehrere Datenbanken hinweg gültig.</span><span class="sxs-lookup"><span data-stu-id="15d68-106">A **TAGREF** is specific to a shim database and valid across multiple databases.</span></span> <span data-ttu-id="15d68-107">Dabei kann es sich um einen ganzzahligen Wert handeln, der den Index darstellt, oder um einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="15d68-107">It can be an integer value that represents the index, or one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="15d68-108"><span id="TAGREF_NULL__0_"></span><span id="tagref_null__0_"></span>Tagref \_ NULL (0)</span><span class="sxs-lookup"><span data-stu-id="15d68-108"><span id="TAGREF_NULL__0_"></span><span id="tagref_null__0_"></span>TAGREF\_NULL (0)</span></span>
</dt> <dd>

<span data-ttu-id="15d68-109">**Tagref** ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="15d68-109">The **TAGREF** does not exist.</span></span> <span data-ttu-id="15d68-110">Dieser Wert wird von einer Funktion zurückgegeben, wenn kein gültiger **tagref**-Wert zurückgegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="15d68-110">This value is returned from a function when it cannot return a valid **TAGREF**.</span></span>

</dd> <dt>

<span data-ttu-id="15d68-111"><span id="TAGREF_ROOT__0_"></span><span id="tagref_root__0_"></span>Tagref-Stamm \_ (0)</span><span class="sxs-lookup"><span data-stu-id="15d68-111"><span id="TAGREF_ROOT__0_"></span><span id="tagref_root__0_"></span>TAGREF\_ROOT (0)</span></span>
</dt> <dd>

<span data-ttu-id="15d68-112">Gibt ein Stamm Listen-Tag an, das als übergeordnetes Element verwendet werden kann, um ein untergeordnetes **tagref** zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="15d68-112">Indicates a root list TAG that can be used as a parent to obtain a child **TAGREF**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="15d68-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15d68-113">Requirements</span></span>



| <span data-ttu-id="15d68-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="15d68-114">Requirement</span></span> | <span data-ttu-id="15d68-115">Wert</span><span class="sxs-lookup"><span data-stu-id="15d68-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="15d68-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="15d68-116">Minimum supported client</span></span><br/> | <span data-ttu-id="15d68-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15d68-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="15d68-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="15d68-118">Minimum supported server</span></span><br/> | <span data-ttu-id="15d68-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15d68-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="15d68-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15d68-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15d68-121">**Sdbtagrebtotagid**</span><span class="sxs-lookup"><span data-stu-id="15d68-121">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
</dt> <dt>

[<span data-ttu-id="15d68-122">**Tag**</span><span class="sxs-lookup"><span data-stu-id="15d68-122">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="15d68-123">Tagtypen</span><span class="sxs-lookup"><span data-stu-id="15d68-123">TAG Types</span></span>](tag-types.md)
</dt> <dt>

[<span data-ttu-id="15d68-124">**TagID**</span><span class="sxs-lookup"><span data-stu-id="15d68-124">**TAGID**</span></span>](tagid.md)
</dt> </dl>

 

 




