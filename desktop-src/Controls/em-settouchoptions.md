---
title: EM_SETTOUCHOPTIONS Meldung (RichEdit. h)
description: Legt die einem Rich-Edit-Steuerelement zugeordneten Berührungs Optionen fest.
ms.assetid: C15036D6-B74F-414D-B731-F1587B616644
keywords:
- Windows-Steuerelemente für EM_SETTOUCHOPTIONS Meldung
topic_type:
- apiref
api_name:
- EM_SETTOUCHOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7613679a574955ef726da9fa10e8d919c8fe53b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477307"
---
# <a name="em_settouchoptions-message"></a><span data-ttu-id="a8b1a-104">EM \_ settouchoptions-Meldung</span><span class="sxs-lookup"><span data-stu-id="a8b1a-104">EM\_SETTOUCHOPTIONS message</span></span>

<span data-ttu-id="a8b1a-105">Legt die einem Rich-Edit-Steuerelement zugeordneten Berührungs Optionen fest.</span><span class="sxs-lookup"><span data-stu-id="a8b1a-105">Sets the touch options associated with a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a8b1a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8b1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8b1a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a8b1a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8b1a-108">Die festzulegende Berührungs Option.</span><span class="sxs-lookup"><span data-stu-id="a8b1a-108">The touch option to set.</span></span> <span data-ttu-id="a8b1a-109">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="a8b1a-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="a8b1a-110">Wert</span><span class="sxs-lookup"><span data-stu-id="a8b1a-110">Value</span></span>                                                                                                                                                                        | <span data-ttu-id="a8b1a-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a8b1a-111">Meaning</span></span>                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTO_SHOWHANDLES"></span><span id="rto_showhandles"></span><dl> <span data-ttu-id="a8b1a-112"><dt>**RTO- \_ showhandles**</dt></span><span class="sxs-lookup"><span data-stu-id="a8b1a-112"><dt>**RTO\_SHOWHANDLES**</dt></span></span> </dl>          | <span data-ttu-id="a8b1a-113">Ein-oder Ausblenden der Berührungs Zieh Punkte, abhängig vom Wert von *LPARAM*.</span><span class="sxs-lookup"><span data-stu-id="a8b1a-113">Show or hide the touch gripper handles, depending on the value of *lParam*.</span></span><br/>                                                                                                                                                       |
| <span id="RTO_DISABLEHANDLES"></span><span id="rto_disablehandles"></span><dl> <span data-ttu-id="a8b1a-114"><dt>**RTO- \_ disablehandles**</dt></span><span class="sxs-lookup"><span data-stu-id="a8b1a-114"><dt>**RTO\_DISABLEHANDLES**</dt></span></span> </dl> | <span data-ttu-id="a8b1a-115">Aktiviert oder deaktiviert die Berührungs Zieh Punkte, abhängig vom Wert von *LPARAM*.</span><span class="sxs-lookup"><span data-stu-id="a8b1a-115">Enable or disable the touch gripper handles, depending on the value of *lParam*.</span></span> <span data-ttu-id="a8b1a-116">Wenn Handles deaktiviert sind, werden Sie ausgeblendet, wenn Sie sichtbar sind und ausgeblendet bleiben, bis eine **EM \_ settouchoptions** -Nachricht ihren Status ändert.</span><span class="sxs-lookup"><span data-stu-id="a8b1a-116">When handles are disabled, they are hidden if they are visible and remain hidden until an **EM\_SETTOUCHOPTIONS** message changes their status.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="a8b1a-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a8b1a-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8b1a-118">Auf **true** festgelegt, um die Berührungs Auswahl Handles anzuzeigen bzw. zu aktivieren, oder **false** , um die Berührungs Auswahl Handles auszublenden bzw. zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="a8b1a-118">Set to **TRUE** to show/enable the touch selection handles, or **FALSE** to hide/disable the touch selection handles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8b1a-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a8b1a-119">Return value</span></span>

<span data-ttu-id="a8b1a-120">Diese Meldung gibt NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="a8b1a-120">This message returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8b1a-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8b1a-121">Requirements</span></span>



| <span data-ttu-id="a8b1a-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8b1a-122">Requirement</span></span> | <span data-ttu-id="a8b1a-123">Wert</span><span class="sxs-lookup"><span data-stu-id="a8b1a-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a8b1a-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a8b1a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a8b1a-125">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8b1a-125">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="a8b1a-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a8b1a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a8b1a-127">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8b1a-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a8b1a-128">Header</span><span class="sxs-lookup"><span data-stu-id="a8b1a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8b1a-129"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8b1a-129"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8b1a-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8b1a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8b1a-131">**EM \_ gettouchoptions**</span><span class="sxs-lookup"><span data-stu-id="a8b1a-131">**EM\_GETTOUCHOPTIONS**</span></span>](em-settouchoptions.md)
</dt> </dl>

 

 





