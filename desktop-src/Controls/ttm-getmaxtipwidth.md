---
title: TTM_GETMAXTIPWIDTH Meldung (kommstrg. h)
description: Ruft die maximale Breite für ein QuickInfo-Fenster ab.
ms.assetid: 0f0a5403-fe2e-4e5a-96c2-a435827a5fd7
keywords:
- Windows-Steuerelemente für TTM_GETMAXTIPWIDTH Meldung
topic_type:
- apiref
api_name:
- TTM_GETMAXTIPWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f89c56692db9d451eb18db61af262cc0f3a715f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956487"
---
# <a name="ttm_getmaxtipwidth-message"></a><span data-ttu-id="3082c-104">TTM \_ GetMaxTipWidth-Meldung</span><span class="sxs-lookup"><span data-stu-id="3082c-104">TTM\_GETMAXTIPWIDTH message</span></span>

<span data-ttu-id="3082c-105">Ruft die maximale Breite für ein QuickInfo-Fenster ab.</span><span class="sxs-lookup"><span data-stu-id="3082c-105">Retrieves the maximum width for a tooltip window.</span></span>

## <a name="parameters"></a><span data-ttu-id="3082c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3082c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3082c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3082c-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3082c-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="3082c-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3082c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3082c-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3082c-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="3082c-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3082c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3082c-111">Return value</span></span>

<span data-ttu-id="3082c-112">Gibt einen **int** -Wert zurück, der die maximale QuickInfo-Breite in Pixel darstellt.</span><span class="sxs-lookup"><span data-stu-id="3082c-112">Returns an **INT** value that represents the maximum tooltip width, in pixels.</span></span> <span data-ttu-id="3082c-113">Wenn zuvor keine maximale Breite festgelegt wurde, gibt die Meldung-1 zurück.</span><span class="sxs-lookup"><span data-stu-id="3082c-113">If no maximum width was set previously, the message returns -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="3082c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3082c-114">Remarks</span></span>

<span data-ttu-id="3082c-115">Der Wert für die maximale QuickInfo-Breite zeigt nicht die tatsächliche Breite eines QuickInfo-Fensters an.</span><span class="sxs-lookup"><span data-stu-id="3082c-115">The maximum tooltip width value does not indicate a tooltip window's actual width.</span></span> <span data-ttu-id="3082c-116">Wenn eine QuickInfo-Zeichenfolge die maximale Breite überschreitet, unterbricht das Steuerelement den Text in mehrere Zeilen und verwendet Leerzeichen, um Zeilenumbrüche zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="3082c-116">Rather, if a tooltip string exceeds the maximum width, the control breaks the text into multiple lines, using spaces to determine line breaks.</span></span> <span data-ttu-id="3082c-117">Wenn der Text nicht in mehrere Zeilen segmentiert werden kann, wird er in einer einzelnen Zeile angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3082c-117">If the text cannot be segmented into multiple lines, it will be displayed on a single line.</span></span> <span data-ttu-id="3082c-118">Die Länge dieser Zeile kann die maximale QuickInfo-Breite überschreiten.</span><span class="sxs-lookup"><span data-stu-id="3082c-118">The length of this line may exceed the maximum tooltip width.</span></span>

## <a name="requirements"></a><span data-ttu-id="3082c-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3082c-119">Requirements</span></span>



| <span data-ttu-id="3082c-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3082c-120">Requirement</span></span> | <span data-ttu-id="3082c-121">Wert</span><span class="sxs-lookup"><span data-stu-id="3082c-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3082c-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3082c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3082c-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3082c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3082c-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3082c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3082c-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3082c-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3082c-126">Header</span><span class="sxs-lookup"><span data-stu-id="3082c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3082c-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="3082c-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3082c-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3082c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3082c-129">**TTM \_ SetMaxTipWidth**</span><span class="sxs-lookup"><span data-stu-id="3082c-129">**TTM\_SETMAXTIPWIDTH**</span></span>](ttm-setmaxtipwidth.md)
</dt> </dl>

 

 





