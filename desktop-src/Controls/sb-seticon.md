---
title: SB_SETICON Meldung (kommstrg. h)
description: Legt das Symbol für einen Teil in einer Statusleiste fest.
ms.assetid: d8528cd1-54d2-44ba-b0d6-29111f75616a
keywords:
- Windows-Steuerelemente für SB_SETICON Meldung
topic_type:
- apiref
api_name:
- SB_SETICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f720c414238eb89cf98bf0556ebabffefceae4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859106"
---
# <a name="sb_seticon-message"></a><span data-ttu-id="a3c52-104">SB- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="a3c52-104">SB\_SETICON message</span></span>

<span data-ttu-id="a3c52-105">Legt das Symbol für einen Teil in einer Statusleiste fest.</span><span class="sxs-lookup"><span data-stu-id="a3c52-105">Sets the icon for a part in a status bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="a3c52-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3c52-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3c52-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a3c52-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a3c52-108">NULL basierter Index des Teils, der das Symbol empfängt.</span><span class="sxs-lookup"><span data-stu-id="a3c52-108">Zero-based index of the part that will receive the icon.</span></span> <span data-ttu-id="a3c52-109">Wenn dieser Parameter-1 ist, wird angenommen, dass es sich bei der Statusleiste um eine einfache Statusleiste handelt.</span><span class="sxs-lookup"><span data-stu-id="a3c52-109">If this parameter is -1, the status bar is assumed to be a simple status bar.</span></span>

</dd> <dt>

<span data-ttu-id="a3c52-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a3c52-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a3c52-111">Handle für das Symbol, das festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a3c52-111">Handle to the icon to be set.</span></span> <span data-ttu-id="a3c52-112">Wenn dieser Wert **null** ist, wird das Symbol aus dem Teil entfernt.</span><span class="sxs-lookup"><span data-stu-id="a3c52-112">If this value is **NULL**, the icon is removed from the part.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3c52-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a3c52-113">Return value</span></span>

<span data-ttu-id="a3c52-114">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="a3c52-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3c52-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3c52-115">Remarks</span></span>

<span data-ttu-id="a3c52-116">Das Symbol wird in der Statusleiste nicht zerstört.</span><span class="sxs-lookup"><span data-stu-id="a3c52-116">The status bar will not destroy the icon.</span></span> <span data-ttu-id="a3c52-117">Es ist die Aufgabe der aufrufenden Anwendung, beliebige Symbole nachzuverfolgen und zu zerstören.</span><span class="sxs-lookup"><span data-stu-id="a3c52-117">It is the calling application's responsibility to keep track of and destroy any icons.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3c52-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3c52-118">Requirements</span></span>



| <span data-ttu-id="a3c52-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a3c52-119">Requirement</span></span> | <span data-ttu-id="a3c52-120">Wert</span><span class="sxs-lookup"><span data-stu-id="a3c52-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a3c52-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a3c52-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a3c52-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a3c52-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a3c52-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a3c52-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a3c52-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a3c52-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a3c52-125">Header</span><span class="sxs-lookup"><span data-stu-id="a3c52-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3c52-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3c52-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





