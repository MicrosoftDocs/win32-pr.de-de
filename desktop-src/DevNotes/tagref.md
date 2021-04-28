---
description: 'TAGREF: Enthält den Index eines Eintrags und seine TAG-Informationen in einer Shimdatenbank.'
ms.assetid: e7d83dca-13a5-4396-b50b-0d068209c03c
title: TAGREF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34e27a60847630e7bbd8e07ccf005dfd7b474d7a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096628"
---
# <a name="tagref"></a><span data-ttu-id="c6aa4-103">TAGREF</span><span class="sxs-lookup"><span data-stu-id="c6aa4-103">TAGREF</span></span>

<span data-ttu-id="c6aa4-104">Enthält den Index eines Eintrags und seine TAG-Informationen in einer Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="c6aa4-104">Contains the index of an entry and its TAG information in a shim database.</span></span>


```C++
typedef DWORD TAGREF;
```



## <a name="remarks"></a><span data-ttu-id="c6aa4-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6aa4-105">Remarks</span></span>

<span data-ttu-id="c6aa4-106">Ein **TAGREF** ist spezifisch für eine Shimdatenbank und für mehrere Datenbanken gültig.</span><span class="sxs-lookup"><span data-stu-id="c6aa4-106">A **TAGREF** is specific to a shim database and valid across multiple databases.</span></span> <span data-ttu-id="c6aa4-107">Dies kann ein ganzzahliger Wert sein, der den Index darstellt, oder einer der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="c6aa4-107">It can be an integer value that represents the index, or one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="c6aa4-108"><span id="TAGREF_NULL__0_"></span><span id="tagref_null__0_"></span>TAGREF \_ NULL (0)</span><span class="sxs-lookup"><span data-stu-id="c6aa4-108"><span id="TAGREF_NULL__0_"></span><span id="tagref_null__0_"></span>TAGREF\_NULL (0)</span></span>
</dt> <dd>

<span data-ttu-id="c6aa4-109">Das **TAGREF** ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c6aa4-109">The **TAGREF** does not exist.</span></span> <span data-ttu-id="c6aa4-110">Dieser Wert wird von einer Funktion zurückgegeben, wenn er kein gültiges **TAGREF** zurückgeben kann.</span><span class="sxs-lookup"><span data-stu-id="c6aa4-110">This value is returned from a function when it cannot return a valid **TAGREF**.</span></span>

</dd> <dt>

<span data-ttu-id="c6aa4-111"><span id="TAGREF_ROOT__0_"></span><span id="tagref_root__0_"></span>TAGREF \_ ROOT (0)</span><span class="sxs-lookup"><span data-stu-id="c6aa4-111"><span id="TAGREF_ROOT__0_"></span><span id="tagref_root__0_"></span>TAGREF\_ROOT (0)</span></span>
</dt> <dd>

<span data-ttu-id="c6aa4-112">Gibt ein Stammlisten-TAG an, das als übergeordnetes Element verwendet werden kann, um ein untergeordnetes **TAGREF** abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c6aa4-112">Indicates a root list TAG that can be used as a parent to obtain a child **TAGREF**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c6aa4-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6aa4-113">Requirements</span></span>



| <span data-ttu-id="c6aa4-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6aa4-114">Requirement</span></span> | <span data-ttu-id="c6aa4-115">Wert</span><span class="sxs-lookup"><span data-stu-id="c6aa4-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c6aa4-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c6aa4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c6aa4-117">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6aa4-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c6aa4-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c6aa4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c6aa4-119">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6aa4-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c6aa4-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c6aa4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6aa4-121">**SdbTagRefToTagID**</span><span class="sxs-lookup"><span data-stu-id="c6aa4-121">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
</dt> <dt>

[<span data-ttu-id="c6aa4-122">**Etikett**</span><span class="sxs-lookup"><span data-stu-id="c6aa4-122">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="c6aa4-123">TAG-Typen</span><span class="sxs-lookup"><span data-stu-id="c6aa4-123">TAG Types</span></span>](tag-types.md)
</dt> <dt>

[<span data-ttu-id="c6aa4-124">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="c6aa4-124">**TAGID**</span></span>](tagid.md)
</dt> </dl>

 

 




