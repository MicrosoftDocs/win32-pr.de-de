---
title: CB_SETLOCALE Meldung (Winuser. h)
description: Eine Anwendung sendet eine CB- \_ setlocale-Nachricht, um das aktuelle Gebiets Schema des Kombinations Felds festzulegen. Wenn das Kombinations Feld den CBS \_ -Sortier Stil hat und mithilfe von CB \_ AddString Zeichen folgen hinzugefügt werden, wirkt sich das Gebiets Schema eines Kombinations Felds darauf aus, wie Listenelemente sortiert werden.
ms.assetid: 06f9c69d-1220-490f-bc67-6e125f696e87
keywords:
- Windows-Steuerelemente für CB_SETLOCALE Meldung
topic_type:
- apiref
api_name:
- CB_SETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 025f33dc8ba236965a98ca984446b04846ecd2ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477649"
---
# <a name="cb_setlocale-message"></a><span data-ttu-id="6001f-105">CB- \_ setlocale-Meldung</span><span class="sxs-lookup"><span data-stu-id="6001f-105">CB\_SETLOCALE message</span></span>

<span data-ttu-id="6001f-106">Eine Anwendung sendet eine **CB- \_ setlocale** -Nachricht, um das aktuelle Gebiets Schema des Kombinations Felds festzulegen.</span><span class="sxs-lookup"><span data-stu-id="6001f-106">An application sends a **CB\_SETLOCALE** message to set the current locale of the combo box.</span></span> <span data-ttu-id="6001f-107">Wenn das Kombinations Feld den [**CBS- \_ Sortier**](combo-box-styles.md) Stil hat und mithilfe von [**CB \_ AddString Zeichen**](cb-addstring.md)folgen hinzugefügt werden, wirkt sich das Gebiets Schema eines Kombinations Felds darauf aus, wie Listenelemente sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="6001f-107">If the combo box has the [**CBS\_SORT**](combo-box-styles.md) style and strings are added using [**CB\_ADDSTRING**](cb-addstring.md), the locale of a combo box affects how list items are sorted.</span></span>

## <a name="parameters"></a><span data-ttu-id="6001f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6001f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6001f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6001f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6001f-110">Gibt den Gebiets Schema Bezeichner für das Kombinations Feld an, das beim Hinzufügen von Text zum Sortieren verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6001f-110">Specifies the locale identifier for the combo box to use for sorting when adding text.</span></span>

</dd> <dt>

<span data-ttu-id="6001f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6001f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6001f-112">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6001f-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6001f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6001f-113">Return value</span></span>

<span data-ttu-id="6001f-114">Der Rückgabewert ist der vorherige Gebiets Schema Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="6001f-114">The return value is the previous locale identifier.</span></span> <span data-ttu-id="6001f-115">Wenn *wParam* ein Gebiets Schema angibt, das nicht auf dem System installiert ist, ist der Rückgabewert CB \_ Err, und das aktuelle Kombinations Feld-Gebiets Schema wird nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="6001f-115">If *wParam* specifies a locale not installed on the system, the return value is CB\_ERR and the current combo box locale is not changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="6001f-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6001f-116">Remarks</span></span>

<span data-ttu-id="6001f-117">Verwenden Sie das [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) -Makro, um einen Gebiets Schema Bezeichner und das [**makelangid-**](/windows/desktop/api/winnt/nf-winnt-makelangid) Makro zum Erstellen eines sprach Bezeichners zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6001f-117">Use the [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) macro to construct a locale identifier and the [**MAKELANGID**](/windows/desktop/api/winnt/nf-winnt-makelangid) macro to construct a language identifier.</span></span> <span data-ttu-id="6001f-118">Die Sprach-ID besteht aus einer primär Sprachen-ID und einer unter Sprachen-ID.</span><span class="sxs-lookup"><span data-stu-id="6001f-118">The language identifier is made up of a primary language identifier and a sublanguage identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="6001f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6001f-119">Requirements</span></span>



| <span data-ttu-id="6001f-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6001f-120">Requirement</span></span> | <span data-ttu-id="6001f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="6001f-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6001f-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6001f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6001f-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6001f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6001f-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6001f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6001f-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6001f-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6001f-126">Header</span><span class="sxs-lookup"><span data-stu-id="6001f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6001f-127"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="6001f-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6001f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6001f-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="6001f-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="6001f-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6001f-130">**CB \_ AddString**</span><span class="sxs-lookup"><span data-stu-id="6001f-130">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="6001f-131">**CB \_ getLocale**</span><span class="sxs-lookup"><span data-stu-id="6001f-131">**CB\_GETLOCALE**</span></span>](cb-getlocale.md)
</dt> <dt>

<span data-ttu-id="6001f-132">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="6001f-132">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="6001f-133">**Makelangid**</span><span class="sxs-lookup"><span data-stu-id="6001f-133">**MAKELANGID**</span></span>](/windows/desktop/api/winnt/nf-winnt-makelangid)
</dt> <dt>

[<span data-ttu-id="6001f-134">**MAKELCID**</span><span class="sxs-lookup"><span data-stu-id="6001f-134">**MAKELCID**</span></span>](/windows/desktop/api/winnt/nf-winnt-makelcid)
</dt> </dl>

 

