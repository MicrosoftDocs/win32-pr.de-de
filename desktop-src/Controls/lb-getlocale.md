---
title: LB_GETLOCALE Meldung (Winuser. h)
description: Ruft das aktuelle Gebiets Schema des Listen Felds ab. Sie können das Gebiets Schema verwenden, um die richtige Sortierreihenfolge des angezeigten Texts (für Listenfelder mit dem lbs \_ -Sortier Stil) und des von der LB AddString-Nachricht hinzugefügten Texts zu bestimmen \_ .
ms.assetid: ec814b03-5ce2-4b81-a36c-ab4c115f88be
keywords:
- Windows-Steuerelemente für LB_GETLOCALE Meldung
topic_type:
- apiref
api_name:
- LB_GETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57620b62011dba234710caf1b5d1c429da37ace9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477289"
---
# <a name="lb_getlocale-message"></a><span data-ttu-id="32b4d-105">\_GetLocale-Nachricht des lb</span><span class="sxs-lookup"><span data-stu-id="32b4d-105">LB\_GETLOCALE message</span></span>

<span data-ttu-id="32b4d-106">Ruft das aktuelle Gebiets Schema des Listen Felds ab.</span><span class="sxs-lookup"><span data-stu-id="32b4d-106">Gets the current locale of the list box.</span></span> <span data-ttu-id="32b4d-107">Sie können das Gebiets Schema verwenden, um die richtige Sortierreihenfolge des angezeigten Texts (für Listenfelder mit dem [**lbs- \_ Sortier**](list-box-styles.md) Stil) und des von der [**lb \_ AddString**](lb-addstring.md) -Nachricht hinzugefügten Texts zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="32b4d-107">You can use the locale to determine the correct sorting order of displayed text (for list boxes with the [**LBS\_SORT**](list-box-styles.md) style) and of text added by the [**LB\_ADDSTRING**](lb-addstring.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="32b4d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="32b4d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32b4d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="32b4d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32b4d-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="32b4d-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="32b4d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="32b4d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32b4d-112">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="32b4d-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32b4d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="32b4d-113">Return value</span></span>

<span data-ttu-id="32b4d-114">Der Rückgabewert gibt das aktuelle Gebiets Schema des Listen Felds an.</span><span class="sxs-lookup"><span data-stu-id="32b4d-114">The return value specifies the current locale of the list box.</span></span> <span data-ttu-id="32b4d-115">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) enthält den Länder-/Regionscode, und das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den sprach Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="32b4d-115">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the country/region code and the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the language identifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="32b4d-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="32b4d-116">Remarks</span></span>

<span data-ttu-id="32b4d-117">Die Sprach-ID besteht aus einer unter Sprachen-ID und einem primären sprach Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="32b4d-117">The language identifier consists of a sublanguage identifier and a primary language identifier.</span></span> <span data-ttu-id="32b4d-118">Verwenden Sie das [**primarylangid**](/windows/desktop/api/winnt/nf-winnt-primarylangid) -Makro, um den Bezeichner der Primärsprache aus dem [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) des Rückgabewerts zu extrahieren, und das [**sublangid**](/windows/desktop/api/winnt/nf-winnt-sublangid) -Makro, um die unter Sprachen-ID zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="32b4d-118">Use the [**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid) macro to extract the primary language identifier from the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) of the return value, and the [**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid) macro to extract the sublanguage identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="32b4d-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="32b4d-119">Requirements</span></span>



| <span data-ttu-id="32b4d-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="32b4d-120">Requirement</span></span> | <span data-ttu-id="32b4d-121">Wert</span><span class="sxs-lookup"><span data-stu-id="32b4d-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32b4d-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="32b4d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="32b4d-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="32b4d-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="32b4d-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="32b4d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="32b4d-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="32b4d-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="32b4d-126">Header</span><span class="sxs-lookup"><span data-stu-id="32b4d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="32b4d-127"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="32b4d-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32b4d-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32b4d-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="32b4d-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="32b4d-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="32b4d-130">**LB- \_ AddString**</span><span class="sxs-lookup"><span data-stu-id="32b4d-130">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="32b4d-131">**LB- \_ setlocale**</span><span class="sxs-lookup"><span data-stu-id="32b4d-131">**LB\_SETLOCALE**</span></span>](lb-setlocale.md)
</dt> <dt>

<span data-ttu-id="32b4d-132">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="32b4d-132">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="32b4d-133">**Primarylangid**</span><span class="sxs-lookup"><span data-stu-id="32b4d-133">**PRIMARYLANGID**</span></span>](/windows/desktop/api/winnt/nf-winnt-primarylangid)
</dt> <dt>

[<span data-ttu-id="32b4d-134">**Sublangid**</span><span class="sxs-lookup"><span data-stu-id="32b4d-134">**SUBLANGID**</span></span>](/windows/desktop/api/winnt/nf-winnt-sublangid)
</dt> </dl>

 

