---
description: Versucht, das TPM vollständig bereit bereitzustellen, und übernimmt den Besitz von TPM, wenn es nicht bereits im Besitz ist.
ms.assetid: D0C09A48-00D0-4BF2-8F0A-451A61EA7810
title: Win32_Tpm::P rovision-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Provision
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 198d7b02b1813002ce55d175ad016ace23ee7da4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867631"
---
# <a name="win32_tpmprovision-method"></a>Win32- \_ TPM::P rovision-Methode

Versucht, das TPM vollständig bereit bereitzustellen, und übernimmt den Besitz von TPM, wenn es nicht bereits im Besitz ist. Die Ausführung dieser Methode ist aufwendig, da viele Überprüfungen durchgeführt werden. Es wird empfohlen, dass Anwendungen diese Methode nur bei Bedarf verwenden.

Diese Methode ist nur für lokale Administratoren zugänglich.

## <a name="syntax"></a>Syntax


```C++
uint32 Provision(
  [in]  BOOL   ForceClear_Allowed,
  [in]  BOOL   PhysicalPresencePrompts_Allowed,
  [out] uint32 Information
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Forceclear \_ Zulässig* \[ in\]
</dt> <dd>

Wenn der Wert auf **true** festgelegt ist, kann die Methode physische Anwesenheits Vorgänge anfordern, um das TPM zu löschen. Wenn **false** festgelegt ist, fordert die Methode keinen physischen Anwesenheits Vorgang an, um das TPM zu löschen.

</dd> <dt>

*Physicalpresenceaufforderungen \_ Zulässig* \[ in\]
</dt> <dd>

Wenn diese Einstellung auf " **true** " festgelegt ist, kann die Methode physische Anwesenheits Vorgänge anfordern, die während des Startvorgangs eine Benutzer Beteiligung erfordern, um die TPM-Statusänderung

</dd> <dt>

*Informationen* \[ vorgenommen\]
</dt> <dd>

Gibt eine Bitmaske von so vielen Informationen zurück, wie verfügbar ist, was für die vollständige Bereitstellung des TPM erforderlich ist. Masken Werte wie \_ der Neustart der Informationen geben an, dass der Methodenaufrufe einen Neustart initiieren soll, um den Bereitstellungs Prozess weiterzuleiten.

Der *Informations* Parameter kann aus den folgenden Werten bestehen.



| Wert                                                                                                                                                                                                                                                                                              | Bedeutung                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INFORMATION_SHUTDOWN"></span><span id="information_shutdown"></span><dl> <dt>**Informationen \_ Herunter**</dt> fahren <dt>0x00000002</dt> </dl>                                                 | Der Neustart der Plattform ist erforderlich (Herunterfahren).<br/>                                                                                                                                                                                    |
| <span id="INFORMATION_REBOOT"></span><span id="information_reboot"></span><dl> <dt>**Informationen \_**</dt> <dt>0x00000004</dt> neu starten </dl>                                                       | Der Neustart der Plattform ist erforderlich (Neustart).<br/>                                                                                                                                                                                      |
| <span id="INFORMATION_TPM_FORCE_CLEAR"></span><span id="information_tpm_force_clear"></span><dl> <dt>**Informationen \_ TPM \_ erzwingen \_**</dt> , dass <dt>0x00000008</dt> gelöscht wird </dl>                          | Das TPM ist bereits im Besitz. Entweder muss das TPM gelöscht werden, oder der TPM-Besitzer Autorisierungs Wert muss importiert werden.<br/>                                                                                                     |
| <span id="INFORMATION_PHYSICAL_PRESENCE"></span><span id="information_physical_presence"></span><dl> <dt>**Informationen \_ Physisches \_ vorhanden sein**</dt> <dt>0x00000010</dt> </dl>                     | Die physische Anwesenheit ist erforderlich, um das TPM bereitzustellen.<br/>                                                                                                                                                                         |
| <span id="INFORMATION_TPM_ACTIVATE"></span><span id="information_tpm_activate"></span><dl> <dt>**Informationen \_ TPM- \_ Aktivierung**</dt> <dt>0x00000020</dt> </dl>                                    | Das TPM ist deaktiviert oder deaktiviert.<br/>                                                                                                                                                                                         |
| <span id="INFORMATION_TPM_TAKE_OWNERSHIP"></span><span id="information_tpm_take_ownership"></span><dl> <dt>**Informationen \_ TPM \_ übernimmt den \_ Besitz**</dt> <dt>0x00000040</dt> </dl>                 | Der TPM-Besitz wurde angenommen.<br/>                                                                                                                                                                                                |
| <span id="INFORMATION_TPM_CREATE_EK"></span><span id="information_tpm_create_ek"></span><dl> <dt>**Informationen \_ TPM \_ Create \_ EK**</dt> <dt>0x00000080</dt> </dl>                                | Ein Endorsement Key (EK) ist im TPM vorhanden. <br/>                                                                                                                                                                                 |
| <span id="INFORMATION_TPM_OWNERAUTH"></span><span id="information_tpm_ownerauth"></span><dl> <dt>**Informationen \_ TPM \_**</dt> -Besitzer- <dt>00000100 0x</dt> </dl>                                 | Die TPM-Besitzer Autorisierung ist nicht ordnungsgemäß in der Registrierung gespeichert.<br/>                                                                                                                                                         |
| <span id="INFORMATION_TPM_SRK_AUTH"></span><span id="information_tpm_srk_auth"></span><dl> <dt>**Informationen \_ TPM- \_ SRK \_**</dt> -Authentifizierung <dt>0x000000200</dt> </dl>                                  | Der SRK-Autorisierungs Wert (Storage Root Key) ist nicht alle Nullen.<br/>                                                                                                                                                            |
| <span id="INFORMATION_TPM_DISABLE_OWNER_CLEAR"></span><span id="information_tpm_disable_owner_clear"></span><dl> <dt>**Informationen \_ TPM \_ - \_ Besitzer \_ Deaktivieren**</dt> <dt>0x00000400</dt> </dl> | Wenn das Betriebssystem so konfiguriert ist, dass das Löschen des TPM mit dem TPM-Besitzer Autorisierungs Wert deaktiviert wird und das TPM noch nicht konfiguriert wurde, um das Löschen des TPM mit dem TPM-Besitzer Autorisierungs Wert zu verhindern.<br/> |
| <span id="INFORMATION_TPM_SRKPUB"></span><span id="information_tpm_srkpub"></span><dl> <dt>**Informationen \_ TPM \_ srkpub**</dt> <dt>0x00000800</dt> </dl>                                          | Die Registrierungsinformationen des Betriebssystems über den Speicher Stamm Schlüssel des TPM stimmen nicht mit dem TPM-Speicher Stamm Schlüssel identisch.<br/>                                                                                                       |
| <span id="INFORMATION_TPM_READ_SRKPUB"></span><span id="information_tpm_read_srkpub"></span><dl> <dt>**Informationen \_ TPM \_ Read \_ srkpub**</dt> <dt>0x00001000</dt> </dl>                          | Das dauerhafte TPM-Flag, das das Lesen des öffentlichen Werts für den Speicher Stamm Schlüssel zulässt, ist nicht festgelegt.<br/>                                                                                                                                    |
| <span id="INFORMATION_TPM_BOOT_COUNTER"></span><span id="information_tpm_boot_counter"></span><dl> <dt>**Informationen \_ TPM- \_ Start \_ Counter**</dt> <dt>0x00002000</dt> </dl>                       | Der monoton Wert, der während des Starts inkrementiert wurde, wurde nicht erstellt.<br/>                                                                                                                                                         |
| <span id="INFORMATION_TPM_AD_BACKUP"></span><span id="information_tpm_ad_backup"></span><dl> <dt>**Informationen \_ TPM \_ AD \_ Backup**</dt> <dt>0x00004000</dt> </dl>                                | Die Besitzer Autorisierung des TPM wurde nicht in Active Directory gesichert.<br/>                                                                                                                                                   |
| <span id="INFORMATION_TPM_AD_BACKUP_PHASE_I"></span><span id="information_tpm_ad_backup_phase_i"></span><dl> <dt>**Informationen \_ TPM \_ AD \_ Backup \_ Phase \_ I**</dt> <dt>0x00008000</dt> </dl>      | Der erste Teil des TPM-Besitzer Autorisierungs Informationsspeichers in Active Directory wird gerade ausgeführt.<br/>                                                                                                                    |
| <span id="INFORMATION_TPM_AD_BACKUP_PHASE_II"></span><span id="information_tpm_ad_backup_phase_ii"></span><dl> <dt>**Informationen \_ TPM \_ AD \_ Backup \_ Phase \_ II**</dt> <dt>0x00010000 bis</dt> </dl>   | Der zweite Teil des TPM-Besitzer Autorisierungs Informationsspeichers in Active Directory wird gerade ausgeführt.<br/>                                                                                                                   |
| <span id="INFORMATION_LEGACY_CONFIGURATION"></span><span id="information_legacy_configuration"></span><dl> <dt>**Informationen \_ Legacy \_ Konfiguration**</dt> <dt>0x00020000</dt> </dl>            | Windows Gruppenrichtlinie ist so konfiguriert, dass keine TPM-Besitzer Autorisierung gespeichert wird, damit das TPM nicht vollständig bereit ist.<br/>                                                                                                               |
| <span id="INFORMATION_EK_CERTIFICATE"></span><span id="information_ek_certificate"></span><dl> <dt>**Informationen \_ EK- \_ Zertifikat**</dt> <dt>0x00040000</dt> </dl>                              | Das EK-Zertifikat wurde nicht aus dem TPM NV-RAM gelesen und in der Registrierung gespeichert. <br/>                                                                                                                                            |
| <span id="INFORMATION_TCG_EVENT_LOG"></span><span id="information_tcg_event_log"></span><dl> <dt>**Informationen \_ TCG- \_ Ereignis \_ Protokoll**</dt> <dt>0x00080000</dt> </dl>                                | Das TCG-Ereignisprotokoll ist leer oder kann nicht gelesen werden. <br/>                                                                                                                                                                              |
| <span id="INFORMATION_NOT_REDUCED"></span><span id="information_not_reduced"></span><dl> <dt>**Informationen \_ \_**</dt> <dt>0x00100000</dt> nicht reduziert </dl>                                       | Das TPM ist nicht im Besitz von.<br/>                                                                                                                                                                                                       |
| <span id="INFORMATION_GENERIC_ERROR"></span><span id="information_generic_error"></span><dl> <dt>**Informationen \_ Generischer \_ Fehler**</dt> <dt>0x00200000</dt> </dl>                                 | Ein Fehler ist aufgetreten, jedoch nicht spezifisch für eine bestimmte Aufgabe.<br/>                                                                                                                                                                   |
| <span id="INFORMATION_DEVICE_LOCK_COUNTER"></span><span id="information_device_lock_counter"></span><dl> <dt>**Informationen \_ Geräte \_ Sperr- \_ Counter**</dt> <dt>0x00400000</dt> </dl>              | Der Geräte Sperr-Counter wurde nicht erstellt.<br/>                                                                                                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Alle TPM-Fehler sowie Fehler, die für die [TPM-Basisdienste](../tbs/tbs-return-codes.md) spezifisch sind, können zurückgegeben werden.

Allgemeine Rückgabecodes sind unten aufgeführt.



| Rückgabecode/-wert                                                                                                                                 | BESCHREIBUNG                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Die Methode war erfolgreich.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                      |
| Namespace<br/>                | \\\\.\\ root \\ CIMV2 \\ Security- \\ mikrosofttpm<br/>                                     |
| MOF<br/>                      | <dl> <dt>Win32- \_ TPM. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32- \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ TPM**](win32-tpm.md)
</dt> </dl>

 

 
