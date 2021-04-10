---
title: PBM_GETSTATE Meldung (kommstrg. h)
description: Ruft den Status der Statusanzeige ab.
ms.assetid: ff240160-7db6-4711-8d4e-25a77dfba118
keywords:
- Windows-Steuerelemente für PBM_GETSTATE Meldung
topic_type:
- apiref
api_name:
- PBM_GETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07d4f7029fca46a046545efd1cea8e0eab99c757
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956813"
---
# <a name="pbm_getstate-message"></a><span data-ttu-id="57cd4-104">PBM \_ GetState-Nachricht</span><span class="sxs-lookup"><span data-stu-id="57cd4-104">PBM\_GETSTATE message</span></span>

<span data-ttu-id="57cd4-105">Ruft den Status der Statusanzeige ab.</span><span class="sxs-lookup"><span data-stu-id="57cd4-105">Gets the state of the progress bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="57cd4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="57cd4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57cd4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="57cd4-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="57cd4-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="57cd4-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="57cd4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="57cd4-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="57cd4-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="57cd4-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57cd4-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="57cd4-111">Return value</span></span>

<span data-ttu-id="57cd4-112">Gibt den aktuellen Status der Statusanzeige zurück.</span><span class="sxs-lookup"><span data-stu-id="57cd4-112">Returns the current state of the progress bar.</span></span> <span data-ttu-id="57cd4-113">Einer der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="57cd4-113">One of the following values.</span></span>



| <span data-ttu-id="57cd4-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="57cd4-114">Return code</span></span>                                                                                 | <span data-ttu-id="57cd4-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="57cd4-115">Description</span></span>             |
|---------------------------------------------------------------------------------------------|-------------------------|
| <dl> <span data-ttu-id="57cd4-116"><dt>**PBST \_ Normal**</dt></span><span class="sxs-lookup"><span data-stu-id="57cd4-116"><dt>**PBST\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="57cd4-117">Läuft.</span><span class="sxs-lookup"><span data-stu-id="57cd4-117">In progress.</span></span><br/> |
| <dl> <span data-ttu-id="57cd4-118"><dt>**PBST- \_ Fehler**</dt></span><span class="sxs-lookup"><span data-stu-id="57cd4-118"><dt>**PBST\_ERROR**</dt></span></span> </dl>  | <span data-ttu-id="57cd4-119">Fehler.</span><span class="sxs-lookup"><span data-stu-id="57cd4-119">Error.</span></span><br/>       |
| <dl> <span data-ttu-id="57cd4-120"><dt>**PBST \_ angehalten**</dt></span><span class="sxs-lookup"><span data-stu-id="57cd4-120"><dt>**PBST\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="57cd4-121">Angehalten.</span><span class="sxs-lookup"><span data-stu-id="57cd4-121">Paused.</span></span><br/>      |



 

## <a name="requirements"></a><span data-ttu-id="57cd4-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="57cd4-122">Requirements</span></span>



| <span data-ttu-id="57cd4-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="57cd4-123">Requirement</span></span> | <span data-ttu-id="57cd4-124">Wert</span><span class="sxs-lookup"><span data-stu-id="57cd4-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="57cd4-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="57cd4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="57cd4-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57cd4-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="57cd4-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="57cd4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="57cd4-128">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57cd4-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="57cd4-129">Header</span><span class="sxs-lookup"><span data-stu-id="57cd4-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="57cd4-130"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="57cd4-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





