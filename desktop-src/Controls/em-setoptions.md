---
title: EM_SETOPTIONS Meldung (RichEdit. h)
description: Legt die Optionen für ein Rich-Edit-Steuerelement fest.
ms.assetid: 98ef2de9-4c34-45ba-8e8a-eaf505f97f56
keywords:
- Windows-Steuerelemente für EM_SETOPTIONS Meldung
topic_type:
- apiref
api_name:
- EM_SETOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c43dda8268b42dc264a86600826d2a6b550e35c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103491"
---
# <a name="em_setoptions-message"></a><span data-ttu-id="2c3df-104">EM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="2c3df-104">EM\_SETOPTIONS message</span></span>

<span data-ttu-id="2c3df-105">Legt die Optionen für ein Rich-Edit-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="2c3df-105">Sets the options for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="2c3df-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c3df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c3df-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2c3df-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c3df-108">Gibt den Vorgang an, bei dem es sich um einen der folgenden Werte handeln kann.</span><span class="sxs-lookup"><span data-stu-id="2c3df-108">Specifies the operation, which can be one of these values.</span></span>



| <span data-ttu-id="2c3df-109">Wert</span><span class="sxs-lookup"><span data-stu-id="2c3df-109">Value</span></span>                                                                                                                                             | <span data-ttu-id="2c3df-110">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2c3df-110">Meaning</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="ECOOP_SET"></span><span id="ecoop_set"></span><dl> <span data-ttu-id="2c3df-111"><dt>**ECOOP- \_ Satz**</dt></span><span class="sxs-lookup"><span data-stu-id="2c3df-111"><dt>**ECOOP\_SET**</dt></span></span> </dl> | <span data-ttu-id="2c3df-112">Legt die Optionen auf die von *LPARAM* angegebenen Optionen fest.</span><span class="sxs-lookup"><span data-stu-id="2c3df-112">Sets the options to those specified by *lParam*.</span></span><br/>                             |
| <span id="ECOOP_OR"></span><span id="ecoop_or"></span><dl> <span data-ttu-id="2c3df-113"><dt>**ECOOP \_ oder**</dt></span><span class="sxs-lookup"><span data-stu-id="2c3df-113"><dt>**ECOOP\_OR**</dt></span></span> </dl>    | <span data-ttu-id="2c3df-114">Kombiniert die angegebenen Optionen mit den aktuellen Optionen.</span><span class="sxs-lookup"><span data-stu-id="2c3df-114">Combines the specified options with the current options.</span></span><br/>                     |
| <span id="ECOOP_AND"></span><span id="ecoop_and"></span><dl> <span data-ttu-id="2c3df-115"><dt>**ECOOP \_ und**</dt></span><span class="sxs-lookup"><span data-stu-id="2c3df-115"><dt>**ECOOP\_AND**</dt></span></span> </dl> | <span data-ttu-id="2c3df-116">Behält nur die aktuellen Optionen bei, die auch von *LPARAM* angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2c3df-116">Retains only those current options that are also specified by *lParam*.</span></span><br/>      |
| <span id="ECOOP_XOR"></span><span id="ecoop_xor"></span><dl> <span data-ttu-id="2c3df-117"><dt>**ECOOP- \_ Xor**</dt></span><span class="sxs-lookup"><span data-stu-id="2c3df-117"><dt>**ECOOP\_XOR**</dt></span></span> </dl> | <span data-ttu-id="2c3df-118">Logisch exklusiv oder die aktuellen Optionen mit den von *LPARAM* angegebenen Optionen.</span><span class="sxs-lookup"><span data-stu-id="2c3df-118">Logically exclusive OR the current options with those specified by *lParam*.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2c3df-119">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2c3df-119">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c3df-120">Gibt einen oder mehrere der folgenden Werte an.</span><span class="sxs-lookup"><span data-stu-id="2c3df-120">Specifies one or more of the following values.</span></span>



