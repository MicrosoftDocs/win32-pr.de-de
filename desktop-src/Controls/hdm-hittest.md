---
title: HDM_HITTEST Meldung (kommstrg. h)
description: Testet einen Punkt, um zu bestimmen, welches Header Element, sofern vorhanden, sich am angegebenen Punkt befindet.
ms.assetid: ff866bd1-9f2a-457c-921d-549610ab9088
keywords:
- Windows-Steuerelemente für HDM_HITTEST Meldung
topic_type:
- apiref
api_name:
- HDM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b6634396dbd5ecd4510a4f7341fc6380dbb0ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104481"
---
# <a name="hdm_hittest-message"></a><span data-ttu-id="e691b-104">HDM- \_ HitTest-Meldung</span><span class="sxs-lookup"><span data-stu-id="e691b-104">HDM\_HITTEST message</span></span>

<span data-ttu-id="e691b-105">Testet einen Punkt, um zu bestimmen, welches Header Element, sofern vorhanden, sich am angegebenen Punkt befindet.</span><span class="sxs-lookup"><span data-stu-id="e691b-105">Tests a point to determine which header item, if any, is at the specified point.</span></span>

## <a name="parameters"></a><span data-ttu-id="e691b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e691b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e691b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e691b-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e691b-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="e691b-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e691b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e691b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e691b-110">Ein Zeiger auf eine [**hdhittestinfo**](/windows/win32/api/commctrl/ns-commctrl-hdhittestinfo) -Struktur, die die zu testende Position enthält und Informationen über die Ergebnisse des Tests empfängt.</span><span class="sxs-lookup"><span data-stu-id="e691b-110">A pointer to an [**HDHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-hdhittestinfo) structure that contains the position to test and receives information about the results of the test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e691b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e691b-111">Return value</span></span>

<span data-ttu-id="e691b-112">Gibt den Index des Elements an der angegebenen Position zurück, sofern vorhanden, oder andernfalls 1.</span><span class="sxs-lookup"><span data-stu-id="e691b-112">Returns the index of the item at the specified position, if any, or   1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="e691b-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e691b-113">Requirements</span></span>



| <span data-ttu-id="e691b-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e691b-114">Requirement</span></span> | <span data-ttu-id="e691b-115">Wert</span><span class="sxs-lookup"><span data-stu-id="e691b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e691b-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e691b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e691b-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e691b-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e691b-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e691b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e691b-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e691b-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e691b-120">Header</span><span class="sxs-lookup"><span data-stu-id="e691b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e691b-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="e691b-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





