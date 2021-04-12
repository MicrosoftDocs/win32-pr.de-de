---
title: TVM_GETEDITCONTROL Meldung (kommstrg. h)
description: Ruft das Handle für das Bearbeitungs Steuerelement ab, das verwendet wird, um den Text eines Struktur Ansichts Elements zu bearbeiten. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ geteditcontrol-Makros senden.
ms.assetid: c89e57e8-e113-47a1-85e6-bb68990f9c1a
keywords:
- Windows-Steuerelemente für TVM_GETEDITCONTROL Meldung
topic_type:
- apiref
api_name:
- TVM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79b4ce0beb125218e65c2c342caf59b57473088e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105962"
---
# <a name="tvm_geteditcontrol-message"></a><span data-ttu-id="fa966-105">TVM \_ geteditcontrol-Meldung</span><span class="sxs-lookup"><span data-stu-id="fa966-105">TVM\_GETEDITCONTROL message</span></span>

<span data-ttu-id="fa966-106">Ruft das Handle für das Bearbeitungs Steuerelement ab, das verwendet wird, um den Text eines Struktur Ansichts Elements zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="fa966-106">Retrieves the handle to the edit control being used to edit a tree-view item's text.</span></span> <span data-ttu-id="fa966-107">Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ geteditcontrol**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_geteditcontrol) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="fa966-107">You can send this message explicitly or by using the [**TreeView\_GetEditControl**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_geteditcontrol) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fa966-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa966-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa966-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fa966-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fa966-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="fa966-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="fa966-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fa966-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="fa966-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="fa966-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa966-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fa966-113">Return value</span></span>

<span data-ttu-id="fa966-114">Gibt das Handle für das Bearbeitungs Steuerelement zurück, wenn erfolgreich, andernfalls **null** .</span><span class="sxs-lookup"><span data-stu-id="fa966-114">Returns the handle to the edit control if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa966-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fa966-115">Remarks</span></span>

<span data-ttu-id="fa966-116">Wenn die Bezeichnungs Bearbeitung beginnt, wird ein Bearbeitungs Steuerelement erstellt, aber nicht positioniert oder angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fa966-116">When label editing begins, an edit control is created, but not positioned or displayed.</span></span> <span data-ttu-id="fa966-117">Bevor es angezeigt wird, sendet das Strukturansicht-Steuerelement seinem übergeordneten Fenster einen [TVN \_ beginlabeledit](tvn-beginlabeledit.md) -Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="fa966-117">Before it is displayed, the tree-view control sends its parent window an [TVN\_BEGINLABELEDIT](tvn-beginlabeledit.md) notification code.</span></span>

<span data-ttu-id="fa966-118">Zum Anpassen der Bezeichnungs Bearbeitung implementieren Sie einen Handler für [TVN \_ beginlabeledit](tvn-beginlabeledit.md) und senden eine **TVM \_ geteditcontrol** -Nachricht an das Strukturansicht-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="fa966-118">To customize label editing, implement a handler for [TVN\_BEGINLABELEDIT](tvn-beginlabeledit.md) and have it send a **TVM\_GETEDITCONTROL** message to the tree-view control.</span></span> <span data-ttu-id="fa966-119">Wenn eine Bezeichnung bearbeitet wird, ist der Rückgabewert ein Handle für das Bearbeitungs Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="fa966-119">If a label is being edited, the return value will be a handle to the edit control.</span></span> <span data-ttu-id="fa966-120">Verwenden Sie dieses Handle, um das Bearbeitungs Steuerelement anzupassen, indem Sie die üblichen **EM \_ xxx** -Meldungen senden.</span><span class="sxs-lookup"><span data-stu-id="fa966-120">Use this handle to customize the edit control by sending the usual **EM\_XXX** messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa966-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa966-121">Requirements</span></span>



| <span data-ttu-id="fa966-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fa966-122">Requirement</span></span> | <span data-ttu-id="fa966-123">Wert</span><span class="sxs-lookup"><span data-stu-id="fa966-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fa966-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fa966-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fa966-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fa966-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fa966-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fa966-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fa966-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fa966-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fa966-128">Header</span><span class="sxs-lookup"><span data-stu-id="fa966-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa966-129"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa966-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





