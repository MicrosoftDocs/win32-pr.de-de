---
title: MM_MCINOTIFY Meldung (MMSYSTEM. h)
description: Die \_ Meldung mm mcinotify benachrichtigt eine Anwendung, dass ein MCI-Gerät einen Vorgang abgeschlossen hat. MCI-Geräte senden diese Nachricht nur, wenn das MCI- \_ Benachrichtigungs Kennzeichen verwendet wird.
ms.assetid: a0840130-2969-4ce5-b098-3e45401eebb1
keywords:
- MM_MCINOTIFY-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_MCINOTIFY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96ee62c4a2b6e17bf5ad6d719dcb7d6e992a2f2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104709"
---
# <a name="mm_mcinotify-message"></a><span data-ttu-id="c9789-105">MM- \_ mcinotifismeldung</span><span class="sxs-lookup"><span data-stu-id="c9789-105">MM\_MCINOTIFY message</span></span>

<span data-ttu-id="c9789-106">Die Meldung **mm \_ mcinotify** benachrichtigt eine Anwendung, dass ein MCI-Gerät einen Vorgang abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="c9789-106">The **MM\_MCINOTIFY** message notifies an application that an MCI device has completed an operation.</span></span> <span data-ttu-id="c9789-107">MCI-Geräte senden diese Nachricht nur, wenn das MCI- \_ Benachrichtigungs Kennzeichen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c9789-107">MCI devices send this message only when the MCI\_NOTIFY flag is used.</span></span>


```C++
MM_MCINOTIFY 
wParam = (WPARAM) wFlags 
lParam = (LONG) lDevID
```



## <a name="parameters"></a><span data-ttu-id="c9789-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9789-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9789-109"><span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*</span><span class="sxs-lookup"><span data-stu-id="c9789-109"><span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c9789-110">Der Grund für die Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="c9789-110">Reason for the notification.</span></span> <span data-ttu-id="c9789-111">Die folgenden Werte sind definiert:</span><span class="sxs-lookup"><span data-stu-id="c9789-111">The following values are defined:</span></span>



| <span data-ttu-id="c9789-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c9789-112">Requirement</span></span> | <span data-ttu-id="c9789-113">Wert</span><span class="sxs-lookup"><span data-stu-id="c9789-113">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9789-114">MCI- \_ Benachrichtigung \_ abgebrochen</span><span class="sxs-lookup"><span data-stu-id="c9789-114">MCI\_NOTIFY\_ABORTED</span></span>    | <span data-ttu-id="c9789-115">Das Gerät hat einen Befehl empfangen, der verhindert hat, dass die aktuellen Bedingungen zum Initiieren der Rückruffunktion erfüllt werden.</span><span class="sxs-lookup"><span data-stu-id="c9789-115">The device received a command that prevented the current conditions for initiating the callback function from being met.</span></span> <span data-ttu-id="c9789-116">Wenn ein neuer Befehl den aktuellen Befehl unterbricht und auch eine Benachrichtigung anfordert, sendet das Gerät nur diese Nachricht, nicht jedoch die \_ MCI-Benachrichtigung. \_</span><span class="sxs-lookup"><span data-stu-id="c9789-116">If a new command interrupts the current command and it also requests notification, the device sends this message only and not MCI\_NOTIFY\_SUPERSEDED</span></span> |
| <span data-ttu-id="c9789-117">MCI- \_ Benachrichtigungs \_ Fehler</span><span class="sxs-lookup"><span data-stu-id="c9789-117">MCI\_NOTIFY\_FAILURE</span></span>    | <span data-ttu-id="c9789-118">Gerätefehler beim Ausführen des Befehls durch das Gerät.</span><span class="sxs-lookup"><span data-stu-id="c9789-118">A device error occurred while the device was executing the command.</span></span>                                                                                                                                                                                                            |
| <span data-ttu-id="c9789-119">MCI- \_ Benachrichtigung \_ erfolgreich</span><span class="sxs-lookup"><span data-stu-id="c9789-119">MCI\_NOTIFY\_SUCCESSFUL</span></span> | <span data-ttu-id="c9789-120">Die Bedingungen, die die Rückruffunktion initiieren, wurden erfüllt.</span><span class="sxs-lookup"><span data-stu-id="c9789-120">The conditions initiating the callback function have been met.</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="c9789-121">MCI- \_ Benachrichtigung \_ abgelöst</span><span class="sxs-lookup"><span data-stu-id="c9789-121">MCI\_NOTIFY\_SUPERSEDED</span></span> | <span data-ttu-id="c9789-122">Das Gerät hat einen weiteren Befehl mit dem festgelegten Flag "Benachrichtigen" erhalten, und die aktuellen Bedingungen zum Initiieren der Rückruffunktion wurden abgelöst.</span><span class="sxs-lookup"><span data-stu-id="c9789-122">The device received another command with the "notify" flag set and the current conditions for initiating the callback function have been superseded.</span></span>                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="c9789-123"><span id="lDevID"></span><span id="ldevid"></span><span id="LDEVID"></span>*ldevid*</span><span class="sxs-lookup"><span data-stu-id="c9789-123"><span id="lDevID"></span><span id="ldevid"></span><span id="LDEVID"></span>*lDevID*</span></span>
</dt> <dd>

