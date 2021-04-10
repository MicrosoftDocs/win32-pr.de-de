---
title: EM_SETPALETTE Meldung (RichEdit. h)
description: Ändert die Palette, die von einem Rich-Edit-Steuerelement für das Anzeige Fenster verwendet wird.
ms.assetid: c1dc0c24-eaf2-47a8-9bb1-59f37b206feb
keywords:
- Windows-Steuerelemente für EM_SETPALETTE Meldung
topic_type:
- apiref
api_name:
- EM_SETPALETTE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 026a0a85001818b6f69366e8dba80ef56a7a8f20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040508"
---
# <a name="em_setpalette-message"></a><span data-ttu-id="ac265-104">EM- \_ SetPalette-Nachricht</span><span class="sxs-lookup"><span data-stu-id="ac265-104">EM\_SETPALETTE message</span></span>

<span data-ttu-id="ac265-105">Ändert die Palette, die von einem Rich-Edit-Steuerelement für das Anzeige Fenster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ac265-105">Changes the palette that a rich edit control uses for its display window.</span></span>

## <a name="parameters"></a><span data-ttu-id="ac265-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac265-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac265-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ac265-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ac265-108">Handle für die neue Palette, die vom Rich Edit-Steuerelement verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ac265-108">Handle to the new palette used by the rich edit control.</span></span>

</dd> <dt>

<span data-ttu-id="ac265-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ac265-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ac265-110">Dieser Parameter wird nicht verwendet. Er muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="ac265-110">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac265-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ac265-111">Return value</span></span>

<span data-ttu-id="ac265-112">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ac265-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac265-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac265-113">Remarks</span></span>

<span data-ttu-id="ac265-114">Das Rich Edit-Steuerelement prüft nicht, ob die neue Palette gültig ist.</span><span class="sxs-lookup"><span data-stu-id="ac265-114">The rich edit control does not check whether the new palette is valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac265-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac265-115">Requirements</span></span>



| <span data-ttu-id="ac265-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac265-116">Requirement</span></span> | <span data-ttu-id="ac265-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ac265-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ac265-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ac265-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ac265-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac265-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ac265-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ac265-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ac265-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac265-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ac265-122">Header</span><span class="sxs-lookup"><span data-stu-id="ac265-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac265-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac265-123"><dt>Richedit.h</dt></span></span> </dl> |



 

 





