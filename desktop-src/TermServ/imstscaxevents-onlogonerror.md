---
title: Imstscaxevents onlogonerror-Methode
description: Wird aufgerufen, wenn ein Anmeldefehler oder ein anderes Logon-Ereignis auftritt.
ms.assetid: 5af9656b-f99b-4535-ab83-6ecc9bc41808
ms.tgt_platform: multiple
keywords:
- Onlogonerror-Methode Remotedesktopdienste
- Onlogonerror-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onlogonerror-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnLogonError
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f45fe23c992f14a421c00a4feefd9c4ed95aff07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742120"
---
# <a name="imstscaxeventsonlogonerror-method"></a><span data-ttu-id="a14c7-106">Imstscaxevents:: onlogonerror-Methode</span><span class="sxs-lookup"><span data-stu-id="a14c7-106">IMsTscAxEvents::OnLogonError method</span></span>

<span data-ttu-id="a14c7-107">Wird aufgerufen, wenn ein Anmeldefehler oder ein anderes Logon-Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="a14c7-107">Called when a logon error or other logon event occurs.</span></span>

## <a name="syntax"></a><span data-ttu-id="a14c7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a14c7-108">Syntax</span></span>


```C++
void OnLogonError(
  [in] LONG lError
);
```



## <a name="parameters"></a><span data-ttu-id="a14c7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a14c7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a14c7-110">*lerror* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a14c7-110">*lError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a14c7-111">Der Fehlercode für die Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="a14c7-111">The logon error code.</span></span> <span data-ttu-id="a14c7-112">Diese Liste der Codes ist nicht vollständig.</span><span class="sxs-lookup"><span data-stu-id="a14c7-112">This list of codes is not exhaustive.</span></span>

<dt>

<span id="ARBITRATION_CODE_BUMP_OPTIONS"></span><span id="arbitration_code_bump_options"></span>

<span data-ttu-id="a14c7-113"><span id="ARBITRATION_CODE_BUMP_OPTIONS"></span><span id="arbitration_code_bump_options"></span>**Schiedsgerichtsbarkeit \_ \_ \_ Optionen für Code Bump** (-5 (0xfffffffb))</span><span class="sxs-lookup"><span data-stu-id="a14c7-113"><span id="ARBITRATION_CODE_BUMP_OPTIONS"></span><span id="arbitration_code_bump_options"></span>**ARBITRATION\_CODE\_BUMP\_OPTIONS** (-5 (0xFFFFFFFB))</span></span>


</dt> <dd>

<span data-ttu-id="a14c7-114">Winlogon zeigt das Dialogfeld **Sitzungs** Konflikte an.</span><span class="sxs-lookup"><span data-stu-id="a14c7-114">Winlogon is displaying the **Session Contention** dialog box.</span></span>

</dd> <dt>

<span id="ARBITRATION_CODE_CONTINUE_LOGON"></span><span id="arbitration_code_continue_logon"></span>

<span data-ttu-id="a14c7-115"><span id="ARBITRATION_CODE_CONTINUE_LOGON"></span><span id="arbitration_code_continue_logon"></span>**Schiedsgerichtsbarkeit \_ Code \_ Continue- \_ Anmeldung** (-2 (0xFFFFFFFE))</span><span class="sxs-lookup"><span data-stu-id="a14c7-115"><span id="ARBITRATION_CODE_CONTINUE_LOGON"></span><span id="arbitration_code_continue_logon"></span>**ARBITRATION\_CODE\_CONTINUE\_LOGON** (-2 (0xFFFFFFFE))</span></span>


</dt> <dd>

<span data-ttu-id="a14c7-116">Die Windows-Anmeldung wird mit dem Anmeldevorgang fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="a14c7-116">Winlogon is continuing with the logon process.</span></span>

</dd> <dt>

<span id="ARBITRATION_CODE_CONTINUE_TERMINATE"></span><span id="arbitration_code_continue_terminate"></span>

<span data-ttu-id="a14c7-117"><span id="ARBITRATION_CODE_CONTINUE_TERMINATE"></span><span id="arbitration_code_continue_terminate"></span>**Schiedsgerichtsbarkeit \_ Code \_ Continue \_ Beenden** (-3 (0xfffffffd))</span><span class="sxs-lookup"><span data-stu-id="a14c7-117"><span id="ARBITRATION_CODE_CONTINUE_TERMINATE"></span><span id="arbitration_code_continue_terminate"></span>**ARBITRATION\_CODE\_CONTINUE\_TERMINATE** (-3 (0xFFFFFFFD))</span></span>


