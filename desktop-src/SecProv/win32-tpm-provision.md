---
description: Versucht, das TPM vollständig bereit zu stellen, und übernimmt den Besitz des TPM, wenn es sich nicht bereits im Besitz des TPM befindet.
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
ms.openlocfilehash: 5153672d91c88597676f65b53a93de6ffac9f4989dd9e231c87a3b7947b1d657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890808"
---
# <a name="win32_tpmprovision-method"></a>Win32 \_ Tpm::P rovision-Methode

Versucht, das TPM vollständig bereit zu stellen, und übernimmt den Besitz des TPM, wenn es sich nicht bereits im Besitz des TPM befindet. Die Ausführung dieser Methode ist teuer, da sie viele Überprüfungen ausführt. Es wird empfohlen, dass Anwendungen diese Methode nur bei Bedarf verwenden.

Auf diese Methode können nur lokale Administratoren zugreifen.

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

*ForceClear \_ Zulässig* \[ in\]
</dt> <dd>

Bei Festlegung auf **TRUE** kann die Methode physische Anwesenheitsvorgänge anfordern, um das TPM zu löschen. Wenn **false** festgelegt ist, fordert die Methode keinen physischen Anwesenheitsvorgang an, um das TPM zu löschen.

</dd> <dt>

*PhysicalPresencePrompts \_ Zulässig* \[ in\]
</dt> <dd>

Bei Festlegung auf **TRUE** kann die Methode physische Anwesenheitsvorgänge anfordern, die eine Benutzereinbindung während des Startvorgangs erfordern, um die TPM-Zustandsänderung zu bestätigen.

</dd> <dt>

*Informationen* \[ out\]
</dt> <dd>

Gibt eine Bitmaske mit so vielen Informationen zurück, die verfügbar sind, was erforderlich ist, um das TPM vollständig bereitstellen zu können. Maskierungswerte wie INFORMATION \_ REBOOT geben an, dass der Methodenaufruf einen Neustart initiieren sollte, um den Bereitstellungsprozess vorwärts zu verschieben.

Der *Information-Parameter* kann aus den folgenden Werten bestehen.



