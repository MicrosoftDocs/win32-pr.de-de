---
title: CB_RESETCONTENT Meldung (Winuser. h)
description: Entfernt alle Elemente aus dem Listenfeld und bearbeitet das Steuerelement eines Kombinations Felds.
ms.assetid: 55203c34-87ca-46e9-a914-a480d43ccadd
keywords:
- Windows-Steuerelemente für CB_RESETCONTENT Meldung
topic_type:
- apiref
api_name:
- CB_RESETCONTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3567f31ef98fffe42e53c4811acc786d41ae9f78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858890"
---
# <a name="cb_resetcontent-message"></a><span data-ttu-id="13566-104">CB \_ resetcontent-Meldung</span><span class="sxs-lookup"><span data-stu-id="13566-104">CB\_RESETCONTENT message</span></span>

<span data-ttu-id="13566-105">Entfernt alle Elemente aus dem Listenfeld und bearbeitet das Steuerelement eines Kombinations Felds.</span><span class="sxs-lookup"><span data-stu-id="13566-105">Removes all items from the list box and edit control of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="13566-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="13566-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13566-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="13566-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="13566-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="13566-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="13566-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="13566-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="13566-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="13566-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13566-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="13566-111">Return value</span></span>

<span data-ttu-id="13566-112">Diese Meldung gibt immer den Wert CB \_ okay zurück.</span><span class="sxs-lookup"><span data-stu-id="13566-112">This message always returns CB\_OKAY.</span></span>

## <a name="remarks"></a><span data-ttu-id="13566-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="13566-113">Remarks</span></span>

<span data-ttu-id="13566-114">Wenn Sie das Kombinations Feld mit einem vom Besitzer gezeichneten Stil, aber ohne den [**CBS \_ hasstrings**](combo-box-styles.md) -Stil erstellen, empfängt der Besitzer des Kombinations Felds eine [**WM \_ DeleteItem**](wm-deleteitem.md) -Meldung für jedes Element im Kombinations Feld.</span><span class="sxs-lookup"><span data-stu-id="13566-114">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the owner of the combo box receives a [**WM\_DELETEITEM**](wm-deleteitem.md) message for each item in the combo box.</span></span>

## <a name="requirements"></a><span data-ttu-id="13566-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13566-115">Requirements</span></span>



| <span data-ttu-id="13566-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13566-116">Requirement</span></span> | <span data-ttu-id="13566-117">Wert</span><span class="sxs-lookup"><span data-stu-id="13566-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13566-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="13566-118">Minimum supported client</span></span><br/> | <span data-ttu-id="13566-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="13566-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="13566-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="13566-120">Minimum supported server</span></span><br/> | <span data-ttu-id="13566-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="13566-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="13566-122">Header</span><span class="sxs-lookup"><span data-stu-id="13566-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="13566-123"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="13566-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13566-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13566-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="13566-125">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="13566-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="13566-126">**CB \_ deletestring**</span><span class="sxs-lookup"><span data-stu-id="13566-126">**CB\_DELETESTRING**</span></span>](cb-deletestring.md)
</dt> <dt>

[<span data-ttu-id="13566-127">**WM- \_ DeleteItem**</span><span class="sxs-lookup"><span data-stu-id="13566-127">**WM\_DELETEITEM**</span></span>](wm-deleteitem.md)
</dt> </dl>

 

 





