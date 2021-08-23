---
description: Wenn das Trusted Platform Module (TPM) verfügbar ist, sichert diese Methode den Verschlüsselungsschlüssel des Volumes.
ms.assetid: 79bee9ca-c86a-482b-a06f-1cfb887e7fae
title: ProtectKeyWithTPM-Methode der Win32_EncryptableVolume Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithTPM
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f7e9c2c424ea84436292158753de29294bbce3a5516b5ab0a9149892640963ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119667170"
---
# <a name="protectkeywithtpm-method-of-the-win32_encryptablevolume-class"></a>ProtectKeyWithTPM-Methode der Win32 \_ EncryptableVolume-Klasse

Die **ProtectKeyWithTPM-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) sichert den Verschlüsselungsschlüssel des Volumes mithilfe der Trusted Platform Module-Sicherheitshardware (TPM) auf dem Computer, sofern verfügbar.

Für das Volume wird eine Schlüsselschutzvorrichtung vom Typ "TPM" erstellt, sofern noch keine vorhanden ist.

Diese Methode gilt nur für das Volume, das das derzeit ausgeführte Betriebssystem enthält, und , wenn noch keine Schlüsselschutzvorrichtung auf dem Volume vorhanden ist.

## <a name="syntax"></a>Syntax


```mof
uint32 ProtectKeyWithTPM(
  [in, optional] string FriendlyName,
  [in, optional] uint8  PlatformValidationProfile[],
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FriendlyName* \[ in, optional\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die einen vom Benutzer zugewiesenen Zeichenfolgenbezeichner für diese Schlüsselschutzvorrichtung angibt. Wenn dieser Parameter nicht angegeben wird, wird ein leerer Wert verwendet.

</dd> <dt>

*PlatformValidationProfile* \[ in, optional\]
</dt> <dd>

Typ: **uint8 \[ \]**

Ein Array von ganzen Zahlen, das angibt, wie die Trusted Platform Module-Sicherheitshardware (TPM) des Computers den Verschlüsselungsschlüssel des Datenträgerdatenträgers sichert.

Ein Plattformvalidierungsprofil besteht aus einem Satz von PCR-Indizes (Platform Configuration Register) im Bereich von 0 bis 23 (einschließlich). Wiederholungswerte im -Parameter werden ignoriert. Jeder PCR-Index ist Diensten zugeordnet, die beim Starten des Betriebssystems ausgeführt werden. Jedes Mal, wenn der Computer gestartet wird, überprüft das TPM, ob die Dienste, die Sie im Plattformvalidierungsprofil angegeben haben, nicht geändert wurden. Wenn einer dieser Dienste geändert wird, während der BitLocker-Laufwerkverschlüsselung-Schutz (BDE) aktiviert bleibt, gibt das TPM den Verschlüsselungsschlüssel nicht frei, um das Datenträgervolumen zu entsperren, und der Computer wird in den Wiederherstellungsmodus wechseln.

Wenn dieser Parameter angegeben wird, während die entsprechende Gruppenrichtlinie aktiviert wurde, muss er mit der Gruppenrichtlinie übereinstimmen.

Wenn dieser Parameter nicht angegeben wird, wird der Standardwert 0, 2, 4, 5, 8, 9, 10 und 11 verwendet. Das Standardprofil für die Plattformvalidierung sichert den Verschlüsselungsschlüssel vor Änderungen am Core Root of Trust of Measurement (CRTM), BIOS und Plattformerweiterungen (PCR 0), am Option ROM-Code (PCR 2), am MBR-Code (Master Boot Record, PCR 4), an der MbR-Partitionstabelle (Master Boot Record, PCR 5), am NTFS-Startbereich (PCR 8), am NTFS-Startcode (PCR 9),  Der Start-Manager (PCR 10) und der BitLocker-Laufwerkverschlüsselung Access Control (PCR 11). Aus Sicherheitsgründen wird das Standardprofil empfohlen. UEFI-basierte Computer (Unified Extensible Firmware Interface) verwenden pcr 5 standardmäßig nicht. Verwenden Sie ein Profil der PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11, um zusätzlichen Schutz vor frühen Startkonfigurationsänderungen zu erhalten.

Das Ändern des Standardprofils wirkt sich auf die Sicherheit und Verwaltbarkeit Ihres Computers aus. Die Empfindlichkeit von BitLocker gegenüber Plattformänderungen (böswillig oder autorisiert) wird je nach Ein- bzw. Ausschluss der PCRs erhöht oder verringert. Damit der BitLocker-Schutz aktiviert wird, muss das Plattformvalidierungsprofil PCR 11 enthalten.



| Wert                                                                         | Bedeutung                                                                             |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  | Core Root of Trust of Measurement (CRTM), BIOS und Plattformerweiterungen.<br/> |
| <dl> <dt>1</dt> </dl>  | Plattform- und Hauptplatinenkonfiguration und -daten<br/>                          |
| <dl> <dt>2</dt> </dl>  | Rom-Code der Option<br/>                                                          |
| <dl> <dt>3</dt> </dl>  | Option ROM-Konfiguration und -Daten<br/>                                        |
| <dl> <dt>4</dt> </dl>  | MbR-Code (Master Boot Record)<br/>                                            |
| <dl> <dt>5</dt> </dl>  | MbR-Partitionstabelle (Master Boot Record)<br/>                                 |
| <dl> <dt>6</dt> </dl>  | Zustandsübergangs- und Aktivierungsereignisse<br/>                                         |
| <dl> <dt>7</dt> </dl>  | Computer Manufacturer-Specific<br/>                                           |
| <dl> <dt>8</dt> </dl>  | NTFS-Startsektor<br/>                                                         |
| <dl> <dt>9</dt> </dl>  | NTFS-Startcode<br/>                                                           |
| <dl> <dt>10</dt> </dl> | Start-Manager<br/>                                                             |
| <dl> <dt>11</dt> </dl> | BitLocker-Laufwerkverschlüsselung Access Control<br/>                                |
| <dl> <dt>12</dt> </dl> | Definiert für die Verwendung durch das statische Betriebssystem<br/>                           |
| <dl> <dt>13</dt> </dl> | Definiert für die Verwendung durch das statische Betriebssystem<br/>                           |
| <dl> <dt>14</dt> </dl> | Definiert für die Verwendung durch das statische Betriebssystem<br/>                           |
| <dl> <dt>15</dt> </dl> | Definiert für die Verwendung durch das statische Betriebssystem<br/>                           |
| <dl> <dt>16</dt> </dl> | Wird zum Debuggen verwendet<br/>                                                       |
| <dl> <dt>17</dt> </dl> | Dynamische CRTM<br/>                                                             |
| <dl> <dt>18</dt> </dl> | Plattformdefiniert<br/>                                                         |
| <dl> <dt>19</dt> </dl> | Wird vom vertrauenswürdigen Betriebssystem verwendet<br/>                                         |
| <dl> <dt>20</dt> </dl> | Wird vom vertrauenswürdigen Betriebssystem verwendet<br/>                                         |
| <dl> <dt>21</dt> </dl> | Wird vom vertrauenswürdigen Betriebssystem verwendet<br/>                                         |
| <dl> <dt>22</dt> </dl> | Wird vom vertrauenswürdigen Betriebssystem verwendet<br/>                                         |
| <dl> <dt>23</dt> </dl> | Anwendungsunterstützung<br/>                                                      |



 

</dd> <dt>

*VolumeKeyProtectorID* \[ out\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die die erstellte Schutzvorrichtung eindeutig identifiziert und zum Verwalten der Schlüsselschutzvorrichtung verwendet werden kann.

Wenn das Laufwerk Hardwareverschlüsselung unterstützt und BitLocker keinen Bandbesitz übernommen hat, wird die ID-Zeichenfolge auf "BitLocker" festgelegt, und die Schlüsselschutzvorrichtung wird in die Metadaten pro Band geschrieben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                         | Beschreibung                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                         | Die Methode war erfolgreich.<br/>                                                                                                                                              |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl>        | Das Volume ist gesperrt.<br/>                                                                                                                                                   |
| <dl> <dt>**TBS \_ E \_ SERVICE NOT RUNNING \_ \_ 2150121480**</dt> <dt>(0x80284008)</dt> </dl> | Auf diesem Computer wurde kein kompatibles TPM gefunden.<br/>                                                                                                                            |
| <dl> <dt>**FVE \_ E \_ FOREIGN \_ VOLUME**</dt> <dt>2150694947 (0x80310023)</dt> </dl>       | Das TPM kann den Verschlüsselungsschlüssel des Volumes nicht sichern, da das Volume nicht das derzeit ausgeführte Betriebssystem enthält.<br/>                                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                 | Der *PlatformValidationProfile-Parameter* wird bereitgestellt, aber seine Werte liegen nicht innerhalb des bekannten Bereichs, oder er Gruppenrichtlinie derzeit wirksamen Einstellung.<br/> |
| <dl> <dt>**FVE \_ E \_ PROTECTOR \_ EXISTS**</dt> <dt>2150694961 (0x80310031)</dt> </dl>            | Eine Schlüsselschutzvorrichtung dieses Typs ist bereits vorhanden.<br/>                                                                                                                             |



 

## <a name="security-considerations"></a>Überlegungen zur Sicherheit

Für die Sicherheit Ihres Computers wird das Standardprofil empfohlen. Verwenden Sie ein Profil der PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11, um zusätzlichen Schutz vor Änderungen an der Frühen Startkonfiguration zu bieten.

Das Ändern des Standardprofils wirkt sich auf die Sicherheit oder Benutzerfreundlichkeit Ihres Computers aus.

## <a name="remarks"></a>Hinweise

Höchstens eine Schlüsselschutzvorrichtung vom Typ "TPM" kann jederzeit für ein Volume vorhanden sein. Wenn Sie den Anzeigenamen oder das Plattformvalidierungsprofil ändern möchten, das von einer vorhandenen TPM-Schlüsselschutzvorrichtung verwendet wird, müssen Sie zuerst die vorhandene Schlüsselschutzvorrichtung entfernen und dann **ProtectKeyWithTPM** aufrufen, um eine neue zu erstellen.

Bei PCR-Indizes 0 bis 5 werden die aktuellen Messungen in den Registern verwendet, um den Verschlüsselungsschlüssel zu schützen. Für die PCR-Werte 8 bis 11 werden die Messungen verwendet, die voraussichtlich im nächsten Startzyklus vorhanden sind.

Es sollten zusätzliche Schlüsselschutzvorrichtungen angegeben werden, um das Volume in Wiederherstellungsszenarien zu entsperren, in denen kein Zugriff auf den Verschlüsselungsschlüssel des Volumes abgerufen werden kann. Beispielsweise, wenn das TPM nicht erfolgreich anhand des Plattformvalidierungsprofils überprüft werden kann. Verwenden Sie [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) oder [**ProtectKeyWithNumericalPassword,**](protectkeywithnumericalpassword-win32-encryptablevolume.md) um eine oder mehrere Schlüsselschutzvorrichtungen zum Wiederherstellen eines ansonsten gesperrten Volumes zu erstellen.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Enterprise, nur Windows Vista \[ Ultimate-Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\CIMV2-Stammsicherheit \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> </dl>

 

 
