---
title: CB_GETMINVISIBLE Meldung (kommstrg. h)
description: Ruft die Mindestanzahl sichtbarer Elemente in der Dropdown Liste eines Kombinations Felds ab.
ms.assetid: 9861358a-1ef9-4d78-8ec8-561b97f3f18e
keywords:
- Windows-Steuerelemente für CB_GETMINVISIBLE Meldung
topic_type:
- apiref
api_name:
- CB_GETMINVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dcf4fe5088d9c994e232a64ba16bbddf11b0d48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858891"
---
# <a name="cb_getminvisible-message"></a><span data-ttu-id="6f708-104">CB \_ getminvisible-Meldung</span><span class="sxs-lookup"><span data-stu-id="6f708-104">CB\_GETMINVISIBLE message</span></span>

<span data-ttu-id="6f708-105">Ruft die Mindestanzahl sichtbarer Elemente in der Dropdown Liste eines Kombinations Felds ab.</span><span class="sxs-lookup"><span data-stu-id="6f708-105">Gets the minimum number of visible items in the drop-down list of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="6f708-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f708-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f708-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6f708-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6f708-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="6f708-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6f708-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6f708-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6f708-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="6f708-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f708-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6f708-111">Return value</span></span>

<span data-ttu-id="6f708-112">Der Rückgabewert ist die Mindestanzahl sichtbarer Elemente.</span><span class="sxs-lookup"><span data-stu-id="6f708-112">The return value is the minimum number of visible items.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f708-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f708-113">Remarks</span></span>

<span data-ttu-id="6f708-114">Wenn die Anzahl der Elemente in der Dropdown Liste den minimalen Wert überschreitet, verwendet das Kombinations Feld eine Schiebe Leiste.</span><span class="sxs-lookup"><span data-stu-id="6f708-114">When the number of items in the drop-down list is greater than the minimum, the combo box uses a scroll bar.</span></span>

<span data-ttu-id="6f708-115">Diese Meldung wird ignoriert, wenn das Kombinations Feld-Steuerelement den Stil [**CBS \_ nointegralheight**](combo-box-styles.md)hat.</span><span class="sxs-lookup"><span data-stu-id="6f708-115">This message is ignored if the combo box control has style [**CBS\_NOINTEGRALHEIGHT**](combo-box-styles.md).</span></span>

<span data-ttu-id="6f708-116">Um **CB \_ getminvisible** verwenden zu können, muss die Anwendung comctl32.dll Version 6 im Manifest angeben.</span><span class="sxs-lookup"><span data-stu-id="6f708-116">To use **CB\_GETMINVISIBLE**, the application must specify comctl32.dll version 6 in the manifest.</span></span> <span data-ttu-id="6f708-117">Weitere Informationen finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6f708-117">For more information, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f708-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6f708-118">Requirements</span></span>



| <span data-ttu-id="6f708-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6f708-119">Requirement</span></span> | <span data-ttu-id="6f708-120">Wert</span><span class="sxs-lookup"><span data-stu-id="6f708-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6f708-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6f708-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6f708-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6f708-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6f708-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6f708-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6f708-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6f708-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6f708-125">Header</span><span class="sxs-lookup"><span data-stu-id="6f708-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f708-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f708-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f708-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f708-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="6f708-128">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="6f708-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6f708-129">**CB \_ setminvisible**</span><span class="sxs-lookup"><span data-stu-id="6f708-129">**CB\_SETMINVISIBLE**</span></span>](cb-setminvisible.md)
</dt> <dt>

[<span data-ttu-id="6f708-130">**ComboBox \_ getminvisible**</span><span class="sxs-lookup"><span data-stu-id="6f708-130">**ComboBox\_GetMinVisible**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-combobox_getminvisible)
</dt> </dl>

 

 





