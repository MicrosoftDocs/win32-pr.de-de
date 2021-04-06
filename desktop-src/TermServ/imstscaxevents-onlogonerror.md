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
# <a name="imstscaxeventsonlogonerror-method"></a>Imstscaxevents:: onlogonerror-Methode

Wird aufgerufen, wenn ein Anmeldefehler oder ein anderes Logon-Ereignis auftritt.

## <a name="syntax"></a>Syntax


```C++
void OnLogonError(
  [in] LONG lError
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lerror* \[ in\]
</dt> <dd>

Der Fehlercode für die Anmeldung. Diese Liste der Codes ist nicht vollständig.

<dt>

<span id="ARBITRATION_CODE_BUMP_OPTIONS"></span><span id="arbitration_code_bump_options"></span>

<span id="ARBITRATION_CODE_BUMP_OPTIONS"></span><span id="arbitration_code_bump_options"></span>**Schiedsgerichtsbarkeit \_ \_ \_ Optionen für Code Bump** (-5 (0xfffffffb))


</dt> <dd>

Winlogon zeigt das Dialogfeld **Sitzungs** Konflikte an.

</dd> <dt>

<span id="ARBITRATION_CODE_CONTINUE_LOGON"></span><span id="arbitration_code_continue_logon"></span>

<span id="ARBITRATION_CODE_CONTINUE_LOGON"></span><span id="arbitration_code_continue_logon"></span>**Schiedsgerichtsbarkeit \_ Code \_ Continue- \_ Anmeldung** (-2 (0xFFFFFFFE))


</dt> <dd>

Die Windows-Anmeldung wird mit dem Anmeldevorgang fortgesetzt.

</dd> <dt>

<span id="ARBITRATION_CODE_CONTINUE_TERMINATE"></span><span id="arbitration_code_continue_terminate"></span>

<span id="ARBITRATION_CODE_CONTINUE_TERMINATE"></span><span id="arbitration_code_continue_terminate"></span>**Schiedsgerichtsbarkeit \_ Code \_ Continue \_ Beenden** (-3 (0xfffffffd))


</dt> <dd>

Winlogon wird im Hintergrund beendet.

</dd> <dt>

<span id="ARBITRATION_CODE_NOPERM_DIALOG"></span><span id="arbitration_code_noperm_dialog"></span>

<span id="ARBITRATION_CODE_NOPERM_DIALOG"></span><span id="arbitration_code_noperm_dialog"></span>**Schiedsgerichtsbarkeit \_ Dialog Feld "Code \_ noperm \_** " (-6 (0xfffffffa))


</dt> <dd>

Winlogon zeigt das Dialogfeld **keine Berechtigungen** an.

</dd> <dt>

<span id="ARBITRATION_CODE_REFUSED_DIALOG"></span><span id="arbitration_code_refused_dialog"></span>

<span id="ARBITRATION_CODE_REFUSED_DIALOG"></span><span id="arbitration_code_refused_dialog"></span>**Schiedsgerichtsbarkeit \_ \_ \_ Dialog Feld "Code verweigert** " (-7 (0xfffffff9))


</dt> <dd>

Winlogon zeigt das Dialogfeld "Verbindung **trennen** " an.

</dd> <dt>

<span id="ARBITRATION_CODE_RECONN_OPTIONS"></span><span id="arbitration_code_reconn_options"></span>

<span id="ARBITRATION_CODE_RECONN_OPTIONS"></span><span id="arbitration_code_reconn_options"></span>**Schiedsgerichtsbarkeit \_ \_ \_ Optionen** für die Code Wiedergabe (-4 (0xfffffffc))


</dt> <dd>

Winlogon zeigt das Dialogfeld **Verbindung wiederherstellen** an.

</dd> <dt>

<span id="ERROR_CODE_ACCESS_DENIED"></span><span id="error_code_access_denied"></span>

<span id="ERROR_CODE_ACCESS_DENIED"></span><span id="error_code_access_denied"></span>**Fehler \_ Code \_ Zugriff \_ verweigert** (-1 (0xFFFFFFFF))


</dt> <dd>

Dem Benutzer wurde der Zugriff verweigert.

</dd> <dt>

<span id="LOGON_FAILED_BAD_PASSWORD"></span><span id="logon_failed_bad_password"></span>

<span id="LOGON_FAILED_BAD_PASSWORD"></span><span id="logon_failed_bad_password"></span>**Anmelden \_ Fehlerhaftes ungültiges \_ \_ Kennwort** (0 (0x0))


</dt> <dd>

Die Anmeldung ist fehlgeschlagen, da die Anmelde Informationen ungültig sind.

</dd> <dt>

<span id="LOGON_FAILED_OTHER"></span><span id="logon_failed_other"></span>

<span id="LOGON_FAILED_OTHER"></span><span id="logon_failed_other"></span>**Anmelden \_ Fehler bei \_ anderen** (2 (0x2))


</dt> <dd>

Ein weiterer Anmelde-oder nach Anmeldefehler ist aufgetreten. Der Remotedesktop-Client zeigt dem Benutzer einen Anmeldebildschirm an.

</dd> <dt>

<span id="LOGON_FAILED_UPDATE_PASSWORD"></span><span id="logon_failed_update_password"></span>

<span id="LOGON_FAILED_UPDATE_PASSWORD"></span><span id="logon_failed_update_password"></span>**Anmelden \_ Fehler beim \_ Aktualisieren des \_ Kennworts** (1 (0x1)).


</dt> <dd>

Das Kennwort ist abgelaufen. Der Benutzer muss sein Kennwort aktualisieren, um die Anmeldung fortsetzen zu können.

</dd> <dt>

<span id="LOGON_WARNING"></span><span id="logon_warning"></span>

<span id="LOGON_WARNING"></span><span id="logon_warning"></span>**Anmelden \_ Warnung** (3 (0x3))


</dt> <dd>

Der Remotedesktop Client zeigt ein Dialogfeld an, das wichtige Informationen für den Benutzer enthält.

</dd> <dt>

<span id="STATUS_ACCOUNT_RESTRICTION"></span><span id="status_account_restriction"></span>

<span id="STATUS_ACCOUNT_RESTRICTION"></span><span id="status_account_restriction"></span>**Status \_ Konto \_ Einschränkung** (-1073741714 (0xc000006e))


</dt> <dd>

Der Benutzername und die Authentifizierungsinformationen sind gültig, aber die Authentifizierung wurde aufgrund von Einschränkungen für das Benutzerkonto blockiert (z. b. Tages Beschränkungen).

</dd> <dt>

<span id="STATUS_LOGON_FAILURE"></span><span id="status_logon_failure"></span>

<span id="STATUS_LOGON_FAILURE"></span><span id="status_logon_failure"></span>**Status \_ Anmelde \_ Fehler** (-1073741715 (0xc000006d))


</dt> <dd>

Die versuchte Anmeldung ist ungültig. Dies liegt daran, dass entweder ein falscher Benutzername oder falsche Authentifizierungsinformationen angezeigt werden.

</dd> <dt>

<span id="STATUS_PASSWORD_MUST_CHANGE"></span><span id="status_password_must_change"></span>

<span id="STATUS_PASSWORD_MUST_CHANGE"></span><span id="status_password_must_change"></span>**Status \_ Kennwort \_ muss \_ geändert** werden (-1073741276 (0xc0000224))


</dt> <dd>

Das Kennwort ist abgelaufen. Der Benutzer muss sein Kennwort aktualisieren, um die Anmeldung fortsetzen zu können.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Implementieren Sie diese Methode in der Ereignis Senke, um die Benachrichtigung zu erhalten, dass ein Anmeldefehler aufgetreten ist.

Diese Liste der Codes ist nicht vollständig.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imstscaxevents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





