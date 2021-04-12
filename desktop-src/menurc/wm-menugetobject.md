---
title: WM_MENUGETOBJECT Meldung (Winuser. h)
description: Wird an den Besitzer eines Drag & Drop-Menüs gesendet, wenn der Maus Cursor in ein Menü Element oder von der Mitte des Elements zum oberen oder unteren Rand des Elements bewegt wird.
ms.assetid: 08348e43-3d21-4543-b624-5504575efced
keywords:
- WM_MENUGETOBJECT von Meldungs Menüs und anderen Ressourcen
topic_type:
- apiref
api_name:
- WM_MENUGETOBJECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08e124c7f2757a0d6d1d2ac0904052b6d3c255ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519204"
---
# <a name="wm_menugetobject-message"></a><span data-ttu-id="e2d21-104">WM \_ menugetobject-Meldung</span><span class="sxs-lookup"><span data-stu-id="e2d21-104">WM\_MENUGETOBJECT message</span></span>

<span data-ttu-id="e2d21-105">Wird an den Besitzer eines Drag & Drop-Menüs gesendet, wenn der Maus Cursor in ein Menü Element oder von der Mitte des Elements zum oberen oder unteren Rand des Elements bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="e2d21-105">Sent to the owner of a drag-and-drop menu when the mouse cursor enters a menu item or moves from the center of the item to the top or bottom of the item.</span></span>


```C++
#define WM_MENUGETOBJECT                0x0124
```



## <a name="parameters"></a><span data-ttu-id="e2d21-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2d21-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2d21-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e2d21-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2d21-108">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e2d21-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e2d21-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e2d21-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2d21-110">Ein Zeiger auf eine [**menugetobjectinfo**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="e2d21-110">A pointer to a [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2d21-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2d21-111">Return value</span></span>

<span data-ttu-id="e2d21-112">Die Anwendung muss einen der folgenden Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e2d21-112">The application should return one of the following values.</span></span>



| <span data-ttu-id="e2d21-113">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="e2d21-113">Return code/value</span></span>                                                                                                                                                | <span data-ttu-id="e2d21-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e2d21-114">Description</span></span>                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e2d21-115"><dt>**Mngo \_ NoError**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="e2d21-115"><dt>**MNGO\_NOERROR**</dt> <dt>0x00000001</dt></span></span> </dl>     | <span data-ttu-id="e2d21-116">Ein Schnittstellen Zeiger wurde im **pvobj** -Member von [**menugetobjectinfo**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e2d21-116">An interface pointer was returned in the **pvObj** member of [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo)</span></span><br/> |
| <dl> <span data-ttu-id="e2d21-117"><dt>**Mngo \_ Nointerface**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="e2d21-117"><dt>**MNGO\_NOINTERFACE**</dt> <dt>0x00000000</dt></span></span> </dl> | <span data-ttu-id="e2d21-118">Die-Schnittstelle wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e2d21-118">The interface is not supported.</span></span><br/>                                                                             |



 

## <a name="requirements"></a><span data-ttu-id="e2d21-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2d21-119">Requirements</span></span>



| <span data-ttu-id="e2d21-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2d21-120">Requirement</span></span> | <span data-ttu-id="e2d21-121">Wert</span><span class="sxs-lookup"><span data-stu-id="e2d21-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2d21-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e2d21-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e2d21-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2d21-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e2d21-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e2d21-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e2d21-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2d21-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e2d21-126">Header</span><span class="sxs-lookup"><span data-stu-id="e2d21-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2d21-127"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="e2d21-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2d21-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2d21-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2d21-129">Übersicht über Menüs</span><span class="sxs-lookup"><span data-stu-id="e2d21-129">Menus Overview</span></span>](menus.md)
</dt> </dl>

 

 





