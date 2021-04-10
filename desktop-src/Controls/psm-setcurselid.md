---
title: PSM_SETCURSELID Meldung (prsht. h)
description: Aktiviert die angegebene Seite in einem Eigenschaften Blatt basierend auf dem Ressourcen Bezeichner der Seite. Sie können diese Nachricht explizit oder mithilfe des propsheet- \_ Makros setcurrselbyid senden.
ms.assetid: 6db5f6ab-77ce-4a80-a84d-cb66eb1cdeaa
keywords:
- Windows-Steuerelemente für PSM_SETCURSELID Meldung
topic_type:
- apiref
api_name:
- PSM_SETCURSELID
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9da6ec827bbf3b9bade0af649f124d25c420d299
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105086"
---
# <a name="psm_setcurselid-message"></a><span data-ttu-id="347aa-105">PSM- \_ setcurrselid-Nachricht</span><span class="sxs-lookup"><span data-stu-id="347aa-105">PSM\_SETCURSELID message</span></span>

<span data-ttu-id="347aa-106">Aktiviert die angegebene Seite in einem Eigenschaften Blatt basierend auf dem Ressourcen Bezeichner der Seite.</span><span class="sxs-lookup"><span data-stu-id="347aa-106">Activates the given page in a property sheet based on the resource identifier of the page.</span></span> <span data-ttu-id="347aa-107">Sie können diese Nachricht explizit oder mithilfe des [**propsheet-Makros \_ setcurrselbyid**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcurselbyid) senden.</span><span class="sxs-lookup"><span data-stu-id="347aa-107">You can send this message explicitly or by using the [**PropSheet\_SetCurSelByID**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcurselbyid) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="347aa-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="347aa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="347aa-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="347aa-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="347aa-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="347aa-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="347aa-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="347aa-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="347aa-112">Der Ressourcen Bezeichner der zu aktivierenden Seite.</span><span class="sxs-lookup"><span data-stu-id="347aa-112">Resource identifier of the page to activate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="347aa-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="347aa-113">Return value</span></span>

<span data-ttu-id="347aa-114">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="347aa-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="347aa-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="347aa-115">Remarks</span></span>

<span data-ttu-id="347aa-116">Das Fenster, das die Aktivierung verliert, empfängt den [PSN- \_ killactive](psn-killactive.md) -Benachrichtigungs Code, und das Fenster, das die Aktivierung erlangt, empfängt den [PSN- \_ SETACTIVE](psn-setactive.md) -Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="347aa-116">The window that is losing the activation receives the [PSN\_KILLACTIVE](psn-killactive.md) notification code, and the window that is gaining the activation receives the [PSN\_SETACTIVE](psn-setactive.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="347aa-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="347aa-117">Requirements</span></span>



| <span data-ttu-id="347aa-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="347aa-118">Requirement</span></span> | <span data-ttu-id="347aa-119">Wert</span><span class="sxs-lookup"><span data-stu-id="347aa-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="347aa-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="347aa-120">Minimum supported client</span></span><br/> | <span data-ttu-id="347aa-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="347aa-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="347aa-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="347aa-122">Minimum supported server</span></span><br/> | <span data-ttu-id="347aa-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="347aa-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="347aa-124">Header</span><span class="sxs-lookup"><span data-stu-id="347aa-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="347aa-125"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="347aa-125"><dt>Prsht.h</dt></span></span> </dl> |



 

 





