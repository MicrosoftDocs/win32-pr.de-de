---
title: PSM_SETTITLE Meldung (prsht. h)
description: Legt den Titel eines Eigenschaften Blatts fest. Sie können diese Nachricht explizit oder mithilfe des propsheet- \_ Makros SetTitle senden.
ms.assetid: 53ce8e20-4554-41f4-bad9-fb24c2c93c34
keywords:
- Windows-Steuerelemente für PSM_SETTITLE Meldung
topic_type:
- apiref
api_name:
- PSM_SETTITLE
- PSM_SETTITLEA
- PSM_SETTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a848a5bdaeaae64b6f1825740d1e8ade07a5a22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949457"
---
# <a name="psm_settitle-message"></a><span data-ttu-id="69cb8-105">PSM- \_ SetTitle-Nachricht</span><span class="sxs-lookup"><span data-stu-id="69cb8-105">PSM\_SETTITLE message</span></span>

<span data-ttu-id="69cb8-106">Legt den Titel eines Eigenschaften Blatts fest.</span><span class="sxs-lookup"><span data-stu-id="69cb8-106">Sets the title of a property sheet.</span></span> <span data-ttu-id="69cb8-107">Sie können diese Nachricht explizit oder mithilfe des [**propsheet-Makros \_ SetTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_settitle) senden.</span><span class="sxs-lookup"><span data-stu-id="69cb8-107">You can send this message explicitly or by using the [**PropSheet\_SetTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_settitle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="69cb8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="69cb8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69cb8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="69cb8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="69cb8-110">Flag, das angibt, ob das Präfix "Eigenschaften für" oder das Suffix "Properties" (abhängig von der Version) mit der angegebenen Titel Zeichenfolge eingeschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="69cb8-110">Flag that indicates whether to include the prefix "Properties for" or the suffix "Properties" (depending on the version) with the specified title string.</span></span> <span data-ttu-id="69cb8-111">Wenn dieser Wert "PSH \_ proptitle" ist, ist das Präfix oder Suffix enthalten.</span><span class="sxs-lookup"><span data-stu-id="69cb8-111">If this value is PSH\_PROPTITLE, the prefix or suffix is included.</span></span>

</dd> <dt>

<span data-ttu-id="69cb8-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="69cb8-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="69cb8-113">Zeiger auf einen Puffer, der die Titel Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="69cb8-113">Pointer to a buffer that contains the title string.</span></span> <span data-ttu-id="69cb8-114">Wenn das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) dieses Parameters **null** ist, lädt das Eigenschaften Blatt die im [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))angegebene Zeichen folgen Ressource.</span><span class="sxs-lookup"><span data-stu-id="69cb8-114">If the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) of this parameter is **NULL**, the property sheet loads the string resource specified in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69cb8-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="69cb8-115">Return value</span></span>

<span data-ttu-id="69cb8-116">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="69cb8-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="69cb8-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="69cb8-117">Remarks</span></span>

<span data-ttu-id="69cb8-118">In einem Aero-Assistenten kann diese Meldung verwendet werden, um den Titel einer inneren Seite dynamisch zu ändern. Dies ist beispielsweise der Fall, wenn die " [PSN \_ SETACTIVE](psn-setactive.md) "-Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="69cb8-118">In an Aero Wizard, this message can be used to change the title of an interior page dynamically; for example, when handling the [PSN\_SETACTIVE](psn-setactive.md) notification.</span></span>

## <a name="requirements"></a><span data-ttu-id="69cb8-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69cb8-119">Requirements</span></span>



| <span data-ttu-id="69cb8-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="69cb8-120">Requirement</span></span> | <span data-ttu-id="69cb8-121">Wert</span><span class="sxs-lookup"><span data-stu-id="69cb8-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="69cb8-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="69cb8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="69cb8-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="69cb8-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="69cb8-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="69cb8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="69cb8-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="69cb8-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="69cb8-126">Header</span><span class="sxs-lookup"><span data-stu-id="69cb8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="69cb8-127"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="69cb8-127"><dt>Prsht.h</dt></span></span> </dl> |
| <span data-ttu-id="69cb8-128">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="69cb8-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="69cb8-129">**PSM \_ Settitlew** (Unicode) und **PSM \_ settitlea** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="69cb8-129">**PSM\_SETTITLEW** (Unicode) and **PSM\_SETTITLEA** (ANSI)</span></span><br/>              |



 

