---
title: EM_ENABLESEARCHWEB Meldung (kommstrg. h)
description: Aktiviert oder deaktiviert das Feature "Internet durchsuchen" und den Kontextmenü Eintrag.
ms.assetid: 9393f03e-0719-458b-8122-616df738c417
keywords:
- Windows-Steuerelemente für EM_ENABLESEARCHWEB Meldung
topic_type:
- apiref
api_name:
- EM_ENABLESEARCHWEB
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdb2638476027f0a7fe2bb1a66a3a00a330e28c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956726"
---
# <a name="em_enablesearchweb-message"></a><span data-ttu-id="ab541-104">EM \_ enablesearchweb-Meldung</span><span class="sxs-lookup"><span data-stu-id="ab541-104">EM\_ENABLESEARCHWEB message</span></span>

<span data-ttu-id="ab541-105">Aktiviert oder deaktiviert das Feature "Internet durchsuchen" und den Kontextmenü Eintrag.</span><span class="sxs-lookup"><span data-stu-id="ab541-105">Enables or disables the "Search the web" feature and context menu entry.</span></span>

## <a name="parameters"></a><span data-ttu-id="ab541-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab541-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab541-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ab541-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ab541-108">Der Wert **true** gibt an, dass das Feature "Web durchsuchen" aktiviert ist, und der Wert **false** gibt an, dass es deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ab541-108">A value of **TRUE** indicates the "Search the web" feature is enabled, and a value of **FALSE** indicates it is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="ab541-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ab541-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ab541-110">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ab541-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab541-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ab541-111">Return value</span></span>

<span data-ttu-id="ab541-112">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ab541-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab541-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab541-113">Remarks</span></span>

<span data-ttu-id="ab541-114">Wenn Sie "Internet durchsuchen" mit dieser Meldung deaktivieren, hat die Nachricht " [**EM \_ Searchweb**](em-searchweb.md) " keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="ab541-114">If you disable "Search the web" using this message, the [**EM\_SEARCHWEB**](em-searchweb.md) message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab541-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab541-115">Requirements</span></span>



| <span data-ttu-id="ab541-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ab541-116">Requirement</span></span> | <span data-ttu-id="ab541-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ab541-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab541-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ab541-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ab541-119">Nur Windows 10, 1809 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ab541-119">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ab541-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ab541-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ab541-121">Nur Windows Server 2019 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ab541-121">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ab541-122">Header</span><span class="sxs-lookup"><span data-stu-id="ab541-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab541-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab541-123"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab541-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab541-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="ab541-125">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="ab541-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ab541-126">**EM \_ Searchweb**</span><span class="sxs-lookup"><span data-stu-id="ab541-126">**EM\_SEARCHWEB**</span></span>](em-searchweb.md)
</dt> </dl>

 

 





