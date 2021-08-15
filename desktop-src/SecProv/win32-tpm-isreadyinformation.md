---
description: Gibt an, ob das TPM bereit ist, und stellt zusätzliche Informationen zum Status des TPM bereit.
ms.assetid: 1E348D77-979C-42FC-824D-7C57F7BAABE5
title: Win32_Tpm::IsReadyInformation-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsReadyInformation
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 319152da3604044500c107520cf1afd1d04e16fc2c7f54f0ecebf7b49d81f0f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890837"
---
# <a name="win32_tpmisreadyinformation-method"></a>Win32 \_ Tpm::IsReadyInformation-Methode

Gibt an, ob das TPM bereit ist, und stellt zusätzliche Informationen zum Status des TPM bereit. Der Information-Parameter gibt eine Bitmaske mit Informationen zurück, die erforderlich sind, um das TPM vollständig bereitstellen zu können.

Auf diese Methode kann nur von lokalen Administratoren zugegriffen werden.

## <a name="syntax"></a>Syntax


```C++
uint32 IsReadyInformation(
  [out] BOOL   IsReady,
  [out] uint32 Information
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IsReady* \[ out\]
</dt> <dd>

Legen Sie **auf TRUE** fest, wenn TPM und System vollständig für die TPM-Verwendung bereitgestellt sind.

</dd> <dt>

*Informationen* \[ out\]
</dt> <dd>

Gibt eine Bitmaske mit so viele Informationen zurück, wie für die vollständige Bereitstellung des TPM verfügbar sind.

Der *Information-Parameter* kann aus den folgenden Werten bestehen.



| Wert                                                                                                                                                                                                                                                                                              | Bedeutung                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INFORMATION_SHUTDOWN"></span><span id="information_shutdown"></span><dl> <dt>**INFORMATIONEN \_ SHUTDOWN**</dt> <dt>0X00000002</dt> </dl>                                                 | Plattformneustart erforderlich (Herunterfahren).<br/>                                                                                                                                                                                    |
| <span id="INFORMATION_REBOOT"></span><span id="information_reboot"></span><dl> <dt>**INFORMATIONEN \_ NEUSTART**</dt> <dt>0X00000004</dt> </dl>                                                       | Ein Neustart der Plattform ist erforderlich (Neustart).<br/>                                                                                                                                                                                      |
| <span id="INFORMATION_TPM_FORCE_CLEAR"></span><span id="information_tpm_force_clear"></span><dl> <dt>**INFORMATIONEN \_ TPM \_ FORCE \_ CLEAR**</dt> <dt>0x00000008</dt> </dl>                          | Das TPM befindet sich bereits im Besitz. Entweder muss das TPM gelöscht werden, oder der Autorisierungswert des TPM-Besitzers muss importiert werden.<br/>                                                                                                     |
| <span id="INFORMATION_PHYSICAL_PRESENCE"></span><span id="information_physical_presence"></span><dl> <dt>**INFORMATIONEN \_ PHYSISCHE \_ PRÄSENZ**</dt> <dt>0X00000010</dt> </dl>                     | Physische Präsenz ist erforderlich, um das TPM bereitstellen zu können.<br/>                                                                                                                                                                         |
| <span id="INFORMATION_TPM_ACTIVATE"></span><span id="information_tpm_activate"></span><dl> <dt>**INFORMATIONEN \_ TPM \_ ACTIVATE**</dt> <dt>0x00000020</dt> </dl>                                    | Das TPM ist deaktiviert oder deaktiviert.<br/>                                                                                                                                                                                         |
| <span id="INFORMATION_TPM_TAKE_OWNERSHIP"></span><span id="information_tpm_take_ownership"></span><dl> <dt>**INFORMATIONEN \_ TPM- \_ \_ UND**</dt> <dt>0X00000040</dt> </dl>                 | Der TPM-Besitz wurde übernommen.<br/>                                                                                                                                                                                                |
| <span id="INFORMATION_TPM_CREATE_EK"></span><span id="information_tpm_create_ek"></span><dl> <dt>**INFORMATIONEN \_ TPM \_ CREATE \_ EK**</dt> <dt>0x00000080</dt> </dl>                                | Im TPM ist ein Endorsement Key (EK) vorhanden. <br/>                                                                                                                                                                                 |
| <span id="INFORMATION_TPM_OWNERAUTH"></span><span id="information_tpm_ownerauth"></span><dl> <dt>**INFORMATIONEN \_ TPM \_ OWNERAUTH-0x00000100**</dt> <dt></dt> </dl>                                 | Die TPM-Besitzerautorisierung wird nicht ordnungsgemäß in der Registrierung gespeichert.<br/>                                                                                                                                                         |
| <span id="INFORMATION_TPM_SRK_AUTH"></span><span id="information_tpm_srk_auth"></span><dl> <dt>**INFORMATIONEN \_ \_ \_ TPM-SRK-Authentifizierung**</dt> <dt>0x00000200</dt> </dl>                                  | Der Storage -Autorisierungswert (Root Key, SRK) ist nicht alle Nullen.<br/>                                                                                                                                                            |
| <span id="INFORMATION_TPM_DISABLE_OWNER_CLEAR"></span><span id="information_tpm_disable_owner_clear"></span><dl> <dt>**INFORMATIONEN \_ TPM \_ DISABLE OWNER CLEAR \_ \_ 0X00000400**</dt> <dt></dt> </dl> | Wenn das Betriebssystem so konfiguriert ist, dass das Löschen des TPM mit dem TPM-Besitzerautorisierungswert deaktiviert wird und das TPM noch nicht konfiguriert wurde, um das Löschen des TPM mit dem TPM-Besitzerautorisierungswert zu verhindern.<br/> |
| <span id="INFORMATION_TPM_SRKPUB"></span><span id="information_tpm_srkpub"></span><dl> <dt>**INFORMATIONEN \_ \_TPM-SRKPUB-0x00000800**</dt> <dt></dt> </dl>                                          | Die Registrierungsinformationen des Betriebssystems über den Storage-Stammschlüssel des TPM passen nicht zum TPM-Storage Stammschlüssel.<br/>                                                                                                       |
| <span id="INFORMATION_TPM_READ_SRKPUB"></span><span id="information_tpm_read_srkpub"></span><dl> <dt>**INFORMATIONEN \_ TPM \_ READ \_ SRKPUB**</dt> <dt>0x00001000</dt> </dl>                          | Das permanente TPM-Flag zum Lesen des öffentlichen Storage stammschlüssels ist nicht festgelegt.<br/>                                                                                                                                    |
| <span id="INFORMATION_TPM_BOOT_COUNTER"></span><span id="information_tpm_boot_counter"></span><dl> <dt>**INFORMATIONEN \_ \_ \_ TPM-STARTZÄHLER 0X00002000**</dt> <dt></dt> </dl>                       | Der monotone Zähler, der während des Startvorgangs inkrementiert wurde, wurde nicht erstellt.<br/>                                                                                                                                                         |
| <span id="INFORMATION_TPM_AD_BACKUP"></span><span id="information_tpm_ad_backup"></span><dl> <dt>**INFORMATIONEN \_ TPM \_ AD \_ BACKUP**</dt> <dt>0X00004000</dt> </dl>                                | Die Besitzerautorisierung des TPM wurde nicht in Active Directory sichern.<br/>                                                                                                                                                   |
| <span id="INFORMATION_TPM_AD_BACKUP_PHASE_I"></span><span id="information_tpm_ad_backup_phase_i"></span><dl> <dt>**INFORMATIONEN \_ TPM \_ AD BACKUP PHASE \_ \_ \_ I**</dt> <dt>0X00008000</dt> </dl>      | Der erste Teil des TPM-Besitzer-Autorisierungsinformationsspeichers in Active Directory wird in Bearbeitung.<br/>                                                                                                                    |
| <span id="INFORMATION_TPM_AD_BACKUP_PHASE_II"></span><span id="information_tpm_ad_backup_phase_ii"></span><dl> <dt>**INFORMATIONEN \_ TPM \_ AD BACKUP PHASE \_ \_ \_ II**</dt> <dt>0X00010000</dt> </dl>   | Der zweite Teil des TPM-Besitzer-Autorisierungsinformationsspeichers in Active Directory wird in Bearbeitung.<br/>                                                                                                                   |
| <span id="INFORMATION_LEGACY_CONFIGURATION"></span><span id="information_legacy_configuration"></span><dl> <dt>**INFORMATIONEN \_ \_LEGACYKONFIGURATIONS-0X00020000**</dt> <dt></dt> </dl>            | Windows Gruppenrichtlinie ist so konfiguriert, dass keine TPM-Besitzerautorisierung gespeichert wird, sodass das TPM nicht vollständig bereit ist.<br/>                                                                                                               |
| <span id="INFORMATION_EK_CERTIFICATE"></span><span id="information_ek_certificate"></span><dl> <dt>**INFORMATIONEN \_ EK \_ CERTIFICATE**</dt> <dt>0x00040000</dt> </dl>                              | Das EK-Zertifikat wurde nicht aus dem TPM NV Ram gelesen und in der Registrierung gespeichert. <br/>                                                                                                                                            |
| <span id="INFORMATION_TCG_EVENT_LOG"></span><span id="information_tcg_event_log"></span><dl> <dt>**INFORMATIONEN \_ \_ \_ TCG-EREIGNISPROTOKOLL-0x00080000**</dt> <dt></dt> </dl>                                | Das TCG-Ereignisprotokoll ist leer oder kann nicht gelesen werden. <br/>                                                                                                                                                                              |
| <span id="INFORMATION_NOT_REDUCED"></span><span id="information_not_reduced"></span><dl> <dt>**INFORMATIONEN \_ NOT \_ REDUCED**</dt> <dt>0x00100000</dt> </dl>                                       | Das TPM befindet sich nicht im Besitz.<br/>                                                                                                                                                                                                       |
| <span id="INFORMATION_GENERIC_ERROR"></span><span id="information_generic_error"></span><dl> <dt>**INFORMATIONEN \_ \_GENERISCHER**</dt> <dt>0X00200000</dt> </dl>                                 | Ein Fehler ist aufgetreten, aber nicht spezifisch für eine bestimmte Aufgabe.<br/>                                                                                                                                                                   |
| <span id="INFORMATION_DEVICE_LOCK_COUNTER"></span><span id="information_device_lock_counter"></span><dl> <dt>**INFORMATIONEN \_ \_ \_ GERÄTESPERRZÄHLER 0X00400000**</dt> <dt></dt> </dl>              | Der Gerätesperrzähler wurde nicht erstellt.<br/>                                                                                                                                                                               |
| <span id="INFORMATION_DEVICEID"></span><span id="information_deviceid"></span><dl> <dt>**INFORMATIONEN \_ DEVICEID-0x00800000**</dt> <dt></dt> </dl>                                                | Die Geräte-ID wurde nicht erstellt.<br/>                                                                                                                                                                                 |
| <span id="INFORMATION_ATTESTATION_VULNERABILITY"></span><span id="information_attestation_vulnerability"></span><dl> <dt>**INFORMATIONEN \_ NACHWEISRISIKO \_**</dt> <dt> 0X01000000</dt> </dl>                                                | Das TPM verfügt über ein Sicherheitsrisiko im Zusammenhang mit integritätsbezogenem Nachweis.<br/>                                                                                                                                                                                 |


 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Alle TPM-Fehler und -Fehler, die für [TPM-Basisdienste](../tbs/tbs-return-codes.md) spezifisch sind, können zurückgegeben werden.

Allgemeine Rückgabecodes sind unten aufgeführt.



| Rückgabecode/-wert                                                                                                                                 | BESCHREIBUNG                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Die Methode war erfolgreich.<br/> |



 

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                      |
| Namespace<br/>                | \\\\.\\ root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                     |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_Win32-tpm.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> </dl>

 

 