<span data-ttu-id="c9789-124">Der Bezeichner des Geräts, das die Rückruffunktion initiiert.</span><span class="sxs-lookup"><span data-stu-id="c9789-124">Identifier of the device initiating the callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9789-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c9789-125">Return Value</span></span>

<span data-ttu-id="c9789-126">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="c9789-126">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9789-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c9789-127">Remarks</span></span>

<span data-ttu-id="c9789-128">Weitere Informationen zum MCI- \_ Benachrichtigungs Kennzeichen finden Sie [unter dem notify-Flag](the-notify-flag.md).</span><span class="sxs-lookup"><span data-stu-id="c9789-128">For more information about the MCI\_NOTIFY flag, see [The Notify Flag](the-notify-flag.md).</span></span>

<span data-ttu-id="c9789-129">Ein Gerät gibt das MCI \_ - \_ Flag zum Benachrichtigen von Benachrichtigungen mit **mm \_ mcinotify** zurück, wenn die Aktion für einen Befehl abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="c9789-129">A device returns the MCI\_NOTIFY\_SUCCESSFUL flag with **MM\_MCINOTIFY** when the action for a command finishes.</span></span> <span data-ttu-id="c9789-130">Beispielsweise verwendet ein CD-Audiogerät dieses Flag für die Benachrichtigung für den [**Wiedergabe**](play.md) Befehl ( [**MCI \_ Play**](mci-play.md)), wenn die Wiedergabe des Geräts abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="c9789-130">For example, a CD audio device uses this flag for notification for the [**play**](play.md) ( [**MCI\_PLAY**](mci-play.md)) command when the device finishes playing.</span></span> <span data-ttu-id="c9789-131">Der **Wiedergabe** Befehl ist nur erfolgreich, wenn er die angegebene Endposition erreicht oder das Ende des Mediums erreicht.</span><span class="sxs-lookup"><span data-stu-id="c9789-131">The **play** command is successful only when it reaches the specified end position or reaches the end of the media.</span></span> <span data-ttu-id="c9789-132">Auf ähnliche Weise wird die MCI-Benachrichtigung durch die Befehle [**Seek**](seek.md) ( [**MCI \_ Seek**](mci-seek.md)) und [**Record**](record.md) ( [**MCI- \_ Datensatz**](mci-record.md)) nicht erfolgreich zurückgegeben, \_ \_ bis die angegebene Endposition erreicht oder das Ende des Mediums erreicht wurde.</span><span class="sxs-lookup"><span data-stu-id="c9789-132">Similarly, the [**seek**](seek.md) ( [**MCI\_SEEK**](mci-seek.md)) and [**record**](record.md) ( [**MCI\_RECORD**](mci-record.md)) commands do not return MCI\_NOTIFY\_SUCCESSFUL until they reach the specified end position or reach the end of the media.</span></span>

