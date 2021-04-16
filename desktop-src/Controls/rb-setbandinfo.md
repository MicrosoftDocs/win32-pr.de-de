---
title: RB_SETBANDINFO Meldung (kommstrg. h)
description: Legt die Eigenschaften eines vorhandenen Bands in einem Grund leisten-Steuerelement fest.
ms.assetid: 00021c35-612d-4278-b10c-6e9f1f45a543
keywords:
- Windows-Steuerelemente für RB_SETBANDINFO Meldung
topic_type:
- apiref
api_name:
- RB_SETBANDINFO
- RB_SETBANDINFOA
- RB_SETBANDINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92e81377a40f8b6054f5d8cfae16837621b77b61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477865"
---
# <a name="rb_setbandinfo-message"></a><span data-ttu-id="ca0e1-104">RB \_ SetBandInfo-Meldung</span><span class="sxs-lookup"><span data-stu-id="ca0e1-104">RB\_SETBANDINFO message</span></span>

<span data-ttu-id="ca0e1-105">Legt die Eigenschaften eines vorhandenen Bands in einem Grund leisten-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="ca0e1-105">Sets characteristics of an existing band in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ca0e1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca0e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca0e1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ca0e1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ca0e1-108">NULL basierter Index des Bands, um die neuen Einstellungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ca0e1-108">Zero-based index of the band to receive the new settings.</span></span>

</dd> <dt>

<span data-ttu-id="ca0e1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ca0e1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ca0e1-110">Ein Zeiger auf eine [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) -Struktur, die das zu ändernde Band und die neuen Einstellungen definiert.</span><span class="sxs-lookup"><span data-stu-id="ca0e1-110">Pointer to a [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure that defines the band to be modified and the new settings.</span></span> <span data-ttu-id="ca0e1-111">Vor dem Senden dieser Nachricht müssen Sie das **CBSIZE** -Element dieser Struktur auf die **sizeof**(REBARBANDINFO)-Struktur festlegen.</span><span class="sxs-lookup"><span data-stu-id="ca0e1-111">Before sending this message, you must set the **cbSize** member of this structure to the **sizeof**(REBARBANDINFO) structure.</span></span> <span data-ttu-id="ca0e1-112">Außerdem müssen Sie den **CCH** -Member der **REBARBANDINFO** -Struktur auf die Größe des **lpText** -Puffers festlegen, wenn rbbim- \_ Text angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ca0e1-112">Additionally, you must set the **cch** member of the **REBARBANDINFO** structure to the size of the **lpText** buffer when RBBIM\_TEXT is specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca0e1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ca0e1-113">Return value</span></span>

<span data-ttu-id="ca0e1-114">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="ca0e1-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca0e1-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca0e1-115">Requirements</span></span>



| <span data-ttu-id="ca0e1-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca0e1-116">Requirement</span></span> | <span data-ttu-id="ca0e1-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ca0e1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca0e1-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ca0e1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ca0e1-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ca0e1-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ca0e1-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ca0e1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ca0e1-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ca0e1-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ca0e1-122">Header</span><span class="sxs-lookup"><span data-stu-id="ca0e1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca0e1-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca0e1-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="ca0e1-124">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="ca0e1-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ca0e1-125">**RB \_ Setbandinfow** (Unicode) und **RB \_ setbandinfoa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ca0e1-125">**RB\_SETBANDINFOW** (Unicode) and **RB\_SETBANDINFOA** (ANSI)</span></span><br/>             |



 

 





