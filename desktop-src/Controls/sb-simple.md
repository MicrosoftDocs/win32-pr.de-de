---
title: SB_SIMPLE Meldung (kommstrg. h)
description: Gibt an, ob ein Statusfenster einfachen Text anzeigt oder alle durch eine vorherige SB SetParts-Meldung festgelegten Fensterteile anzeigt \_ .
ms.assetid: 457209cb-67d4-4a9f-8d18-75aa5eb9ca1d
keywords:
- Windows-Steuerelemente für SB_SIMPLE Meldung
topic_type:
- apiref
api_name:
- SB_SIMPLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f7a462a917c86531cd70f5f5c8ea60bf448ff6f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105063"
---
# <a name="sb_simple-message"></a><span data-ttu-id="1f55f-104">Einfache SB- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="1f55f-104">SB\_SIMPLE message</span></span>

<span data-ttu-id="1f55f-105">Gibt an, ob ein Statusfenster einfachen Text anzeigt oder alle durch eine vorherige [**SB \_ SetParts**](sb-setparts.md) -Meldung festgelegten Fensterteile anzeigt.</span><span class="sxs-lookup"><span data-stu-id="1f55f-105">Specifies whether a status window displays simple text or displays all window parts set by a previous [**SB\_SETPARTS**](sb-setparts.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="1f55f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f55f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f55f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1f55f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f55f-108">Flag des Anzeige Typs.</span><span class="sxs-lookup"><span data-stu-id="1f55f-108">Display type flag.</span></span> <span data-ttu-id="1f55f-109">Wenn dieser Parameter **true** ist, wird im Fenster einfacher Text angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1f55f-109">If this parameter is **TRUE**, the window displays simple text.</span></span> <span data-ttu-id="1f55f-110">Wenn der Wert **false** ist, werden mehrere Teile angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1f55f-110">If it is **FALSE**, it displays multiple parts.</span></span>

</dd> <dt>

<span data-ttu-id="1f55f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1f55f-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1f55f-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="1f55f-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f55f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1f55f-113">Return value</span></span>

<span data-ttu-id="1f55f-114">Der Rückgabewert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1f55f-114">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f55f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f55f-115">Remarks</span></span>

<span data-ttu-id="1f55f-116">Wenn das Statusfenster von nicht einfache in Simple geändert wird oder umgekehrt, wird das Fenster sofort neu gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1f55f-116">If the status window is being changed from nonsimple to simple, or vice versa, the window is immediately redrawn.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f55f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1f55f-117">Requirements</span></span>



| <span data-ttu-id="1f55f-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1f55f-118">Requirement</span></span> | <span data-ttu-id="1f55f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="1f55f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1f55f-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1f55f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1f55f-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1f55f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1f55f-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1f55f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1f55f-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1f55f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1f55f-124">Header</span><span class="sxs-lookup"><span data-stu-id="1f55f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f55f-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f55f-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