</dt> <dd>

<span data-ttu-id="a14c7-118">Winlogon wird im Hintergrund beendet.</span><span class="sxs-lookup"><span data-stu-id="a14c7-118">Winlogon is ending silently.</span></span>

</dd> <dt>

<span id="ARBITRATION_CODE_NOPERM_DIALOG"></span><span id="arbitration_code_noperm_dialog"></span>

<span data-ttu-id="a14c7-119"><span id="ARBITRATION_CODE_NOPERM_DIALOG"></span><span id="arbitration_code_noperm_dialog"></span>**Schiedsgerichtsbarkeit \_ Dialog Feld "Code \_ noperm \_** " (-6 (0xfffffffa))</span><span class="sxs-lookup"><span data-stu-id="a14c7-119"><span id="ARBITRATION_CODE_NOPERM_DIALOG"></span><span id="arbitration_code_noperm_dialog"></span>**ARBITRATION\_CODE\_NOPERM\_DIALOG** (-6 (0xFFFFFFFA))</span></span>


</dt> <dd>

<span data-ttu-id="a14c7-120">Winlogon zeigt das Dialogfeld **keine Berechtigungen** an.</span><span class="sxs-lookup"><span data-stu-id="a14c7-120">Winlogon is displaying the **No Permissions** dialog box.</span></span>

</dd> <dt>

<span id="ARBITRATION_CODE_REFUSED_DIALOG"></span><span id="arbitration_code_refused_dialog"></span>

<span data-ttu-id="a14c7-121"><span id="ARBITRATION_CODE_REFUSED_DIALOG"></span><span id="arbitration_code_refused_dialog"></span>**Schiedsgerichtsbarkeit \_ \_ \_ Dialog Feld "Code verweigert** " (-7 (0xfffffff9))</span><span class="sxs-lookup"><span data-stu-id="a14c7-121"><span id="ARBITRATION_CODE_REFUSED_DIALOG"></span><span id="arbitration_code_refused_dialog"></span>**ARBITRATION\_CODE\_REFUSED\_DIALOG** (-7 (0xFFFFFFF9))</span></span>


</dt> <dd>

<span data-ttu-id="a14c7-122">Winlogon zeigt das Dialogfeld "Verbindung **trennen** " an.</span><span class="sxs-lookup"><span data-stu-id="a14c7-122">Winlogon is displaying the **Disconnect Refused** dialog box.</span></span>

</dd> <dt>

<span id="ARBITRATION_CODE_RECONN_OPTIONS"></span><span id="arbitration_code_reconn_options"></span>

<span data-ttu-id="a14c7-123"><span id="ARBITRATION_CODE_RECONN_OPTIONS"></span><span id="arbitration_code_reconn_options"></span>**Schiedsgerichtsbarkeit \_ \_ \_ Optionen** für die Code Wiedergabe (-4 (0xfffffffc))</span><span class="sxs-lookup"><span data-stu-id="a14c7-123"><span id="ARBITRATION_CODE_RECONN_OPTIONS"></span><span id="arbitration_code_reconn_options"></span>**ARBITRATION\_CODE\_RECONN\_OPTIONS** (-4 (0xFFFFFFFC))</span></span>


</dt> <dd>

<span data-ttu-id="a14c7-124">Winlogon zeigt das Dialogfeld **Verbindung wiederherstellen** an.</span><span class="sxs-lookup"><span data-stu-id="a14c7-124">Winlogon is displaying the **Reconnect** dialog box.</span></span>

</dd> <dt>

<span id="ERROR_CODE_ACCESS_DENIED"></span><span id="error_code_access_denied"></span>

<span data-ttu-id="a14c7-125"><span id="ERROR_CODE_ACCESS_DENIED"></span><span id="error_code_access_denied"></span>**Fehler \_ Code \_ Zugriff \_ verweigert** (-1 (0xFFFFFFFF))</span><span class="sxs-lookup"><span data-stu-id="a14c7-125"><span id="ERROR_CODE_ACCESS_DENIED"></span><span id="error_code_access_denied"></span>**ERROR\_CODE\_ACCESS\_DENIED** (-1 (0xFFFFFFFF))</span></span>


</dt> <dd>

<span data-ttu-id="a14c7-126">Dem Benutzer wurde der Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="a14c7-126">The user was denied access.</span></span>

