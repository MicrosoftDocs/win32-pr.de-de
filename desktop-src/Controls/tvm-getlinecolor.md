---
title: TVM_GETLINECOLOR Meldung (kommstrg. h)
description: Die TVM \_ getLineColor-Meldung Ruft die aktuelle Linien Farbe ab.
ms.assetid: e74441b3-5d4f-4454-b896-2e96ce649419
keywords:
- Windows-Steuerelemente für TVM_GETLINECOLOR Meldung
topic_type:
- apiref
api_name:
- TVM_GETLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fd55149f38fb17238e13135e798ebbe55b15009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040757"
---
# <a name="tvm_getlinecolor-message"></a><span data-ttu-id="c3426-104">TVM \_ getLineColor-Meldung</span><span class="sxs-lookup"><span data-stu-id="c3426-104">TVM\_GETLINECOLOR message</span></span>

<span data-ttu-id="c3426-105">Die **TVM \_ getLineColor** -Meldung Ruft die aktuelle Linien Farbe ab.</span><span class="sxs-lookup"><span data-stu-id="c3426-105">The **TVM\_GETLINECOLOR** message gets the current line color.</span></span>

## <a name="parameters"></a><span data-ttu-id="c3426-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3426-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3426-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c3426-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c3426-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="c3426-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c3426-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c3426-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c3426-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="c3426-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3426-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c3426-111">Return value</span></span>

<span data-ttu-id="c3426-112">Gibt die aktuelle Linien Farbe oder den CLR- \_ Standardwert zurück, wenn kein Wert angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="c3426-112">Returns the current line color, or the CLR\_DEFAULT value if none has been specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3426-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c3426-113">Remarks</span></span>

<span data-ttu-id="c3426-114">Diese Meldung ruft nur Linien Farben ab.</span><span class="sxs-lookup"><span data-stu-id="c3426-114">This message only retrieves line colors.</span></span> <span data-ttu-id="c3426-115">Um die Farben von "+" und "-" in den Schaltflächen abzurufen, verwenden Sie die [**TVM \_ gettextcolor**](tvm-gettextcolor.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="c3426-115">To retrieve the colors of the '+' and '-' inside the buttons, use the [**TVM\_GETTEXTCOLOR**](tvm-gettextcolor.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3426-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3426-116">Requirements</span></span>



| <span data-ttu-id="c3426-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3426-117">Requirement</span></span> | <span data-ttu-id="c3426-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c3426-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c3426-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c3426-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c3426-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3426-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c3426-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c3426-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c3426-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3426-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c3426-123">Header</span><span class="sxs-lookup"><span data-stu-id="c3426-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3426-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3426-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3426-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3426-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3426-126">**TVM \_ setlinecolor**</span><span class="sxs-lookup"><span data-stu-id="c3426-126">**TVM\_SETLINECOLOR**</span></span>](tvm-setlinecolor.md)
</dt> </dl>

 

 





