---
title: RB_SIZETORECT Meldung (kommstrg. h)
description: Versucht, das beste Layout der Bänder für das angegebene Rechteck zu finden.
ms.assetid: c6242b54-bd65-489b-b417-9680cc39b64a
keywords:
- Windows-Steuerelemente für RB_SIZETORECT Meldung
topic_type:
- apiref
api_name:
- RB_SIZETORECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3db5727ee8c94d2473b503c9a81b7669bb829a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106251"
---
# <a name="rb_sizetorect-message"></a><span data-ttu-id="61d6c-104">RB \_ sizetorect-Nachricht</span><span class="sxs-lookup"><span data-stu-id="61d6c-104">RB\_SIZETORECT message</span></span>

<span data-ttu-id="61d6c-105">Versucht, das beste Layout der Bänder für das angegebene Rechteck zu finden.</span><span class="sxs-lookup"><span data-stu-id="61d6c-105">Attempts to find the best layout of the bands for the given rectangle.</span></span>

## <a name="parameters"></a><span data-ttu-id="61d6c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="61d6c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61d6c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="61d6c-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="61d6c-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="61d6c-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="61d6c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="61d6c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="61d6c-110">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die das Rechteck angibt, mit dem das Grund leisten Steuerelement vergrößert werden soll.</span><span class="sxs-lookup"><span data-stu-id="61d6c-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the rectangle to which the rebar control should be sized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61d6c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="61d6c-111">Return value</span></span>

<span data-ttu-id="61d6c-112">Gibt einen Wert ungleich 0 (null) zurück, wenn eine Layoutänderung aufgetreten ist, andernfalls</span><span class="sxs-lookup"><span data-stu-id="61d6c-112">Returns nonzero if a layout change occurred, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="61d6c-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61d6c-113">Remarks</span></span>

<span data-ttu-id="61d6c-114">Die Grund leisten Bänder werden nach Bedarf angeordnet und umschließt, damit Sie an das Rechteck angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="61d6c-114">The rebar bands will be arranged and wrapped as necessary to fit the rectangle.</span></span> <span data-ttu-id="61d6c-115">Für Bänder mit dem RBBS- \_ variableheight-Stil wird die Größe so gleichmäßig wie möglich angepasst, damit Sie dem Rechteck entspricht.</span><span class="sxs-lookup"><span data-stu-id="61d6c-115">Bands that have the RBBS\_VARIABLEHEIGHT style will be resized as evenly as possible to fit the rectangle.</span></span> <span data-ttu-id="61d6c-116">Abhängig vom neuen Layout kann die Höhe einer horizontalen Info Leiste oder die Breite einer vertikalen Grund Leiste geändert werden.</span><span class="sxs-lookup"><span data-stu-id="61d6c-116">The height of a horizontal rebar or the width of a vertical rebar may change, depending on the new layout.</span></span>

## <a name="requirements"></a><span data-ttu-id="61d6c-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61d6c-117">Requirements</span></span>



| <span data-ttu-id="61d6c-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61d6c-118">Requirement</span></span> | <span data-ttu-id="61d6c-119">Wert</span><span class="sxs-lookup"><span data-stu-id="61d6c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61d6c-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="61d6c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="61d6c-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="61d6c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="61d6c-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="61d6c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="61d6c-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="61d6c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="61d6c-124">Header</span><span class="sxs-lookup"><span data-stu-id="61d6c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="61d6c-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="61d6c-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

