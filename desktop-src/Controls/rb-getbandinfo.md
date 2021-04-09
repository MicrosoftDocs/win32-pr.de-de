---
title: RB_GETBANDINFO Meldung (kommstrg. h)
description: Ruft Informationen zu einem angegebenen Band in einem Grund leisten-Steuerelement ab.
ms.assetid: c2a76c91-7d44-4278-823d-bd263520e7a8
keywords:
- Windows-Steuerelemente für RB_GETBANDINFO Meldung
topic_type:
- apiref
api_name:
- RB_GETBANDINFO
- RB_GETBANDINFOA
- RB_GETBANDINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b87715cf61b4eb2726eab83d500330721f41719f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104792"
---
# <a name="rb_getbandinfo-message"></a><span data-ttu-id="bcb2e-104">RB \_ GetBandInfo-Meldung</span><span class="sxs-lookup"><span data-stu-id="bcb2e-104">RB\_GETBANDINFO message</span></span>

<span data-ttu-id="bcb2e-105">Ruft Informationen zu einem angegebenen Band in einem Grund leisten-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="bcb2e-105">Retrieves information about a specified band in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="bcb2e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bcb2e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcb2e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bcb2e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bcb2e-108">Der null basierte Index des Bands, für das die Informationen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="bcb2e-108">Zero-based index of the band for which the information will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="bcb2e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bcb2e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bcb2e-110">Ein Zeiger auf eine [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) -Struktur, die die angeforderten Bandinformationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="bcb2e-110">Pointer to a [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure that will receive the requested band information.</span></span> <span data-ttu-id="bcb2e-111">Vor dem Senden dieser Nachricht müssen Sie das **CBSIZE** -Element dieser Struktur auf die Größe der **REBARBANDINFO** -Struktur festlegen und das **fmask** -Element auf die Elemente festlegen, die Sie abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="bcb2e-111">Before sending this message, you must set the **cbSize** member of this structure to the size of the **REBARBANDINFO** structure and set the **fMask** member to the items you want to retrieve.</span></span> <span data-ttu-id="bcb2e-112">Außerdem müssen Sie den **CCH** -Member der **REBARBANDINFO** -Struktur auf die Größe des **lpText** -Puffers festlegen, wenn rbbim- \_ Text angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bcb2e-112">Additionally, you must set the **cch** member of the **REBARBANDINFO** structure to the size of the **lpText** buffer when RBBIM\_TEXT is specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcb2e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bcb2e-113">Return value</span></span>

<span data-ttu-id="bcb2e-114">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="bcb2e-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcb2e-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bcb2e-115">Requirements</span></span>



| <span data-ttu-id="bcb2e-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bcb2e-116">Requirement</span></span> | <span data-ttu-id="bcb2e-117">Wert</span><span class="sxs-lookup"><span data-stu-id="bcb2e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bcb2e-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bcb2e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bcb2e-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bcb2e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bcb2e-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bcb2e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bcb2e-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bcb2e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bcb2e-122">Header</span><span class="sxs-lookup"><span data-stu-id="bcb2e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcb2e-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcb2e-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="bcb2e-124">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="bcb2e-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bcb2e-125">**RB \_ Getbandinfow** (Unicode) und **RB \_ getbandinfoa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="bcb2e-125">**RB\_GETBANDINFOW** (Unicode) and **RB\_GETBANDINFOA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="bcb2e-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bcb2e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcb2e-127">**RB \_ SetBandInfo**</span><span class="sxs-lookup"><span data-stu-id="bcb2e-127">**RB\_SETBANDINFO**</span></span>](rb-setbandinfo.md)
</dt> </dl>

 

 





