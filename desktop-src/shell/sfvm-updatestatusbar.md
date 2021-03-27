---
description: 'Benachrichtigt das Rückruf Objekt, dass die Statusleiste aktualisiert wird. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
title: SFVM_UPDATESTATUSBAR Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: f1bac364-1011-4308-8b9b-8ed1800dd30d
api_name:
- SFVM_UPDATESTATUSBAR
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 14045c797d7292099c1c7b2c67f5958609d8d6b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994814"
---
# <a name="sfvm_updatestatusbar-message"></a><span data-ttu-id="90624-104">Sfvm \_ updatestatusbar-Meldung</span><span class="sxs-lookup"><span data-stu-id="90624-104">SFVM\_UPDATESTATUSBAR message</span></span>

<span data-ttu-id="90624-105">Benachrichtigt das Rückruf Objekt, dass die Statusleiste aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="90624-105">Notifies the callback object that the status bar is being updated.</span></span> <span data-ttu-id="90624-106">Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.</span><span class="sxs-lookup"><span data-stu-id="90624-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_UPDATESTATUSBAR 

    wParam = (WPARAM)(BOOL) fInitialize;

            
```



## <a name="parameters"></a><span data-ttu-id="90624-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="90624-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90624-108">*finitialize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90624-108">*fInitialize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90624-109">Ein **boolescher** Wert, der auf **true** festgelegt wird, wenn die Statusleiste initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="90624-109">A **BOOL** value that is set to **TRUE** if the status bar is being initialized.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="90624-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90624-110">Remarks</span></span>

<span data-ttu-id="90624-111">Wenn Sie diese Benachrichtigung erhalten:</span><span class="sxs-lookup"><span data-stu-id="90624-111">When you receive this notification:</span></span>

-   <span data-ttu-id="90624-112">Gibt "S OK" zurück, \_ Wenn Sie das Update verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="90624-112">Return S\_OK if you will handle the update.</span></span>
-   <span data-ttu-id="90624-113">Geben \_ Sie HRESULT (Schweregrad \_ erfolgreich, 0, 1) zurück, damit das Systemordner-Ansichts Objekt den Text der Statusleiste festlegen kann.</span><span class="sxs-lookup"><span data-stu-id="90624-113">Return MAKE\_HRESULT(SEVERITY\_SUCCESS,0,1) to have the system folder view object set the status bar text.</span></span>
-   <span data-ttu-id="90624-114">Return E \_ schlägt fehl, wenn das Ansichts Objekt des System Ordners die Statusleiste nicht verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="90624-114">Return E\_FAIL to have the system folder view object handle the status bar.</span></span>

<span data-ttu-id="90624-115">Der Standardtext der Statusleiste lautet wie folgt.</span><span class="sxs-lookup"><span data-stu-id="90624-115">The default status bar text is as follows.</span></span>



| <span data-ttu-id="90624-116">Status</span><span class="sxs-lookup"><span data-stu-id="90624-116">Status</span></span>                      | <span data-ttu-id="90624-117">Statusleistentext</span><span class="sxs-lookup"><span data-stu-id="90624-117">Status bar text</span></span>                         |
|-----------------------------|-----------------------------------------|
| <span data-ttu-id="90624-118">Keine Elemente ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="90624-118">No items selected</span></span>           | <span data-ttu-id="90624-119">" \# \# Objects" (im Ordner)</span><span class="sxs-lookup"><span data-stu-id="90624-119">"\#\# objects" (in the folder)</span></span>          |
| <span data-ttu-id="90624-120">Ein ausgewähltes Element</span><span class="sxs-lookup"><span data-stu-id="90624-120">One item selected</span></span>           | <span data-ttu-id="90624-121">Der Infotipp für das Element, falls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="90624-121">The infotip for the item, if available.</span></span> |
| <span data-ttu-id="90624-122">Es wurden mehrere Elemente ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="90624-122">More than one item selected</span></span> | <span data-ttu-id="90624-123">" \# \# ausgewählte Objekte"</span><span class="sxs-lookup"><span data-stu-id="90624-123">"\#\# objects selected"</span></span>                 |



 

## <a name="requirements"></a><span data-ttu-id="90624-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="90624-124">Requirements</span></span>



| <span data-ttu-id="90624-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="90624-125">Requirement</span></span> | <span data-ttu-id="90624-126">Wert</span><span class="sxs-lookup"><span data-stu-id="90624-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="90624-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="90624-127">Minimum supported client</span></span><br/> | <span data-ttu-id="90624-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90624-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="90624-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="90624-129">Minimum supported server</span></span><br/> | <span data-ttu-id="90624-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90624-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="90624-131">Header</span><span class="sxs-lookup"><span data-stu-id="90624-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="90624-132"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="90624-132"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
