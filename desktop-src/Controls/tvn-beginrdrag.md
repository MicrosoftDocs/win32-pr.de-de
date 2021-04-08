---
title: TVN_BEGINRDRAG Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Baumansicht-Steuer Elements über die Initiierung eines Drag & Drop-Vorgangs mit der rechten Maustaste. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 4a61d8b5-ceb9-46a3-95ef-27e843e8c986
keywords:
- Windows-Steuerelemente für TVN_BEGINRDRAG Benachrichtigungs
topic_type:
- apiref
api_name:
- TVN_BEGINRDRAG
- TVN_BEGINRDRAGA
- TVN_BEGINRDRAGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bec15b5f48d4ed5612778622bb3655ae153c1b9f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957092"
---
# <a name="tvn_beginrdrag-notification-code"></a><span data-ttu-id="a7545-105">TVN \_ beginrdrag-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="a7545-105">TVN\_BEGINRDRAG notification code</span></span>

<span data-ttu-id="a7545-106">Benachrichtigt das übergeordnete Fenster eines Baumansicht-Steuer Elements über die Initiierung eines Drag & Drop-Vorgangs mit der rechten Maustaste.</span><span class="sxs-lookup"><span data-stu-id="a7545-106">Notifies a tree-view control's parent window about the initiation of a drag-and-drop operation involving the right mouse button.</span></span> <span data-ttu-id="a7545-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="a7545-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_BEGINRDRAG 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="a7545-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7545-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7545-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a7545-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a7545-110">Zeiger auf eine [**nmtreeview**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="a7545-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="a7545-111">Der **itemnew** -Member ist eine [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Struktur, die gültige Informationen in den **Hitem**-, **State**-und **LPARAM** -Membern zu dem Element enthält, das gezogen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a7545-111">The **itemNew** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains valid information in the **hItem**, **state**, and **lParam** members about the item to be dragged.</span></span> <span data-ttu-id="a7545-112">Der **ptdrag** -Member gibt die aktuellen Bildschirm Koordinaten der Maus an.</span><span class="sxs-lookup"><span data-stu-id="a7545-112">The **ptDrag** member specifies the current screen coordinates of the mouse.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7545-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a7545-113">Return value</span></span>

<span data-ttu-id="a7545-114">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a7545-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7545-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a7545-115">Requirements</span></span>



| <span data-ttu-id="a7545-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a7545-116">Requirement</span></span> | <span data-ttu-id="a7545-117">Wert</span><span class="sxs-lookup"><span data-stu-id="a7545-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a7545-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a7545-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a7545-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a7545-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a7545-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a7545-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a7545-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a7545-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a7545-122">Header</span><span class="sxs-lookup"><span data-stu-id="a7545-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7545-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7545-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="a7545-124">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="a7545-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a7545-125">**TVN \_ Beginrdragw** (Unicode) und **TVN \_ beginrdraga** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a7545-125">**TVN\_BEGINRDRAGW** (Unicode) and **TVN\_BEGINRDRAGA** (ANSI)</span></span><br/>             |



 

 





