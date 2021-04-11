---
title: CB_GETLOCALE Meldung (Winuser. h)
description: Ruft das aktuelle Gebiets Schema des Kombinations Felds ab. Das Gebiets Schema wird verwendet, um die richtige Sortierreihenfolge des angezeigten Texts für Kombinations Felder mit dem CBS \_ -Sortier Stil und Text zu bestimmen, der mithilfe der CB \_ AddString-Nachricht hinzugefügt wurde.
ms.assetid: 57c77ce2-bad0-43f3-8325-f2a7227994ec
keywords:
- Windows-Steuerelemente für CB_GETLOCALE Meldung
topic_type:
- apiref
api_name:
- CB_GETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 847d9f73e8bf0b1d533d0b79ba86d939bee0e9b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040599"
---
# <a name="cb_getlocale-message"></a><span data-ttu-id="02e09-105">CB \_ getLocale-Meldung</span><span class="sxs-lookup"><span data-stu-id="02e09-105">CB\_GETLOCALE message</span></span>

<span data-ttu-id="02e09-106">Ruft das aktuelle Gebiets Schema des Kombinations Felds ab.</span><span class="sxs-lookup"><span data-stu-id="02e09-106">Gets the current locale of the combo box.</span></span> <span data-ttu-id="02e09-107">Das Gebiets Schema wird verwendet, um die richtige Sortierreihenfolge des angezeigten Texts für Kombinations Felder mit dem [**CBS- \_ Sortier**](combo-box-styles.md) Stil und Text zu bestimmen, der mithilfe der [**CB \_ AddString**](cb-addstring.md) -Nachricht hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="02e09-107">The locale is used to determine the correct sorting order of displayed text for combo boxes with the [**CBS\_SORT**](combo-box-styles.md) style and text added by using the [**CB\_ADDSTRING**](cb-addstring.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="02e09-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="02e09-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02e09-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="02e09-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="02e09-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="02e09-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="02e09-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="02e09-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="02e09-112">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="02e09-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02e09-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="02e09-113">Return value</span></span>

<span data-ttu-id="02e09-114">Der Rückgabewert gibt das aktuelle Gebiets Schema des Kombinations Felds an.</span><span class="sxs-lookup"><span data-stu-id="02e09-114">The return value specifies the current locale of the combo box.</span></span> <span data-ttu-id="02e09-115">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) enthält den Länder-/Regionscode, und das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den sprach Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="02e09-115">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the country/region code and the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the language identifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="02e09-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02e09-116">Remarks</span></span>

<span data-ttu-id="02e09-117">Die Sprach-ID besteht aus einer unter Sprachen-ID und einem primär Sprachen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="02e09-117">The language identifier is made up of a sublanguage identifier and a primary language identifier.</span></span> <span data-ttu-id="02e09-118">Das [**primarylangid**](/windows/desktop/api/winnt/nf-winnt-primarylangid) -Makro erhält die primäre Sprachen-ID, und das [**sublangid**](/windows/desktop/api/winnt/nf-winnt-sublangid) -Makro erhält die unter Sprachen-ID.</span><span class="sxs-lookup"><span data-stu-id="02e09-118">The [**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid) macro obtains the primary language identifier and the [**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid) macro obtains the sublanguage identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="02e09-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02e09-119">Requirements</span></span>



| <span data-ttu-id="02e09-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02e09-120">Requirement</span></span> | <span data-ttu-id="02e09-121">Wert</span><span class="sxs-lookup"><span data-stu-id="02e09-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02e09-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="02e09-122">Minimum supported client</span></span><br/> | <span data-ttu-id="02e09-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="02e09-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="02e09-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="02e09-124">Minimum supported server</span></span><br/> | <span data-ttu-id="02e09-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="02e09-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="02e09-126">Header</span><span class="sxs-lookup"><span data-stu-id="02e09-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="02e09-127"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="02e09-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02e09-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02e09-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="02e09-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="02e09-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="02e09-130">**CB \_ AddString**</span><span class="sxs-lookup"><span data-stu-id="02e09-130">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="02e09-131">**CB \_ setlocale**</span><span class="sxs-lookup"><span data-stu-id="02e09-131">**CB\_SETLOCALE**</span></span>](cb-setlocale.md)
</dt> <dt>

<span data-ttu-id="02e09-132">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="02e09-132">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="02e09-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="02e09-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="02e09-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="02e09-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="02e09-135">**Primarylangid**</span><span class="sxs-lookup"><span data-stu-id="02e09-135">**PRIMARYLANGID**</span></span>](/windows/desktop/api/winnt/nf-winnt-primarylangid)
</dt> <dt>

[<span data-ttu-id="02e09-136">**Sublangid**</span><span class="sxs-lookup"><span data-stu-id="02e09-136">**SUBLANGID**</span></span>](/windows/desktop/api/winnt/nf-winnt-sublangid)
</dt> </dl>

 

