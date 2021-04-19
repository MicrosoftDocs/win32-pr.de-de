---
title: WINBIO_EVENT Struktur (winbio \_ types. h)
description: Enthält Statusinformationen, die an die Rückruf Routine gesendet werden, wenn ein Ereignis Hinweis ausgelöst wird.
ms.assetid: f46df7ff-8197-49cb-b1f8-4e7e3288e3df
keywords:
- WINBIO_EVENT Struktur Windows-Biometrieframework-API
- PWINBIO_EVENT Struktur Zeiger Windows-Biometrieframework API
topic_type:
- apiref
api_name:
- WINBIO_EVENT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75b6a8301ea5dab7d860e5bd7fb32c69277bad63
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346527"
---
# <a name="winbio_event-structure"></a><span data-ttu-id="fb30e-105">Winbio- \_ Ereignis Struktur</span><span class="sxs-lookup"><span data-stu-id="fb30e-105">WINBIO\_EVENT structure</span></span>

<span data-ttu-id="fb30e-106">Die **winbio- \_ Ereignis** Struktur enthält Statusinformationen, die an die Rückruf Routine gesendet werden, wenn ein Ereignis Hinweis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="fb30e-106">The **WINBIO\_EVENT** structure contains status information sent to the callback routine when an event notice is raised.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb30e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb30e-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EVENT {
  WINBIO_EVENT_TYPE Type;
  union {
    struct {
      WINBIO_UNIT_ID       UnitId;
      WINBIO_REJECT_DETAIL RejectDetail;
    } Unclaimed;
    struct {
      WINBIO_UNIT_ID           UnitId;
      WINBIO_IDENTITY          Identity;
      WINBIO_BIOMETRIC_SUBTYPE SubFactor;
      WINBIO_REJECT_DETAIL     RejectDetail;
    } UnclaimedIdentify;
    struct {
      HRESULT ErrorCode;
    } Error;
  } Parameters;
} WINBIO_EVENT, *PWINBIO_EVENT;
```



## <a name="members"></a><span data-ttu-id="fb30e-108">Member</span><span class="sxs-lookup"><span data-stu-id="fb30e-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="fb30e-109">**Type**</span><span class="sxs-lookup"><span data-stu-id="fb30e-109">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="fb30e-110">Ein-Wert, der den Typ des abgelegten Ereignis Hinweises des Dienstanbieters angibt.</span><span class="sxs-lookup"><span data-stu-id="fb30e-110">A value that specifies the type of service provider event notice raised.</span></span> <span data-ttu-id="fb30e-111">Der einzige derzeit unterstützte Anbieter ist der Fingerabdrucksensor.</span><span class="sxs-lookup"><span data-stu-id="fb30e-111">The only provider currently supported is the fingerprint sensor.</span></span> <span data-ttu-id="fb30e-112">Dieser Sensor unterstützt die folgenden Flags.</span><span class="sxs-lookup"><span data-stu-id="fb30e-112">This sensor supports the following flags.</span></span>

<dl> <dt>

<span data-ttu-id="fb30e-113"><span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span>**Winbio \_ Event \_ FP \_** wurde nicht beansprucht (der Sensor hat einen Fingerring erkannt, der nicht von der Anwendung angefordert wurde, oder das Fenster, das den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="fb30e-113"><span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span>**WINBIO\_EVENT\_FP\_UNCLAIMED** (The sensor detected a finger swipe that was not requested by the application or by the window that currently has focus.</span></span> <span data-ttu-id="fb30e-114">Der Windows-Biometrieframework Ruft die Rückruffunktion auf, um anzugeben, dass ein Finger schwenken aufgetreten ist, aber nicht versucht, den Fingerabdruck zu identifizieren.)</span><span class="sxs-lookup"><span data-stu-id="fb30e-114">The Windows Biometric Framework calls into your callback function to indicate that a finger swipe has occurred but does not try to identify the fingerprint.)</span></span>
</dt> <dt>

<span data-ttu-id="fb30e-115"><span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span>**Winbio \_ Das Ereignis FP hat eine nicht \_ \_ beanspruchte \_ Identifizierung** (der Sensor hat einen Fingerring erkannt, der nicht von der Anwendung angefordert wurde, oder das Fenster, das gerade den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="fb30e-115"><span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span>**WINBIO\_EVENT\_FP\_UNCLAIMED\_IDENTIFY** (The sensor detected a finger swipe that was not requested by the application or by the window that currently has focus.</span></span> <span data-ttu-id="fb30e-116">Der Windows-Biometrieframework versucht, den Fingerabdruck zu identifizieren, und übergibt das Ergebnis dieses Prozesses an Ihre Rückruffunktion.)</span><span class="sxs-lookup"><span data-stu-id="fb30e-116">The Windows Biometric Framework attempts to identify the fingerprint and passes the result of that process to your callback function.)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="fb30e-117">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="fb30e-117">**Parameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb30e-118">**Genommene**</span><span class="sxs-lookup"><span data-stu-id="fb30e-118">**Unclaimed**</span></span>
</dt> <dd>

<span data-ttu-id="fb30e-119">Struktur, die für die biometrische Beispiel Erfassung zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="fb30e-119">Structure returned for biometric sample capture.</span></span>

<dl> <dt>

<span data-ttu-id="fb30e-120">**Unitid**</span><span class="sxs-lookup"><span data-stu-id="fb30e-120">**UnitId**</span></span>
</dt> <dd>

<span data-ttu-id="fb30e-121">Die biometrische Einheit, die das Beispiel generiert hat.</span><span class="sxs-lookup"><span data-stu-id="fb30e-121">The biometric unit that generated the sample.</span></span>

</dd> <dt>

<span data-ttu-id="fb30e-122">**Rejectdetail**</span><span class="sxs-lookup"><span data-stu-id="fb30e-122">**RejectDetail**</span></span>
</dt> <dd>

<span data-ttu-id="fb30e-123">Ein **ulong** -Wert, der zusätzliche Informationen zu Fehlern bei der Erfassung eines biometrischen Beispiels enthält.</span><span class="sxs-lookup"><span data-stu-id="fb30e-123">A **ULONG** value that contains additional information regarding failure to capture a biometric sample.</span></span> <span data-ttu-id="fb30e-124">Wenn eine Erfassung erfolgreich war, wird dieser Parameter auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fb30e-124">If a capture succeeded, this parameter is set to zero.</span></span> <span data-ttu-id="fb30e-125">Die folgenden Werte sind für die Fingerabdruck Erfassung definiert:</span><span class="sxs-lookup"><span data-stu-id="fb30e-125">The following values are defined for fingerprint capture:</span></span>

-   <span data-ttu-id="fb30e-126">winbio \_ FP \_ zu \_ hoch</span><span class="sxs-lookup"><span data-stu-id="fb30e-126">WINBIO\_FP\_TOO\_HIGH</span></span>
-   <span data-ttu-id="fb30e-127">winbio \_ FP \_ zu \_ niedrig</span><span class="sxs-lookup"><span data-stu-id="fb30e-127">WINBIO\_FP\_TOO\_LOW</span></span>
-   <span data-ttu-id="fb30e-128">winbio \_ FP \_ zu \_ Links</span><span class="sxs-lookup"><span data-stu-id="fb30e-128">WINBIO\_FP\_TOO\_LEFT</span></span>
-   <span data-ttu-id="fb30e-129">winbio \_ FP \_ zu \_ Recht</span><span class="sxs-lookup"><span data-stu-id="fb30e-129">WINBIO\_FP\_TOO\_RIGHT</span></span>
-   <span data-ttu-id="fb30e-130">winbio \_ FP \_ zu \_ schnell</span><span class="sxs-lookup"><span data-stu-id="fb30e-130">WINBIO\_FP\_TOO\_FAST</span></span>
-   <span data-ttu-id="fb30e-131">winbio \_ FP \_ zu \_ langsam</span><span class="sxs-lookup"><span data-stu-id="fb30e-131">WINBIO\_FP\_TOO\_SLOW</span></span>
-   <span data-ttu-id="fb30e-132">winbio \_ fp, \_ schlechte \_ Qualität</span><span class="sxs-lookup"><span data-stu-id="fb30e-132">WINBIO\_FP\_POOR\_QUALITY</span></span>
-   <span data-ttu-id="fb30e-133">winbio \_ FP \_ zu \_ verzerrt</span><span class="sxs-lookup"><span data-stu-id="fb30e-133">WINBIO\_FP\_TOO\_SKEWED</span></span>
-   <span data-ttu-id="fb30e-134">winbio \_ FP \_ zu \_ kurz</span><span class="sxs-lookup"><span data-stu-id="fb30e-134">WINBIO\_FP\_TOO\_SHORT</span></span>
-   <span data-ttu-id="fb30e-135">winbio \_ FP- \_ Merge- \_ Fehler</span><span class="sxs-lookup"><span data-stu-id="fb30e-135">WINBIO\_FP\_MERGE\_FAILURE</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="fb30e-136">**Unclaimedidentifizieren**</span><span class="sxs-lookup"><span data-stu-id="fb30e-136">**UnclaimedIdentify**</span></span>
</dt> <dd>

<span data-ttu-id="fb30e-137">Struktur, die für die biometrische Erfassung und Identifizierung zurückgegeben wird</span><span class="sxs-lookup"><span data-stu-id="fb30e-137">Structure returned for biometric capture and identification.</span></span> <span data-ttu-id="fb30e-138">Identifikation bestimmt, ob eine Stichprobe mit einer vorhandenen biometrischen Vorlage verknüpft werden kann.</span><span class="sxs-lookup"><span data-stu-id="fb30e-138">Identification determines whether a sample can be associated with an existing biometric template.</span></span>

<dl> <dt>

<span data-ttu-id="fb30e-139">**Unitid**</span><span class="sxs-lookup"><span data-stu-id="fb30e-139">**UnitId**</span></span>
</dt> <dd>

<span data-ttu-id="fb30e-140">Die biometrische Einheit, die das Beispiel generiert hat.</span><span class="sxs-lookup"><span data-stu-id="fb30e-140">The biometric unit that generated the sample.</span></span>

</dd> <dt>

<span data-ttu-id="fb30e-141">**Identität**</span><span class="sxs-lookup"><span data-stu-id="fb30e-141">**Identity**</span></span>
</dt> <dd>

<span data-ttu-id="fb30e-142">Eine [**winbio- \_ Identitäts**](winbio-identity.md) Struktur, die die GUID oder SID des Benutzers enthält, der das biometrische Beispiel bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="fb30e-142">A [**WINBIO\_IDENTITY**](winbio-identity.md) structure that contains the GUID or SID of the user providing the biometric sample.</span></span>

</dd> <dt>

<span data-ttu-id="fb30e-143">**Teilfaktor**</span><span class="sxs-lookup"><span data-stu-id="fb30e-143">**SubFactor**</span></span>
</dt> <dd>

<span data-ttu-id="fb30e-144">Ein [**untergeordneter winbio- \_ \_ Untertyp**](winbio-biometric-subtype-constants.md) Wert, der den einem biometrischen Beispiel zugeordneten unter Faktor angibt.</span><span class="sxs-lookup"><span data-stu-id="fb30e-144">A [**WINBIO\_BIOMETRIC\_SUBTYPE**](winbio-biometric-subtype-constants.md) value that specifies the sub-factor associated with a biometric sample.</span></span> <span data-ttu-id="fb30e-145">Der Windows-Biometrieframework (WBF) unterstützt derzeit nur die Fingerabdruck Erfassung und verwendet die folgenden Konstanten, um Untertyp Informationen darzustellen.</span><span class="sxs-lookup"><span data-stu-id="fb30e-145">The Windows Biometric Framework (WBF) currently supports only fingerprint capture and uses the following constants to represent sub-type information.</span></span>

-   <span data-ttu-id="fb30e-146">Winbio \_ ANSI \_ 381 Torys \_ \_ unbekannt</span><span class="sxs-lookup"><span data-stu-id="fb30e-146">WINBIO\_ANSI\_381\_POS\_UNKNOWN</span></span>
-   <span data-ttu-id="fb30e-147">Winbio \_ ANSI \_ 381 \_ POS, \_ RH \_ Thumb</span><span class="sxs-lookup"><span data-stu-id="fb30e-147">WINBIO\_ANSI\_381\_POS\_RH\_THUMB</span></span>
-   <span data-ttu-id="fb30e-148">Winbio \_ ANSI \_ 381 POS-Zeige- \_ \_ \_ \_ Finger</span><span class="sxs-lookup"><span data-stu-id="fb30e-148">WINBIO\_ANSI\_381\_POS\_RH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="fb30e-149">Winbio \_ ANSI \_ 381 \_ Torpo- \_ \_ \_ Mittelfinger</span><span class="sxs-lookup"><span data-stu-id="fb30e-149">WINBIO\_ANSI\_381\_POS\_RH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="fb30e-150">Winbio \_ ANSI \_ 381 \_ POS, \_ RH- \_ Klingel \_ Finger</span><span class="sxs-lookup"><span data-stu-id="fb30e-150">WINBIO\_ANSI\_381\_POS\_RH\_RING\_FINGER</span></span>
-   <span data-ttu-id="fb30e-151">Winbio \_ ANSI \_ 381 Torys \_ \_ RH \_ Little \_ Finger</span><span class="sxs-lookup"><span data-stu-id="fb30e-151">WINBIO\_ANSI\_381\_POS\_RH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="fb30e-152">Winbio \_ ANSI \_ 381 \_ POS \_ LH \_ Thumb</span><span class="sxs-lookup"><span data-stu-id="fb30e-152">WINBIO\_ANSI\_381\_POS\_LH\_THUMB</span></span>
-   <span data-ttu-id="fb30e-153">Winbio \_ ANSI \_ 381 Torys \_ \_ LH \_ Index \_ Finger</span><span class="sxs-lookup"><span data-stu-id="fb30e-153">WINBIO\_ANSI\_381\_POS\_LH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="fb30e-154">Winbio \_ ANSI \_ 381 \_ POS \_ - \_ Mittel \_ Fingerabdruck</span><span class="sxs-lookup"><span data-stu-id="fb30e-154">WINBIO\_ANSI\_381\_POS\_LH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="fb30e-155">Winbio \_ ANSI \_ 381 Torys LH- \_ \_ \_ Klingel \_ Finger</span><span class="sxs-lookup"><span data-stu-id="fb30e-155">WINBIO\_ANSI\_381\_POS\_LH\_RING\_FINGER</span></span>
-   <span data-ttu-id="fb30e-156">Winbio \_ ANSI \_ 381 Torys \_ \_ LH \_ wenig \_ Finger</span><span class="sxs-lookup"><span data-stu-id="fb30e-156">WINBIO\_ANSI\_381\_POS\_LH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="fb30e-157">Winbio \_ ANSI 381 Torys mit \_ \_ \_ \_ vier \_ Fingern</span><span class="sxs-lookup"><span data-stu-id="fb30e-157">WINBIO\_ANSI\_381\_POS\_RH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="fb30e-158">Winbio \_ ANSI 381 Torys mit \_ \_ \_ \_ vier \_ Fingern</span><span class="sxs-lookup"><span data-stu-id="fb30e-158">WINBIO\_ANSI\_381\_POS\_LH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="fb30e-159">Winbio \_ ANSI \_ 381 \_ POS \_ zwei \_ Daumen</span><span class="sxs-lookup"><span data-stu-id="fb30e-159">WINBIO\_ANSI\_381\_POS\_TWO\_THUMBS</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="fb30e-160">Versuchen Sie nicht, den Wert zu überprüfen, der für den *subfaktorwert* angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="fb30e-160">Do not attempt to validate the value supplied for the *SubFactor* value.</span></span> <span data-ttu-id="fb30e-161">Der Windows-Biometrie-Dienst überprüft den angegebenen Wert vor der Übergabe an Ihre Implementierung.</span><span class="sxs-lookup"><span data-stu-id="fb30e-161">The Windows Biometrics Service will validate the supplied value before passing it through to your implementation.</span></span> <span data-ttu-id="fb30e-162">Wenn der Wert " **winbio \_ SubType \_ No \_ Information** " oder " **winbio \_ SubType \_ any**" lautet, überprüfen Sie ggf. ggf.</span><span class="sxs-lookup"><span data-stu-id="fb30e-162">If the value is **WINBIO\_SUBTYPE\_NO\_INFORMATION** or **WINBIO\_SUBTYPE\_ANY**, then validate where appropriate.</span></span>

 

</dd> <dt>

<span data-ttu-id="fb30e-163">**Rejectdetail**</span><span class="sxs-lookup"><span data-stu-id="fb30e-163">**RejectDetail**</span></span>
</dt> <dd>

<span data-ttu-id="fb30e-164">Ein **ulong** -Wert, der zusätzliche Informationen über den Fehler beim Erfassen eines biometrischen Beispiels enthält.</span><span class="sxs-lookup"><span data-stu-id="fb30e-164">A **ULONG** value that contains additional information about the failure to capture a biometric sample.</span></span> <span data-ttu-id="fb30e-165">Wenn die Erfassung erfolgreich war, wird dieser Parameter auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fb30e-165">If the capture succeeded, this parameter is set to zero.</span></span> <span data-ttu-id="fb30e-166">Die folgenden Werte sind für die Fingerabdruck Erfassung definiert:</span><span class="sxs-lookup"><span data-stu-id="fb30e-166">The following values are defined for fingerprint capture:</span></span>

-   <span data-ttu-id="fb30e-167">winbio \_ FP \_ zu \_ hoch</span><span class="sxs-lookup"><span data-stu-id="fb30e-167">WINBIO\_FP\_TOO\_HIGH</span></span>
-   <span data-ttu-id="fb30e-168">winbio \_ FP \_ zu \_ niedrig</span><span class="sxs-lookup"><span data-stu-id="fb30e-168">WINBIO\_FP\_TOO\_LOW</span></span>
-   <span data-ttu-id="fb30e-169">winbio \_ FP \_ zu \_ Links</span><span class="sxs-lookup"><span data-stu-id="fb30e-169">WINBIO\_FP\_TOO\_LEFT</span></span>
-   <span data-ttu-id="fb30e-170">winbio \_ FP \_ zu \_ Recht</span><span class="sxs-lookup"><span data-stu-id="fb30e-170">WINBIO\_FP\_TOO\_RIGHT</span></span>
-   <span data-ttu-id="fb30e-171">winbio \_ FP \_ zu \_ schnell</span><span class="sxs-lookup"><span data-stu-id="fb30e-171">WINBIO\_FP\_TOO\_FAST</span></span>
-   <span data-ttu-id="fb30e-172">winbio \_ FP \_ zu \_ langsam</span><span class="sxs-lookup"><span data-stu-id="fb30e-172">WINBIO\_FP\_TOO\_SLOW</span></span>
-   <span data-ttu-id="fb30e-173">winbio \_ fp, \_ schlechte \_ Qualität</span><span class="sxs-lookup"><span data-stu-id="fb30e-173">WINBIO\_FP\_POOR\_QUALITY</span></span>
-   <span data-ttu-id="fb30e-174">winbio \_ FP \_ zu \_ verzerrt</span><span class="sxs-lookup"><span data-stu-id="fb30e-174">WINBIO\_FP\_TOO\_SKEWED</span></span>
-   <span data-ttu-id="fb30e-175">winbio \_ FP \_ zu \_ kurz</span><span class="sxs-lookup"><span data-stu-id="fb30e-175">WINBIO\_FP\_TOO\_SHORT</span></span>
-   <span data-ttu-id="fb30e-176">winbio \_ FP- \_ Merge- \_ Fehler</span><span class="sxs-lookup"><span data-stu-id="fb30e-176">WINBIO\_FP\_MERGE\_FAILURE</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="fb30e-177">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="fb30e-177">**Error**</span></span>
</dt> <dd>

<span data-ttu-id="fb30e-178">-Struktur, die den Erfolg oder Misserfolg des Vorgangs angibt, der überwacht wird.</span><span class="sxs-lookup"><span data-stu-id="fb30e-178">Structure that identifies the success or failure of the operation being monitored.</span></span>

<dl> <dt>

<span data-ttu-id="fb30e-179">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="fb30e-179">**ErrorCode**</span></span>
</dt> <dd>

<span data-ttu-id="fb30e-180">**HRESULT** -Wert, der S \_ OK enthält, oder ein Fehlercode, der aus Berechnungen resultiert, die vom Windows-Biometrieframework ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="fb30e-180">**HRESULT** value that contains S\_OK or an error code that resulted from computations performed by the Windows Biometric Framework.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fb30e-181">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb30e-181">Remarks</span></span>

<span data-ttu-id="fb30e-182">Rufen Sie die [**winbioregistereventmonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) -Funktion auf, um eine Rückruf Routine zu registrieren, um Ereignis Benachrichtigungen vom Windows-Biometrieframework zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="fb30e-182">Call the [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) function to register a callback routine to receive event notifications from the Windows Biometric Framework.</span></span> <span data-ttu-id="fb30e-183">Der Rückruf ist eine benutzerdefinierte Funktion, die Sie für Ihre Anwendung definieren müssen.</span><span class="sxs-lookup"><span data-stu-id="fb30e-183">The callback is a custom function that you must define for your application.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb30e-184">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb30e-184">Requirements</span></span>



| <span data-ttu-id="fb30e-185">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb30e-185">Requirement</span></span> | <span data-ttu-id="fb30e-186">Wert</span><span class="sxs-lookup"><span data-stu-id="fb30e-186">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb30e-187">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fb30e-187">Minimum supported client</span></span><br/> | <span data-ttu-id="fb30e-188">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fb30e-188">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="fb30e-189">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fb30e-189">Minimum supported server</span></span><br/> | <span data-ttu-id="fb30e-190">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fb30e-190">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="fb30e-191">Header</span><span class="sxs-lookup"><span data-stu-id="fb30e-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb30e-192"><dt>Winbio \_ types. h (Include winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fb30e-192"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb30e-193">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb30e-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb30e-194">Client Anwendungs Strukturen</span><span class="sxs-lookup"><span data-stu-id="fb30e-194">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="fb30e-195">**Winbioregistereventmonitor**</span><span class="sxs-lookup"><span data-stu-id="fb30e-195">**WinBioRegisterEventMonitor**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor)
</dt> </dl>

 

 





