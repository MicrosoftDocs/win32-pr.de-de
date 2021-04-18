---
title: Menuhelpid-Struktur
description: Enthält die abschließenden Daten, die in die RT- \_ Menü Ressource für ein Menü oder ein Untermenü geschrieben werden, wenn der ResInfo-Member der popupmenuitem-Struktur auf MFR-Popup festgelegt ist \_ .
ms.assetid: f17fdaaa-b37c-4902-bad4-a1181ffee9f9
keywords:
- Menuhelpid-Struktur Menüs und weitere Ressourcen
topic_type:
- apiref
api_name:
- MENUHELPID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b90b5a4745433c92a859a168611aa1c14f1fa45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344268"
---
# <a name="menuhelpid-structure"></a><span data-ttu-id="eed08-104">Menuhelpid-Struktur</span><span class="sxs-lookup"><span data-stu-id="eed08-104">MENUHELPID structure</span></span>

<span data-ttu-id="eed08-105">Enthält die abschließenden Daten, die in die [**RT- \_ Menü**](/windows/desktop/menurc/resource-types) Ressource für ein Menü oder ein Untermenü geschrieben werden, wenn der **ResInfo** -Member der [**popupmenuitem**](popupmenuitem.md) -Struktur auf **MFR- \_ Popup** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="eed08-105">Contains the final data written to the [**RT\_MENU**](/windows/desktop/menurc/resource-types) resource for a menu or submenu if the **resInfo** member of the [**POPUPMENUITEM**](popupmenuitem.md) structure is set to **MFR\_POPUP**.</span></span> <span data-ttu-id="eed08-106">Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.</span><span class="sxs-lookup"><span data-stu-id="eed08-106">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="eed08-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="eed08-107">Syntax</span></span>


```C++
typedef struct {
  DWORD helpID;
} MENUHELPID;
```



## <a name="members"></a><span data-ttu-id="eed08-108">Member</span><span class="sxs-lookup"><span data-stu-id="eed08-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="eed08-109">**HelpID**</span><span class="sxs-lookup"><span data-stu-id="eed08-109">**helpID**</span></span>
</dt> <dd>

<span data-ttu-id="eed08-110">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="eed08-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="eed08-111">Der Bezeichner, der zum Identifizieren des Menüs während der [**WM- \_ Hilfe**](/windows/desktop/shell/wm-help) Verarbeitung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="eed08-111">The identifier used to identify the menu during [**WM\_HELP**](/windows/desktop/shell/wm-help) processing.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eed08-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eed08-112">Requirements</span></span>



| <span data-ttu-id="eed08-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eed08-113">Requirement</span></span> | <span data-ttu-id="eed08-114">Wert</span><span class="sxs-lookup"><span data-stu-id="eed08-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="eed08-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eed08-115">Minimum supported client</span></span><br/> | <span data-ttu-id="eed08-116">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eed08-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="eed08-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eed08-117">Minimum supported server</span></span><br/> | <span data-ttu-id="eed08-118">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eed08-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="eed08-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eed08-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="eed08-120">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="eed08-120">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="eed08-121">**Menuheader**</span><span class="sxs-lookup"><span data-stu-id="eed08-121">**MENUHEADER**</span></span>](menuheader.md)
</dt> <dt>

[<span data-ttu-id="eed08-122">**Popupmenuitem**</span><span class="sxs-lookup"><span data-stu-id="eed08-122">**POPUPMENUITEM**</span></span>](popupmenuitem.md)
</dt> <dt>

<span data-ttu-id="eed08-123">**Licher**</span><span class="sxs-lookup"><span data-stu-id="eed08-123">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="eed08-124">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="eed08-124">Resources</span></span>](resources.md)
</dt> </dl>

 

