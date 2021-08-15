---
description: Wenn die Trusted Platform Module (TPM) verfügbar ist, schützt diese Methode den Verschlüsselungsschlüssel des Volumes, der durch eine vom Benutzer angegebene persönliche ID erweitert wurde.
ms.assetid: 8c4c434a-dd60-491a-a983-b3fa78c91c0d
title: ProtectKeyWithTPMAndPIN-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithTPMAndPIN
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0eab283a0eaec97d7f7c9e03cf8d8064e08e0e25bea606b393fb35a38143f7fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891405"
---
# <a name="protectkeywithtpmandpin-method-of-the-win32_encryptablevolume-class"></a>ProtectKeyWithTPMAndPIN-Methode der Win32 \_ EncryptableVolume-Klasse

Die **ProtectKeyWithTPMAndPIN-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) schützt den Verschlüsselungsschlüssel des Volumes mithilfe der Trusted Platform Module -Sicherheitshardware (TPM) auf dem Computer, sofern verfügbar, erweitert durch eine vom Benutzer angegebene persönliche ID (PIN), die dem Computer beim Start bereitgestellt werden muss.

Sowohl die Überprüfung durch das TPM als auch die Eingabe der persönlichen Identifikationszeichenfolge sind erforderlich, um auf den Verschlüsselungsschlüssel des Volumes zuzugreifen und Volumeinhalte zu entsperren.

Diese Methode gilt nur für das Volume, das das derzeit ausgeführte Betriebssystem enthält.

Eine Schlüsselschutzvorrichtung vom Typ "TPM und PIN" wird für das Volume erstellt, sofern noch keine vorhanden ist.

## <a name="syntax"></a>Syntax


