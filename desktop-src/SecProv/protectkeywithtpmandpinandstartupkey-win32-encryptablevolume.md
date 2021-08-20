---
description: Sichert den Verschlüsselungsschlüssel des Volumes mithilfe des Trusted Platform Module (TPM) auf dem Computer , sofern verfügbar, erweitert durch eine vom Benutzer angegebene persönliche Identifikationsnummer (PIN) und durch einen externen Schlüssel, der dem Computer beim Start angezeigt werden muss.
ms.assetid: 8991c22c-1e36-415e-a82b-c5ddf9c3b24a
title: ProtectKeyWithTPMAndPINAndStartupKey-Methode der Win32_EncryptableVolume Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithTPMAndPINAndStartupKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: c4a77c0e5687319bbea438127ce9c30b27ff3122f42359237df5d4cd158b1393
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004348"
---
# <a name="protectkeywithtpmandpinandstartupkey-method-of-the-win32_encryptablevolume-class"></a>ProtectKeyWithTPMAndPINAndStartupKey-Methode der Win32 \_ EncryptableVolume-Klasse

Die **ProtectKeyWithTPMAndPINAndStartupKey-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) schützt den Verschlüsselungsschlüssel des Volumes mithilfe des Trusted Platform Module (TPM) auf dem Computer, sofern verfügbar, erweitert durch eine vom Benutzer angegebene persönliche Identifikationsnummer (PIN) und durch einen externen Schlüssel, der dem Computer beim Start angezeigt werden muss.

Zum Entsperren des verschlüsselten Inhalts des Volumes sind drei Authentifizierungsfaktoren erforderlich:

1.  Überprüfung durch das TPM
2.  Eingabe einer 4 bis 20-stelligen PIN oder, wenn die Gruppenrichtlinie "Erweiterte PINs für Den Start zulassen" aktiviert ist, 4 bis 20 Buchstaben, Symbole, Leerzeichen oder Zahlen
3.  Eingabe eines USB-Speichergeräts, das den externen Schlüssel enthält

Verwenden Sie [**die SaveExternalKeyToFile-Methode,**](saveexternalkeytofile-win32-encryptablevolume.md) um diesen externen Schlüssel zur Verwendung als Startschlüssel in einer Datei auf einem USB-Speichergerät zu speichern. Diese Methode gilt nur für das Betriebssystem-Volume. Es wird eine Schlüsselschutzvorrichtung vom Typ "TPM und PIN und Startschlüssel" erstellt.

## <a name="syntax"></a>Syntax


