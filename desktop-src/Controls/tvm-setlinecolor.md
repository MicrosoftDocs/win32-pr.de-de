---
title: TVM_SETLINECOLOR Meldung (kommstrg. h)
description: Die TVM- \_ setlinecolor-Meldung legt die aktuelle Linien Farbe fest.
ms.assetid: c5fc28af-5603-489f-aa6b-73e153f9aebc
keywords:
- Windows-Steuerelemente für TVM_SETLINECOLOR Meldung
topic_type:
- apiref
api_name:
- TVM_SETLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d70340ea0d2339055faa3fb473269f3b244f335
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040719"
---
# <a name="tvm_setlinecolor-message"></a><span data-ttu-id="a6f6b-104">TVM- \_ setlinecolor-Meldung</span><span class="sxs-lookup"><span data-stu-id="a6f6b-104">TVM\_SETLINECOLOR message</span></span>

<span data-ttu-id="a6f6b-105">Die **TVM- \_ setlinecolor** -Meldung legt die aktuelle Linien Farbe fest.</span><span class="sxs-lookup"><span data-stu-id="a6f6b-105">The **TVM\_SETLINECOLOR** message sets the current line color.</span></span>

## <a name="parameters"></a><span data-ttu-id="a6f6b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6f6b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6f6b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a6f6b-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a6f6b-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="a6f6b-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a6f6b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a6f6b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a6f6b-110">Neue Zeilen Farbe.</span><span class="sxs-lookup"><span data-stu-id="a6f6b-110">New line color.</span></span> <span data-ttu-id="a6f6b-111">Verwenden Sie den CLR- \_ Standardwert, um die System Standardfarben wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="a6f6b-111">Use the CLR\_DEFAULT value to restore the system default colors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6f6b-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a6f6b-112">Return value</span></span>

<span data-ttu-id="a6f6b-113">Gibt die vorherige Linien Farbe zurück.</span><span class="sxs-lookup"><span data-stu-id="a6f6b-113">Returns the previous line color.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6f6b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6f6b-114">Remarks</span></span>

<span data-ttu-id="a6f6b-115">Diese Meldung ändert nur die Linien Farben.</span><span class="sxs-lookup"><span data-stu-id="a6f6b-115">This message only changes line colors.</span></span> <span data-ttu-id="a6f6b-116">Um die Farben von ' + ' und '-' innerhalb der Schaltflächen zu ändern, verwenden Sie die [**TVM \_ SetTextColor**](tvm-settextcolor.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="a6f6b-116">To change the colors of the '+' and '-' inside the buttons, use the [**TVM\_SETTEXTCOLOR**](tvm-settextcolor.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6f6b-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6f6b-117">Requirements</span></span>



| <span data-ttu-id="a6f6b-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a6f6b-118">Requirement</span></span> | <span data-ttu-id="a6f6b-119">Wert</span><span class="sxs-lookup"><span data-stu-id="a6f6b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a6f6b-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a6f6b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a6f6b-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a6f6b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a6f6b-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a6f6b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a6f6b-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a6f6b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a6f6b-124">Header</span><span class="sxs-lookup"><span data-stu-id="a6f6b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6f6b-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6f6b-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6f6b-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6f6b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6f6b-127">**TVM \_ getLineColor**</span><span class="sxs-lookup"><span data-stu-id="a6f6b-127">**TVM\_GETLINECOLOR**</span></span>](tvm-getlinecolor.md)
</dt> </dl>

 

 





