---
title: CB_SHOWDROPDOWN Meldung (Winuser. h)
description: Eine Anwendung sendet eine CB- \_ ShowDropDown-Nachricht, um das Listenfeld eines Kombinations Felds mit dem Format "CBS \_ Dropdown" oder "CBS DropDownList" anzuzeigen oder auszublenden \_ .
ms.assetid: 32b995d7-eed6-4173-8525-0d356dea39b3
keywords:
- Windows-Steuerelemente für CB_SHOWDROPDOWN Meldung
topic_type:
- apiref
api_name:
- CB_SHOWDROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb66e9a0ecf3b6680fce9aca7f680fd6e6fd13e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105603"
---
# <a name="cb_showdropdown-message"></a><span data-ttu-id="b5533-104">CB- \_ ShowDropDown-Meldung</span><span class="sxs-lookup"><span data-stu-id="b5533-104">CB\_SHOWDROPDOWN message</span></span>

<span data-ttu-id="b5533-105">Eine Anwendung sendet eine **CB- \_ ShowDropDown** -Nachricht, um das Listenfeld eines Kombinations Felds mit dem Format " [**CBS \_ Dropdown**](combo-box-styles.md) " oder " [**CBS \_ DropDownList**](combo-box-styles.md) " anzuzeigen oder auszublenden.</span><span class="sxs-lookup"><span data-stu-id="b5533-105">An application sends a **CB\_SHOWDROPDOWN** message to show or hide the list box of a combo box that has the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="b5533-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5533-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5533-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b5533-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5533-108">Ein **boolescher** Wert, der angibt, ob das Dropdown-Listenfeld angezeigt oder ausgeblendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b5533-108">A **BOOL** that specifies whether the drop-down list box is to be shown or hidden.</span></span> <span data-ttu-id="b5533-109">Der Wert **true** zeigt das Listenfeld an. der Wert **false** blendet ihn aus.</span><span class="sxs-lookup"><span data-stu-id="b5533-109">A value of **TRUE** shows the list box; a value of **FALSE** hides it.</span></span>

</dd> <dt>

<span data-ttu-id="b5533-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b5533-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5533-111">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b5533-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5533-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b5533-112">Return value</span></span>

<span data-ttu-id="b5533-113">Der Rückgabewert ist immer " **true**".</span><span class="sxs-lookup"><span data-stu-id="b5533-113">The return value is always **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5533-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b5533-114">Remarks</span></span>

<span data-ttu-id="b5533-115">Diese Meldung hat keine Auswirkung auf ein Kombinations Feld, das mit [**dem \_ einfachen CBS**](combo-box-styles.md) -Stil erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5533-115">This message has no effect on a combo box created with the [**CBS\_SIMPLE**](combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5533-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5533-116">Requirements</span></span>



| <span data-ttu-id="b5533-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5533-117">Requirement</span></span> | <span data-ttu-id="b5533-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b5533-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5533-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b5533-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b5533-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5533-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b5533-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b5533-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b5533-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5533-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b5533-123">Header</span><span class="sxs-lookup"><span data-stu-id="b5533-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5533-124"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="b5533-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5533-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5533-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5533-126">**CB \_ getdroppedstate**</span><span class="sxs-lookup"><span data-stu-id="b5533-126">**CB\_GETDROPPEDSTATE**</span></span>](cb-getdroppedstate.md)
</dt> </dl>

 

 





