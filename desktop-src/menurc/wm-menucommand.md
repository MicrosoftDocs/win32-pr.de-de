---
title: WM_MENUCOMMAND Meldung (Winuser. h)
description: Wird gesendet, wenn der Benutzer eine Auswahl aus einem Menü trifft.
ms.assetid: 1ed702ef-8d32-4d4c-a68a-ffd199112ced
keywords:
- WM_MENUCOMMAND von Meldungs Menüs und anderen Ressourcen
topic_type:
- apiref
api_name:
- WM_MENUCOMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13288c49327b536db6ebef8a41526facd3fb2d51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392222"
---
# <a name="wm_menucommand-message"></a><span data-ttu-id="39af0-104">WM- \_ MenuCommand-Meldung</span><span class="sxs-lookup"><span data-stu-id="39af0-104">WM\_MENUCOMMAND message</span></span>

<span data-ttu-id="39af0-105">Wird gesendet, wenn der Benutzer eine Auswahl aus einem Menü trifft.</span><span class="sxs-lookup"><span data-stu-id="39af0-105">Sent when the user makes a selection from a menu.</span></span>


```C++
#define WM_MENUCOMMAND                  0x0126
```



## <a name="parameters"></a><span data-ttu-id="39af0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="39af0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39af0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="39af0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39af0-108">Der null basierte Index des ausgewählten Elements.</span><span class="sxs-lookup"><span data-stu-id="39af0-108">The zero-based index of the item selected.</span></span>

</dd> <dt>

<span data-ttu-id="39af0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="39af0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39af0-110">Ein Handle für das Menü für das ausgewählte Element.</span><span class="sxs-lookup"><span data-stu-id="39af0-110">A handle to the menu for the item selected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39af0-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39af0-111">Remarks</span></span>

<span data-ttu-id="39af0-112">Mit der " **WM \_ MenuCommand** "-Meldung erhalten Sie ein Handle für das Menü, sodass Sie auf die Menü Daten in der [**menuinfo**](/windows/win32/api/winuser/ns-winuser-menuinfo) -Struktur zugreifen können. Außerdem erhalten Sie den Index des ausgewählten Elements, das in der Regel von den Anwendungen benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="39af0-112">The **WM\_MENUCOMMAND** message gives you a handle to the menu so you can access the menu data in the [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) structure and also gives you the index of the selected item, which is typically what applications need.</span></span> <span data-ttu-id="39af0-113">Im Gegensatz dazu gibt Ihnen die [**WM- \_ Befehls**](wm-command.md) Meldung den Menü Element Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="39af0-113">In contrast, the [**WM\_COMMAND**](wm-command.md) message gives you the menu item identifier.</span></span>

<span data-ttu-id="39af0-114">Die " **WM \_ MenuCommand** "-Meldung wird nur für Menüs gesendet, die mit dem im **dwstyle** -Member der [**menuinfo**](/windows/win32/api/winuser/ns-winuser-menuinfo) -Struktur festgelegten **MNS- \_ notifybypos** -Flag definiert werden.</span><span class="sxs-lookup"><span data-stu-id="39af0-114">The **WM\_MENUCOMMAND** message is sent only for menus that are defined with the **MNS\_NOTIFYBYPOS** flag set in the **dwStyle** member of the [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="39af0-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39af0-115">Requirements</span></span>



| <span data-ttu-id="39af0-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39af0-116">Requirement</span></span> | <span data-ttu-id="39af0-117">Wert</span><span class="sxs-lookup"><span data-stu-id="39af0-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39af0-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="39af0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="39af0-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39af0-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="39af0-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="39af0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="39af0-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39af0-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="39af0-122">Header</span><span class="sxs-lookup"><span data-stu-id="39af0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="39af0-123"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="39af0-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39af0-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39af0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39af0-125">Übersicht über Menüs</span><span class="sxs-lookup"><span data-stu-id="39af0-125">Menus Overview</span></span>](menus.md)
</dt> </dl>

 

 





