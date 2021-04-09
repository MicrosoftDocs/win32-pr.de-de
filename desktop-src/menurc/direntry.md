---
title: Direntry-Struktur
description: Enthält eine eindeutige Ordinalzahl, die eine einzelne Schriftart in der Schriftarten Ressourcengruppe identifiziert. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.
ms.assetid: 4afc561e-bc98-4968-9a00-5002870b0c5e
keywords:
- Direntry-Struktur Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- DIRENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: caed8f05a92abbeda39084b99b6806c2e28777a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742032"
---
# <a name="direntry-structure"></a><span data-ttu-id="ea96b-105">Direntry-Struktur</span><span class="sxs-lookup"><span data-stu-id="ea96b-105">DIRENTRY structure</span></span>

<span data-ttu-id="ea96b-106">Enthält eine eindeutige Ordinalzahl, die eine einzelne Schriftart in der Schriftarten Ressourcengruppe identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ea96b-106">Contains a unique ordinal that identifies an individual font in the font resource group.</span></span> <span data-ttu-id="ea96b-107">Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ea96b-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea96b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea96b-108">Syntax</span></span>


```C++
typedef struct {
  WORD fontOrdinal;
} DIRENTRY;
```



## <a name="members"></a><span data-ttu-id="ea96b-109">Member</span><span class="sxs-lookup"><span data-stu-id="ea96b-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="ea96b-110">**fontorion**</span><span class="sxs-lookup"><span data-stu-id="ea96b-110">**fontOrdinal**</span></span>
</dt> <dd>

<span data-ttu-id="ea96b-111">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="ea96b-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="ea96b-112">Ein eindeutiger ordinalbezeichner für eine einzelne Schriftart in einer Schriftart Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ea96b-112">A unique ordinal identifier for an individual font in a font resource group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ea96b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ea96b-113">Remarks</span></span>

<span data-ttu-id="ea96b-114">Die [**fontdirentry**](fontdirentry.md) -Struktur für die angegebene Schriftart folgt direkt der **direntry** -Struktur für diese Schriftart.</span><span class="sxs-lookup"><span data-stu-id="ea96b-114">The [**FONTDIRENTRY**](fontdirentry.md) structure for the specified font directly follows the **DIRENTRY** structure for that font.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea96b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea96b-115">Requirements</span></span>



| <span data-ttu-id="ea96b-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea96b-116">Requirement</span></span> | <span data-ttu-id="ea96b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ea96b-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="ea96b-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ea96b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ea96b-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea96b-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ea96b-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ea96b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ea96b-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea96b-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="ea96b-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea96b-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="ea96b-123">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="ea96b-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ea96b-124">**Fontdirentry**</span><span class="sxs-lookup"><span data-stu-id="ea96b-124">**FONTDIRENTRY**</span></span>](fontdirentry.md)
</dt> <dt>

[<span data-ttu-id="ea96b-125">**Fontgrouphdr**</span><span class="sxs-lookup"><span data-stu-id="ea96b-125">**FONTGROUPHDR**</span></span>](fontgrouphdr.md)
</dt> <dt>

<span data-ttu-id="ea96b-126">**Licher**</span><span class="sxs-lookup"><span data-stu-id="ea96b-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ea96b-127">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ea96b-127">Resources</span></span>](resources.md)
</dt> </dl>

 

 





