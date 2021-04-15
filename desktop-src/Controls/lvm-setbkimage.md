---
title: LVM_SETBKIMAGE Meldung (kommstrg. h)
description: Legt das Hintergrundbild in einem Listenansicht-Steuerelement fest. Sie können diese Nachricht explizit oder mithilfe des ListView- \_ Makros setbkimage senden.
ms.assetid: 8fdd363c-ac12-498b-80b7-aaa5741cfd76
keywords:
- Windows-Steuerelemente für LVM_SETBKIMAGE Meldung
topic_type:
- apiref
api_name:
- LVM_SETBKIMAGE
- LVM_SETBKIMAGEA
- LVM_SETBKIMAGEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e22bebdcb36faff56dfabab721731acb55fdec14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477565"
---
# <a name="lvm_setbkimage-message"></a><span data-ttu-id="c8016-105">LVM- \_ setbkimage-Meldung</span><span class="sxs-lookup"><span data-stu-id="c8016-105">LVM\_SETBKIMAGE message</span></span>

<span data-ttu-id="c8016-106">Legt das Hintergrundbild in einem Listenansicht-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="c8016-106">Sets the background image in a list-view control.</span></span> <span data-ttu-id="c8016-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView-Makros \_ setbkimage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkimage) senden.</span><span class="sxs-lookup"><span data-stu-id="c8016-107">You can send this message explicitly or by using the [**ListView\_SetBkImage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c8016-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8016-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8016-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c8016-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8016-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="c8016-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c8016-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c8016-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8016-112">Ein Zeiger auf eine " [**lvbkimage**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) "-Struktur, die die neuen Hintergrundbild Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="c8016-112">Pointer to a [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) structure that contains the new background image information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8016-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c8016-113">Return value</span></span>

<span data-ttu-id="c8016-114">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="c8016-114">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="c8016-115">Gibt 0 (null) zurück, wenn der **ulflags** -Member der Struktur " [**lvbkimage**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) " " **lvbkif \_ Source \_ None**" ist</span><span class="sxs-lookup"><span data-stu-id="c8016-115">Returns zero if the **ulFlags** member of the [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) structure is **LVBKIF\_SOURCE\_NONE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8016-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c8016-116">Remarks</span></span>

<span data-ttu-id="c8016-117">Da das Listenansicht-Steuerelement OLE com zum Bearbeiten der Hintergrundbilder verwendet, muss die aufrufende Anwendung vor dem Senden dieser Nachricht [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) oder [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c8016-117">Because the list-view control uses OLE COM to manipulate the background images, the calling application must call [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) before sending this message.</span></span> <span data-ttu-id="c8016-118">Es empfiehlt sich, eine dieser Funktionen aufzurufen, wenn die Anwendung initialisiert wird, und beim Beenden der Anwendung entweder " [**zählinitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) " oder " [**OleUninitialize**](/windows/desktop/api/ole2/nf-ole2-oleuninitialize) " aufruft.</span><span class="sxs-lookup"><span data-stu-id="c8016-118">It is best to call one of these functions when the application is initialized and call either [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) or [**OleUninitialize**](/windows/desktop/api/ole2/nf-ole2-oleuninitialize) when the application is terminating.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8016-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8016-119">Requirements</span></span>



| <span data-ttu-id="c8016-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c8016-120">Requirement</span></span> | <span data-ttu-id="c8016-121">Wert</span><span class="sxs-lookup"><span data-stu-id="c8016-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c8016-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c8016-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c8016-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c8016-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c8016-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c8016-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c8016-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c8016-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c8016-126">Header</span><span class="sxs-lookup"><span data-stu-id="c8016-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8016-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8016-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="c8016-128">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="c8016-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c8016-129">**LVM \_ Setbkimagew** (Unicode) und **LVM \_ setbkimagea** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c8016-129">**LVM\_SETBKIMAGEW** (Unicode) and **LVM\_SETBKIMAGEA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="c8016-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8016-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8016-131">**LVM \_ getbkimage**</span><span class="sxs-lookup"><span data-stu-id="c8016-131">**LVM\_GETBKIMAGE**</span></span>](lvm-getbkimage.md)
</dt> </dl>

 

