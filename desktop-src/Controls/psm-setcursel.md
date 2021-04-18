---
title: PSM_SETCURSEL Meldung (prsht. h)
description: Aktiviert die angegebene Seite in einem Eigenschaften Blatt. Sie können diese Nachricht explizit oder mithilfe des propsheet- \_ Makros setcurrsel senden.
ms.assetid: 800aadde-cabc-424e-8e63-60fc7ce952d7
keywords:
- Windows-Steuerelemente für PSM_SETCURSEL Meldung
topic_type:
- apiref
api_name:
- PSM_SETCURSEL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12f41f0ba2ec8d13a7bfc932b553b355399f76b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103470"
---
# <a name="psm_setcursel-message"></a><span data-ttu-id="30396-105">PSM- \_ setcurrsel-Nachricht</span><span class="sxs-lookup"><span data-stu-id="30396-105">PSM\_SETCURSEL message</span></span>

<span data-ttu-id="30396-106">Aktiviert die angegebene Seite in einem Eigenschaften Blatt.</span><span class="sxs-lookup"><span data-stu-id="30396-106">Activates the specified page in a property sheet.</span></span> <span data-ttu-id="30396-107">Sie können diese Nachricht explizit oder mithilfe des [**propsheet-Makros \_ setcurrsel**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcursel) senden.</span><span class="sxs-lookup"><span data-stu-id="30396-107">You can send this message explicitly or by using the [**PropSheet\_SetCurSel**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcursel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="30396-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="30396-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30396-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="30396-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30396-110">Der null basierte Index der Seite.</span><span class="sxs-lookup"><span data-stu-id="30396-110">The zero-based index of the page.</span></span> <span data-ttu-id="30396-111">Eine Anwendung kann den Index oder das Handle oder beides angeben.</span><span class="sxs-lookup"><span data-stu-id="30396-111">An application can specify the index or the handle or both.</span></span> <span data-ttu-id="30396-112">Wenn beide angegeben sind, hat *LPARAM* Vorrang.</span><span class="sxs-lookup"><span data-stu-id="30396-112">If both are specified, *lParam* takes precedence.</span></span>

</dd> <dt>

<span data-ttu-id="30396-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="30396-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30396-114">Das Handle für die zu Aktivier elnde Seite.</span><span class="sxs-lookup"><span data-stu-id="30396-114">The handle to the page to activate.</span></span> <span data-ttu-id="30396-115">Eine Anwendung kann den Index oder das Handle oder beides angeben.</span><span class="sxs-lookup"><span data-stu-id="30396-115">An application can specify the index or the handle or both.</span></span> <span data-ttu-id="30396-116">Wenn beide angegeben sind, hat *LPARAM* Vorrang.</span><span class="sxs-lookup"><span data-stu-id="30396-116">If both are specified, *lParam* takes precedence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30396-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30396-117">Return value</span></span>

<span data-ttu-id="30396-118">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="30396-118">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="30396-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30396-119">Remarks</span></span>

<span data-ttu-id="30396-120">Das Fenster, das die Aktivierung verliert, empfängt den [PSN- \_ killactive](psn-killactive.md) -Benachrichtigungs Code, und das Fenster, das die Aktivierung erlangt, empfängt den [PSN- \_ SETACTIVE](psn-setactive.md) -Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="30396-120">The window that is losing the activation receives the [PSN\_KILLACTIVE](psn-killactive.md) notification code, and the window that is gaining the activation receives the [PSN\_SETACTIVE](psn-setactive.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="30396-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30396-121">Requirements</span></span>



| <span data-ttu-id="30396-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30396-122">Requirement</span></span> | <span data-ttu-id="30396-123">Wert</span><span class="sxs-lookup"><span data-stu-id="30396-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="30396-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="30396-124">Minimum supported client</span></span><br/> | <span data-ttu-id="30396-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30396-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="30396-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="30396-126">Minimum supported server</span></span><br/> | <span data-ttu-id="30396-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30396-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="30396-128">Header</span><span class="sxs-lookup"><span data-stu-id="30396-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="30396-129"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="30396-129"><dt>Prsht.h</dt></span></span> </dl> |



 

 





