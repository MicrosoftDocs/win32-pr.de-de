---
description: Für die Laufwerkverschlüsselung oder zum Erstellen von Verschlüsselungssicherheitssoftware können Sie die Windows-Verschlüsselungssoftware BitLocker-Laufwerkverschlüsselung verwenden, eine Verschlüsselungs-API, die Sie mithilfe der WMI-Anbieterklasse Win32 \_ EncryptableVolume verwenden können.
ms.assetid: 464fa664-4330-43fa-a5e0-144d1e73cf58
title: Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume
- Win32_EncryptableVolume.DeviceID
- Win32_EncryptableVolume.PersistentVolumeID
- Win32_EncryptableVolume.DriveLetter
- Win32_EncryptableVolume.ProtectionStatus
api_type:
- Schema
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3beb3498cf9e3d2873ea7dcfe3a108618eeddb513bc8207d1e819cce2fe976d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891003"
---
# <a name="win32_encryptablevolume-class"></a>Win32 \_ EncryptableVolume-Klasse

Die WMI-Anbieterklasse **\_ "Win32 EncryptableVolume"** stellt einen Speicherbereich auf einer Festplatte dar, der mithilfe von BitLocker-Laufwerkverschlüsselung. Nur NTFS-Volumes können verschlüsselt werden. Dabei kann es sich um ein Volume mit einem Betriebssystem oder um ein Datenvolumen auf dem lokalen Datenträger befinden. Es darf kein Netzwerklaufwerk sein.

Um die Vorteile von BitLocker zu nutzen, müssen Sie eine Schutzmethode für den Verschlüsselungsschlüssel des Volumes angeben und das Volume dann vollständig verschlüsseln.

Um den Verschlüsselungsschlüssel des Volumes zu schützen, fügen Sie Mithilfe der folgenden Methoden Schlüsselschutzvorrichtungen hinzu:

-   [**ProtectKeyWithCertificateFile**](protectkeywithcertificatefile-win32-encryptablevolume.md)
-   [**ProtectKeyWithCertificateThumbprint**](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
-   [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md)
-   [**ProtectKeyWithPassphrase**](protectkeywithpassphrase-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPM**](protectkeywithtpm-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPIN**](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPINAndStartupKey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndStartupKey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

Jeder Typ der Schlüsselschutzvorrichtung bietet eine andere Authentifizierungserfahrung zum Entsperren des Zugriffs auf die verschlüsselten Daten. Externe Schlüssel und numerische Kennwörter können während Wiederherstellungsszenarien eine Authentifizierung ermöglichen. Bei TPM-basierten Schlüsselschutzvorrichtungen müssen Sie das TPM möglicherweise zuerst ordnungsgemäß initialisieren. Weitere Informationen finden Sie in der [**WMI-Anbieterklasse Win32 \_ Tpm.**](win32-tpm.md)

Verwenden Sie die [**Encrypt-**](encrypt-win32-encryptablevolume.md) oder [**EncryptAfterHardwareTest-Methode,**](encryptafterhardwaretest-win32-encryptablevolume.md) um mit der Verschlüsselung zu beginnen. Vor dem Starten der Verschlüsselung müssen Schlüsselschutzvorrichtungen hinzugefügt werden, oder Sie müssen die [**DisableKeyProtectors-Methode**](disablekeyprotectors-win32-encryptablevolume.md) verwenden, um einen ungeschützten unverschlüsselten Schlüssel verfügbar zu machen. Wenn der Computer während der Verschlüsselung ausgeschaltet wird, wird die Verschlüsselung automatisch fortgesetzt, wenn der Computer neu gestartet wird.

Sie können die [**Methoden GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) und [**GetProtectionStatus**](getprotectionstatus-win32-encryptablevolume.md) verwenden, um den Status eines zugänglichen Volumes zu überprüfen.

## <a name="syntax"></a>Syntax

``` syntax
class Win32_EncryptableVolume
{
  string DeviceID;
  string PersistentVolumeID;
  string DriveLetter;
  uint32 ProtectionStatus;
};
```

## <a name="members"></a>Member

Die **Win32 \_ EncryptableVolume-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ EncryptableVolume-Klasse** verfügt über diese Methoden.



| Methode                                                                                                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BackupRecoveryInformationToActiveDirectory**](backuprecoveryinformationtoactivedirectory-win32-encryptablevolume.md) | Speichert alle externen Schlüssel und zugehörigen Informationen, die für die Wiederherstellung in Active Directory erforderlich sind.<br/>                                                                                                                                                                       |
| [**ChangeExternalKey**](changeexternalkey-win32-encryptablevolume.md)                                                   | Ändert den externen Schlüssel, der einem verschlüsselten Volume zugeordnet ist.<br/>                                                                                                                                                                                                              |
| [**ChangePassphrase**](changepassphrase-win32-encryptablevolume.md)                                                     | Verwendet die neue Passphrase, um einen neuen abgeleiteten Schlüssel zu erhalten.<br/>                                                                                                                                                                                                                       |
| [**ChangePIN**](changepin-win32-encryptablevolume.md)                                                                   | Ändert eine PIN, die einem verschlüsselten Volume zugeordnet ist.<br/>                                                                                                                                                                                                                         |
| [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md)                                         | Entfernt alle externen Schlüssel und zugehörigen Informationen, die auf dem aktuell ausgeführten Betriebssystemvolume gespeichert sind und zum automatischen Entsperren von Datenvolumes verwendet werden.<br/>                                                                                                             |
| [**Entschlüsseln**](decrypt-win32-encryptablevolume.md)                                                                       | Beginnt mit der Entschlüsselung eines vollständig verschlüsselten Volumes oder setzt die Entschlüsselung eines teilweise verschlüsselten Volumes wieder ein.<br/>                                                                                                                                                                       |
| [**DeleteKeyProtector**](deletekeyprotector-win32-encryptablevolume.md)                                                 | Löscht eine bestimmte Schlüsselschutzvorrichtung für das Volume.<br/>                                                                                                                                                                                                                              |
| [**DeleteKeyProtectors**](deletekeyprotectors-win32-encryptablevolume.md)                                               | Löscht alle Schlüsselschutzvorrichtungen für das Volume.<br/>                                                                                                                                                                                                                                 |
| [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md)                                                   | Entfernt den externen Schlüssel, der auf dem aktuell ausgeführten Betriebssystem-Volume gespeichert ist, sodass das Volume nicht automatisch entsperrt wird, wenn es bereitgestellt wird.<br/>                                                                                                                       |
| [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md)                                             | Deaktiviert alle Schlüsselschutzvorrichtungen, die diesem Volume zugeordnet sind.<br/>                                                                                                                                                                                                                   |
| [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md)                                                     | Ermöglicht das automatische Entsperren eines Datenvolumens, wenn das Volume bereitgestellt wird.<br/>                                                                                                                                                                                              |
| [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md)                                               | Aktiviert alle deaktivierten Schlüsselschutzvorrichtungen.<br/>                                                                                                                                                                                                                                       |
| [**Encrypt**](encrypt-win32-encryptablevolume.md)                                                                       | Beginnt mit der Verschlüsselung eines vollständig entschlüsselten Volumes oder setzt die Verschlüsselung eines teilweise verschlüsselten Volumes wieder ein.<br/>                                                                                                                                                                       |
| [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md)                                     | Beginnt die Verschlüsselung eines vollständig entschlüsselten Volumes nach einem Hardwaretest.<br/>                                                                                                                                                                                                       |
| [**FindValidCertificates**](findvalidcertificates-win32-encryptablevolume.md)                                           | Listet alle Zertifikate im System auf, die den angegebenen Kriterien entsprechen, und gibt eine Liste von Fingerabdrucks zurück.<br/>                                                                                                                                                             |
| [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md)                                               | Gibt den Status der Verschlüsselung oder Entschlüsselung auf dem Volume an.<br/>                                                                                                                                                                                                        |
| [**GetEncryptionMethod**](getencryptionmethod-win32-encryptablevolume.md)                                               | Gibt den Verschlüsselungsalgorithmus und die Schlüsselgröße an, die auf dem Volume verwendet werden.<br/>                                                                                                                                                                                                        |
| [**GetExternalKeyFileName**](getexternalkeyfilename-win32-encryptablevolume.md)                                         | Gibt den Namen der Datei zurück, die den externen Schlüssel enthält.<br/>                                                                                                                                                                                                               |
| [**GetExternalKeyFromFile**](getexternalkeyfromfile-win32-encryptablevolume.md)                                         | Gibt den externen Schlüssel aus einer Datei zurück.<br/>                                                                                                                                                                                                                                      |
| [**GetHardwareTestStatus**](gethardwareteststatus-win32-encryptablevolume.md)                                           | Gibt Statusinformationen zu einem Hardwaretest zurück.<br/>                                                                                                                                                                                                                             |
| [**GetIdentificationField**](getidentificationfield-win32-encryptablevolume.md)                                         | Gibt die Bezeichnerzeichenfolge zurück, die in den Metadaten des Volumes verfügbar ist.<br/>                                                                                                                                                                                                  |
| [**GetKeyPackage**](getkeypackage-win32-encryptablevolume.md)                                                           | Gibt Informationen zurück, die dazu beitragen, verschlüsselte Daten zu wiederherstellen, wenn das Laufwerk stark beschädigt ist.<br/>                                                                                                                                                                              |
| [**GetKeyProtectorCertificate**](getkeyprotectorcertificate-win32-encryptablevolume.md)                                 | Ruft den öffentlichen Schlüssel und den Zertifikatfingerabdruck für eine Schutzvorrichtung für öffentliche Schlüssel ab.<br/>                                                                                                                                                                                            |
| [**GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md)                                 | Ruft den externen Schlüssel für eine bestimmte Schlüsselschutzvorrichtung des entsprechenden Typs ab.<br/>                                                                                                                                                                                              |
| [**GetKeyProtectorFriendlyName**](getkeyprotectorfriendlyname-win32-encryptablevolume.md)                               | Ruft den Anzeigenamen ab, mit dem eine bestimmte Schlüsselschutzvorrichtung identifiziert wird.<br/>                                                                                                                                                                                                         |
| [**GetKeyProtectorNumericalPassword**](getkeyprotectornumericalpassword-win32-encryptablevolume.md)                     | Ruft das numerische Kennwort für eine bestimmte Schlüsselschutzvorrichtung des entsprechenden Typs ab.<br/>                                                                                                                                                                                        |
| [**GetKeyProtectorPlatformValidationProfile**](getkeyprotectorplatformvalidationprofile-win32-encryptablevolume.md)     | Ruft das Plattformvalidierungsprofil für eine bestimmte Schlüsselschutzvorrichtung des entsprechenden Typs ab.<br/>                                                                                                                                                                               |
| [**GetKeyProtectors**](getkeyprotectors-win32-encryptablevolume.md)                                                     | Listet die Schutzvorrichtungen auf, die zum Schützen des Verschlüsselungsschlüssels des Volumes verwendet werden.<br/>                                                                                                                                                                                                           |
| [**GetKeyProtectorType**](getkeyprotectortype-win32-encryptablevolume.md)                                               | Gibt den Typ einer bestimmten Schlüsselschutzvorrichtung an.<br/>                                                                                                                                                                                                                               |
| [**GetLockStatus**](getlockstatus-win32-encryptablevolume.md)                                                           | Gibt an, ob vom derzeit ausgeführten Betriebssystem aus auf den Inhalt des Volumes zugegriffen werden kann.<br/>                                                                                                                                                                   |
| [**GetProtectionStatus**](getprotectionstatus-win32-encryptablevolume.md)                                               | Gibt an, ob das Volume und sein Verschlüsselungsschlüssel (falls erforderlich) geschützt sind.<br/>                                                                                                                                                                                                  |
| [**Getversion**](getversion-win32-encryptablevolume.md)                                                                 | Gibt die FVE-Metadatenversion des Volumes an.<br/>                                                                                                                                                                                                                          |
| [**IsAutoUnlockEnabled**](isautounlockenabled-win32-encryptablevolume.md)                                               | Gibt an, ob das Volume automatisch entsperrt wird, wenn es bereitgestellt wird.<br/>                                                                                                                                                                                                       |
| [**IsAutoUnlockKeyStored**](isautounlockkeystored-win32-encryptablevolume.md)                                           | Gibt an, ob auf dem aktuell ausgeführten Betriebssystemvolume externe Schlüssel und zugehörige Informationen vorhanden sind, die zum automatischen Entsperren von Datenvolumes verwendet werden können.<br/>                                                                                           |
| [**IsKeyProtectorAvailable**](iskeyprotectoravailable-win32-encryptablevolume.md)                                       | Gibt an, ob Schutzvorrichtungen für das Volume verfügbar sind.<br/>                                                                                                                                                                                                                 |
| [**IsNumericalPasswordValid**](isnumericalpasswordvalid-win32-encryptablevolume.md)                                     | Gibt an, ob das numerische Kennwort die speziellen Formatanforderungen erfüllt.<br/>                                                                                                                                                                                            |
| [**Sperre**](lock-win32-encryptablevolume.md)                                                                             | Entfernt die Bereitstellung des Volumes und entfernt den Verschlüsselungsschlüssel des Volumes aus dem Systemspeicher.<br/>                                                                                                                                                                                           |
| [**PauseConversion**](pauseconversion-win32-encryptablevolume.md)                                                       | Hält die Verschlüsselung oder Entschlüsselung eines Volumes an.<br/>                                                                                                                                                                                                                           |
| [**PrepareVolume**](preparevolume-win32-encryptablevolume.md)                                                           | Erstellt ein BitLocker-Volume mit dem angegebenen Dateisystemtyp des Ermittlungsvolumens.<br/>                                                                                                                                                                                    |
| [**ProtectKeyWithCertificateFile**](protectkeywithcertificatefile-win32-encryptablevolume.md)                           | Überprüft den OID (Enhanced Key Usage)-Objektbezeichner (Enhanced Key Usage, erweiterte Schlüsselverwendung) der bereitgestellten Zertifikatdatei.<br/>                                                                                                                                                                           |
| [**ProtectKeyWithCertificateThumbprint**](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)               | Überprüft den EKU-Objektbezeichner (Enhanced Key Usage, erweiterte Schlüsselverwendung) des bereitgestellten Zertifikatfingerabdrucks.<br/>                                                                                                                                                                     |
| [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md)                                   | Sichert den Verschlüsselungsschlüssel des Volumes mit einem externen 256-Bit-Schlüssel.<br/>                                                                                                                                                                                                           |
| [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md)                       | Sichert den Verschlüsselungsschlüssel des Volumes mit einem speziell formatierten 48-stelligen Kennwort.<br/>                                                                                                                                                                                          |
| [**ProtectKeyWithPassphrase**](protectkeywithpassphrase-win32-encryptablevolume.md)                                     | Verwendet die Passphrase, um den abgeleiteten Schlüssel zu erhalten.<br/>                                                                                                                                                                                                                             |
| [**ProtectKeyWithTPM**](protectkeywithtpm-win32-encryptablevolume.md)                                                   | Sichert den Verschlüsselungsschlüssel des Volumes mithilfe der Trusted Platform Module -Sicherheitshardware (TPM) auf dem Computer, sofern verfügbar.<br/>                                                                                                                                            |
| [**ProtectKeyWithTPMAndPIN**](protectkeywithtpmandpin-win32-encryptablevolume.md)                                       | Sichert den Verschlüsselungsschlüssel des Volumes mithilfe der Trusted Platform Module-Sicherheitshardware (TPM) auf dem Computer, sofern verfügbar, erweitert durch eine vom Benutzer angegebene persönliche IDENTIFIKATIONsnummer (PIN), die dem Computer beim Start bereitgestellt werden muss.<br/>                        |
| [**ProtectKeyWithTPMAndPINAndStartupKey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)             | Sichert den Verschlüsselungsschlüssel des Volumes mithilfe der Trusted Platform Module-Sicherheitshardware (TPM) auf dem Computer, sofern verfügbar, erweitert durch eine vom Benutzer angegebene persönliche ID (PIN) und durch einen externen Schlüssel, der dem Computer beim Start bereitgestellt werden muss.<br/> |
| [**ProtectKeyWithTPMAndStartupKey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)                         | Sichert den Verschlüsselungsschlüssel des Volumes mithilfe der Trusted Platform Module-Sicherheitshardware (TPM) auf dem Computer, sofern verfügbar, erweitert durch einen externen Schlüssel, der dem Computer beim Start bereitgestellt werden muss.<br/>                                                              |
| [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md)                                                     | Setzt die Verschlüsselung oder Entschlüsselung eines Volumes wieder auf.<br/>                                                                                                                                                                                                                          |
| [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md)                                           | Schreibt den externen Schlüssel, der der angegebenen Volumeschlüsselschutzvorrichtung zugeordnet ist, an einen angegebenen Dateispeicherort.<br/>                                                                                                                                                                   |
| [**SetIdentificationField**](setidentificationfield-win32-encryptablevolume.md)                                         | Legt die angegebene Bezeichnerzeichenfolge in den Metadaten des Volumes fest.<br/>                                                                                                                                                                                                             |
| [**UnlockWithCertificateFile**](unlockwithcertificatefile-win32-encryptablevolume.md)                                   | Verwendet die bereitgestellte Zertifikatdatei, um den abgeleiteten Schlüssel zu erhalten und das verschlüsselte Volume zu entsperren.<br/>                                                                                                                                                                              |
| [**UnlockWithCertificateThumbprint**](unlockwithcertificatethumbprint-win32-encryptablevolume.md)                       | Verwendet den bereitgestellten Zertifikatfingerabdruck, um den abgeleiteten Schlüssel zu erhalten und das verschlüsselte Volume zu entsperren.<br/>                                                                                                                                                                        |
| [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md)                                           | Verwendet einen bereitgestellten externen Schlüssel für den Zugriff auf den Inhalt eines Datenvolumens.<br/>                                                                                                                                                                                                      |
| [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md)                               | Verwendet ein bereitgestelltes numerisches Kennwort für den Zugriff auf den Inhalt eines Datenvolumens.<br/>                                                                                                                                                                                                |
| [**UnlockWithPassphrase**](unlockwithpassphrase-win32-encryptablevolume.md)                                             | Verwendet die Passphrase, um den abgeleiteten Schlüssel zu erhalten. Nachdem der abgeleitete Schlüssel berechnet wurde, wird der abgeleitete Schlüssel verwendet, um den Hauptschlüssel des verschlüsselten Volumes zu entsperren.<br/>                                                                                                                   |
| [**UpgradeVolume**](upgradevolume-win32-encryptablevolume.md)                                                           | Aktualisiert ein Volume vom Windows Vista-Format auf das Windows 7-Format.<br/>                                                                                                                                                                                                   |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ EncryptableVolume-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Deviceid**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Ein eindeutiger Bezeichner für das Volume auf diesem System. Verwenden Sie diese, um ein Volume anderen WMI-Anbieterklassen zu zuordnen, z. B. **Win32 \_ Volume**.

</dd> <dt>

**DriveLetter**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Laufwerkbuchstaben des Volumes. Dieser Bezeichner kann verwendet werden, um ein Volume anderen WMI-Anbieterklassen zu zuordnen, z. B. [**Win32 \_ Volume**](/previous-versions/windows/desktop/legacy/aa394515(v=vs.85)).

Bei Volumes ohne Laufwerkbuchstaben ist dieser Wert **NULL.**

</dd> <dt>

**PersistentVolumeID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein persistenter Bezeichner für das Volume auf diesem System. Dieser Bezeichner gilt ausschließlich für **Win32 \_ EncryptableVolume.**

Dieser Bezeichner ist eine leere Zeichenfolge, wenn es sich bei dem Volume um ein standardmäßiges, vollständig entschlüsseltes NTFS-Volume handelt. andernfalls hat sie einen eindeutigen Wert.

</dd> <dt>

**ProtectionStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Status des Volumes, unabhängig davon, ob BitLocker das Volume schützt. Dieser Wert wird gespeichert, wenn die Klasse instanziiert wird. Es ist möglich, dass der Schutzstatus den Zustand zwischen der Instanziierung und dem Überprüfen des Werts ändert. Verwenden Sie die [**GetProtectionStatus-Methode,**](getprotectionstatus-win32-encryptablevolume.md) um den Wert der **ProtectionStatus-Eigenschaft** in Echtzeit zu überprüfen.



| Wert                                                                        | Bedeutung                                                                                                                                                                           |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | PROTECTION OFF<br/> Das Volume ist nicht verschlüsselt, teilweise verschlüsselt, oder der Verschlüsselungsschlüssel des Volumes für das Volume ist auf der Festplatte eindeutig verfügbar. <br/> |
| <dl> <dt>1</dt> </dl> | PROTECTION ON<br/> Das Volume ist vollständig verschlüsselt, und der Verschlüsselungsschlüssel für das Volume ist auf der Festplatte nicht eindeutig verfügbar. <br/>                          |
| <dl> <dt>2</dt> </dl> | SCHUTZ UNBEKANNT<br/> Der Volumeschutzstatus kann nicht bestimmt werden. Eine mögliche Ursache ist, dass sich das Volume in einem gesperrten Zustand befindet.<br/>                          |



 

</dd> </dl>

## <a name="security-considerations"></a>Überlegungen zur Sicherheit

Die WMI-Anbieterklasse **\_ "Win32 EncryptableVolume"** basiert auf der WMI-Namespacesicherheit und auf dem BitLocker-Laufwerkverschlüsselung-Subsystem für die Zugriffssteuerung.

Um die **Win32 \_ EncryptableVolume-Methoden verwenden zu** können, müssen die folgenden Bedingungen erfüllt sein:

-   Sie müssen über Administratorrechte verfügen.
-   Die Verbindungsverschlüsselung muss eine Verbindung mit dem Anbieter herstellen können.

    Weitere Informationen zum Erstellen einer verschlüsselten Verbindung finden Sie unter [Erfordern einer verschlüsselten Verbindung mit einem Namespace.](../wmisdk/requiring-an-encrypted-connection-to-a-namespace.md)

Um Remoteverbindungen zu aktivieren, muss WMI-Remotedatenverkehr zugelassen werden. Weitere Informationen zum Aktivieren von WMI-Datenverkehr finden Sie unter Herstellen einer Remoteverbindung [mit WMI ab Vista.](../wmisdk/connecting-to-wmi-remotely-starting-with-vista.md)

Die Standardeinstellung für die Namespacesicherheit enthält einen Eintrag, um die Bearbeitung standardmäßig zu ermöglichen. Weitere Informationen zur Überwachung von WMI-Namespaces finden Sie unter [Zugriff auf WMI-Namespaces.](../wmisdk/access-to-wmi-namespaces.md)

## <a name="remarks"></a>Hinweise

Managed Object Format (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Enterprise, Windows Vista \[ Ultimate-Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\CimV2-Stammsicherheit \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



 

 
