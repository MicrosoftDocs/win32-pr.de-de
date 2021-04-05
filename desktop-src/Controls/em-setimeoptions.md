---
title: EM_SETIMEOPTIONS Meldung (RichEdit. h)
description: Legt die Optionen für den Eingabemethoden-Editor (IME) fest.
ms.assetid: 8a72ee1c-f6b8-44eb-b8df-57cd834db326
keywords:
- Windows-Steuerelemente für EM_SETIMEOPTIONS Meldung
topic_type:
- apiref
api_name:
- EM_SETIMEOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59be3148bd00abd998af200368f2ed77ad3ff911
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859013"
---
# <a name="em_setimeoptions-message"></a><span data-ttu-id="19820-104">EM- \_ /timeoptions-Meldung</span><span class="sxs-lookup"><span data-stu-id="19820-104">EM\_SETIMEOPTIONS message</span></span>

<span data-ttu-id="19820-105">Legt die Optionen für den Eingabemethoden-Editor (IME) fest.</span><span class="sxs-lookup"><span data-stu-id="19820-105">Sets the Input Method Editor (IME) options.</span></span>

> [!Note]  
> <span data-ttu-id="19820-106">Diese Meldung wird nur in asiatischen Sprachversionen von Microsoft Rich Edit 1,0 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="19820-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="19820-107">Sie wird in späteren Versionen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="19820-107">It is not supported in any later versions.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="19820-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="19820-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19820-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="19820-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19820-110">Gibt einen der folgenden Werte an.</span><span class="sxs-lookup"><span data-stu-id="19820-110">Specifies one of the following values.</span></span>



| <span data-ttu-id="19820-111">Wert</span><span class="sxs-lookup"><span data-stu-id="19820-111">Value</span></span>                                                                                                                                             | <span data-ttu-id="19820-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="19820-112">Meaning</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="ECOOP_SET"></span><span id="ecoop_set"></span><dl> <span data-ttu-id="19820-113"><dt>**ECOOP- \_ Satz**</dt></span><span class="sxs-lookup"><span data-stu-id="19820-113"><dt>**ECOOP\_SET**</dt></span></span> </dl> | <span data-ttu-id="19820-114">Legt die Optionen auf die von *LPARAM* angegebenen Optionen fest.</span><span class="sxs-lookup"><span data-stu-id="19820-114">Sets the options to those specified by *lParam*.</span></span><br/>                             |
| <span id="ECOOP_OR"></span><span id="ecoop_or"></span><dl> <span data-ttu-id="19820-115"><dt>**ECOOP \_ oder**</dt></span><span class="sxs-lookup"><span data-stu-id="19820-115"><dt>**ECOOP\_OR**</dt></span></span> </dl>    | <span data-ttu-id="19820-116">Kombiniert die angegebenen Optionen mit den aktuellen Optionen.</span><span class="sxs-lookup"><span data-stu-id="19820-116">Combines the specified options with the current options.</span></span><br/>                     |
| <span id="ECOOP_AND"></span><span id="ecoop_and"></span><dl> <span data-ttu-id="19820-117"><dt>**ECOOP \_ und**</dt></span><span class="sxs-lookup"><span data-stu-id="19820-117"><dt>**ECOOP\_AND**</dt></span></span> </dl> | <span data-ttu-id="19820-118">Behält nur die aktuellen Optionen bei, die auch von *LPARAM* angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="19820-118">Retains only those current options that are also specified by *lParam*.</span></span><br/>      |
| <span id="ECOOP_XOR"></span><span id="ecoop_xor"></span><dl> <span data-ttu-id="19820-119"><dt>**ECOOP- \_ Xor**</dt></span><span class="sxs-lookup"><span data-stu-id="19820-119"><dt>**ECOOP\_XOR**</dt></span></span> </dl> | <span data-ttu-id="19820-120">Logisch exklusiv oder die aktuellen Optionen mit den von *LPARAM* angegebenen Optionen.</span><span class="sxs-lookup"><span data-stu-id="19820-120">Logically exclusive OR the current options with those specified by *lParam.*</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="19820-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="19820-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19820-122">Gibt einen der folgenden Werte an.</span><span class="sxs-lookup"><span data-stu-id="19820-122">Specifies one of more of the following values.</span></span>



