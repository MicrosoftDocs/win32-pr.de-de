---
title: TB_GETRECT Meldung (kommstrg. h)
description: Ruft das umgebende Rechteck für eine angegebene Symbolleisten Schaltfläche ab.
ms.assetid: a93885eb-7eb7-4434-ad51-80fb30d3bfa1
keywords:
- Windows-Steuerelemente für TB_GETRECT Meldung
topic_type:
- apiref
api_name:
- TB_GETRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 889d067eb282e3d834ba4dc0cf6711c0561d86e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859293"
---
# <a name="tb_getrect-message"></a><span data-ttu-id="72c8c-104">TB \_ GetRect-Nachricht</span><span class="sxs-lookup"><span data-stu-id="72c8c-104">TB\_GETRECT message</span></span>

<span data-ttu-id="72c8c-105">Ruft das umgebende Rechteck für eine angegebene Symbolleisten Schaltfläche ab.</span><span class="sxs-lookup"><span data-stu-id="72c8c-105">Retrieves the bounding rectangle for a specified toolbar button.</span></span>

## <a name="parameters"></a><span data-ttu-id="72c8c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="72c8c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72c8c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="72c8c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="72c8c-108">Der Befehls Bezeichner der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="72c8c-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="72c8c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="72c8c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="72c8c-110">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die umschließenden Rechteck Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="72c8c-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the bounding rectangle information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72c8c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="72c8c-111">Return value</span></span>

<span data-ttu-id="72c8c-112">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="72c8c-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="72c8c-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="72c8c-113">Remarks</span></span>

<span data-ttu-id="72c8c-114">Diese Nachricht ruft nicht das umgebende Rechteck für Schaltflächen ab, deren Zustand auf den [**ausgeblendeten \_ TBSTATE**](toolbar-button-states.md) -Wert festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="72c8c-114">This message does not retrieve the bounding rectangle for buttons whose state is set to the [**TBSTATE\_HIDDEN**](toolbar-button-states.md) value.</span></span>

## <a name="requirements"></a><span data-ttu-id="72c8c-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72c8c-115">Requirements</span></span>



| <span data-ttu-id="72c8c-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="72c8c-116">Requirement</span></span> | <span data-ttu-id="72c8c-117">Wert</span><span class="sxs-lookup"><span data-stu-id="72c8c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="72c8c-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="72c8c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="72c8c-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="72c8c-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="72c8c-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="72c8c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="72c8c-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="72c8c-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="72c8c-122">Header</span><span class="sxs-lookup"><span data-stu-id="72c8c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="72c8c-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="72c8c-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

