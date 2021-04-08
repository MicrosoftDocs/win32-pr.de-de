---
title: LVM_GETBKIMAGE Meldung (kommstrg. h)
description: Ruft das Hintergrundbild in einem Listenansicht-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des ListView \_ getbkimage-Makros senden.
ms.assetid: db0e8f31-746a-4a16-b689-68da696e3657
keywords:
- Windows-Steuerelemente für LVM_GETBKIMAGE Meldung
topic_type:
- apiref
api_name:
- LVM_GETBKIMAGE
- LVM_GETBKIMAGEA
- LVM_GETBKIMAGEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29e178bae10b9bed880213ca4a4ab2a1b4e07239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739960"
---
# <a name="lvm_getbkimage-message"></a><span data-ttu-id="bb11f-105">LVM \_ getbkimage-Nachricht</span><span class="sxs-lookup"><span data-stu-id="bb11f-105">LVM\_GETBKIMAGE message</span></span>

<span data-ttu-id="bb11f-106">Ruft das Hintergrundbild in einem Listenansicht-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="bb11f-106">Gets the background image in a list-view control.</span></span> <span data-ttu-id="bb11f-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ getbkimage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getbkimage) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="bb11f-107">You can send this message explicitly or by using the [**ListView\_GetBkImage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getbkimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bb11f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb11f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb11f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bb11f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bb11f-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="bb11f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bb11f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bb11f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb11f-112">Ein Zeiger auf eine " [**lvbkimage**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) "-Struktur, die die Hintergrundbild Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="bb11f-112">A pointer to an [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) structure that will receive the background image information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb11f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bb11f-113">Return value</span></span>

<span data-ttu-id="bb11f-114">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="bb11f-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb11f-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb11f-115">Requirements</span></span>



| <span data-ttu-id="bb11f-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb11f-116">Requirement</span></span> | <span data-ttu-id="bb11f-117">Wert</span><span class="sxs-lookup"><span data-stu-id="bb11f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb11f-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bb11f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bb11f-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bb11f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bb11f-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bb11f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bb11f-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bb11f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bb11f-122">Header</span><span class="sxs-lookup"><span data-stu-id="bb11f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb11f-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb11f-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="bb11f-124">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="bb11f-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bb11f-125">**LVM \_ Getbkimagew** (Unicode) und **LVM \_ getbkimagea** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="bb11f-125">**LVM\_GETBKIMAGEW** (Unicode) and **LVM\_GETBKIMAGEA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="bb11f-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb11f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb11f-127">**LVM- \_ setbkimage**</span><span class="sxs-lookup"><span data-stu-id="bb11f-127">**LVM\_SETBKIMAGE**</span></span>](lvm-setbkimage.md)
</dt> </dl>

 

 





