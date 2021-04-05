---
title: TB_GETITEMRECT Meldung (kommstrg. h)
description: Ruft das umgebende Rechteck einer Schaltfläche in einer Symbolleiste ab.
ms.assetid: 42c2c86e-0002-4029-be6a-fdfdf405b78c
keywords:
- Windows-Steuerelemente für TB_GETITEMRECT Meldung
topic_type:
- apiref
api_name:
- TB_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e71a4c6540a1a7ff918b97b3a331e692f6d44529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859103"
---
# <a name="tb_getitemrect-message"></a><span data-ttu-id="09e3b-104">TB- \_ GetItemRect-Nachricht</span><span class="sxs-lookup"><span data-stu-id="09e3b-104">TB\_GETITEMRECT message</span></span>

<span data-ttu-id="09e3b-105">Ruft das umgebende Rechteck einer Schaltfläche in einer Symbolleiste ab.</span><span class="sxs-lookup"><span data-stu-id="09e3b-105">Retrieves the bounding rectangle of a button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="09e3b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="09e3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09e3b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="09e3b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="09e3b-108">NULL basierter Index der Schaltfläche, für die Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="09e3b-108">Zero-based index of the button for which to retrieve information.</span></span>

</dd> <dt>

<span data-ttu-id="09e3b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="09e3b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="09e3b-110">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die Client Koordinaten des umschließenden Rechtecks empfängt.</span><span class="sxs-lookup"><span data-stu-id="09e3b-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the client coordinates of the bounding rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09e3b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="09e3b-111">Return value</span></span>

<span data-ttu-id="09e3b-112">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="09e3b-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="09e3b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="09e3b-113">Remarks</span></span>

<span data-ttu-id="09e3b-114">Diese Nachricht ruft nicht das umgebende Rechteck für Schaltflächen ab, deren Zustand auf den [**ausgeblendeten \_ TBSTATE**](toolbar-button-states.md) -Wert festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="09e3b-114">This message does not retrieve the bounding rectangle for buttons whose state is set to the [**TBSTATE\_HIDDEN**](toolbar-button-states.md) value.</span></span>

## <a name="requirements"></a><span data-ttu-id="09e3b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="09e3b-115">Requirements</span></span>



| <span data-ttu-id="09e3b-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="09e3b-116">Requirement</span></span> | <span data-ttu-id="09e3b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="09e3b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="09e3b-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="09e3b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="09e3b-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="09e3b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="09e3b-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="09e3b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="09e3b-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="09e3b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="09e3b-122">Header</span><span class="sxs-lookup"><span data-stu-id="09e3b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="09e3b-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="09e3b-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

