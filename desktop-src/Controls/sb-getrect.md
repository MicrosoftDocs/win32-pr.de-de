---
title: SB_GETRECT Meldung (kommstrg. h)
description: Ruft das umgebende Rechteck eines Teils in einem Statusfenster ab.
ms.assetid: 76b8d470-07ae-440b-9bf5-7875b80b0168
keywords:
- Windows-Steuerelemente für SB_GETRECT Meldung
topic_type:
- apiref
api_name:
- SB_GETRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b48808b7bdf9c97fa6b9da53112e505e8cb8e66e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478102"
---
# <a name="sb_getrect-message"></a><span data-ttu-id="118bd-104">SB \_ GetRect-Nachricht</span><span class="sxs-lookup"><span data-stu-id="118bd-104">SB\_GETRECT message</span></span>

<span data-ttu-id="118bd-105">Ruft das umgebende Rechteck eines Teils in einem Statusfenster ab.</span><span class="sxs-lookup"><span data-stu-id="118bd-105">Retrieves the bounding rectangle of a part in a status window.</span></span>

## <a name="parameters"></a><span data-ttu-id="118bd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="118bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="118bd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="118bd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="118bd-108">NULL basierter Index des Teils, dessen Begrenzungs Rechteck abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="118bd-108">Zero-based index of the part whose bounding rectangle is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="118bd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="118bd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="118bd-110">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die das umschließende Rechteck empfängt.</span><span class="sxs-lookup"><span data-stu-id="118bd-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the bounding rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="118bd-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="118bd-111">Return value</span></span>

<span data-ttu-id="118bd-112">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="118bd-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="118bd-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="118bd-113">Requirements</span></span>



| <span data-ttu-id="118bd-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="118bd-114">Requirement</span></span> | <span data-ttu-id="118bd-115">Wert</span><span class="sxs-lookup"><span data-stu-id="118bd-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="118bd-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="118bd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="118bd-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="118bd-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="118bd-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="118bd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="118bd-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="118bd-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="118bd-120">Header</span><span class="sxs-lookup"><span data-stu-id="118bd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="118bd-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="118bd-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

