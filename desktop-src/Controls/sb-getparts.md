---
title: SB_GETPARTS Meldung (kommstrg. h)
description: Ruft die Anzahl der Teile in einem Statusfenster ab. Die Meldung ruft auch die Koordinate des rechten Rands der angegebenen Anzahl von Teilen ab.
ms.assetid: 2535f490-4d6b-468a-b13c-096941e61bf4
keywords:
- Windows-Steuerelemente für SB_GETPARTS Meldung
topic_type:
- apiref
api_name:
- SB_GETPARTS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cee0f33331c579490cf66a38b9ce6655215ae673
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518446"
---
# <a name="sb_getparts-message"></a><span data-ttu-id="b6da6-105">SB \_ GetParts-Nachricht</span><span class="sxs-lookup"><span data-stu-id="b6da6-105">SB\_GETPARTS message</span></span>

<span data-ttu-id="b6da6-106">Ruft die Anzahl der Teile in einem Statusfenster ab.</span><span class="sxs-lookup"><span data-stu-id="b6da6-106">Retrieves a count of the parts in a status window.</span></span> <span data-ttu-id="b6da6-107">Die Meldung ruft auch die Koordinate des rechten Rands der angegebenen Anzahl von Teilen ab.</span><span class="sxs-lookup"><span data-stu-id="b6da6-107">The message also retrieves the coordinate of the right edge of the specified number of parts.</span></span>

## <a name="parameters"></a><span data-ttu-id="b6da6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6da6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6da6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b6da6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6da6-110">Anzahl der Teile, für die Koordinaten abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b6da6-110">Number of parts for which to retrieve coordinates.</span></span> <span data-ttu-id="b6da6-111">Wenn dieser Parameter größer als die Anzahl der Teile im Fenster ist, ruft die Nachricht nur die Koordinaten für vorhandene Teile ab.</span><span class="sxs-lookup"><span data-stu-id="b6da6-111">If this parameter is greater than the number of parts in the window, the message retrieves coordinates for existing parts only.</span></span>

</dd> <dt>

<span data-ttu-id="b6da6-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b6da6-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6da6-113">Zeiger auf ein ganzzahliges Array, das über die gleiche Anzahl von Elementen wie von *wParam* angegebene Teile verfügt.</span><span class="sxs-lookup"><span data-stu-id="b6da6-113">Pointer to an integer array that has the same number of elements as parts specified by *wParam*.</span></span> <span data-ttu-id="b6da6-114">Jedes Element im Array empfängt die Client Koordinate des rechten Rands des entsprechenden Teils.</span><span class="sxs-lookup"><span data-stu-id="b6da6-114">Each element in the array receives the client coordinate of the right edge of the corresponding part.</span></span> <span data-ttu-id="b6da6-115">Wenn ein Element auf-1 festgelegt ist, wird die Position des rechten Rands für diesen Teil auf den rechten Rand des Fensters erweitert.</span><span class="sxs-lookup"><span data-stu-id="b6da6-115">If an element is set to -1, the position of the right edge for that part extends to the right edge of the window.</span></span> <span data-ttu-id="b6da6-116">Wenn Sie die aktuelle Anzahl von Teilen abrufen möchten, legen Sie diesen Parameter auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="b6da6-116">To retrieve the current number of parts, set this parameter to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6da6-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b6da6-117">Return value</span></span>

<span data-ttu-id="b6da6-118">Gibt die Anzahl der Teile im Fenster zurück.</span><span class="sxs-lookup"><span data-stu-id="b6da6-118">Returns the number of parts in the window.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6da6-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b6da6-119">Remarks</span></span>

<span data-ttu-id="b6da6-120">Diese Meldung gibt immer die Anzahl der Teile in der Statusleiste zurück.</span><span class="sxs-lookup"><span data-stu-id="b6da6-120">This message always returns the number of parts in the status bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6da6-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6da6-121">Requirements</span></span>



| <span data-ttu-id="b6da6-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6da6-122">Requirement</span></span> | <span data-ttu-id="b6da6-123">Wert</span><span class="sxs-lookup"><span data-stu-id="b6da6-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b6da6-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b6da6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b6da6-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6da6-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b6da6-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b6da6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b6da6-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6da6-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b6da6-128">Header</span><span class="sxs-lookup"><span data-stu-id="b6da6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6da6-129"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6da6-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