</dd> <dt>

<span id="LOGON_FAILED_BAD_PASSWORD"></span><span id="logon_failed_bad_password"></span>

<span data-ttu-id="a14c7-127"><span id="LOGON_FAILED_BAD_PASSWORD"></span><span id="logon_failed_bad_password"></span>**Anmelden \_ Fehlerhaftes ungültiges \_ \_ Kennwort** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="a14c7-127"><span id="LOGON_FAILED_BAD_PASSWORD"></span><span id="logon_failed_bad_password"></span>**LOGON\_FAILED\_BAD\_PASSWORD** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="a14c7-128">Die Anmeldung ist fehlgeschlagen, da die Anmelde Informationen ungültig sind.</span><span class="sxs-lookup"><span data-stu-id="a14c7-128">The logon failed because the logon credentials are not valid.</span></span>

</dd> <dt>

<span id="LOGON_FAILED_OTHER"></span><span id="logon_failed_other"></span>

<span data-ttu-id="a14c7-129"><span id="LOGON_FAILED_OTHER"></span><span id="logon_failed_other"></span>**Anmelden \_ Fehler bei \_ anderen** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="a14c7-129"><span id="LOGON_FAILED_OTHER"></span><span id="logon_failed_other"></span>**LOGON\_FAILED\_OTHER** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="a14c7-130">Ein weiterer Anmelde-oder nach Anmeldefehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="a14c7-130">Another logon or post-logon error occurred.</span></span> <span data-ttu-id="a14c7-131">Der Remotedesktop-Client zeigt dem Benutzer einen Anmeldebildschirm an.</span><span class="sxs-lookup"><span data-stu-id="a14c7-131">The Remote Desktop client displays a logon screen to the user.</span></span>

</dd> <dt>

<span id="LOGON_FAILED_UPDATE_PASSWORD"></span><span id="logon_failed_update_password"></span>

<span data-ttu-id="a14c7-132"><span id="LOGON_FAILED_UPDATE_PASSWORD"></span><span id="logon_failed_update_password"></span>**Anmelden \_ Fehler beim \_ Aktualisieren des \_ Kennworts** (1 (0x1)).</span><span class="sxs-lookup"><span data-stu-id="a14c7-132"><span id="LOGON_FAILED_UPDATE_PASSWORD"></span><span id="logon_failed_update_password"></span>**LOGON\_FAILED\_UPDATE\_PASSWORD** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="a14c7-133">Das Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="a14c7-133">The password is expired.</span></span> <span data-ttu-id="a14c7-134">Der Benutzer muss sein Kennwort aktualisieren, um die Anmeldung fortsetzen zu können.</span><span class="sxs-lookup"><span data-stu-id="a14c7-134">The user must update their password to continue logging on.</span></span>

</dd> <dt>

<span id="LOGON_WARNING"></span><span id="logon_warning"></span>

<span data-ttu-id="a14c7-135"><span id="LOGON_WARNING"></span><span id="logon_warning"></span>**Anmelden \_ Warnung** (3 (0x3))</span><span class="sxs-lookup"><span data-stu-id="a14c7-135"><span id="LOGON_WARNING"></span><span id="logon_warning"></span>**LOGON\_WARNING** (3 (0x3))</span></span>


</dt> <dd>

<span data-ttu-id="a14c7-136">Der Remotedesktop Client zeigt ein Dialogfeld an, das wichtige Informationen für den Benutzer enthält.</span><span class="sxs-lookup"><span data-stu-id="a14c7-136">The Remote Desktop client displays a dialog box that contains important information for the user.</span></span>

</dd> <dt>

<span id="STATUS_ACCOUNT_RESTRICTION"></span><span id="status_account_restriction"></span>

<span data-ttu-id="a14c7-137"><span id="STATUS_ACCOUNT_RESTRICTION"></span><span id="status_account_restriction"></span>**Status \_ Konto \_ Einschränkung** (-1073741714 (0xc000006e))</span><span class="sxs-lookup"><span data-stu-id="a14c7-137"><span id="STATUS_ACCOUNT_RESTRICTION"></span><span id="status_account_restriction"></span>**STATUS\_ACCOUNT\_RESTRICTION** (-1073741714 (0xC000006E))</span></span>


</dt> <dd>