<span data-ttu-id="c9789-133">Ein Gerät gibt das MCI \_ - \_ Flag zum Benachrichtigen von Benachrichtigungen mit mm- **\_ mcinotifinur** dann zurück, wenn es einen Befehl empfängt, der verhindert, dass die Benachrichtigungs Bedingungen erfüllt werden.</span><span class="sxs-lookup"><span data-stu-id="c9789-133">A device returns the MCI\_NOTIFY\_ABORTED flag with **MM\_MCINOTIFY** only when it receives a command that prevents it from meeting the notification conditions.</span></span> <span data-ttu-id="c9789-134">Beispielsweise würde der [**Wiedergabe**](play.md) Befehl die Benachrichtigung für einen vorherigen **Wiedergabe** Befehl nicht abbrechen, vorausgesetzt, dass der neue Befehl die Wiedergabe Richtung nicht ändert oder die Endposition ändert.</span><span class="sxs-lookup"><span data-stu-id="c9789-134">For example, the [**play**](play.md) command would not abort notification for a previous **play** command provided that the new command does not change the play direction or change the ending position.</span></span> <span data-ttu-id="c9789-135">Die [**Such**](seek.md) -und [**Daten Satz**](record.md) Befehle Verhalten sich ähnlich.</span><span class="sxs-lookup"><span data-stu-id="c9789-135">The [**seek**](seek.md) and [**record**](record.md) commands behave similarly.</span></span> <span data-ttu-id="c9789-136">MCI sendet auch keine MCI- \_ Benachrichtigung, \_ die abgebrochen wird, wenn die Wiedergabe oder Aufzeichnung mit dem Befehl [**Pause**](pause.md) ( [**MCI- \_ Pause**](mci-pause.md)) angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="c9789-136">MCI also does not send MCI\_NOTIFY\_ABORTED when playback or recording is paused with the [**pause**](pause.md) ( [**MCI\_PAUSE**](mci-pause.md)) command.</span></span> <span data-ttu-id="c9789-137">Durch das Senden des Befehls [**Resume**](resume.md) ( [**MCI \_ Resume**](mci-resume.md)) können die Rückruf Bedingungen weiterhin erfüllt werden.</span><span class="sxs-lookup"><span data-stu-id="c9789-137">Sending the [**resume**](resume.md) ( [**MCI\_RESUME**](mci-resume.md)) command allows them to continue to meet the callback conditions.</span></span>

<span data-ttu-id="c9789-138">Wenn Ihre Anwendung eine Benachrichtigung für einen Befehl anfordert, überprüfen Sie die Fehlerrückgabe der Funktionen [**mciSendString**](/previous-versions//dd757161(v=vs.85)) oder [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c9789-138">When your application requests notification for a command, check the error return of the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) or [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) functions.</span></span> <span data-ttu-id="c9789-139">Wenn diese Funktionen auf einen Fehler stoßen und einen Wert ungleich 0 (null) zurückgeben, wird von MCI keine Benachrichtigung für den Befehl festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c9789-139">If these functions encounter an error and return a nonzero value, MCI will not set notification for the command.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9789-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c9789-140">Requirements</span></span>



| <span data-ttu-id="c9789-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c9789-141">Requirement</span></span> | <span data-ttu-id="c9789-142">Wert</span><span class="sxs-lookup"><span data-stu-id="c9789-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9789-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c9789-143">Minimum supported client</span></span><br/> | <span data-ttu-id="c9789-144">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9789-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c9789-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c9789-145">Minimum supported server</span></span><br/> | <span data-ttu-id="c9789-146">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9789-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c9789-147">Header</span><span class="sxs-lookup"><span data-stu-id="c9789-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9789-148"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c9789-148"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9789-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9789-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9789-150">MCI</span><span class="sxs-lookup"><span data-stu-id="c9789-150">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c9789-151">MCI-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="c9789-151">MCI Messages</span></span>](mci-messages.md)
</dt> <dt>

[<span data-ttu-id="c9789-152">**Brechung**</span><span class="sxs-lookup"><span data-stu-id="c9789-152">**pause**</span></span>](pause.md)
</dt> <dt>

[<span data-ttu-id="c9789-153">**Theater**</span><span class="sxs-lookup"><span data-stu-id="c9789-153">**play**</span></span>](play.md)
</dt> <dt>

[<span data-ttu-id="c9789-154">**Aufnahme**</span><span class="sxs-lookup"><span data-stu-id="c9789-154">**record**</span></span>](record.md)
</dt> <dt>

[<span data-ttu-id="c9789-155">**zusetzen**</span><span class="sxs-lookup"><span data-stu-id="c9789-155">**resume**</span></span>](resume.md)
</dt> <dt>

[<span data-ttu-id="c9789-156">**einzuholen**</span><span class="sxs-lookup"><span data-stu-id="c9789-156">**seek**</span></span>](seek.md)
</dt> </dl>

 