| <span data-ttu-id="2c3df-121">Wert</span><span class="sxs-lookup"><span data-stu-id="2c3df-121">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="2c3df-122">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2c3df-122">Meaning</span></span>                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="ECO_AUTOWORDSELECTION"></span><span id="eco_autowordselection"></span><dl> <span data-ttu-id="2c3df-123"><dt>**" \_ ecoautowordselection"**</dt></span><span class="sxs-lookup"><span data-stu-id="2c3df-123"><dt>**ECO\_AUTOWORDSELECTION**</dt></span></span> </dl> | <span data-ttu-id="2c3df-124">Automatische Auswahl von Word bei Doppelklick.</span><span class="sxs-lookup"><span data-stu-id="2c3df-124">Automatic selection of word on double-click.</span></span><br/>                                                                           |
| <span id="ECO_AUTOVSCROLL"></span><span id="eco_autovscroll"></span><dl> <span data-ttu-id="2c3df-125"><dt>**\_ecoautovscroll**</dt></span><span class="sxs-lookup"><span data-stu-id="2c3df-125"><dt>**ECO\_AUTOVSCROLL**</dt></span></span> </dl>                   | <span data-ttu-id="2c3df-126">Identisch mit [**dem \_ autovscroll**](rich-edit-control-styles.md) -Stil von es.</span><span class="sxs-lookup"><span data-stu-id="2c3df-126">Same as [**ES\_AUTOVSCROLL**](rich-edit-control-styles.md) style.</span></span><br/>                                      |
| <span id="ECO_AUTOHSCROLL"></span><span id="eco_autohscroll"></span><dl> <span data-ttu-id="2c3df-127"><dt>**\_ecoautohscroll**</dt></span><span class="sxs-lookup"><span data-stu-id="2c3df-127"><dt>**ECO\_AUTOHSCROLL**</dt></span></span> </dl>                   | <span data-ttu-id="2c3df-128">Identisch mit [**dem \_ autohscroll**](rich-edit-control-styles.md) -Stil von es.</span><span class="sxs-lookup"><span data-stu-id="2c3df-128">Same as [**ES\_AUTOHSCROLL**](rich-edit-control-styles.md) style.</span></span><br/>                                      |
| <span id="ECO_NOHIDESEL"></span><span id="eco_nohidesel"></span><dl> <span data-ttu-id="2c3df-129"><dt>**Öko- \_ nohidesel**</dt></span><span class="sxs-lookup"><span data-stu-id="2c3df-129"><dt>**ECO\_NOHIDESEL**</dt></span></span> </dl>                         | <span data-ttu-id="2c3df-130">Identisch mit [**es \_ nohidesel**](rich-edit-control-styles.md) Style.</span><span class="sxs-lookup"><span data-stu-id="2c3df-130">Same as [**ES\_NOHIDESEL**](rich-edit-control-styles.md) style.</span></span><br/>                                          |
| <span id="ECO_READONLY"></span><span id="eco_readonly"></span><dl> <span data-ttu-id="2c3df-131"><dt>**nur für die Umweltschutz \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2c3df-131"><dt>**ECO\_READONLY**</dt></span></span> </dl>                            | <span data-ttu-id="2c3df-132">Identisch mit dem schreibgeschützten Stil von [**es \_**](rich-edit-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="2c3df-132">Same as [**ES\_READONLY**](rich-edit-control-styles.md) style.</span></span><br/>                                            |
| <span id="ECO_WANTRETURN"></span><span id="eco_wantreturn"></span><dl> <span data-ttu-id="2c3df-133"><dt>**\_ecowantreturn**</dt></span><span class="sxs-lookup"><span data-stu-id="2c3df-133"><dt>**ECO\_WANTRETURN**</dt></span></span> </dl>                      | <span data-ttu-id="2c3df-134">Identisch mit [**es \_ wantreturn**](rich-edit-control-styles.md) Style.</span><span class="sxs-lookup"><span data-stu-id="2c3df-134">Same as [**ES\_WANTRETURN**](rich-edit-control-styles.md) style.</span></span><br/>                                        |
| <span id="ECO_SELECTIONBAR"></span><span id="eco_selectionbar"></span><dl> <span data-ttu-id="2c3df-135"><dt>**Öko- \_ selectionbar**</dt></span><span class="sxs-lookup"><span data-stu-id="2c3df-135"><dt>**ECO\_SELECTIONBAR**</dt></span></span> </dl>                | <span data-ttu-id="2c3df-136">Identisch mit dem- [**\_ selectionbar**](rich-edit-control-styles.md) -Stil.</span><span class="sxs-lookup"><span data-stu-id="2c3df-136">Same as [**ES\_SELECTIONBAR**](rich-edit-control-styles.md) style.</span></span><br/>                                    |
| <span id="ECO_VERTICAL"></span><span id="eco_vertical"></span><dl> <span data-ttu-id="2c3df-137"><dt>**Umwelt \_ vertikal**</dt></span><span class="sxs-lookup"><span data-stu-id="2c3df-137"><dt>**ECO\_VERTICAL**</dt></span></span> </dl>                            | <span data-ttu-id="2c3df-138">Identisch mit [**dem \_ vertikalen**](rich-edit-control-styles.md) Stil.</span><span class="sxs-lookup"><span data-stu-id="2c3df-138">Same as [**ES\_VERTICAL**](rich-edit-control-styles.md) style.</span></span> <span data-ttu-id="2c3df-139">Nur in den Versionen der asiatischen Sprache verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2c3df-139">Available in Asian-language versions only.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c3df-140">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2c3df-140">Return value</span></span>

<span data-ttu-id="2c3df-141">Diese Meldung gibt die aktuellen Optionen des Bearbeitungs Steuer Elements zurück.</span><span class="sxs-lookup"><span data-stu-id="2c3df-141">This message returns the current options of the edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c3df-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c3df-142">Requirements</span></span>



| <span data-ttu-id="2c3df-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c3df-143">Requirement</span></span> | <span data-ttu-id="2c3df-144">Wert</span><span class="sxs-lookup"><span data-stu-id="2c3df-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2c3df-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2c3df-145">Minimum supported client</span></span><br/> | <span data-ttu-id="2c3df-146">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c3df-146">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2c3df-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2c3df-147">Minimum supported server</span></span><br/> | <span data-ttu-id="2c3df-148">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c3df-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2c3df-149">Header</span><span class="sxs-lookup"><span data-stu-id="2c3df-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c3df-150"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c3df-150"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c3df-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c3df-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c3df-152">**Rich Edit-Steuerelement Stile**</span><span class="sxs-lookup"><span data-stu-id="2c3df-152">**Rich Edit Control Styles**</span></span>](rich-edit-control-styles.md)
</dt> </dl>

 

 