<span data-ttu-id="a14c7-138">Der Benutzername und die Authentifizierungsinformationen sind gültig, aber die Authentifizierung wurde aufgrund von Einschränkungen für das Benutzerkonto blockiert (z. b. Tages Beschränkungen).</span><span class="sxs-lookup"><span data-stu-id="a14c7-138">The user name and authentication information are valid, but authentication was blocked due to restrictions on the user account, such as time-of-day restrictions.</span></span>

</dd> <dt>

<span id="STATUS_LOGON_FAILURE"></span><span id="status_logon_failure"></span>

<span data-ttu-id="a14c7-139"><span id="STATUS_LOGON_FAILURE"></span><span id="status_logon_failure"></span>**Status \_ Anmelde \_ Fehler** (-1073741715 (0xc000006d))</span><span class="sxs-lookup"><span data-stu-id="a14c7-139"><span id="STATUS_LOGON_FAILURE"></span><span id="status_logon_failure"></span>**STATUS\_LOGON\_FAILURE** (-1073741715 (0xC000006D))</span></span>


</dt> <dd>

<span data-ttu-id="a14c7-140">Die versuchte Anmeldung ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="a14c7-140">The attempted logon is not valid.</span></span> <span data-ttu-id="a14c7-141">Dies liegt daran, dass entweder ein falscher Benutzername oder falsche Authentifizierungsinformationen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a14c7-141">This is due to either an incorrect user name or incorrect authentication information.</span></span>

</dd> <dt>

<span id="STATUS_PASSWORD_MUST_CHANGE"></span><span id="status_password_must_change"></span>

<span data-ttu-id="a14c7-142"><span id="STATUS_PASSWORD_MUST_CHANGE"></span><span id="status_password_must_change"></span>**Status \_ Kennwort \_ muss \_ geändert** werden (-1073741276 (0xc0000224))</span><span class="sxs-lookup"><span data-stu-id="a14c7-142"><span id="STATUS_PASSWORD_MUST_CHANGE"></span><span id="status_password_must_change"></span>**STATUS\_PASSWORD\_MUST\_CHANGE** (-1073741276 (0xC0000224))</span></span>


</dt> <dd>

<span data-ttu-id="a14c7-143">Das Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="a14c7-143">The password is expired.</span></span> <span data-ttu-id="a14c7-144">Der Benutzer muss sein Kennwort aktualisieren, um die Anmeldung fortsetzen zu können.</span><span class="sxs-lookup"><span data-stu-id="a14c7-144">The user must update their password to continue logging on.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a14c7-145">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a14c7-145">Return value</span></span>

<span data-ttu-id="a14c7-146">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a14c7-146">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a14c7-147">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a14c7-147">Remarks</span></span>

<span data-ttu-id="a14c7-148">Implementieren Sie diese Methode in der Ereignis Senke, um die Benachrichtigung zu erhalten, dass ein Anmeldefehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="a14c7-148">Implement this method in your event sink to receive notification that a logon error has occurred.</span></span>

<span data-ttu-id="a14c7-149">Diese Liste der Codes ist nicht vollständig.</span><span class="sxs-lookup"><span data-stu-id="a14c7-149">This list of codes is not exhaustive.</span></span>

## <a name="requirements"></a><span data-ttu-id="a14c7-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a14c7-150">Requirements</span></span>



| <span data-ttu-id="a14c7-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a14c7-151">Requirement</span></span> | <span data-ttu-id="a14c7-152">Wert</span><span class="sxs-lookup"><span data-stu-id="a14c7-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a14c7-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a14c7-153">Minimum supported client</span></span><br/> | <span data-ttu-id="a14c7-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a14c7-154">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a14c7-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a14c7-155">Minimum supported server</span></span><br/> | <span data-ttu-id="a14c7-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a14c7-156">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a14c7-157">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="a14c7-157">Type library</span></span><br/>             | <dl> <span data-ttu-id="a14c7-158"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a14c7-158"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a14c7-159">DLL</span><span class="sxs-lookup"><span data-stu-id="a14c7-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a14c7-160"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a14c7-160"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a14c7-161">IID</span><span class="sxs-lookup"><span data-stu-id="a14c7-161">IID</span></span><br/>                      | <span data-ttu-id="a14c7-162">Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.</span><span class="sxs-lookup"><span data-stu-id="a14c7-162">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="a14c7-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a14c7-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a14c7-164">**Imstscaxevents**</span><span class="sxs-lookup"><span data-stu-id="a14c7-164">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





