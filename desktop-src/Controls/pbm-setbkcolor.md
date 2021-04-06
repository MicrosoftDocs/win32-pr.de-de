---
title: PBM_SETBKCOLOR Meldung (kommstrg. h)
description: Legt die Hintergrundfarbe in der Statusanzeige fest.
ms.assetid: e28af958-babb-4c2e-9202-89b608c22f8e
keywords:
- Windows-Steuerelemente für PBM_SETBKCOLOR Meldung
topic_type:
- apiref
api_name:
- PBM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ddfaf84695221cf998275d76a9d2d67773150da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742537"
---
# <a name="pbm_setbkcolor-message"></a><span data-ttu-id="4ce7a-104">PBM- \_ SetBkColor-Meldung</span><span class="sxs-lookup"><span data-stu-id="4ce7a-104">PBM\_SETBKCOLOR message</span></span>

<span data-ttu-id="4ce7a-105">Legt die Hintergrundfarbe in der Statusanzeige fest.</span><span class="sxs-lookup"><span data-stu-id="4ce7a-105">Sets the background color in the progress bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="4ce7a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ce7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ce7a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4ce7a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4ce7a-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="4ce7a-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4ce7a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4ce7a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4ce7a-110">**COLORREF** -Wert, der die neue Hintergrundfarbe angibt.</span><span class="sxs-lookup"><span data-stu-id="4ce7a-110">**COLORREF** value that specifies the new background color.</span></span> <span data-ttu-id="4ce7a-111">Geben Sie den CLR- \_ Standardwert an, damit die Statusanzeige Ihre Standard Hintergrundfarbe verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ce7a-111">Specify the CLR\_DEFAULT value to cause the progress bar to use its default background color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ce7a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4ce7a-112">Return value</span></span>

<span data-ttu-id="4ce7a-113">Gibt die vorherige Hintergrundfarbe bzw. CLR-Standardwert zurück, \_ Wenn die Hintergrundfarbe die Standardfarbe ist.</span><span class="sxs-lookup"><span data-stu-id="4ce7a-113">Returns the previous background color, or CLR\_DEFAULT if the background color is the default color.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ce7a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ce7a-114">Remarks</span></span>

<span data-ttu-id="4ce7a-115">Wenn visuelle Stile aktiviert sind, hat diese Nachricht keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="4ce7a-115">When visual styles are enabled, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ce7a-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4ce7a-116">Requirements</span></span>



| <span data-ttu-id="4ce7a-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4ce7a-117">Requirement</span></span> | <span data-ttu-id="4ce7a-118">Wert</span><span class="sxs-lookup"><span data-stu-id="4ce7a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4ce7a-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4ce7a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4ce7a-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4ce7a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4ce7a-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4ce7a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4ce7a-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4ce7a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4ce7a-123">Header</span><span class="sxs-lookup"><span data-stu-id="4ce7a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ce7a-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ce7a-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





