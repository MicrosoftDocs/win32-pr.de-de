---
title: LVM_GETFOOTERRECT Meldung (kommstrg. h)
description: Ruft die Koordinaten der Fußzeile für ein Listenansicht-Steuerelement ab. Senden Sie diese Nachricht explizit oder mithilfe des ListView \_ getfooterrect-Makros.
ms.assetid: f8816f35-c1d2-4072-81d3-0a9a3df53d64
keywords:
- Windows-Steuerelemente für LVM_GETFOOTERRECT Meldung
topic_type:
- apiref
api_name:
- LVM_GETFOOTERRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31df3a1b7b29e5ad9191da9e990e04daec99e948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102894"
---
# <a name="lvm_getfooterrect-message"></a><span data-ttu-id="1ad74-105">LVM- \_ getfooterrect-Nachricht</span><span class="sxs-lookup"><span data-stu-id="1ad74-105">LVM\_GETFOOTERRECT message</span></span>

<span data-ttu-id="1ad74-106">Ruft die Koordinaten der Fußzeile für ein Listenansicht-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="1ad74-106">Retrieves the coordinates of the footer for a list-view control.</span></span> <span data-ttu-id="1ad74-107">Senden Sie diese Nachricht explizit oder mithilfe des [**ListView \_ getfooterrect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterrect) -Makros.</span><span class="sxs-lookup"><span data-stu-id="1ad74-107">Send this message explicitly or by using the [**ListView\_GetFooterRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1ad74-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ad74-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ad74-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1ad74-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ad74-110">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1ad74-110">Not used.</span></span> <span data-ttu-id="1ad74-111">Muss den Wert 0 (null) haben.</span><span class="sxs-lookup"><span data-stu-id="1ad74-111">Must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="1ad74-112">*LPARAM* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1ad74-112">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ad74-113">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die Koordinaten empfängt.</span><span class="sxs-lookup"><span data-stu-id="1ad74-113">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to receive the coordinates.</span></span> <span data-ttu-id="1ad74-114">Der Aufrufprozess ist für die Zuordnung dieser Struktur verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="1ad74-114">The calling process is responsible for allocating this structure.</span></span> <span data-ttu-id="1ad74-115">Die empfangenen Koordinaten werden als Client Koordinaten ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="1ad74-115">The coordinates received are expressed as client coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ad74-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1ad74-116">Return value</span></span>

<span data-ttu-id="1ad74-117">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="1ad74-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ad74-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ad74-118">Requirements</span></span>



| <span data-ttu-id="1ad74-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1ad74-119">Requirement</span></span> | <span data-ttu-id="1ad74-120">Wert</span><span class="sxs-lookup"><span data-stu-id="1ad74-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ad74-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1ad74-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1ad74-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1ad74-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1ad74-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1ad74-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1ad74-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1ad74-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1ad74-125">Header</span><span class="sxs-lookup"><span data-stu-id="1ad74-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ad74-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ad74-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

