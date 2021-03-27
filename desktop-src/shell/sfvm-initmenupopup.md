---
description: 'Ermöglicht dem Rückruf Objekt das Ändern eines Windows-Explorer-Popup Menüs, bevor es angezeigt wird. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
title: SFVM_INITMENUPOPUP Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9d7e96e9-c52e-43bd-945b-05db33c8dfd0
api_name:
- SFVM_INITMENUPOPUP
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1f9a2a169b232fe3ad16eeee8816536ed81c74dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980833"
---
# <a name="sfvm_initmenupopup-message"></a><span data-ttu-id="aa8dd-104">Sfvm- \_ initmenupopup-Meldung</span><span class="sxs-lookup"><span data-stu-id="aa8dd-104">SFVM\_INITMENUPOPUP message</span></span>

<span data-ttu-id="aa8dd-105">Ermöglicht dem Rückruf Objekt das Ändern eines Windows-Explorer-Popup Menüs, bevor es angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="aa8dd-105">Allows the callback object to modify a Windows Explorer pop-up menu before it is displayed.</span></span> <span data-ttu-id="aa8dd-106">Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.</span><span class="sxs-lookup"><span data-stu-id="aa8dd-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_INITMENUPOPUP 

    wParam = (WPARAM)(int) idCmd,nIndex;

    lParam = (LPARAM)(HMENU) hmenu;

            
```



## <a name="parameters"></a><span data-ttu-id="aa8dd-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa8dd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa8dd-108">*idcmd \_ nIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa8dd-108">*idCmd\_nIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa8dd-109">Das nieder wertige Wort dieses Parameters enthält den Wert der ersten Befehls-ID, die für Client Befehle reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="aa8dd-109">The low-order word of this parameter holds the value of the first command ID reserved for client commands.</span></span> <span data-ttu-id="aa8dd-110">Das hochwertige Wort enthält den Index des Menüs.</span><span class="sxs-lookup"><span data-stu-id="aa8dd-110">The high-order word holds the index of the menu.</span></span>

</dd> <dt>

<span data-ttu-id="aa8dd-111">*HMENU* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="aa8dd-111">*hmenu* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa8dd-112">Das Handle des Menüs.</span><span class="sxs-lookup"><span data-stu-id="aa8dd-112">The menu's handle.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aa8dd-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aa8dd-113">Remarks</span></span>

<span data-ttu-id="aa8dd-114">Das Objekt "Systemordner Ansicht" sendet diese Nachricht, wenn ein Menü ausgewählt wird, aber bevor es angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="aa8dd-114">The system folder view object sends this message when a menu is selected, but before it is displayed.</span></span> <span data-ttu-id="aa8dd-115">Verarbeiten Sie diese Meldung, wenn Sie beispielsweise Menübefehle aktivieren oder deaktivieren müssen.</span><span class="sxs-lookup"><span data-stu-id="aa8dd-115">Process this message if, for instance, you need to enable or disable menu commands.</span></span> <span data-ttu-id="aa8dd-116">Das Popup Menü kann wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="aa8dd-116">The popup menu can be:</span></span>

-   <span data-ttu-id="aa8dd-117">Das Menü "Datei", "Bearbeiten" oder "Ansicht".</span><span class="sxs-lookup"><span data-stu-id="aa8dd-117">The File, Edit, or View menu.</span></span>
-   <span data-ttu-id="aa8dd-118">Ein Menü der obersten Ebene, das vom Client definiert wird.</span><span class="sxs-lookup"><span data-stu-id="aa8dd-118">A top-level menu defined by the client.</span></span>
-   <span data-ttu-id="aa8dd-119">Ein Client definiertes Untermenü.</span><span class="sxs-lookup"><span data-stu-id="aa8dd-119">A client-defined submenu.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa8dd-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="aa8dd-120">Requirements</span></span>



| <span data-ttu-id="aa8dd-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa8dd-121">Requirement</span></span> | <span data-ttu-id="aa8dd-122">Wert</span><span class="sxs-lookup"><span data-stu-id="aa8dd-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="aa8dd-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aa8dd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="aa8dd-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aa8dd-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="aa8dd-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aa8dd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="aa8dd-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aa8dd-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="aa8dd-127">Header</span><span class="sxs-lookup"><span data-stu-id="aa8dd-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa8dd-128"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa8dd-128"><dt>Shlobj.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa8dd-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="aa8dd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa8dd-130">**sfvm \_ MergeMenu**</span><span class="sxs-lookup"><span data-stu-id="aa8dd-130">**SFVM\_MERGEMENU**</span></span>](sfvm-mergemenu.md)
</dt> </dl>

 

 
