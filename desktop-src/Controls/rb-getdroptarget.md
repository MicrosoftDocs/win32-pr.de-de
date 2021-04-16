---
title: RB_GETDROPTARGET Meldung (kommstrg. h)
description: Ruft den IDropTarget-Schnittstellen Zeiger eines Grund leisten-Steuer Elements ab.
ms.assetid: f429c5d1-406b-47f0-a654-47cabccc1d0e
keywords:
- Windows-Steuerelemente für RB_GETDROPTARGET Meldung
topic_type:
- apiref
api_name:
- RB_GETDROPTARGET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55b7960cc13230a2715348bc55e5e65de6f72e5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477871"
---
# <a name="rb_getdroptarget-message"></a><span data-ttu-id="65b85-104">RB \_ getdroptarget-Meldung</span><span class="sxs-lookup"><span data-stu-id="65b85-104">RB\_GETDROPTARGET message</span></span>

<span data-ttu-id="65b85-105">Ruft den [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) -Schnittstellen Zeiger eines Grund leisten-Steuer Elements ab.</span><span class="sxs-lookup"><span data-stu-id="65b85-105">Retrieves a rebar control's [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) interface pointer.</span></span>

## <a name="parameters"></a><span data-ttu-id="65b85-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="65b85-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65b85-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="65b85-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="65b85-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="65b85-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="65b85-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="65b85-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="65b85-110">Zeiger auf einen [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) -Zeiger, der den Schnittstellen Zeiger empfängt.</span><span class="sxs-lookup"><span data-stu-id="65b85-110">Pointer to an [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) pointer that receives the interface pointer.</span></span> <span data-ttu-id="65b85-111">Es ist Aufgabe des Aufrufers, die [**Freigabe**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf diesem Zeiger aufzurufen, wenn er nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="65b85-111">It is the caller's responsibility to call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on this pointer when it is no longer needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65b85-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="65b85-112">Return value</span></span>

<span data-ttu-id="65b85-113">Der Rückgabewert für diese Nachricht wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="65b85-113">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="65b85-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="65b85-114">Requirements</span></span>



| <span data-ttu-id="65b85-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="65b85-115">Requirement</span></span> | <span data-ttu-id="65b85-116">Wert</span><span class="sxs-lookup"><span data-stu-id="65b85-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="65b85-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="65b85-117">Minimum supported client</span></span><br/> | <span data-ttu-id="65b85-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="65b85-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="65b85-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="65b85-119">Minimum supported server</span></span><br/> | <span data-ttu-id="65b85-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="65b85-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="65b85-121">Header</span><span class="sxs-lookup"><span data-stu-id="65b85-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="65b85-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="65b85-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

