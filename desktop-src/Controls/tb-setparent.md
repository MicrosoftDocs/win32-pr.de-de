---
title: TB_SETPARENT Meldung (kommstrg. h)
description: Legt das Fenster fest, in das das Symbolleisten-Steuerelement Benachrichtigungs Meldungen sendet.
ms.assetid: 4863bd9f-021b-4295-9483-459fc19325d9
keywords:
- Windows-Steuerelemente für TB_SETPARENT Meldung
topic_type:
- apiref
api_name:
- TB_SETPARENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8137406c8e6854f86ed81d8d6b96293074ae67b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859205"
---
# <a name="tb_setparent-message"></a><span data-ttu-id="7ecb7-104">TB- \_ SetParent-Nachricht</span><span class="sxs-lookup"><span data-stu-id="7ecb7-104">TB\_SETPARENT message</span></span>

<span data-ttu-id="7ecb7-105">Legt das Fenster fest, in das das Symbolleisten-Steuerelement Benachrichtigungs Meldungen sendet.</span><span class="sxs-lookup"><span data-stu-id="7ecb7-105">Sets the window to which the toolbar control sends notification messages.</span></span>

## <a name="parameters"></a><span data-ttu-id="7ecb7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ecb7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ecb7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7ecb7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7ecb7-108">Handle für das Fenster, um Benachrichtigungs Meldungen zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="7ecb7-108">Handle to the window to receive notification messages.</span></span>

</dd> <dt>

<span data-ttu-id="7ecb7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7ecb7-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7ecb7-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="7ecb7-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ecb7-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7ecb7-111">Return value</span></span>

<span data-ttu-id="7ecb7-112">Der Rückgabewert ist ein Handle für das vorherige Benachrichtigungsfenster, oder **null** , wenn kein vorheriges Benachrichtigungsfenster vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7ecb7-112">The return value is a handle to the previous notification window, or **NULL** if there is no previous notification window.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ecb7-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7ecb7-113">Remarks</span></span>

<span data-ttu-id="7ecb7-114">Die **TB- \_ SetParent** -Nachricht ändert das übergeordnete Fenster nicht, das beim Erstellen des Steuer Elements angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="7ecb7-114">The **TB\_SETPARENT** message does not change the parent window that was specified when the control was created.</span></span> <span data-ttu-id="7ecb7-115">Wenn Sie die [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) -Funktion für ein ToolBar-Steuerelement aufrufen, wird das tatsächliche übergeordnete Fenster zurückgegeben, nicht das in **TB \_ SetParent** angegebene Fenster.</span><span class="sxs-lookup"><span data-stu-id="7ecb7-115">Calling the [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) function for a toolbar control will return the actual parent window, not the window specified in **TB\_SETPARENT**.</span></span> <span data-ttu-id="7ecb7-116">Um das übergeordnete Fenster des Steuer Elements zu ändern, müssen Sie die [**SetParent**](/windows/desktop/api/winuser/nf-winuser-setparent) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7ecb7-116">To change the control's parent window, call the [**SetParent**](/windows/desktop/api/winuser/nf-winuser-setparent) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ecb7-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7ecb7-117">Requirements</span></span>



| <span data-ttu-id="7ecb7-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7ecb7-118">Requirement</span></span> | <span data-ttu-id="7ecb7-119">Wert</span><span class="sxs-lookup"><span data-stu-id="7ecb7-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7ecb7-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7ecb7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7ecb7-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7ecb7-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7ecb7-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7ecb7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7ecb7-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7ecb7-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7ecb7-124">Header</span><span class="sxs-lookup"><span data-stu-id="7ecb7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ecb7-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ecb7-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

