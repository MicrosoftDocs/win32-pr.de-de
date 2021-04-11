---
title: EM_SETEXTENDEDSTYLE Meldung (kommstrg. h)
description: Informiert das Bearbeitungs Steuerelement, dass erweiterte Stile festgelegt werden sollen. Senden Sie diese Nachricht, oder verwenden Sie die Makro Bearbeitung von "* \_ textendedstyle".
ms.assetid: 4ca010c3-2c70-41e5-ade4-11e1895fda26
keywords:
- Windows-Steuerelemente für EM_SETEXTENDEDSTYLE Meldung
topic_type:
- apiref
api_name:
- EM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 560b675927b4497810b8d492fd89b5765aa5a2c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105572"
---
# <a name="em_setextendedstyle-message"></a><span data-ttu-id="29f02-105">EM/ \_ textendedstyle-Nachricht</span><span class="sxs-lookup"><span data-stu-id="29f02-105">EM\_SETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="29f02-106">Informiert das Bearbeitungs Steuerelement, dass erweiterte Stile festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="29f02-106">Informs the edit control to set extended styles.</span></span> <span data-ttu-id="29f02-107">Senden Sie diese Nachricht, oder verwenden Sie die Makro Bearbeitung von "\* [**\_ textendedstyle**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setextendedstyle)".</span><span class="sxs-lookup"><span data-stu-id="29f02-107">Send this message or use the macro [**Edit\_SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setextendedstyle).</span></span>

## <a name="parameters"></a><span data-ttu-id="29f02-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="29f02-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29f02-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="29f02-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="29f02-110">Maske, die verwendet wird, um die festzulegenden Stile auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="29f02-110">Mask used to select the styles to be set.</span></span>

</dd> <dt>

<span data-ttu-id="29f02-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="29f02-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="29f02-112">Der-Wert, der den erweiterten Stil angibt.</span><span class="sxs-lookup"><span data-stu-id="29f02-112">Value that indicates the extended style.</span></span> <span data-ttu-id="29f02-113">Weitere Informationen zu Stilen finden Sie unter [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="29f02-113">For more information on styles, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29f02-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="29f02-114">Return value</span></span>

<span data-ttu-id="29f02-115">Wenn diese Nachricht erfolgreich ist, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="29f02-115">If this message succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="29f02-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="29f02-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="29f02-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29f02-117">Remarks</span></span>

<span data-ttu-id="29f02-118">Die erweiterten Stile für ein Bearbeitungs Steuerelement haben nichts mit den erweiterten Stilen zu tun, die mit der Funktion " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " oder der Funktion " [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="29f02-118">The extended styles for an edit control have nothing to do with the extended styles used with function [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) or function [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span></span>

## <a name="requirements"></a><span data-ttu-id="29f02-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29f02-119">Requirements</span></span>



| <span data-ttu-id="29f02-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29f02-120">Requirement</span></span> | <span data-ttu-id="29f02-121">Wert</span><span class="sxs-lookup"><span data-stu-id="29f02-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="29f02-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="29f02-122">Minimum supported client</span></span><br/> | <span data-ttu-id="29f02-123">Windows 10, Version 1809, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="29f02-123">Windows 10, version 1809 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="29f02-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="29f02-124">Minimum supported server</span></span><br/> | <span data-ttu-id="29f02-125">Nur Windows Server 2019 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="29f02-125">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="29f02-126">Header</span><span class="sxs-lookup"><span data-stu-id="29f02-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="29f02-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="29f02-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

