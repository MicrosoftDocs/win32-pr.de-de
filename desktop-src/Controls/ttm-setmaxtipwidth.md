---
title: TTM_SETMAXTIPWIDTH Meldung (kommstrg. h)
description: Legt die maximale Breite für ein QuickInfo-Fenster fest.
ms.assetid: 3cfb6011-d0c3-4a57-aead-d4ec09a057cc
keywords:
- Windows-Steuerelemente für TTM_SETMAXTIPWIDTH Meldung
topic_type:
- apiref
api_name:
- TTM_SETMAXTIPWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55ce930b289205b5fb0d2768068b8cb28cd11aec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104213715"
---
# <a name="ttm_setmaxtipwidth-message"></a><span data-ttu-id="bdd9a-104">TTM \_ SetMaxTipWidth-Meldung</span><span class="sxs-lookup"><span data-stu-id="bdd9a-104">TTM\_SETMAXTIPWIDTH message</span></span>

<span data-ttu-id="bdd9a-105">Legt die maximale Breite für ein QuickInfo-Fenster fest.</span><span class="sxs-lookup"><span data-stu-id="bdd9a-105">Sets the maximum width for a tooltip window.</span></span>

## <a name="parameters"></a><span data-ttu-id="bdd9a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bdd9a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdd9a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bdd9a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bdd9a-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="bdd9a-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bdd9a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bdd9a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bdd9a-110">Maximale QuickInfo-Fensterbreite oder-1, um eine beliebige Breite zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="bdd9a-110">Maximum tooltip window width, or -1 to allow any width.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdd9a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bdd9a-111">Return value</span></span>

<span data-ttu-id="bdd9a-112">Gibt die vorherige maximale QuickInfo-Breite zurück.</span><span class="sxs-lookup"><span data-stu-id="bdd9a-112">Returns the previous maximum tooltip width.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdd9a-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bdd9a-113">Remarks</span></span>

<span data-ttu-id="bdd9a-114">Der Wert für die maximale Breite zeigt nicht die tatsächliche Breite eines QuickInfo-Fensters an.</span><span class="sxs-lookup"><span data-stu-id="bdd9a-114">The maximum width value does not indicate a tooltip window's actual width.</span></span> <span data-ttu-id="bdd9a-115">Wenn eine QuickInfo-Zeichenfolge die maximale Breite überschreitet, unterbricht das Steuerelement den Text in mehrere Zeilen und verwendet Leerzeichen, um Zeilenumbrüche zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="bdd9a-115">Rather, if a tooltip string exceeds the maximum width, the control breaks the text into multiple lines, using spaces to determine line breaks.</span></span> <span data-ttu-id="bdd9a-116">Wenn der Text nicht in mehrere Zeilen segmentiert werden kann, wird er in einer einzelnen Zeile angezeigt, die die maximale QuickInfo-Breite überschreiten kann.</span><span class="sxs-lookup"><span data-stu-id="bdd9a-116">If the text cannot be segmented into multiple lines, it is displayed on a single line, which may exceed the maximum tooltip width.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdd9a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bdd9a-117">Requirements</span></span>



| <span data-ttu-id="bdd9a-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bdd9a-118">Requirement</span></span> | <span data-ttu-id="bdd9a-119">Wert</span><span class="sxs-lookup"><span data-stu-id="bdd9a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bdd9a-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bdd9a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bdd9a-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bdd9a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bdd9a-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bdd9a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bdd9a-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bdd9a-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bdd9a-124">Header</span><span class="sxs-lookup"><span data-stu-id="bdd9a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdd9a-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdd9a-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdd9a-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bdd9a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdd9a-127">**TTM \_ GetMaxTipWidth**</span><span class="sxs-lookup"><span data-stu-id="bdd9a-127">**TTM\_GETMAXTIPWIDTH**</span></span>](ttm-getmaxtipwidth.md)
</dt> </dl>

 

 





