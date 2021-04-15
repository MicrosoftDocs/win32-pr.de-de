---
title: PGM_GETDROPTARGET Meldung (kommstrg. h)
description: Ruft den IDropTarget-Schnittstellen Zeiger eines Pager-Steuer Elements ab. Sie können diese Nachricht explizit senden oder das Pager \_ getdroptarget-Makro verwenden.
ms.assetid: 6b548c30-2d32-4372-90e4-346a27dda218
keywords:
- Windows-Steuerelemente für PGM_GETDROPTARGET Meldung
topic_type:
- apiref
api_name:
- PGM_GETDROPTARGET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b90f7f9667dd30a79b9345eec211a6ebfcd7a12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477898"
---
# <a name="pgm_getdroptarget-message"></a><span data-ttu-id="b3863-105">PGM \_ getdroptarget-Meldung</span><span class="sxs-lookup"><span data-stu-id="b3863-105">PGM\_GETDROPTARGET message</span></span>

<span data-ttu-id="b3863-106">Ruft den [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) -Schnittstellen Zeiger eines Pager-Steuer Elements ab.</span><span class="sxs-lookup"><span data-stu-id="b3863-106">Retrieves a pager control's [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) interface pointer.</span></span> <span data-ttu-id="b3863-107">Sie können diese Nachricht explizit senden oder das [**Pager \_ getdroptarget**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="b3863-107">You can send this message explicitly or use the [**Pager\_GetDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b3863-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3863-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3863-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b3863-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b3863-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="b3863-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b3863-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b3863-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b3863-112">Zeiger auf einen [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) -Zeiger, der den Schnittstellen Zeiger empfängt.</span><span class="sxs-lookup"><span data-stu-id="b3863-112">Pointer to an [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) pointer that receives the interface pointer.</span></span> <span data-ttu-id="b3863-113">Es ist Aufgabe des Aufrufers, die [**Freigabe**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf diesem Zeiger aufzurufen, wenn er nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="b3863-113">It is the caller's responsibility to call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on this pointer when it is no longer needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3863-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b3863-114">Return value</span></span>

<span data-ttu-id="b3863-115">Der Rückgabewert für diese Nachricht wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b3863-115">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3863-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3863-116">Requirements</span></span>



| <span data-ttu-id="b3863-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b3863-117">Requirement</span></span> | <span data-ttu-id="b3863-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b3863-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b3863-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b3863-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b3863-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b3863-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b3863-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b3863-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b3863-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b3863-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b3863-123">Header</span><span class="sxs-lookup"><span data-stu-id="b3863-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3863-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3863-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