```mof
uint32 ProtectKeyWithTPMAndPINAndStartupKey(
  [in, optional] string FriendlyName,
  [in, optional] uint8  PlatformValidationProfile,
  [in]           string PIN,
  [in, optional] uint8  ExternalKey[],
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FriendlyName* \[ in, optional\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die diese Schlüsselschutzvorrichtung bezeichnet. Wenn dieser Parameter nicht angegeben wird, wird ein leerer Wert verwendet.

</dd> <dt>

*PlatformValidationProfile* \[ in, optional\]
</dt> <dd>

Typ: **uint8**

Ein Array von ganzen Zahlen, das angibt, wie das TPM des Computers den Verschlüsselungsschlüssel des Volumes sichert. Ein Plattformvalidierungsprofil besteht aus einem Satz von PCR-Indizes (Platform Configuration Register) im Bereich von 0 bis 23 (einschließlich). Wiederholungswerte im -Parameter werden ignoriert. Jeder PCR-Index ist Diensten zugeordnet, die beim Starten des Betriebssystems ausgeführt werden. Jedes Mal, wenn der Computer gestartet wird, überprüft das TPM, ob die Dienste, die Sie im Plattformvalidierungsprofil angegeben haben, nicht geändert wurden. Wenn sich einer dieser Dienste ändert, während der BitLocker-Schutz aktiviert bleibt, gibt das TPM den Verschlüsselungsschlüssel nicht frei, um das Volume zu entsperren, und der Computer wird in den Wiederherstellungsmodus wechseln.

Wenn dieser Parameter nicht angegeben wird, werden die Standardindizes 0, 2, 4, 5, 8, 9, 10 und 11 verwendet. Das Standardprofil für die Plattformvalidierung sichert den Verschlüsselungsschlüssel vor Änderungen am Core Root of Trust of Measurement (CRTM), BIOS und Plattformerweiterungen (PCR 0), Option ROM Code (PCR 2), Master Boot Record (MBR) Code (PCR 4), Master Boot Record (MBR) Partition Table (PCR 5), NTFS Boot Sector (PCR 8), NTFS Boot Block (PCR 9),  Der Start-Manager (PCR 10) und der BitLocker-Access Control (PCR 11). UEFI-basierte Computer (Unified Extensible Firmware Interface) verwenden pcr 5 standardmäßig nicht.

Das Standardprofil für die Plattformvalidierung wird empfohlen. Verwenden Sie ein Profil der PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11, um zusätzlichen Schutz vor frühen Startkonfigurationsänderungen zu erhalten.

Das Ändern des Standardprofils wirkt sich auf die Sicherheit und Verwaltbarkeit Ihres Computers aus. Die Empfindlichkeit von BitLocker gegenüber Plattformänderungen (böswillig oder autorisiert) wird je nach Ein- bzw. Ausschluss der PCRs erhöht oder verringert. Damit der BitLocker-Schutz aktiviert wird, muss das Plattformvalidierungsprofil PCR 11 enthalten.



| Wert                                                                         | Bedeutung                                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  | Core Root of Trust of Measurement (CRTM), BIOS und Plattformerweiterungen<br/> |
| <dl> <dt>1</dt> </dl>  | Plattform- und Hauptplatinenkonfiguration und -daten<br/>                         |
| <dl> <dt>2</dt> </dl>  | Rom-Code der Option<br/>                                                         |
| <dl> <dt>3</dt> </dl>  | Option ROM-Konfiguration und -Daten<br/>                                       |
| <dl> <dt>4</dt> </dl>  | MbR-Code (Master Boot Record)<br/>                                           |
| <dl> <dt>5</dt> </dl>  | MbR-Partitionstabelle (Master Boot Record)<br/>                                |
| <dl> <dt>6</dt> </dl>  | Zustandsübergangs- und Aktivierungsereignisse<br/>                                        |
| <dl> <dt>7</dt> </dl>  | Computer Manufacturer-Specific<br/>                                          |
| <dl> <dt>8</dt> </dl>  | NTFS-Startsektor<br/>                                                        |
| <dl> <dt>9</dt> </dl>  | NTFS-Startblock<br/>                                                         |
| <dl> <dt>10</dt> </dl> | Start-Manager<br/>                                                            |
| <dl> <dt>11</dt> </dl> | BitLocker-Access Control<br/>                                                |
| <dl> <dt>12</dt> </dl> | Definiert für die Verwendung durch das statische Betriebssystem<br/>                          |
| <dl> <dt>13</dt> </dl> | Definiert für die Verwendung durch das statische Betriebssystem<br/>                          |
| <dl> <dt>14</dt> </dl> | Definiert für die Verwendung durch das statische Betriebssystem<br/>                          |
| <dl> <dt>15</dt> </dl> | Definiert für die Verwendung durch das statische Betriebssystem<br/>                          |
| <dl> <dt>16</dt> </dl> | Wird zum Debuggen verwendet<br/>                                                      |
| <dl> <dt>17</dt> </dl> | Dynamische CRTM<br/>                                                            |
| <dl> <dt>18</dt> </dl> | Plattformdefiniert<br/>                                                        |
| <dl> <dt>19</dt> </dl> | Wird von einem vertrauenswürdigen Betriebssystem verwendet.<br/>                                      |
| <dl> <dt>20</dt> </dl> | Wird von einem vertrauenswürdigen Betriebssystem verwendet.<br/>                                      |
| <dl> <dt>21</dt> </dl> | Wird von einem vertrauenswürdigen Betriebssystem verwendet.<br/>                                      |
| <dl> <dt>22</dt> </dl> | Wird von einem vertrauenswürdigen Betriebssystem verwendet.<br/>                                      |
| <dl> <dt>23</dt> </dl> | Anwendungsunterstützung<br/>                                                     |



 

</dd> <dt>

*PIN* \[ In\]
</dt> <dd>

Typ: **Zeichenfolge**

Enthält eine 4 bis 20-stellige persönliche Identifikationsnummer (PIN) oder, wenn die Gruppenrichtlinie "Erweiterte PINs für den Start zulassen" aktiviert ist, 4 und 20 Buchstaben, Symbole, Leerzeichen oder Zahlen. Diese Zeichenfolge muss dem Computer beim Start bereitgestellt werden.

</dd> <dt>

*ExternalKey* \[ in, optional\]
</dt> <dd>

Typ: **uint8 \[ \]**

Ein Bytearray, das den externen 256-Bit-Schlüssel angibt, mit dem das Volume beim Starten des Computers entsperrt wird. Lassen Sie diesen Parameter leer, um den externen Schlüssel nach dem Zufallsprinzip zu generieren. Verwenden Sie [**die GetKeyProtectorExternalKey-Methode,**](getkeyprotectorexternalkey-win32-encryptablevolume.md) um den zufällig generierten Schlüssel zu erhalten.

</dd> <dt>

*VolumeKeyProtectorID* \[ out\]
</dt> <dd>

Typ: **Zeichenfolge**

Der aktualisierte eindeutige Zeichenfolgenbezeichner, der zum Verwalten einer verschlüsselten Volumeschlüsselschutzvorrichtung verwendet wird.

Wenn das Laufwerk Hardwareverschlüsselung unterstützt und BitLocker keinen Bandbesitz übernommen hat, wird die ID-Zeichenfolge auf "BitLocker" festgelegt, und die Schlüsselschutzvorrichtung wird in die Metadaten pro Band geschrieben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                                | Beschreibung                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                | Die Methode war erfolgreich.<br/>                                                                                                                                                                                                                                             |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                        | Der *PlatformValidationProfile-Parameter* wird bereitgestellt, aber seine Werte liegen nicht innerhalb des bekannten Bereichs, oder er stimmt nicht mit der Gruppenrichtlinie Einstellung überein, die derzeit wirksam ist.<br/> Der *ExternalKey-Parameter* wird bereitgestellt, ist aber kein Array der Größe 32.<br/> |
| <dl> <dt>**FVE \_ E \_ BOOTABLE \_ CDDVD**</dt> <dt>2150694960 (0x80310030)</dt> </dl>              | Auf diesem Computer befindet sich eine startbare CD/DVD. Entfernen Sie die CD/DVD, und starten Sie den Computer neu.<br/>                                                                                                                                                                               |
| <dl> <dt>**FVE \_ E \_ FOREIGN \_ VOLUME**</dt> <dt>2150694947 (0x80310023)</dt> </dl>              | Das TPM kann den Verschlüsselungsschlüssel des Volumes nicht sichern, da das Volume nicht das derzeit ausgeführte Betriebssystem enthält.<br/>                                                                                                                                          |
| <dl> <dt>**FVE \_ E \_ UNGÜLTIGE \_ \_ PIN-2150695066**</dt> <dt>(0x8031009A)</dt> </dl>          | Der *NewPIN-Parameter* enthält ungültige Zeichen. Wenn die Gruppenrichtlinie "Erweiterte PINs für Start zulassen" deaktiviert ist, werden nur Zahlen unterstützt.<br/>                                                                                                        |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl>               | Das Volume ist gesperrt.<br/>                                                                                                                                                                                                                                                  |
| <dl> <dt>**FVE \_ E \_ POLICY INVALID PIN \_ \_ \_ LENGTH**</dt> <dt>2150695016 (0x80310068)</dt> </dl> | Der angegebene *NewPIN-Parameter* ist entweder länger als 20 Zeichen, kürzer als 4 Zeichen oder kürzer als die durch Gruppenrichtlinie angegebene Mindestlänge.<br/>                                                                                                          |
| <dl> <dt>**FVE \_ \_E-SCHUTZVORRICHTUNG \_ EXISTS**</dt> <dt>2150694961 (0x80310031)</dt> </dl>            | Eine Schlüsselschutzvorrichtung dieses Typs ist bereits vorhanden.<br/>                                                                                                                                                                                                                           |
| <dl> <dt>**TBS \_ \_E-DIENST \_ WIRD NICHT \_ AUSGEFÜHRT**</dt> <dt>2150121480 (0x80284008)</dt> </dl>        | Auf diesem Computer wurde kein kompatibles TPM gefunden.<br/>                                                                                                                                                                                                                           |



 

## <a name="remarks"></a>Hinweise

Höchstens eine Schlüsselschutzvorrichtung vom Typ "TPM und PIN und Startschlüssel" kann jederzeit für ein Volume vorhanden sein. Wenn Sie den Anzeigenamen oder das Plattformvalidierungsprofil ändern möchten, das von einer vorhandenen Schlüsselschutzvorrichtung "TPM und PIN und Startschlüssel" verwendet wird, müssen Sie zuerst die vorhandene Schlüsselschutzvorrichtung entfernen und dann **ProtectKeyWithTPMAndPINAndStartupKey** aufrufen, um eine neue zu erstellen.

Es sollten zusätzliche Schlüsselschutzvorrichtungen angegeben werden, um das Volume in Wiederherstellungsszenarien zu entsperren, in denen kein Zugriff auf den Verschlüsselungsschlüssel des Volumes abgerufen werden kann. Beispielsweise, wenn das TPM nicht erfolgreich anhand des Plattformvalidierungsprofils überprüft werden kann oder wenn die PIN verloren geht. Verwenden Sie [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) oder [**ProtectKeyWithNumericalPassword,**](protectkeywithnumericalpassword-win32-encryptablevolume.md) um eine oder mehrere Schlüsselschutzvorrichtungen zum Wiederherstellen eines ansonsten gesperrten Volumes zu erstellen.

Es ist zwar möglich, sowohl eine Schlüsselschutzvorrichtung vom Typ "TPM" als auch einen anderen vom Typ "TPM und PIN und Startschlüssel" zu verwenden, aber das Vorhandensein des Schlüsselschutzvorrichtungstyps "TPM" negiert die Auswirkungen anderer TPM-basierter Schlüsselschutzvorrichtungen.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Enterprise mit SP1, Windows Vista Ultimate nur mit \[ SP1-Desktop-Apps\]<br/>     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\CIMV2-Stammsicherheit \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
