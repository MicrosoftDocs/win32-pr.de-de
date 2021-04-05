---
title: RB_SETPARENT Meldung (kommstrg. h)
description: Legt das übergeordnete Fenster eines Info leisten Steuer Elements fest.
ms.assetid: bb8036d4-cab8-4887-86c6-66460bdbe64b
keywords:
- Windows-Steuerelemente für RB_SETPARENT Meldung
topic_type:
- apiref
api_name:
- RB_SETPARENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6fafd054d9438b6aedd268620097847b42f3d60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859067"
---
# <a name="rb_setparent-message"></a><span data-ttu-id="0ebac-104">RB- \_ SetParent-Nachricht</span><span class="sxs-lookup"><span data-stu-id="0ebac-104">RB\_SETPARENT message</span></span>

<span data-ttu-id="0ebac-105">Legt das übergeordnete Fenster eines Info leisten Steuer Elements fest.</span><span class="sxs-lookup"><span data-stu-id="0ebac-105">Sets a rebar control's parent window.</span></span>

## <a name="parameters"></a><span data-ttu-id="0ebac-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ebac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ebac-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0ebac-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0ebac-108">Handle für das übergeordnete Fenster, das festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0ebac-108">Handle to the parent window to be set.</span></span>

</dd> <dt>

<span data-ttu-id="0ebac-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0ebac-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0ebac-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="0ebac-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ebac-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0ebac-111">Return value</span></span>

<span data-ttu-id="0ebac-112">Gibt das Handle für das vorherige übergeordnete Fenster zurück, oder **null** , wenn kein vorheriges übergeordnetes Element vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0ebac-112">Returns the handle to the previous parent window, or **NULL** if there is no previous parent.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ebac-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ebac-113">Remarks</span></span>

<span data-ttu-id="0ebac-114">Das Grund leisten-Steuerelement sendet Benachrichtigungs Meldungen an das Fenster, das Sie mit dieser Meldung angeben.</span><span class="sxs-lookup"><span data-stu-id="0ebac-114">The rebar control sends notification messages to the window you specify with this message.</span></span> <span data-ttu-id="0ebac-115">Mit dieser Meldung wird das übergeordnete Element des Grund leisten-Steuer Elements nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="0ebac-115">This message does not actually change the parent of the rebar control.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ebac-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ebac-116">Requirements</span></span>



| <span data-ttu-id="0ebac-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ebac-117">Requirement</span></span> | <span data-ttu-id="0ebac-118">Wert</span><span class="sxs-lookup"><span data-stu-id="0ebac-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0ebac-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0ebac-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0ebac-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0ebac-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0ebac-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0ebac-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0ebac-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0ebac-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0ebac-123">Header</span><span class="sxs-lookup"><span data-stu-id="0ebac-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ebac-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ebac-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