| Wert                                                                                                                                                                                                                                                                                              | Bedeutung                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INFORMATION_SHUTDOWN"></span><span id="information_shutdown"></span><dl> <dt>**INFORMATIONEN \_ SHUTDOWN**</dt> <dt>0x00000002</dt> </dl>                                                 | Ein Plattformneustart ist erforderlich (Herunterfahren).<br/>                                                                                                                                                                                    |
| <span id="INFORMATION_REBOOT"></span><span id="information_reboot"></span><dl> <dt>**INFORMATIONEN \_ NEUSTART**</dt> <dt>0x00000004</dt> </dl>                                                       | Ein Plattformneustart ist erforderlich (Neustart).<br/>                                                                                                                                                                                      |
| <span id="INFORMATION_TPM_FORCE_CLEAR"></span><span id="information_tpm_force_clear"></span><dl> <dt>**INFORMATIONEN \_ TPM \_ FORCE \_ CLEAR**</dt> <dt>0x00000008</dt> </dl>                          | Das TPM befindet sich bereits im Besitz des TPM. Entweder muss das TPM gelöscht werden, oder der TPM-Besitzerautorisierungswert muss importiert werden.<br/>                                                                                                     |
| <span id="INFORMATION_PHYSICAL_PRESENCE"></span><span id="information_physical_presence"></span><dl> <dt>**INFORMATIONEN \_ PHYSISCHE \_ PRÄSENZ**</dt> <dt>0x00000010</dt> </dl>                     | Physische Präsenz ist erforderlich, um das TPM bereitstellen zu können.<br/>                                                                                                                                                                         |
| <span id="INFORMATION_TPM_ACTIVATE"></span><span id="information_tpm_activate"></span><dl> <dt>**INFORMATIONEN \_ TPM \_ ACTIVATE**</dt> <dt>0x00000020</dt> </dl>                                    | Das TPM ist deaktiviert oder deaktiviert.<br/>                                                                                                                                                                                         |
| <span id="INFORMATION_TPM_TAKE_OWNERSHIP"></span><span id="information_tpm_take_ownership"></span><dl> <dt>**INFORMATIONEN \_ TPM \_ TAKE \_ OWNERSHIP**</dt> <dt>0x00000040</dt> </dl>                 | Der TPM-Besitz wurde übernommen.<br/>                                                                                                                                                                                                |
| <span id="INFORMATION_TPM_CREATE_EK"></span><span id="information_tpm_create_ek"></span><dl> <dt>**INFORMATIONEN \_ TPM \_ CREATE \_ EK**</dt> <dt>0x00000080</dt> </dl>                                | Ein Endorsement Key (EK) ist im TPM vorhanden. <br/>                                                                                                                                                                                 |
| <span id="INFORMATION_TPM_OWNERAUTH"></span><span id="information_tpm_ownerauth"></span><dl> <dt>**INFORMATIONEN \_ TPM \_ OWNERAUTH**</dt> <dt>0x00000100</dt> </dl>                                 | Die TPM-Besitzerautorisierung wird nicht ordnungsgemäß in der Registrierung gespeichert.<br/>                                                                                                                                                         |
| <span id="INFORMATION_TPM_SRK_AUTH"></span><span id="information_tpm_srk_auth"></span><dl> <dt>**INFORMATIONEN \_ TPM \_ SRK \_ AUTH**</dt> <dt>0x000000200</dt> </dl>                                  | Der Autorisierungswert Storage Stammschlüssels (Root Key, SRK) ist nicht alle Nullen.<br/>                                                                                                                                                            |
| <span id="INFORMATION_TPM_DISABLE_OWNER_CLEAR"></span><span id="information_tpm_disable_owner_clear"></span><dl> <dt>**INFORMATIONEN \_ TPM \_ DISABLE \_ OWNER \_ CLEAR**</dt> <dt>0x00000400</dt> </dl> | Wenn das Betriebssystem so konfiguriert ist, dass das Löschen des TPM mit dem TPM-Besitzerautorisierungswert deaktiviert wird und das TPM noch nicht konfiguriert wurde, um das Löschen des TPM mit dem TPM-Besitzerautorisierungswert zu verhindern.<br/> |
| <span id="INFORMATION_TPM_SRKPUB"></span><span id="information_tpm_srkpub"></span><dl> <dt>**INFORMATIONEN \_ TPM \_ SRKPUB**</dt> <dt>0x00000800</dt> </dl>                                          | Die Registrierungsinformationen des Betriebssystems zum Storage Stammschlüssel des TPM stimmen nicht mit dem TPM-Storage Stammschlüssel überein.<br/>                                                                                                       |
| <span id="INFORMATION_TPM_READ_SRKPUB"></span><span id="information_tpm_read_srkpub"></span><dl> <dt>**INFORMATIONEN \_ TPM \_ READ \_ SRKPUB**</dt> <dt>0x00001000</dt> </dl>                          | Das permanente TPM-Flag, um das Lesen des öffentlichen Werts des Storage Stammschlüssels zu ermöglichen, ist nicht festgelegt.<br/>                                                                                                                                    |
| <span id="INFORMATION_TPM_BOOT_COUNTER"></span><span id="information_tpm_boot_counter"></span><dl> <dt>**INFORMATIONEN \_ \_ \_ TPM-STARTZÄHLER-0x00002000**</dt> <dt></dt> </dl>                       | Der monotone Indikator, der während des Starts erhöht wurde, wurde nicht erstellt.<br/>                                                                                                                                                         |
| <span id="INFORMATION_TPM_AD_BACKUP"></span><span id="information_tpm_ad_backup"></span><dl> <dt>**INFORMATIONEN \_ TPM \_ AD \_ BACKUP**</dt> <dt>0x00004000</dt> </dl>                                | Die Besitzerautorisierung des TPM wurde nicht in Active Directory gesichert.<br/>                                                                                                                                                   |
| <span id="INFORMATION_TPM_AD_BACKUP_PHASE_I"></span><span id="information_tpm_ad_backup_phase_i"></span><dl> <dt>**INFORMATIONEN \_ TPM \_ AD BACKUP PHASE \_ \_ \_ I**</dt> <dt>0x00008000</dt> </dl>      | Der erste Teil des Tpm-Besitzer-Autorisierungsinformationsspeichers in Active Directory wird ausgeführt.<br/>                                                                                                                    |
| <span id="INFORMATION_TPM_AD_BACKUP_PHASE_II"></span><span id="information_tpm_ad_backup_phase_ii"></span><dl> <dt>**INFORMATIONEN \_ TPM \_ AD BACKUP PHASE \_ \_ \_ II**</dt> <dt>0x00010000</dt> </dl>   | Der zweite Teil des TPM-Besitzer-Autorisierungsinformationsspeichers in Active Directory wird ausgeführt.<br/>                                                                                                                   |
| <span id="INFORMATION_LEGACY_CONFIGURATION"></span><span id="information_legacy_configuration"></span><dl> <dt>**INFORMATIONEN \_ LEGACY \_ CONFIGURATION**</dt> <dt>0x00020000</dt> </dl>            | Windows Gruppenrichtlinie ist so konfiguriert, dass keine TPM-Besitzerautorisierung gespeichert wird, sodass das TPM nicht vollständig bereit sein kann.<br/>                                                                                                               |
| <span id="INFORMATION_EK_CERTIFICATE"></span><span id="information_ek_certificate"></span><dl> <dt>**INFORMATIONEN \_ EK \_ CERTIFICATE**</dt> <dt>0x00040000</dt> </dl>                              | Das EK-Zertifikat wurde nicht aus dem TPM NV Ram gelesen und in der Registrierung gespeichert. <br/>                                                                                                                                            |
| <span id="INFORMATION_TCG_EVENT_LOG"></span><span id="information_tcg_event_log"></span><dl> <dt>**INFORMATIONEN \_ TCG \_ EVENT \_ LOG**</dt> <dt>0x00080000</dt> </dl>                                | Das TCG-Ereignisprotokoll ist leer oder kann nicht gelesen werden. <br/>                                                                                                                                                                              |
| <span id="INFORMATION_NOT_REDUCED"></span><span id="information_not_reduced"></span><dl> <dt>**INFORMATIONEN \_ NICHT \_ REDUZIERTE**</dt> <dt>0x00100000</dt> </dl>                                       | Das TPM befindet sich nicht im Besitz des TPM.<br/>                                                                                                                                                                                                       |
| <span id="INFORMATION_GENERIC_ERROR"></span><span id="information_generic_error"></span><dl> <dt>**INFORMATIONEN \_ GENERIC \_ ERROR**</dt> <dt>0x00200000</dt> </dl>                                 | Ein Fehler ist aufgetreten, aber nicht spezifisch für eine bestimmte Aufgabe.<br/>                                                                                                                                                                   |
| <span id="INFORMATION_DEVICE_LOCK_COUNTER"></span><span id="information_device_lock_counter"></span><dl> <dt>**INFORMATIONEN \_ 0X00400000 DES \_ \_ GERÄTESPERRZÄHLERS**</dt> <dt></dt> </dl>              | Der Gerätesperrzähler wurde nicht erstellt.<br/>                                                                                                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Alle TPM-Fehler sowie Fehler, die spezifisch für [TPM-Basisdienste](../tbs/tbs-return-codes.md) sind, können zurückgegeben werden.

Allgemeine Rückgabecodes sind unten aufgeführt.



| Rückgabecode/-wert                                                                                                                                 | BESCHREIBUNG                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Die Methode war erfolgreich.<br/> |



 

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                      |
| Namespace<br/>                | \\\\.\\ root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                     |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> </dl>

 

 
