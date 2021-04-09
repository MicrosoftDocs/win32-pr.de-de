---
title: RB_SHOWBAND Meldung (kommstrg. h)
description: Zeigt ein bestimmtes Band in einem Grund leisten-Steuerelement an oder blendet es aus.
ms.assetid: 18097aca-e1b4-4359-9d08-4e62406f3f7f
keywords:
- Windows-Steuerelemente für RB_SHOWBAND Meldung
topic_type:
- apiref
api_name:
- RB_SHOWBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e27c9cedeb42e7eeed9432af9c2a040ac4991810
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106250"
---
# <a name="rb_showband-message"></a><span data-ttu-id="1481f-104">RB- \_ Showband-Meldung</span><span class="sxs-lookup"><span data-stu-id="1481f-104">RB\_SHOWBAND message</span></span>

<span data-ttu-id="1481f-105">Zeigt ein bestimmtes Band in einem Grund leisten-Steuerelement an oder blendet es aus.</span><span class="sxs-lookup"><span data-stu-id="1481f-105">Shows or hides a given band in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1481f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1481f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1481f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1481f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1481f-108">NULL basierter Index eines Bands im Grund leisten-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="1481f-108">Zero-based index of a band in the rebar control.</span></span>

</dd> <dt>

<span data-ttu-id="1481f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1481f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1481f-110">**Boolescher** Wert, der angibt, ob das Band angezeigt oder ausgeblendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1481f-110">**BOOL** value that indicates if the band should be shown or hidden.</span></span> <span data-ttu-id="1481f-111">Wenn dieser Wert ungleich 0 (null) ist, wird das Band angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1481f-111">If this value is nonzero, the band will be shown.</span></span> <span data-ttu-id="1481f-112">Andernfalls wird das Band ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="1481f-112">Otherwise, the band will be hidden.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1481f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1481f-113">Return value</span></span>

<span data-ttu-id="1481f-114">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="1481f-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="1481f-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1481f-115">Requirements</span></span>



| <span data-ttu-id="1481f-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1481f-116">Requirement</span></span> | <span data-ttu-id="1481f-117">Wert</span><span class="sxs-lookup"><span data-stu-id="1481f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1481f-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1481f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1481f-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1481f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1481f-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1481f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1481f-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1481f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1481f-122">Header</span><span class="sxs-lookup"><span data-stu-id="1481f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1481f-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="1481f-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





