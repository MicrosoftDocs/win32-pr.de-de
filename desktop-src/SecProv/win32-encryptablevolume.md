---
description: Für die Laufwerk Verschlüsselung oder zum Erstellen von Verschlüsselungs Sicherheitssoftware können Sie die Windows-Verschlüsselungssoftware (BitLocker-Laufwerkverschlüsselung) verwenden, um eine Verschlüsselungs-API zu verwenden, die Sie mithilfe der \_ WMI-Anbieter Klasse "Win32 verschlüsseltablevolume" verwenden können.
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
ms.openlocfilehash: b202a536f3c20126c05f072c029fe316f90ce4fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958829"
---
# <a name="win32_encryptablevolume-class"></a>Win32- \_ Klasse "verschlüsseltablevolume"

Die WMI-Anbieter Klasse " **Win32 \_ verschlüsseltablevolume** " stellt einen Speicherbereich auf einer Festplatte dar, der mithilfe von BitLocker-Laufwerkverschlüsselung geschützt werden kann. Nur NTFS-Volumes können verschlüsselt werden. Dabei kann es sich um ein Volume mit einem Betriebssystem oder ein Daten Volume auf dem lokalen Datenträger handeln. Es darf sich nicht um ein Netzwerklaufwerk handeln.

Um die Vorteile von BitLocker zu nutzen, müssen Sie eine Schutzmethode für den Verschlüsselungsschlüssel des Volumes angeben und dann das Volume vollständig verschlüsseln.

Fügen Sie zum Schutz des Verschlüsselungsschlüssels des Volumes Schlüssel Schutzvorrichtungen mithilfe der folgenden Methoden hinzu:

-   [**Protectkeywithcertificatefile**](protectkeywithcertificatefile-win32-encryptablevolume.md)
-   [**Protectkeywithcertifierkeybibprint**](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
-   [**Protectkeywithexternalkey**](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [**Protectkeywithnumericalpassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md)
-   [**Protectkeywithpasspphrase**](protectkeywithpassphrase-win32-encryptablevolume.md)
-   [**Protectkeywithtpm**](protectkeywithtpm-win32-encryptablevolume.md)
-   [**Protectkeywithtpmandpin**](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [**Protectkeywithtpmandpinandstartupkey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [**Protectkeywithtpmandstartupkey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

Jeder Typ der Schlüssel Schutzvorrichtung bietet eine andere Authentifizierungs Möglichkeit, um den Zugriff auf die verschlüsselten Daten zu entsperren. Externe Schlüssel und numerische Kenn Wörter können während Wiederherstellungs Szenarien Authentifizierung bereitstellen. Bei TPM-basierten Schlüssel Schutzvorrichtungen muss das TPM möglicherweise zuerst ordnungsgemäß initialisiert werden. Weitere Informationen finden Sie in der WMI-Anbieter Klasse für den [**Win32- \_ TPM**](win32-tpm.md) .

Verwenden Sie die Encryption [**-oder**](encrypt-win32-encryptablevolume.md) [**verschlüsseltafterhardwaretest**](encryptafterhardwaretest-win32-encryptablevolume.md) -Methode, um die Verschlüsselung zu starten. Vor dem Starten der Verschlüsselung müssen Schlüssel Schutzvorrichtungen hinzugefügt werden. andernfalls müssen Sie die [**disablekeyprotector**](disablekeyprotectors-win32-encryptablevolume.md) -Methode verwenden, um einen ungeschützten ungeschützten Schlüssel verfügbar zu machen. Wenn der Computer ausgeschaltet wird, während die Verschlüsselung ausgeführt wird, wird die Verschlüsselung automatisch fortgesetzt, wenn der Computer neu gestartet wird.

Sie können den Status eines barrierefreien Volumes mithilfe der Methoden [**getby versionstatus**](getconversionstatus-win32-encryptablevolume.md) und [**getschutzstatus**](getprotectionstatus-win32-encryptablevolume.md) überprüfen.

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

Die Win32-Klasse " **\_ verschlüsseltablevolume** " verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die Win32-Klasse " **\_ verschlüsseltablevolume** " verfügt über diese Methoden.



| Methode                                                                                                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Backuprecoveryinformationbackactivedirectory**](backuprecoveryinformationtoactivedirectory-win32-encryptablevolume.md) | Speichert alle externen Schlüssel und zugehörigen Informationen, die für die Wiederherstellung im Active Directory benötigt werden.<br/>                                                                                                                                                                       |
| [**Changeexternalkey**](changeexternalkey-win32-encryptablevolume.md)                                                   | Ändert den externen Schlüssel, der einem verschlüsselten Volume zugeordnet ist.<br/>                                                                                                                                                                                                              |
| [**Changepasspphrase**](changepassphrase-win32-encryptablevolume.md)                                                     | Verwendet die neue Passphrase zum Abrufen eines neuen abgeleiteten Schlüssels.<br/>                                                                                                                                                                                                                       |
| [**Changepin**](changepin-win32-encryptablevolume.md)                                                                   | Ändert eine PIN, die einem verschlüsselten Volume zugeordnet ist.<br/>                                                                                                                                                                                                                         |
| [**Clearallautounlockkeys**](clearallautounlockkeys-win32-encryptablevolume.md)                                         | Entfernt alle externen Schlüssel und zugehörigen Informationen, die auf dem momentan laufenden Betriebssystem Volume gespeichert sind, das zum automatischen Entsperren von Datenvolumes verwendet wird.<br/>                                                                                                             |
| [**Entschlüsseln**](decrypt-win32-encryptablevolume.md)                                                                       | Startet die Entschlüsselung eines vollständig verschlüsselten Volumes oder setzt das Entschlüsseln eines teilweise verschlüsselten Volumes fort.<br/>                                                                                                                                                                       |
| [**Deletekeyprotector**](deletekeyprotector-win32-encryptablevolume.md)                                                 | Löscht eine angegebene Schlüssel Schutzvorrichtung für das Volume.<br/>                                                                                                                                                                                                                              |
| [**Deletekeyprotector**](deletekeyprotectors-win32-encryptablevolume.md)                                               | Löscht alle Schlüssel Schutzvorrichtungen für das Volume.<br/>                                                                                                                                                                                                                                 |
| [**Disableautounlock**](disableautounlock-win32-encryptablevolume.md)                                                   | Entfernt den externen Schlüssel, der auf dem aktuell laufenden Betriebssystem Volume gespeichert ist, sodass das Volume bei der Bereitstellung nicht automatisch entsperrt wird.<br/>                                                                                                                       |
| [**Disablekeyprotector**](disablekeyprotectors-win32-encryptablevolume.md)                                             | Deaktiviert alle diesem Volume zugeordneten Schlüssel Schutzvorrichtungen.<br/>                                                                                                                                                                                                                   |
| [**Enableautounlock**](enableautounlock-win32-encryptablevolume.md)                                                     | Ermöglicht das automatische Entsperren eines Datenvolumens, wenn das Volume eingebunden wird.<br/>                                                                                                                                                                                              |
| [**Enablekeyprotector**](enablekeyprotectors-win32-encryptablevolume.md)                                               | Aktiviert alle deaktivierten Schlüsselschutz Vorrichtungen.<br/>                                                                                                                                                                                                                                       |
| [**Verschlüsseln**](encrypt-win32-encryptablevolume.md)                                                                       | Startet die Verschlüsselung eines vollständig entschlüsselten Volumes oder nimmt die Verschlüsselung eines teilweise verschlüsselten Volumes wieder auf.<br/>                                                                                                                                                                       |
| [**Verschlüsselter Test**](encryptafterhardwaretest-win32-encryptablevolume.md)                                     | Startet die Verschlüsselung eines vollständig entschlüsselten Volumes nach einem Hardware Test.<br/>                                                                                                                                                                                                       |
| [**Findvalidzertifikate**](findvalidcertificates-win32-encryptablevolume.md)                                           | Listet alle Zertifikate auf dem System auf, die mit den angegebenen Kriterien übereinstimmen, und gibt eine Liste von Fingerabdrücken zurück.<br/>                                                                                                                                                             |
| [**Getsystemversionstatus**](getconversionstatus-win32-encryptablevolume.md)                                               | Gibt den Status der Verschlüsselung oder Entschlüsselung auf dem Volume an.<br/>                                                                                                                                                                                                        |
| [**Getencryptionmethod**](getencryptionmethod-win32-encryptablevolume.md)                                               | Gibt den Verschlüsselungsalgorithmus und die Schlüsselgröße an, die auf dem Volume verwendet werden.<br/>                                                                                                                                                                                                        |
| [**Getexternalkeyfilename**](getexternalkeyfilename-win32-encryptablevolume.md)                                         | Gibt den Namen der Datei zurück, die den externen Schlüssel enthält.<br/>                                                                                                                                                                                                               |
| [**Getexternalkeyfromfile**](getexternalkeyfromfile-win32-encryptablevolume.md)                                         | Gibt den externen Schlüssel aus einer Datei zurück.<br/>                                                                                                                                                                                                                                      |
| [**Gethardwareteststatus**](gethardwareteststatus-win32-encryptablevolume.md)                                           | Gibt Statusinformationen zu einem Hardware Test zurück.<br/>                                                                                                                                                                                                                             |
| [**Getidentificationfield**](getidentificationfield-win32-encryptablevolume.md)                                         | Gibt die Bezeichnerzeichenfolge zurück, die in den Metadaten des Volumes verfügbar ist.<br/>                                                                                                                                                                                                  |
| [**Getkeypackage**](getkeypackage-win32-encryptablevolume.md)                                                           | Gibt Informationen zurück, die die Wiederherstellung verschlüsselter Daten unterstützen, wenn das Laufwerk stark beschädigt ist.<br/>                                                                                                                                                                              |
| [**Getkeyprotector Certificate**](getkeyprotectorcertificate-win32-encryptablevolume.md)                                 | Ruft den öffentlichen Schlüssel und den Zertifikat Fingerabdruck für die Schutzvorrichtung eines öffentlichen Schlüssels ab.<br/>                                                                                                                                                                                            |
| [**Getkeyprotector ExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md)                                 | Ruft den externen Schlüssel für eine angegebene Schlüssel Schutzvorrichtung des entsprechenden Typs ab.<br/>                                                                                                                                                                                              |
| [**Getkeyprotector FriendlyName**](getkeyprotectorfriendlyname-win32-encryptablevolume.md)                               | Ruft den anzeigen Amen ab, der verwendet wird, um eine angegebene Schlüssel Schutzvorrichtung zu identifizieren.<br/>                                                                                                                                                                                                         |
| [**Getkeyprotector numericalpassword**](getkeyprotectornumericalpassword-win32-encryptablevolume.md)                     | Ruft das numerische Kennwort für eine angegebene Schlüssel Schutzvorrichtung des entsprechenden Typs ab.<br/>                                                                                                                                                                                        |
| [**Getkeyprotector platformvalidationprofile**](getkeyprotectorplatformvalidationprofile-win32-encryptablevolume.md)     | Ruft das Platt Form Validierungs Profil für eine angegebene Schlüssel Schutzvorrichtung des entsprechenden Typs ab.<br/>                                                                                                                                                                               |
| [**Getkeyprotector**](getkeyprotectors-win32-encryptablevolume.md)                                                     | Listet die Schutzvorrichtungen auf, mit denen der Verschlüsselungsschlüssel des Volumes geschützt wird.<br/>                                                                                                                                                                                                           |
| [**Getkeyprotector Type**](getkeyprotectortype-win32-encryptablevolume.md)                                               | Gibt den Typ einer angegebenen Schlüssel Schutzvorrichtung an.<br/>                                                                                                                                                                                                                               |
| [**Getlockstatus**](getlockstatus-win32-encryptablevolume.md)                                                           | Gibt an, ob der Inhalt des Volumes von dem aktuell laufenden Betriebssystem aus zugänglich ist.<br/>                                                                                                                                                                   |
| [**Getschutzstatus**](getprotectionstatus-win32-encryptablevolume.md)                                               | Gibt an, ob das Volume und der zugehörige Verschlüsselungsschlüssel (sofern vorhanden) gesichert sind.<br/>                                                                                                                                                                                                  |
| [**GetVersion**](getversion-win32-encryptablevolume.md)                                                                 | Gibt die Version der Vollversion des Volumes an.<br/>                                                                                                                                                                                                                          |
| [**Isautounlockaktivierte**](isautounlockenabled-win32-encryptablevolume.md)                                               | Gibt an, ob das Volume bei der Bereitstellung automatisch entsperrt wird.<br/>                                                                                                                                                                                                       |
| [**Isautounlockkeygespeicherter**](isautounlockkeystored-win32-encryptablevolume.md)                                           | Gibt an, ob das aktuell vorhandene Betriebssystem Volume externe Schlüssel und zugehörige Informationen enthält, die zum automatischen Entsperren von Datenvolumes verwendet werden können.<br/>                                                                                           |
| [**Iskeyprotector available**](iskeyprotectoravailable-win32-encryptablevolume.md)                                       | Gibt an, ob Schutzvorrichtungen für das Volume verfügbar sind.<br/>                                                                                                                                                                                                                 |
| [**Isnumericalpasswordvalid**](isnumericalpasswordvalid-win32-encryptablevolume.md)                                     | Gibt an, ob das numerische Kennwort den speziellen Formatanforderungen entspricht.<br/>                                                                                                                                                                                            |
| [**Sperre**](lock-win32-encryptablevolume.md)                                                                             | Hebt die Bereitstellung des Volumes auf und entfernt den Verschlüsselungsschlüssel des Volumes aus dem System Arbeitsspeicher.<br/>                                                                                                                                                                                           |
| [**Pauseconversion**](pauseconversion-win32-encryptablevolume.md)                                                       | Hält die Verschlüsselung oder Entschlüsselung eines Volumes an.<br/>                                                                                                                                                                                                                           |
| [**Preparevolume**](preparevolume-win32-encryptablevolume.md)                                                           | Erstellt ein BitLocker-Volume mit dem angegebenen Dateisystemtyp des Discovery-Volumes.<br/>                                                                                                                                                                                    |
| [**Protectkeywithcertificatefile**](protectkeywithcertificatefile-win32-encryptablevolume.md)                           | Überprüft die EKU-Objekt Kennung (Enhanced Key Usage, EKU) der angegebenen Zertifikatsdatei.<br/>                                                                                                                                                                           |
| [**Protectkeywithcertifierkeybibprint**](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)               | Überprüft die EKU-Objekt Kennung (Enhanced Key Usage, EKU) des angegebenen Zertifikat Fingerabdrucks.<br/>                                                                                                                                                                     |
| [**Protectkeywithexternalkey**](protectkeywithexternalkey-win32-encryptablevolume.md)                                   | Sichert den Verschlüsselungsschlüssel des Volumes mit einem externen 256-Bit-Schlüssel.<br/>                                                                                                                                                                                                           |
| [**Protectkeywithnumericalpassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md)                       | Sichert den Verschlüsselungsschlüssel des Volumes mit einem speziell formatierten 48-stelligen Kennwort.<br/>                                                                                                                                                                                          |
| [**Protectkeywithpasspphrase**](protectkeywithpassphrase-win32-encryptablevolume.md)                                     | Verwendet die Passphrase zum Abrufen des abgeleiteten Schlüssels.<br/>                                                                                                                                                                                                                             |
| [**Protectkeywithtpm**](protectkeywithtpm-win32-encryptablevolume.md)                                                   | Sichert den Verschlüsselungsschlüssel des Volumes mithilfe der Trusted Platform Module (TPM)-Sicherheits Hardware auf dem Computer (falls verfügbar).<br/>                                                                                                                                            |
| [**Protectkeywithtpmandpin**](protectkeywithtpmandpin-win32-encryptablevolume.md)                                       | Sichert den Verschlüsselungsschlüssel des Volumes mithilfe der TPM-Sicherheits Hardware (Trusted Platform Module) auf dem Computer, sofern verfügbar, erweitert durch eine benutzerdefinierte ID (Personal Identification Number, PIN), die dem Computer beim startbereit gestellt werden muss.<br/>                        |
| [**Protectkeywithtpmandpinandstartupkey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)             | Sichert den Verschlüsselungsschlüssel des Volumes mithilfe der TPM-Sicherheits Hardware (Trusted Platform Module) auf dem Computer, sofern verfügbar, erweitert durch eine benutzerdefinierte ID (Personal Identification Number, PIN) und durch einen externen Schlüssel, der beim Start für den Computer bereitgestellt werden muss.<br/> |
| [**Protectkeywithtpmandstartupkey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)                         | Sichert den Verschlüsselungsschlüssel des Volumes mithilfe der TPM-Sicherheits Hardware (Trusted Platform Module) auf dem Computer, sofern verfügbar, erweitert durch einen externen Schlüssel, der beim Start für den Computer bereitgestellt werden muss.<br/>                                                              |
| [**Resumeconversion**](resumeconversion-win32-encryptablevolume.md)                                                     | Nimmt die Verschlüsselung oder Entschlüsselung eines Volumes wieder auf.<br/>                                                                                                                                                                                                                          |
| [**Saveexternalkeydefile**](saveexternalkeytofile-win32-encryptablevolume.md)                                           | Schreibt den externen Schlüssel, der der angegebenen volumeschlüsselschutzvorrichtung zugeordnet ist, in einen angegebenen Datei Speicherort.<br/>                                                                                                                                                                   |
| [**"Cationfield"**](setidentificationfield-win32-encryptablevolume.md)                                         | Legt die angegebene Bezeichnerzeichenfolge in den Metadaten des Volumes fest.<br/>                                                                                                                                                                                                             |
| [**Unlockwithcertificatefile**](unlockwithcertificatefile-win32-encryptablevolume.md)                                   | Verwendet die angegebene Zertifikat Datei, um den abgeleiteten Schlüssel abzurufen und das verschlüsselte Volume zu entsperren.<br/>                                                                                                                                                                              |
| [**Unlockwithcertifierethbibprint**](unlockwithcertificatethumbprint-win32-encryptablevolume.md)                       | Verwendet den angegebenen Zertifikat Fingerabdruck, um den abgeleiteten Schlüssel abzurufen und das verschlüsselte Volume zu entsperren.<br/>                                                                                                                                                                        |
| [**Unlockwithexternalkey**](unlockwithexternalkey-win32-encryptablevolume.md)                                           | Verwendet einen bereitgestellten externen Schlüssel für den Zugriff auf den Inhalt eines Datenvolumens.<br/>                                                                                                                                                                                                      |
| [**Unlockwithnumericalpassword**](unlockwithnumericalpassword-win32-encryptablevolume.md)                               | Verwendet ein bereitgestelltes numerisches Kennwort für den Zugriff auf den Inhalt eines Datenvolumens.<br/>                                                                                                                                                                                                |
| [**Unlockwithpasspphrase**](unlockwithpassphrase-win32-encryptablevolume.md)                                             | Verwendet die Passphrase zum Abrufen des abgeleiteten Schlüssels. Nachdem der abgeleitete Schlüssel berechnet wurde, wird der abgeleitete Schlüssel verwendet, um den Hauptschlüssel des verschlüsselten Volumes zu entsperren.<br/>                                                                                                                   |
| [**Upgradezvolume**](upgradevolume-win32-encryptablevolume.md)                                                           | Aktualisiert ein Volume vom Windows Vista-Format auf das Windows 7-Format.<br/>                                                                                                                                                                                                   |



 

### <a name="properties"></a>Eigenschaften

Die Win32-Klasse " **\_ verschlüsseltablevolume** " verfügt über diese Eigenschaften.

<dl> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Ein eindeutiger Bezeichner für das Volume auf diesem System. Verwenden Sie diese Informationen, um einem Volume andere WMI-Anbieter Klassen zuzuordnen, z. b. **Win32- \_ Volume**.

</dd> <dt>

**DriveLetter**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Laufwerk Buchstabe des Volumes. Dieser Bezeichner kann verwendet werden, um ein Volume anderen WMI-Anbieter Klassen zuzuordnen, z. b. [**Win32- \_ Volume**](/previous-versions/windows/desktop/legacy/aa394515(v=vs.85)).

Für Volumes ohne Laufwerk Buchstaben ist dieser Wert **null**.

</dd> <dt>

**Persistentvolumeid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein beständiger Bezeichner für das Volume auf diesem System. Dieser Bezeichner ist exklusiv für **Win32 \_ verschlüsseltablevolume**.

Dieser Bezeichner ist eine leere Zeichenfolge, wenn das Volume ein Standardmäßiges vollständig entschlüsselter NTFS-Volume ist. Andernfalls hat Sie einen eindeutigen Wert.

</dd> <dt>

**ProtectionStatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Status des Volumes, unabhängig davon, ob BitLocker das Volume schützt. Dieser Wert wird gespeichert, wenn die-Klasse instanziiert wird. Der Schutzstatus kann den Status zwischen der Instanziierung und dem Zeitpunkt der Überprüfung des Werts ändern. Verwenden Sie die [**getschutzstatus**](getprotectionstatus-win32-encryptablevolume.md) -Methode, um den Wert der Eigenschaft " **Schutzstatus** " in Echtzeit zu überprüfen.



| Wert                                                                        | Bedeutung                                                                                                                                                                           |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Schutz deaktiviert<br/> Das Volume ist nicht verschlüsselt, teilweise verschlüsselt, oder der Verschlüsselungsschlüssel des Volumes für das Volume ist im Klartext auf der Festplatte verfügbar. <br/> |
| <dl> <dt>1</dt> </dl> | Schutz für<br/> Das Volume ist vollständig verschlüsselt, und der Verschlüsselungsschlüssel für das Volume ist nicht im Klartext auf der Festplatte verfügbar. <br/>                          |
| <dl> <dt>2</dt> </dl> | Schutz unbekannt<br/> Der volumeschutzstatus kann nicht bestimmt werden. Eine mögliche Ursache ist, dass sich das Volume im gesperrten Zustand befindet.<br/>                          |



 

</dd> </dl>

## <a name="security-considerations"></a>Überlegungen zur Sicherheit

Die **Win32 \_ verschlüsseltablevolume** -WMI-Anbieter Klasse basiert auf der WMI-Namespace Sicherheit und auf dem BitLocker-Laufwerkverschlüsselung Subsystem für die Zugriffs Steuerung.

Die folgenden Bedingungen müssen erfüllt sein, damit die Win32-Methoden **\_ verschlüsseltablevolume** verwendet werden können:

-   Sie müssen über Administratorrechte verfügen.
-   Die Verbindungs Verschlüsselung muss in der Lage sein, eine Verbindung mit dem Anbieter herzustellen.

    Weitere Informationen zum Erstellen einer verschlüsselten Verbindung finden Sie unter [erfordern einer verschlüsselten Verbindung mit einem Namespace](../wmisdk/requiring-an-encrypted-connection-to-a-namespace.md).

Um Remote Verbindungen zu aktivieren, muss der WMI-Remote Datenverkehr zugelassen werden. Weitere Informationen zum Aktivieren des WMI-Datenverkehrs finden [Sie unter Herstellen einer Remote Verbindung mit WMI ab Vista](../wmisdk/connecting-to-wmi-remotely-starting-with-vista.md).

Die Standardeinstellung für den-Namespace enthält einen Eintrag, der die Bearbeitung standardmäßig zulässt. Weitere Informationen zur Überwachung von WMI- [Namespaces finden Sie unter Zugreifen auf WMI-Namespaces](../wmisdk/access-to-wmi-namespaces.md).

## <a name="remarks"></a>Bemerkungen

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ verschlüsseltablevolume. MOF</dt> </dl> |



 

 
