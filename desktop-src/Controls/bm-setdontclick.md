---
title: BM_SETDONTCLICK Meldung (Winuser. h)
description: Legt ein Flag für ein Optionsfeld fest, das die Generierung von Milliarden- \_ Nachrichten steuert, wenn die Schaltfläche den Fokus erhält.
ms.assetid: 91d98bce-abea-4afc-a995-0f426ba7a518
keywords:
- Windows-Steuerelemente für BM_SETDONTCLICK Meldung
topic_type:
- apiref
api_name:
- BM_SETDONTCLICK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8596ec679ff07b87b3433d5b5a7805698f56f84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339543"
---
# <a name="bm_setdontclick-message"></a><span data-ttu-id="e6f72-104">BM- \_ setdontclick-Meldung</span><span class="sxs-lookup"><span data-stu-id="e6f72-104">BM\_SETDONTCLICK message</span></span>

<span data-ttu-id="e6f72-105">Legt ein Flag für ein Optionsfeld fest, das die Generierung [von \_ Milliarden](bn-clicked.md) -Nachrichten steuert, wenn die Schaltfläche den Fokus erhält.</span><span class="sxs-lookup"><span data-stu-id="e6f72-105">Sets a flag on a radio button that controls the generation of [BN\_CLICKED](bn-clicked.md) messages when the button receives focus.</span></span>

## <a name="parameters"></a><span data-ttu-id="e6f72-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6f72-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6f72-107">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e6f72-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6f72-108">Ein **boolescher** Wert, der den Zustand angibt.</span><span class="sxs-lookup"><span data-stu-id="e6f72-108">A **BOOL** that specifies the state.</span></span> <span data-ttu-id="e6f72-109">**True** , wenn das Flag festgelegt werden soll, andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="e6f72-109">**TRUE** to set the flag, otherwise **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="e6f72-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e6f72-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6f72-111">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e6f72-111">Not used.</span></span> <span data-ttu-id="e6f72-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="e6f72-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6f72-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e6f72-113">Return value</span></span>

<span data-ttu-id="e6f72-114">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="e6f72-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6f72-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6f72-115">Requirements</span></span>



| <span data-ttu-id="e6f72-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6f72-116">Requirement</span></span> | <span data-ttu-id="e6f72-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e6f72-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6f72-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e6f72-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e6f72-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6f72-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e6f72-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e6f72-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e6f72-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6f72-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e6f72-122">Header</span><span class="sxs-lookup"><span data-stu-id="e6f72-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6f72-123"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="e6f72-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





