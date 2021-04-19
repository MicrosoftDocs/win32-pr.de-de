---
title: MENUEX_TEMPLATE_HEADER Struktur
description: Definiert den Header für eine erweiterte Menüvorlage. Diese Struktur Definition dient lediglich der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.
ms.assetid: df763349-7127-482e-8613-74e68addde5d
keywords:
- MENUEX_TEMPLATE_HEADER Struktur Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- MENUEX_TEMPLATE_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: caa255ccdbe76c3959d9c730bcaa52ec07428742
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341783"
---
# <a name="menuex_template_header-structure"></a><span data-ttu-id="7d683-105">Menuex- \_ Vorlagen \_ Header Struktur</span><span class="sxs-lookup"><span data-stu-id="7d683-105">MENUEX\_TEMPLATE\_HEADER structure</span></span>

<span data-ttu-id="7d683-106">Definiert den Header für eine erweiterte Menüvorlage.</span><span class="sxs-lookup"><span data-stu-id="7d683-106">Defines the header for an extended menu template.</span></span> <span data-ttu-id="7d683-107">Diese Struktur Definition dient lediglich der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.</span><span class="sxs-lookup"><span data-stu-id="7d683-107">This structure definition is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d683-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d683-108">Syntax</span></span>


```C++
typedef struct {
  WORD  wVersion;
  WORD  wOffset;
  DWORD dwHelpId;
} MENUEX_TEMPLATE_HEADER;
```



## <a name="members"></a><span data-ttu-id="7d683-109">Member</span><span class="sxs-lookup"><span data-stu-id="7d683-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="7d683-110">**wversion**</span><span class="sxs-lookup"><span data-stu-id="7d683-110">**wVersion**</span></span>
</dt> <dd>

<span data-ttu-id="7d683-111">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="7d683-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="7d683-112">Die Versionsnummer der Vorlage.</span><span class="sxs-lookup"><span data-stu-id="7d683-112">The template version number.</span></span> <span data-ttu-id="7d683-113">Dieser Member muss für erweiterte Menü Vorlagen 1 sein.</span><span class="sxs-lookup"><span data-stu-id="7d683-113">This member must be 1 for extended menu templates.</span></span>

</dd> <dt>

<span data-ttu-id="7d683-114">**woffset**</span><span class="sxs-lookup"><span data-stu-id="7d683-114">**wOffset**</span></span>
</dt> <dd>

<span data-ttu-id="7d683-115">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="7d683-115">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="7d683-116">Der Offset zur ersten [**menuex- \_ Vorlagen \_ Element**](menuex-template-item.md) Struktur, relativ zum Ende dieses Strukturmembers.</span><span class="sxs-lookup"><span data-stu-id="7d683-116">The offset to the first [**MENUEX\_TEMPLATE\_ITEM**](menuex-template-item.md) structure, relative to the end of this structure member.</span></span> <span data-ttu-id="7d683-117">Wenn die erste Element Definition direkt auf den **dwhelpid** -Member folgt, sollte dieser Member 4 sein.</span><span class="sxs-lookup"><span data-stu-id="7d683-117">If the first item definition immediately follows the **dwHelpId** member, this member should be 4.</span></span>

</dd> <dt>

<span data-ttu-id="7d683-118">**dwhelpid**</span><span class="sxs-lookup"><span data-stu-id="7d683-118">**dwHelpId**</span></span>
</dt> <dd>

<span data-ttu-id="7d683-119">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="7d683-119">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="7d683-120">Der Hilfe Bezeichner der Menüleiste.</span><span class="sxs-lookup"><span data-stu-id="7d683-120">The help identifier of menu bar.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d683-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d683-121">Remarks</span></span>

<span data-ttu-id="7d683-122">Eine erweiterte Menüvorlage besteht aus einer **menuex- \_ Vorlagen \_ Header** Struktur, gefolgt von einer oder mehreren zusammenhängenden [**menuex- \_ Vorlagen \_ Element**](menuex-template-item.md) Strukturen.</span><span class="sxs-lookup"><span data-stu-id="7d683-122">An extended menu template consists of a **MENUEX\_TEMPLATE\_HEADER** structure followed by one or more contiguous [**MENUEX\_TEMPLATE\_ITEM**](menuex-template-item.md) structures.</span></span> <span data-ttu-id="7d683-123">Die **menuex- \_ Vorlagen \_ Element** Strukturen, die eine Variable Länge haben, werden an den **DWORD** -Grenzen ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="7d683-123">The **MENUEX\_TEMPLATE\_ITEM** structures, which are variable in length, are aligned on **DWORD** boundaries.</span></span> <span data-ttu-id="7d683-124">Verwenden Sie die [**loadmenuindirekte**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) -Funktion, um ein Menü aus einer erweiterten Menüvorlage im Arbeitsspeicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7d683-124">To create a menu from an extended menu template in memory, use the [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d683-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d683-125">Requirements</span></span>



| <span data-ttu-id="7d683-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d683-126">Requirement</span></span> | <span data-ttu-id="7d683-127">Wert</span><span class="sxs-lookup"><span data-stu-id="7d683-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="7d683-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7d683-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7d683-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7d683-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7d683-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7d683-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7d683-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7d683-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="7d683-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d683-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="7d683-133">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="7d683-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7d683-134">**Loadmenuindirekte**</span><span class="sxs-lookup"><span data-stu-id="7d683-134">**LoadMenuIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)
</dt> <dt>

[<span data-ttu-id="7d683-135">**menuex- \_ Vorlagen \_ Element**</span><span class="sxs-lookup"><span data-stu-id="7d683-135">**MENUEX\_TEMPLATE\_ITEM**</span></span>](menuex-template-item.md)
</dt> <dt>

<span data-ttu-id="7d683-136">**Licher**</span><span class="sxs-lookup"><span data-stu-id="7d683-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7d683-137">Menüs</span><span class="sxs-lookup"><span data-stu-id="7d683-137">Menus</span></span>](menus.md)
</dt> </dl>

 

 