| <span data-ttu-id="19820-123">Wert</span><span class="sxs-lookup"><span data-stu-id="19820-123">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="19820-124">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="19820-124">Meaning</span></span>                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="IMF_CLOSESTATUSWINDOW"></span><span id="imf_closestatuswindow"></span><dl> <span data-ttu-id="19820-125"><dt>**IMF \_ closestatus Window**</dt></span><span class="sxs-lookup"><span data-stu-id="19820-125"><dt>**IMF\_CLOSESTATUSWINDOW**</dt></span></span> </dl> | <span data-ttu-id="19820-126">Schließt das Fenster "IME-Status", wenn das Steuerelement den Eingabefokus erhält.</span><span class="sxs-lookup"><span data-stu-id="19820-126">Closes the IME status window when the control receives the input focus.</span></span><br/>                                                                                                               |
| <span id="IMF_FORCEACTIVE"></span><span id="imf_forceactive"></span><dl> <span data-ttu-id="19820-127"><dt>**IMF \_ forceactive**</dt></span><span class="sxs-lookup"><span data-stu-id="19820-127"><dt>**IMF\_FORCEACTIVE**</dt></span></span> </dl>                   | <span data-ttu-id="19820-128">Aktiviert den IME, wenn das Steuerelement den Eingabefokus erhält.</span><span class="sxs-lookup"><span data-stu-id="19820-128">Activates the IME when the control receives the input focus.</span></span><br/>                                                                                                                          |
| <span id="IMF_FORCEDISABLE"></span><span id="imf_forcedisable"></span><dl> <span data-ttu-id="19820-129"><dt>**IMF \_ forcedeaktivieren**</dt></span><span class="sxs-lookup"><span data-stu-id="19820-129"><dt>**IMF\_FORCEDISABLE**</dt></span></span> </dl>                | <span data-ttu-id="19820-130">Deaktiviert den IME, wenn das Steuerelement den Eingabefokus erhält.</span><span class="sxs-lookup"><span data-stu-id="19820-130">Disables the IME when the control receives the input focus.</span></span><br/>                                                                                                                           |
| <span id="IMF_FORCEENABLE"></span><span id="imf_forceenable"></span><dl> <span data-ttu-id="19820-131"><dt>**IMF \_ forceenable**</dt></span><span class="sxs-lookup"><span data-stu-id="19820-131"><dt>**IMF\_FORCEENABLE**</dt></span></span> </dl>                   | <span data-ttu-id="19820-132">Aktiviert den IME, wenn das Steuerelement den Eingabefokus erhält.</span><span class="sxs-lookup"><span data-stu-id="19820-132">Enables the IME when the control receives the input focus.</span></span><br/>                                                                                                                            |
| <span id="IMF_FORCEINACTIVE"></span><span id="imf_forceinactive"></span><dl> <span data-ttu-id="19820-133"><dt>**IMF \_ forceingeactive**</dt></span><span class="sxs-lookup"><span data-stu-id="19820-133"><dt>**IMF\_FORCEINACTIVE**</dt></span></span> </dl>             | <span data-ttu-id="19820-134">Deaktiviert den IME, wenn das Steuerelement den Eingabefokus erhält.</span><span class="sxs-lookup"><span data-stu-id="19820-134">Inactivates the IME when the control receives the input focus.</span></span><br/>                                                                                                                        |
| <span id="IMF_FORCENONE"></span><span id="imf_forcenone"></span><dl> <span data-ttu-id="19820-135"><dt>**IMF ( \_ forcenone)**</dt></span><span class="sxs-lookup"><span data-stu-id="19820-135"><dt>**IMF\_FORCENONE**</dt></span></span> </dl>                         | <span data-ttu-id="19820-136">Deaktiviert die IME-Behandlung.</span><span class="sxs-lookup"><span data-stu-id="19820-136">Disables IME handling.</span></span><br/>                                                                                                                                                                |
| <span id="IMF_FORCEREMEMBER"></span><span id="imf_forceremember"></span><dl> <span data-ttu-id="19820-137"><dt>**IMF- \_ forceremember**</dt></span><span class="sxs-lookup"><span data-stu-id="19820-137"><dt>**IMF\_FORCEREMEMBER**</dt></span></span> </dl>             | <span data-ttu-id="19820-138">Stellt den vorherigen IME-Status wieder her, wenn das Steuerelement den Eingabefokus erhält.</span><span class="sxs-lookup"><span data-stu-id="19820-138">Restores the previous IME status when the control receives the input focus.</span></span><br/>                                                                                                           |
| <span id="IMF_MULTIPLEEDIT"></span><span id="imf_multipleedit"></span><dl> <span data-ttu-id="19820-139"><dt>**IWF \_ multipleedit**</dt></span><span class="sxs-lookup"><span data-stu-id="19820-139"><dt>**IMF\_MULTIPLEEDIT**</dt></span></span> </dl>                | <span data-ttu-id="19820-140">Gibt an, dass die Kompositions Zeichenfolge nicht abgebrochen oder durch Fokus Änderungen bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="19820-140">Specifies that the composition string will not be canceled or determined by focus changes.</span></span> <span data-ttu-id="19820-141">Dies ermöglicht es einer Anwendung, separate Kompositions Zeichenfolgen für jedes Rich Edit-Steuerelement zu haben.</span><span class="sxs-lookup"><span data-stu-id="19820-141">This allows an application to have separate composition strings on each rich edit control.</span></span><br/> |
| <span id="IMF_VERTICAL"></span><span id="imf_vertical"></span><dl> <span data-ttu-id="19820-142"><dt>**IMF ( \_ vertikal)**</dt></span><span class="sxs-lookup"><span data-stu-id="19820-142"><dt>**IMF\_VERTICAL**</dt></span></span> </dl>                            | <span data-ttu-id="19820-143">Hinweis wird in Rich Edit 2,0 und höher verwendet.</span><span class="sxs-lookup"><span data-stu-id="19820-143">Note used in Rich Edit 2.0 and later.</span></span> <br/>                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19820-144">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="19820-144">Return value</span></span>

<span data-ttu-id="19820-145">Wenn der Vorgang erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="19820-145">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="19820-146">Wenn der Vorgang fehlschlägt, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="19820-146">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="19820-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19820-147">Requirements</span></span>



| <span data-ttu-id="19820-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19820-148">Requirement</span></span> | <span data-ttu-id="19820-149">Wert</span><span class="sxs-lookup"><span data-stu-id="19820-149">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="19820-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="19820-150">Minimum supported client</span></span><br/> | <span data-ttu-id="19820-151">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19820-151">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="19820-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="19820-152">Minimum supported server</span></span><br/> | <span data-ttu-id="19820-153">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19820-153">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="19820-154">Header</span><span class="sxs-lookup"><span data-stu-id="19820-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="19820-155"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="19820-155"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19820-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19820-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19820-157">**EM \_ getIMEOptions**</span><span class="sxs-lookup"><span data-stu-id="19820-157">**EM\_GETIMEOPTIONS**</span></span>](em-getimeoptions.md)
</dt> </dl>

 

 





