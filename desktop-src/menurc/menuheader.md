---
title: Menuheader-Struktur
description: Enthält Versionsinformationen für die Menü Ressource. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.
ms.assetid: 1e34b0b6-18ff-4cb6-901e-a2aabad0df74
keywords:
- Menuheader-Struktur Menüs und weitere Ressourcen
topic_type:
- apiref
api_name:
- MENUHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eacc67d34d04502aa17eeaca78240a0a3e0e219d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338321"
---
# <a name="menuheader-structure"></a><span data-ttu-id="8b292-105">Menuheader-Struktur</span><span class="sxs-lookup"><span data-stu-id="8b292-105">MENUHEADER structure</span></span>

<span data-ttu-id="8b292-106">Enthält Versionsinformationen für die Menü Ressource.</span><span class="sxs-lookup"><span data-stu-id="8b292-106">Contains version information for the menu resource.</span></span> <span data-ttu-id="8b292-107">Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8b292-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b292-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b292-108">Syntax</span></span>


```C++
typedef struct {
  WORD wVersion;
  WORD cbHeaderSize;
} MENUHEADER;
```



## <a name="members"></a><span data-ttu-id="8b292-109">Member</span><span class="sxs-lookup"><span data-stu-id="8b292-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="8b292-110">**wversion**</span><span class="sxs-lookup"><span data-stu-id="8b292-110">**wVersion**</span></span>
</dt> <dd>

<span data-ttu-id="8b292-111">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="8b292-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="8b292-112">Die Versionsnummer der Menüvorlage.</span><span class="sxs-lookup"><span data-stu-id="8b292-112">The version number of the menu template.</span></span> <span data-ttu-id="8b292-113">Dieser Member muss gleich NULL sein, um anzugeben, dass es sich um ein [**RT- \_ Menü**](/windows/desktop/menurc/resource-types) handelt, das mit einer Standardmenü Vorlage erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="8b292-113">This member must be equal to zero to indicate that this is an [**RT\_MENU**](/windows/desktop/menurc/resource-types) created with a standard menu template.</span></span>

</dd> <dt>

<span data-ttu-id="8b292-114">**cbheadersize**</span><span class="sxs-lookup"><span data-stu-id="8b292-114">**cbHeaderSize**</span></span>
</dt> <dd>

<span data-ttu-id="8b292-115">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="8b292-115">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="8b292-116">Die Größe des Menü Vorlagen Headers.</span><span class="sxs-lookup"><span data-stu-id="8b292-116">The size of the menu template header.</span></span> <span data-ttu-id="8b292-117">Dieser Wert ist 0 (null) für Menüs, die Sie mit einer Standardmenü Vorlage erstellen.</span><span class="sxs-lookup"><span data-stu-id="8b292-117">This value is zero for menus you create with a standard menu template.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8b292-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b292-118">Requirements</span></span>



| <span data-ttu-id="8b292-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b292-119">Requirement</span></span> | <span data-ttu-id="8b292-120">Wert</span><span class="sxs-lookup"><span data-stu-id="8b292-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="8b292-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8b292-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8b292-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b292-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8b292-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8b292-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8b292-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b292-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="8b292-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b292-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="8b292-126">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="8b292-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8b292-127">**menuex- \_ Vorlagen \_ Header**</span><span class="sxs-lookup"><span data-stu-id="8b292-127">**MENUEX\_TEMPLATE\_HEADER**</span></span>](menuex-template-header.md)
</dt> <dt>

[<span data-ttu-id="8b292-128">**menuex- \_ Vorlagen \_ Element**</span><span class="sxs-lookup"><span data-stu-id="8b292-128">**MENUEX\_TEMPLATE\_ITEM**</span></span>](menuex-template-item.md)
</dt> <dt>

[<span data-ttu-id="8b292-129">**Menuitemtemplate**</span><span class="sxs-lookup"><span data-stu-id="8b292-129">**MENUITEMTEMPLATE**</span></span>](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate)
</dt> <dt>

[<span data-ttu-id="8b292-130">**Menuitemtemplateheader**</span><span class="sxs-lookup"><span data-stu-id="8b292-130">**MENUITEMTEMPLATEHEADER**</span></span>](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader)
</dt> <dt>

[<span data-ttu-id="8b292-131">**Normalmenuitem**</span><span class="sxs-lookup"><span data-stu-id="8b292-131">**NORMALMENUITEM**</span></span>](normalmenuitem.md)
</dt> <dt>

[<span data-ttu-id="8b292-132">**Popupmenuitem**</span><span class="sxs-lookup"><span data-stu-id="8b292-132">**POPUPMENUITEM**</span></span>](popupmenuitem.md)
</dt> <dt>

<span data-ttu-id="8b292-133">**Licher**</span><span class="sxs-lookup"><span data-stu-id="8b292-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8b292-134">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8b292-134">Resources</span></span>](resources.md)
</dt> </dl>

 

