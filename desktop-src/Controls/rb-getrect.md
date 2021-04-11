---
title: RB_GETRECT Meldung (kommstrg. h)
description: Ruft das umschließende Rechteck für ein bestimmtes Band in einem Grund leisten-Steuerelement ab.
ms.assetid: e272b090-1e4d-4cff-87f0-557ad8116e7e
keywords:
- Windows-Steuerelemente für RB_GETRECT Meldung
topic_type:
- apiref
api_name:
- RB_GETRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76b9d5de00b638a3767df461595ff01316b23183
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104213721"
---
# <a name="rb_getrect-message"></a><span data-ttu-id="9f0aa-104">RB \_ GetRect-Nachricht</span><span class="sxs-lookup"><span data-stu-id="9f0aa-104">RB\_GETRECT message</span></span>

<span data-ttu-id="9f0aa-105">Ruft das umschließende Rechteck für ein bestimmtes Band in einem Grund leisten-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="9f0aa-105">Retrieves the bounding rectangle for a given band in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="9f0aa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f0aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f0aa-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9f0aa-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f0aa-108">NULL basierter Index eines Bands im Grund leisten-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="9f0aa-108">Zero-based index of a band in the rebar control.</span></span>

</dd> <dt>

<span data-ttu-id="9f0aa-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9f0aa-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f0aa-110">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die Begrenzungen des Bereichs der Info Leiste empfängt.</span><span class="sxs-lookup"><span data-stu-id="9f0aa-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the bounds of the rebar band.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f0aa-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9f0aa-111">Return value</span></span>

<span data-ttu-id="9f0aa-112">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="9f0aa-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f0aa-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f0aa-113">Requirements</span></span>



| <span data-ttu-id="9f0aa-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f0aa-114">Requirement</span></span> | <span data-ttu-id="9f0aa-115">Wert</span><span class="sxs-lookup"><span data-stu-id="9f0aa-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9f0aa-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9f0aa-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9f0aa-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f0aa-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9f0aa-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9f0aa-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9f0aa-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f0aa-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9f0aa-120">Header</span><span class="sxs-lookup"><span data-stu-id="9f0aa-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f0aa-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f0aa-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

