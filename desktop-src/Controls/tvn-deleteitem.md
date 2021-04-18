---
title: TVN_DELETEITEM Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Baumansicht-Steuer Elements, dass ein Element gelöscht wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 0d8801e0-02ae-40c9-8625-83d98b434d0a
keywords:
- Windows-Steuerelemente für TVN_DELETEITEM Benachrichtigungs
topic_type:
- apiref
api_name:
- TVN_DELETEITEM
- TVN_DELETEITEMA
- TVN_DELETEITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2953ca0cf272b102a08fba0516d4891dccde9daf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476947"
---
# <a name="tvn_deleteitem-notification-code"></a><span data-ttu-id="a9b7c-105">TVN \_ DeleteItem-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="a9b7c-105">TVN\_DELETEITEM notification code</span></span>

<span data-ttu-id="a9b7c-106">Benachrichtigt das übergeordnete Fenster eines Baumansicht-Steuer Elements, dass ein Element gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="a9b7c-106">Notifies a tree-view control's parent window that an item is being deleted.</span></span> <span data-ttu-id="a9b7c-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="a9b7c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_DELETEITEM 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="a9b7c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9b7c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9b7c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a9b7c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9b7c-110">Zeiger auf eine [**nmtreeview**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="a9b7c-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="a9b7c-111">Der **itemold** -Member ist eine [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Struktur, deren **Hitem** -Member und **LPARAM** -Member gültige Informationen über das Element enthalten, das gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="a9b7c-111">The **itemOld** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure whose **hItem** and **lParam** members contain valid information about the item being deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9b7c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a9b7c-112">Return value</span></span>

<span data-ttu-id="a9b7c-113">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a9b7c-113">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9b7c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9b7c-114">Remarks</span></span>

<span data-ttu-id="a9b7c-115">Wenn der **LPARAM** -Member der [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Struktur auf den von der Anwendung belegten Arbeitsspeicher verweist, können Sie ihn freigeben, wenn Sie den TVN \_ DeleteItem-Benachrichtigungs Code erhalten.</span><span class="sxs-lookup"><span data-stu-id="a9b7c-115">If the **lParam** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure points to memory allocated by your application, you can free it when you receive the TVN\_DELETEITEM notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9b7c-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9b7c-116">Requirements</span></span>



| <span data-ttu-id="a9b7c-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a9b7c-117">Requirement</span></span> | <span data-ttu-id="a9b7c-118">Wert</span><span class="sxs-lookup"><span data-stu-id="a9b7c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a9b7c-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a9b7c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a9b7c-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9b7c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a9b7c-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a9b7c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a9b7c-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9b7c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a9b7c-123">Header</span><span class="sxs-lookup"><span data-stu-id="a9b7c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9b7c-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9b7c-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="a9b7c-125">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="a9b7c-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a9b7c-126">**TVN \_ Deleteitemw** (Unicode) und **TVN \_ deleteitema** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a9b7c-126">**TVN\_DELETEITEMW** (Unicode) and **TVN\_DELETEITEMA** (ANSI)</span></span><br/>             |



 

 





