---
title: LB_SETLOCALE Meldung (Winuser. h)
description: Legt das aktuelle Gebiets Schema des Listen Felds fest. Sie können das Gebiets Schema verwenden, um die richtige Sortierreihenfolge des angezeigten Texts (für Listenfelder mit dem lbs \_ -Sortier Stil) und des von der LB AddString-Nachricht hinzugefügten Texts zu bestimmen \_ .
ms.assetid: e9503124-de9f-4b92-a59e-ec9320864ae7
keywords:
- Windows-Steuerelemente für LB_SETLOCALE Meldung
topic_type:
- apiref
api_name:
- LB_SETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd8ea7bb7b6d19144a84ab166f56cd2c0ad49e05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040892"
---
# <a name="lb_setlocale-message"></a><span data-ttu-id="46253-105">SLB- \_ setlocale-Meldung</span><span class="sxs-lookup"><span data-stu-id="46253-105">LB\_SETLOCALE message</span></span>

<span data-ttu-id="46253-106">Legt das aktuelle Gebiets Schema des Listen Felds fest.</span><span class="sxs-lookup"><span data-stu-id="46253-106">Sets the current locale of the list box.</span></span> <span data-ttu-id="46253-107">Sie können das Gebiets Schema verwenden, um die richtige Sortierreihenfolge des angezeigten Texts (für Listenfelder mit dem [**lbs- \_ Sortier**](list-box-styles.md) Stil) und des von der [**lb \_ AddString**](lb-addstring.md) -Nachricht hinzugefügten Texts zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="46253-107">You can use the locale to determine the correct sorting order of displayed text (for list boxes with the [**LBS\_SORT**](list-box-styles.md) style) and of text added by the [**LB\_ADDSTRING**](lb-addstring.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="46253-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="46253-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46253-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="46253-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="46253-110">Gibt den Gebiets Schema Bezeichner an, der beim Hinzufügen von Text vom Listenfeld zum Sortieren verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="46253-110">Specifies the locale identifier that the list box will use for sorting when adding text.</span></span>

</dd> <dt>

<span data-ttu-id="46253-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="46253-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="46253-112">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="46253-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46253-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="46253-113">Return value</span></span>

<span data-ttu-id="46253-114">Der Rückgabewert ist der vorherige Gebiets Schema Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="46253-114">The return value is the previous locale identifier.</span></span> <span data-ttu-id="46253-115">Wenn der *wParam* -Parameter ein Gebiets Schema angibt, das nicht auf dem System installiert ist, lautet der Rückgabewert "lb err", \_ und das aktuelle Listenfeld "locale" wird nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="46253-115">If the *wParam* parameter specifies a locale that is not installed on the system, the return value is LB\_ERR and the current list box locale is not changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="46253-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46253-116">Remarks</span></span>

<span data-ttu-id="46253-117">Verwenden Sie das [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) -Makro zum Erstellen eines Gebiets Schema Bezeichners.</span><span class="sxs-lookup"><span data-stu-id="46253-117">Use the [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) macro to construct a locale identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="46253-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46253-118">Requirements</span></span>



| <span data-ttu-id="46253-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46253-119">Requirement</span></span> | <span data-ttu-id="46253-120">Wert</span><span class="sxs-lookup"><span data-stu-id="46253-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46253-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="46253-121">Minimum supported client</span></span><br/> | <span data-ttu-id="46253-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="46253-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="46253-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="46253-123">Minimum supported server</span></span><br/> | <span data-ttu-id="46253-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="46253-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="46253-125">Header</span><span class="sxs-lookup"><span data-stu-id="46253-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="46253-126"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="46253-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46253-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46253-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="46253-128">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="46253-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="46253-129">**LB- \_ AddString**</span><span class="sxs-lookup"><span data-stu-id="46253-129">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="46253-130">**LB \_ getLocale**</span><span class="sxs-lookup"><span data-stu-id="46253-130">**LB\_GETLOCALE**</span></span>](lb-getlocale.md)
</dt> </dl>

 

