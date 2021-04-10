---
title: PGM_GETBUTTONSTATE Meldung (kommstrg. h)
description: Ruft den Zustand der angegebenen Schaltfläche in einem Pager-Steuerelement ab. Sie können diese Nachricht explizit senden oder das Pager \_ GetButtonState-Makro verwenden.
ms.assetid: 58f99b67-fef7-4695-86e2-0579a2f6de2f
keywords:
- Windows-Steuerelemente für PGM_GETBUTTONSTATE Meldung
topic_type:
- apiref
api_name:
- PGM_GETBUTTONSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d8c9eebbc0aa91651a01de1fe193544f0c8afcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956807"
---
# <a name="pgm_getbuttonstate-message"></a><span data-ttu-id="f05ed-105">PGM- \_ GetButtonState-Meldung</span><span class="sxs-lookup"><span data-stu-id="f05ed-105">PGM\_GETBUTTONSTATE message</span></span>

<span data-ttu-id="f05ed-106">Ruft den Zustand der angegebenen Schaltfläche in einem Pager-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="f05ed-106">Retrieves the state of the specified button in a pager control.</span></span> <span data-ttu-id="f05ed-107">Sie können diese Nachricht explizit senden oder das [**Pager \_ GetButtonState**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="f05ed-107">You can send this message explicitly or use the [**Pager\_GetButtonState**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f05ed-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f05ed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f05ed-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f05ed-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f05ed-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="f05ed-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f05ed-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f05ed-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f05ed-112">Gibt an, für welche Schaltfläche der Status abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f05ed-112">Indicates which button to retrieve the state for.</span></span> <span data-ttu-id="f05ed-113">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="f05ed-113">This can be one of the following values:</span></span>



| <span data-ttu-id="f05ed-114">Wert</span><span class="sxs-lookup"><span data-stu-id="f05ed-114">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="f05ed-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f05ed-115">Meaning</span></span>                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PGB_TOPORLEFT"></span><span id="pgb_toporleft"></span><dl> <span data-ttu-id="f05ed-116"><dt>**PGB- \_ toporleft**</dt></span><span class="sxs-lookup"><span data-stu-id="f05ed-116"><dt>**PGB\_TOPORLEFT**</dt></span></span> </dl>             | <span data-ttu-id="f05ed-117">Gibt die oberste Schaltfläche in einem [**PGS \_**](pager-control-styles.md) -Steuerelement "Pager" oder die linke Schaltfläche in einem [**PGS- \_ Horz**](pager-control-styles.md) -Pager-Steuerelement an</span><span class="sxs-lookup"><span data-stu-id="f05ed-117">Indicates the top button in a [**PGS\_VERT**](pager-control-styles.md) pager control or the left button in a [**PGS\_HORZ**](pager-control-styles.md) pager control.</span></span> <br/>     |
| <span id="PGB_BOTTOMORRIGHT"></span><span id="pgb_bottomorright"></span><dl> <span data-ttu-id="f05ed-118"><dt>**PGB \_ bottomorright**</dt></span><span class="sxs-lookup"><span data-stu-id="f05ed-118"><dt>**PGB\_BOTTOMORRIGHT**</dt></span></span> </dl> | <span data-ttu-id="f05ed-119">Gibt die untere Schaltfläche in einem [**PGS \_**](pager-control-styles.md) -Steuerelement des Pager-Steuer Elements oder die Rechte Taste in einem [**PGS- \_ Horz**](pager-control-styles.md) -Pager-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="f05ed-119">Indicates the bottom button in a [**PGS\_VERT**](pager-control-styles.md) pager control or the right button in a [**PGS\_HORZ**](pager-control-styles.md) pager control.</span></span> <br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f05ed-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f05ed-120">Return value</span></span>

<span data-ttu-id="f05ed-121">Gibt den Zustand der in *LPARAM* angegebenen Schaltfläche zurück.</span><span class="sxs-lookup"><span data-stu-id="f05ed-121">Returns the state of the button specified in *lParam*.</span></span> <span data-ttu-id="f05ed-122">Dabei handelt es sich um einen oder mehrere der folgenden Werte (wenn mehr als ein Wert zurückgegeben wird, werden Sie mit einem bitweisen OR kombiniert):</span><span class="sxs-lookup"><span data-stu-id="f05ed-122">This will be one or more of the following values (if more then one value is returned they will be combined using a bitwise OR):</span></span>



| <span data-ttu-id="f05ed-123">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f05ed-123">Return code</span></span>                                                                                   | <span data-ttu-id="f05ed-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f05ed-124">Description</span></span>                                 |
|-----------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="f05ed-125"><dt>**pgf \_ unsichtbar**</dt></span><span class="sxs-lookup"><span data-stu-id="f05ed-125"><dt>**PGF\_INVISIBLE**</dt></span></span> </dl> | <span data-ttu-id="f05ed-126">Die Schaltfläche ist nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="f05ed-126">The button is not visible.</span></span> <br/>      |
| <dl> <span data-ttu-id="f05ed-127"><dt>**pgf \_ Normal**</dt></span><span class="sxs-lookup"><span data-stu-id="f05ed-127"><dt>**PGF\_NORMAL**</dt></span></span> </dl>    | <span data-ttu-id="f05ed-128">Die Schaltfläche befindet sich im normalen Zustand.</span><span class="sxs-lookup"><span data-stu-id="f05ed-128">The button is in normal state.</span></span> <br/>  |
| <dl> <span data-ttu-id="f05ed-129"><dt>**pgf-abgeblendet \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f05ed-129"><dt>**PGF\_GRAYED**</dt></span></span> </dl>    | <span data-ttu-id="f05ed-130">Die Schaltfläche befindet sich in einem ausgefallenen Zustand.</span><span class="sxs-lookup"><span data-stu-id="f05ed-130">The button is in grayed state.</span></span> <br/>  |
| <dl> <span data-ttu-id="f05ed-131"><dt>**pgf- \_ depressiv**</dt></span><span class="sxs-lookup"><span data-stu-id="f05ed-131"><dt>**PGF\_DEPRESSED**</dt></span></span> </dl> | <span data-ttu-id="f05ed-132">Die Schaltfläche befindet sich im gedrückten Zustand.</span><span class="sxs-lookup"><span data-stu-id="f05ed-132">The button is in pressed state.</span></span> <br/> |
| <dl> <span data-ttu-id="f05ed-133"><dt>**pgf- \_ heiß**</dt></span><span class="sxs-lookup"><span data-stu-id="f05ed-133"><dt>**PGF\_HOT**</dt></span></span> </dl>       | <span data-ttu-id="f05ed-134">Die Schaltfläche befindet sich im aktiven Zustand.</span><span class="sxs-lookup"><span data-stu-id="f05ed-134">The button is in hot state.</span></span> <br/>     |



 

## <a name="requirements"></a><span data-ttu-id="f05ed-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f05ed-135">Requirements</span></span>



| <span data-ttu-id="f05ed-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f05ed-136">Requirement</span></span> | <span data-ttu-id="f05ed-137">Wert</span><span class="sxs-lookup"><span data-stu-id="f05ed-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f05ed-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f05ed-138">Minimum supported client</span></span><br/> | <span data-ttu-id="f05ed-139">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f05ed-139">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f05ed-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f05ed-140">Minimum supported server</span></span><br/> | <span data-ttu-id="f05ed-141">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f05ed-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f05ed-142">Header</span><span class="sxs-lookup"><span data-stu-id="f05ed-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="f05ed-143"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="f05ed-143"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