```mof
uint32 ProtectKeyWithTPMAndPIN(
  [in, optional] string FriendlyName,
  [in, optional] uint8  PlatformValidationProfile[],
  [in]           string PIN,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FriendlyName* \[ in, optional\]
</dt> <dd>

Typ: **Zeichenfolge**

Ein vom Benutzer zugewiesener Zeichenfolgenbezeichner für diese Schlüsselschutzvorrichtung. Wenn dieser Parameter nicht angegeben ist, wird ein leerer Wert verwendet.

</dd> <dt>

*PlatformValidationProfile* \[ in, optional\]
</dt> <dd>

Typ: **uint8 \[ \]**

Ein Array von ganzen Zahlen, das angibt, wie der Verschlüsselungsschlüssel des Datenträgervolumes durch die TPM-Sicherheitshardware (Trusted Platform Module) des Datenträgervolumes geschützt wird.

Ein Plattformvalidierungsprofil besteht aus einer Reihe von PCR-Indizes (Platform Configuration Register) im Bereich von 0 bis einschließlich 23. Wiederholungswerte im -Parameter werden ignoriert. Jeder PCR-Index ist Diensten zugeordnet, die beim Starten des Betriebssystems ausgeführt werden. Bei jedem Start des Computers überprüft das TPM, ob sich die dienste, die Sie im Plattformvalidierungsprofil angegeben haben, nicht geändert haben. Wenn sich einer dieser Dienste ändert, während BitLocker-Laufwerkverschlüsselung Schutz (BDE) aktiviert bleibt, gibt das TPM den Verschlüsselungsschlüssel nicht frei, um das Datenträgervolume zu entsperren, und der Computer wechselt in den Wiederherstellungsmodus.

Wenn dieser Parameter angegeben wird, während die entsprechende Gruppenrichtlinie Einstellung aktiviert wurde, muss er mit der einstellung Gruppenrichtlinie übereinstimmen.

Wenn dieser Parameter nicht angegeben ist, wird der Standardwert 0, 2, 4, 5, 8, 9, 10 und 11 verwendet. Das Standardmäßige Plattformvalidierungsprofil schützt den Verschlüsselungsschlüssel vor Änderungen an den folgenden Elementen:

-   Core Root of Trust of Measurement (CRTM)
-   BIOS
-   Plattformerweiterungen (PCR 0)
-   Options-ROM-Code (PCR 2)
-   Master Boot Record (MBR)-Code (PCR 4)
-   Master Boot Record (MBR)-Partitionstabelle (PCR 5)
-   NTFS-Startsektor (PCR 8)
-   NTFS-Startblock (PCR 9)
-   Start-Manager (PCR 10)
-   BitLocker-Zugriffssteuerung (PCR 11)

Für die Sicherheit Ihres Computers wird das Standardprofil empfohlen. Verwenden Sie ein Profil der PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11, um zusätzlichen Schutz vor Änderungen an der Frühen Startkonfiguration zu bieten. UEFI-basierte Computer (Unified Extensible Firmware Interface) verwenden pcr 5 standardmäßig nicht.

Das Ändern des Standardprofils wirkt sich auf die Sicherheit und Verwaltbarkeit Ihres Computers aus. Die Empfindlichkeit von BitLocker gegenüber Plattformänderungen (schädlich oder autorisiert) wird je nach Ein- bzw. Ausschluss der PCRs erhöht oder verringert. Damit der BitLocker-Schutz aktiviert wird, muss das Plattformvalidierungsprofil PCR 11 enthalten.



| Wert                                                                         | Bedeutung                                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  | Core Root of Trust of Measurement (CRTM), BIOS und Plattformerweiterungen<br/> |
| <dl> <dt>1</dt> </dl>  | Plattform- und Hauptplatinenkonfiguration und Daten<br/>                         |
| <dl> <dt>2</dt> </dl>  | Option ROM-Code<br/>                                                         |
| <dl> <dt>3</dt> </dl>  | Option ROM-Konfiguration und -Daten<br/>                                       |
| <dl> <dt>4</dt> </dl>  | MBR-Code (Master Boot Record)<br/>                                           |
| <dl> <dt>5</dt> </dl>  | MBR-Partitionstabelle (Master Boot Record)<br/>                                |
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
| <dl> <dt>19</dt> </dl> | Wird von einem vertrauenswürdigen Betriebssystem verwendet<br/>                                      |
| <dl> <dt>20</dt> </dl> | Wird von einem vertrauenswürdigen Betriebssystem verwendet<br/>                                      |
| <dl> <dt>21</dt> </dl> | Wird von einem vertrauenswürdigen Betriebssystem verwendet<br/>                                      |
| <dl> <dt>22</dt> </dl> | Wird von einem vertrauenswürdigen Betriebssystem verwendet<br/>                                      |
| <dl> <dt>23</dt> </dl> | Anwendungsunterstützung<br/>                                                     |



 

</dd> <dt>

*PIN* \[ In\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine benutzerdefinierte persönliche Identifikationszeichenfolge. Diese Zeichenfolge muss aus einer Sequenz von 6 bis 20 Ziffern bestehen, oder, wenn die Gruppenrichtlinie "Erweiterte PINs für Start zulassen" aktiviert ist, 6 bis 20 Buchstaben, Symbole, Leerzeichen oder Zahlen.

</dd> <dt>

*VolumeKeyProtectorID* \[ out\]
</dt> <dd>

Typ: **Zeichenfolge**

Der aktualisierte eindeutige Zeichenfolgenbezeichner, der zum Verwalten einer verschlüsselten Volumeschlüsselschutzvorrichtung verwendet wird.

Wenn das Laufwerk Hardwareverschlüsselung unterstützt und BitLocker keinen Bandbesitz übernommen hat, wird die ID-Zeichenfolge auf "BitLocker" festgelegt, und die Schlüsselschutzvorrichtung wird pro Bandmetadaten in geschrieben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                                | BESCHREIBUNG                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                | Die Methode war erfolgreich.<br/>                                                                                                                                               |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                        | Der *PlatformValidationProfile-Parameter* wird bereitgestellt, aber seine Werte liegen nicht innerhalb des bekannten Bereichs oder stimmen nicht mit der Gruppenrichtlinie derzeit in Kraft.<br/> |
| <dl> <dt>**FVE \_ E \_ BOOTABLE \_ CDDVD**</dt> <dt>2150694960 (0x80310030)</dt> </dl>              | Auf diesem Computer befindet sich eine startbare CD/DVD. Entfernen Sie die CD/DVD, und starten Sie den Computer neu.<br/>                                                                                 |
| <dl> <dt>**FVE \_ E \_ FOREIGN \_ VOLUME**</dt> <dt>2150694947 (0x80310023)</dt> </dl>              | Das TPM kann den Verschlüsselungsschlüssel des Volumes nicht sichern, da das Volume nicht das derzeit ausgeführte Betriebssystem enthält.<br/>                                            |
| <dl> <dt>**FVE \_ E \_ INVALID \_ PIN \_ CHARS**</dt> <dt>2150695066 (0x8031009A)</dt> </dl>          | Der *NewPIN-Parameter* enthält ungültige Zeichen. Wenn die "Erweiterte PINs für den Start zulassen" Gruppenrichtlinie deaktiviert ist, werden nur Zahlen unterstützt.<br/>          |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl>               | Das Volume ist gesperrt.<br/>                                                                                                                                                    |
| <dl> <dt>**FVE \_ E \_ POLICY INVALID PIN LENGTH \_ \_ \_ 2150695016**</dt> <dt>(0x80310068)</dt> </dl> | Der *angegebene NewPIN-Parameter* ist entweder länger als 20 Zeichen, kürzer als 6 Zeichen oder kürzer als die von Gruppenrichtlinie.<br/>            |
| <dl> <dt>**FVE \_ E \_ PROTECTOR \_ EXISTS**</dt> <dt>2150694961 (0x80310031)</dt> </dl>            | Eine Schlüsselschutzvorrichtung dieses Typs ist bereits vorhanden.<br/>                                                                                                                             |
| <dl> <dt>**TBS \_ E \_ SERVICE NOT RUNNING \_ \_ 2150121480**</dt> <dt>(0x80284008)</dt> </dl>        | Auf diesem Computer wurde kein kompatibles TPM gefunden.<br/>                                                                                                                             |



 

## <a name="security-considerations"></a>Überlegungen zur Sicherheit

Aus Sicherheitsgründen wird das Standardprofil empfohlen. Verwenden Sie ein Profil der PCRs 0, 2, 4, 5, 8, 9, 10 und 11, um zusätzlichen Schutz vor frühen Codeänderungen zu erhalten. Verwenden Sie ein Profil der PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11, um zusätzlichen Schutz vor frühen Startkonfigurationsänderungen zu erhalten.

Das Ändern des Standardprofils wirkt sich auf die Sicherheit oder Nutzbarkeit Ihres Computers aus.

## <a name="remarks"></a>Hinweise

Für ein Volume kann jederzeit mindestens eine Schlüsselschutzvorrichtung vom Typ "TPM und PIN" vorhanden sein. Wenn Sie den Anzeigenamen oder das Plattformvalidierungsprofil ändern möchten, das von einer vorhandenen Schlüsselschutzvorrichtung "TPM und PIN" verwendet wird, müssen Sie zuerst die vorhandene Schlüsselschutzvorrichtung entfernen und dann **ProtectKeyWithTPMAndPIN** aufrufen, um eine neue zu erstellen.

Es sollten zusätzliche Schlüsselschutzvorrichtungen angegeben werden, um das Volume in Wiederherstellungsszenarien zu entsperren, in denen kein Zugriff auf den Verschlüsselungsschlüssel des Volumes möglich ist. Beispielsweise, wenn das TPM nicht erfolgreich anhand des Plattformvalidierungsprofils überprüft werden kann oder wenn die PIN verloren geht.

Verwenden [**Sie ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) oder [**ProtectKeyWithNumericalPassword,**](protectkeywithnumericalpassword-win32-encryptablevolume.md) um eine oder mehrere Schlüsselschutzvorrichtungen zum Wiederherstellen eines ansonsten gesperrten Volumes zu erstellen.

Es ist zwar möglich, sowohl eine Schlüsselschutzvorrichtung vom Typ "TPM" als auch eine andere des Typs "TPM und PIN" zu verwenden, aber das Vorhandensein des Schlüsselschutzvorrichtungstyps "TPM" negiert die Auswirkungen anderer TPM-basierter Schlüsselschutzvorrichtungen.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Enterprise, Windows Vista \[ Ultimate-Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\CimV2-Stammsicherheit \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> </dl>

 

 
