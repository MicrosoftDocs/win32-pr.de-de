---
title: TB_MOVEBUTTON Meldung (kommstrg. h)
description: Verschiebt eine Schaltfläche von einem Index zu einem anderen.
ms.assetid: 030aedc5-2de5-4751-90b2-63794322f503
keywords:
- Windows-Steuerelemente für TB_MOVEBUTTON Meldung
topic_type:
- apiref
api_name:
- TB_MOVEBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dac4cd303e895998b12e710910432ba2c38b230
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105045"
---
# <a name="tb_movebutton-message"></a><span data-ttu-id="63f18-104">TB-Meldungs \_ Tasten Meldung</span><span class="sxs-lookup"><span data-stu-id="63f18-104">TB\_MOVEBUTTON message</span></span>

<span data-ttu-id="63f18-105">Verschiebt eine Schaltfläche von einem Index zu einem anderen.</span><span class="sxs-lookup"><span data-stu-id="63f18-105">Moves a button from one index to another.</span></span>

## <a name="parameters"></a><span data-ttu-id="63f18-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="63f18-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63f18-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="63f18-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63f18-108">NULL basierter Index der Schaltfläche, die verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="63f18-108">Zero-based index of the button to be moved.</span></span>

</dd> <dt>

<span data-ttu-id="63f18-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="63f18-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63f18-110">Der null basierte Index, an dem die Schaltfläche verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="63f18-110">Zero-based index where the button will be moved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63f18-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="63f18-111">Return value</span></span>

<span data-ttu-id="63f18-112">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="63f18-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="63f18-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63f18-113">Requirements</span></span>



| <span data-ttu-id="63f18-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="63f18-114">Requirement</span></span> | <span data-ttu-id="63f18-115">Wert</span><span class="sxs-lookup"><span data-stu-id="63f18-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="63f18-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="63f18-116">Minimum supported client</span></span><br/> | <span data-ttu-id="63f18-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="63f18-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="63f18-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="63f18-118">Minimum supported server</span></span><br/> | <span data-ttu-id="63f18-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="63f18-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="63f18-120">Header</span><span class="sxs-lookup"><span data-stu-id="63f18-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="63f18-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="63f18-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63f18-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63f18-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63f18-123">**TB \_**</span><span class="sxs-lookup"><span data-stu-id="63f18-123">**TB\_SETANCHORHIGHLIGHT**</span></span>](tb-setanchorhighlight.md)
</dt> </dl>

 

 





