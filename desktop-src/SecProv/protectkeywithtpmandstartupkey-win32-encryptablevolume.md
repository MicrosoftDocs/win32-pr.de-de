---
description: Wenn die Trusted Platform Module (TPM) verfügbar ist, sichert diese Methode den Verschlüsselungsschlüssel des Volumes, der durch einen externen Schlüssel erweitert wurde.
ms.assetid: 58bc2de7-645f-4049-949c-975062f8c8ce
title: Protectkeywithtpmandstartupkey-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithTPMAndStartupKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 06ab2b9474b3564a567374490d9aeb70448338be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346087"
---
# <a name="protectkeywithtpmandstartupkey-method-of-the-win32_encryptablevolume-class"></a>Protectkeywithtpmandstartupkey-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **protectkeywithtpmandstartupkey** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " sichert den Verschlüsselungsschlüssel des Volumes mithilfe der TPM-Sicherheits Hardware (Trusted Platform Module) auf dem Computer, sofern verfügbar, erweitert durch einen externen Schlüssel, der dem Computer beim Start angezeigt werden muss.

Sowohl die Überprüfung durch das TPM als auch die Eingabe eines USB-Speichergeräts, das den externen Schlüssel enthält, sind erforderlich, um auf den Verschlüsselungsschlüssel des Volumes zuzugreifen und den volumeinhalt freizugeben. Verwenden Sie die [**saveexternalkeytofile**](saveexternalkeytofile-win32-encryptablevolume.md) -Methode, um diesen externen Schlüssel in einer Datei auf einem USB-Speichergerät für die Verwendung als Systemstart Schlüssel zu speichern.

Diese Methode ist nur für das Volume anwendbar, das das aktuell laufende Betriebssystem enthält.

Eine Schlüssel Schutzvorrichtung vom Typ "TPM und Systemstart Schlüssel" wird für das Volume erstellt, sofern nicht bereits vorhanden.

## <a name="syntax"></a>Syntax


```mof
uint32 ProtectKeyWithTPMAndStartupKey(
  [in, optional] string FriendlyName,
  [in, optional] uint8  PlatformValidationProfile[],
  [in, optional] uint8  ExternalKey[],
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FriendlyName* \[ in, optional\]
</dt> <dd>

Typ: **Zeichenfolge**

Ein vom Benutzer zugewiesener Zeichen folgen Bezeichner für diese Schlüssel Schutzvorrichtung. Wenn dieser Parameter nicht angegeben wird, wird ein leerer Wert verwendet.

</dd> <dt>

*Platformvalidationprofile* \[ in, optional\]
</dt> <dd>

Typ: **Uint8 \[ \]**

Ein Array von ganzen Zahlen, das angibt, wie die Sicherheits Hardware des Computers Trusted Platform Module (TPM) den Verschlüsselungsschlüssel des Datenträgervolumes sichert.

Ein Platt Form Validierungs Profil besteht aus einem Satz von Platt Form Konfigurations Register Indizes (PCR), der zwischen 0 und 23 (einschließlich) liegt. Wiederholungswerte im-Parameter werden ignoriert. Jeder PCR-Index ist mit Diensten verknüpft, die beim Starten des Betriebssystems ausgeführt werden. Jedes Mal, wenn der Computer gestartet wird, prüft das TPM, ob die Dienste, die Sie im Platt Form Validierungs Profil angegeben haben, nicht geändert wurden. Wenn sich einer dieser Dienste ändert, während BitLocker-Laufwerkverschlüsselung (BDE)-Schutz beibehalten wird, gibt das TPM den Verschlüsselungsschlüssel nicht frei, um das Datenträger Volume zu entsperren, und der Computer wechselt in den Wiederherstellungs Modus.

Wenn dieser Parameter angegeben wird, während die entsprechende Gruppenrichtlinie Einstellung aktiviert ist, muss er mit der Gruppenrichtlinie Einstellung übereinstimmen.

Wenn dieser Parameter nicht angegeben wird, wird der Standardwert 0, 2, 4, 5, 8, 9, 10 und 11 verwendet. Das standardmäßige Platt Form Validierungs Profil sichert den Verschlüsselungsschlüssel vor Änderungen an den folgenden Elementen:

-   Kern Stamm der Messgeräte Vertrauensstellung (CRTM)
-   BIOS
-   Platt Form Erweiterungen (PCR 0)
-   Options-ROM-Code (PCR 2)
-   Master Boot Record (MBR)-Code (PCR 4)
-   MBR-Partitionstabelle (Master Boot Record) (PCR 5)
-   NTFS-Startsektor (PCR 8)
-   NTFS-Startblock (PCR 9)
-   Start-Manager (PCR 10)
-   BitLocker-Zugriffssteuerung (PCR 11)

Für die Sicherheit Ihres Computers wird das Standardprofil empfohlen. Um zusätzlichen Schutz vor Änderungen der frühen Startkonfiguration zu erhalten, verwenden Sie ein Profil von PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11. Unified Extensible Firmware Interface (UEFI) – Computer verwenden standardmäßig nicht PCR 5.

Das Ändern des Standard Profils wirkt sich auf die Sicherheit und Verwaltbarkeit Ihres Computers aus. Die Vertraulichkeit von BitLocker zu Platt Formänderungen (bösartig oder autorisiert) wird abhängig vom Inklusions-oder Ausschluss Wert des PCRs angehoben oder verringert. Damit der BitLocker-Schutz aktiviert werden kann, muss das Platt Form Validierungs Profil PCR 11 enthalten.



| Wert                                                                         | Bedeutung                                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  | Kern Stamm der Vertrauens Stellungen von Messgeräten (CRTM), BIOS und Plattformen<br/> |
| <dl> <dt>1</dt> </dl>  | Konfiguration und Daten von Plattform und Motherboard<br/>                         |
| <dl> <dt>2</dt> </dl>  | Option-ROM-Code<br/>                                                         |
| <dl> <dt>3</dt> </dl>  | Option ROM-Konfiguration und-Daten<br/>                                       |
| <dl> <dt>4</dt> </dl>  | MBR-Code (Master Boot Record)<br/>                                           |
| <dl> <dt>5</dt> </dl>  | MBR-Partitionstabelle (Master Boot Record)<br/>                                |
| <dl> <dt>6</dt> </dl>  | Zustandsübergänge und Aktivierungs Ereignisse<br/>                                        |
| <dl> <dt>7</dt> </dl>  | Computer Manufacturer-Specific<br/>                                          |
| <dl> <dt>8</dt> </dl>  | NTFS-Startsektor<br/>                                                        |
| <dl> <dt>9</dt> </dl>  | NTFS-Start Block<br/>                                                         |
| <dl> <dt>10</dt> </dl> | Start-Manager<br/>                                                            |
| <dl> <dt>11</dt> </dl> | BitLocker-Access Control<br/>                                                |
| <dl> <dt>12</dt> </dl> | Definiert für die Verwendung durch das statische Betriebssystem<br/>                          |
| <dl> <dt>13</dt> </dl> | Definiert für die Verwendung durch das statische Betriebssystem<br/>                          |
| <dl> <dt>14</dt> </dl> | Definiert für die Verwendung durch das statische Betriebssystem<br/>                          |
| <dl> <dt>15</dt> </dl> | Definiert für die Verwendung durch das statische Betriebssystem<br/>                          |
| <dl> <dt>16</dt> </dl> | Zum Debuggen verwendet<br/>                                                      |
| <dl> <dt>17</dt> </dl> | Dynamische CRTM<br/>                                                            |
| <dl> <dt>Jahren</dt> </dl> | Plattform definiert<br/>                                                        |
| <dl> <dt>19</dt> </dl> | Wird von einem vertrauenswürdigen Betriebssystem verwendet<br/>                                      |
| <dl> <dt>20</dt> </dl> | Wird von einem vertrauenswürdigen Betriebssystem verwendet<br/>                                      |
| <dl> <dt>21</dt> </dl> | Wird von einem vertrauenswürdigen Betriebssystem verwendet<br/>                                      |
| <dl> <dt>22</dt> </dl> | Wird von einem vertrauenswürdigen Betriebssystem verwendet<br/>                                      |
| <dl> <dt>23</dt> </dl> | Anwendungsunterstützung<br/>                                                     |



 

</dd> <dt>

*ExternalKey* \[ in, optional\]
</dt> <dd>

Typ: **Uint8 \[ \]**

Ein Bytearray, das den externen 256-Bit-Schlüssel angibt, der zum Entsperren des Volumes beim Starten des Computers verwendet wird.

Wenn kein externer Schlüssel angegeben ist, wird eine nach dem Zufallsprinzip generiert. Verwenden Sie die [**getkeyprotectorexternalkey**](getkeyprotectorexternalkey-win32-encryptablevolume.md) -Methode, um den zufällig generierten Schlüssel abzurufen.

</dd> <dt>

*Volumekeyprotectorid* \[ vorgenommen\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die der eindeutige Bezeichner ist, der der erstellten Schlüssel Schutzvorrichtung zugeordnet ist und zum Verwalten der Schlüssel Schutzvorrichtung verwendet werden kann.

Wenn das Laufwerk die Hardware Verschlüsselung unterstützt und BitLocker keinen bandbesitz hat, wird die ID-Zeichenfolge auf "BitLocker" festgelegt, und die Schlüssel Schutzvorrichtung wird in die pro-Band-Metadaten geschrieben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                         | BESCHREIBUNG                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                         | Die Methode war erfolgreich.<br/>                                                                                                                                                                                                                                  |
| <dl> <dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl>        | Das Volume ist gesperrt.<br/>                                                                                                                                                                                                                                       |
| <dl> <dt>**TSB \_ E- \_ Dienst wird \_ nicht \_ ausgeführt**</dt> <dt>2150121480 (0x80284008)</dt> </dl> | Auf diesem Computer wurde kein kompatibles TPM gefunden.<br/>                                                                                                                                                                                                                |
| <dl> <dt>**F \_ E- \_ Fremd \_ Volume**</dt> <dt>2150694947 (0x80310023)</dt> </dl>       | Das TPM kann den Verschlüsselungsschlüssel des Volumes nicht sichern, da das Volume nicht das aktuell Betriebssystem enthält.<br/>                                                                                                                               |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                 | Der *platformvalidationprofile* -Parameter wird bereitgestellt, seine Werte befinden sich jedoch nicht innerhalb des bekannten Bereichs oder stimmen nicht mit der derzeit gültigen Gruppenrichtlinie Einstellung identisch.<br/> Der *ExternalKey* -Parameter wird bereitgestellt, ist aber kein Array der Größe 32.<br/> |
| <dl> <dt>**F \_ E \_ Bootable \_ CDDVD**</dt> <dt>2150694960 (0x80310030)</dt> </dl>       | Auf diesem Computer wurde eine Start fähige CD/DVD gefunden. Entfernen Sie die CD/DVD, und starten Sie den Computer neu.<br/>                                                                                                                                                                    |
| <dl> <dt>**F \_ E \_ Protector \_ vorhanden**</dt> <dt>2150694961 (0x80310031)</dt> </dl>     | Eine Schlüssel Schutzvorrichtung dieses Typs ist bereits vorhanden.<br/>                                                                                                                                                                                                                |



 

## <a name="security-considerations"></a>Überlegungen zur Sicherheit

Für die Sicherheit Ihres Computers wird das Standardprofil empfohlen. Verwenden Sie ein Profil von PCRs 0, 2, 4, 5, 8, 9, 10 und 11, um zusätzlichen Schutz vor den Änderungen am Anfang des Start Codes zu erhalten. Um zusätzlichen Schutz vor Änderungen der frühen Startkonfiguration zu erhalten, verwenden Sie ein Profil von PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.

Das Ändern des Standard Profils wirkt sich auf die Sicherheit oder Nutzbarkeit Ihres Computers aus.

## <a name="remarks"></a>Bemerkungen

Es kann höchstens eine Schlüssel Schutzvorrichtung vom Typ "TPM und Systemstart Schlüssel" für ein Volume vorhanden sein. Wenn Sie den anzeigen Amen oder das Platt Form Validierungs Profil ändern möchten, das von einer vorhandenen Schlüssel Schutzvorrichtung vom Typ "TPM plus Startup Key" verwendet wird, müssen Sie zunächst die vorhandene Schlüssel Schutzvorrichtung entfernen und dann **protectkeywithtpmandstartupkey** aufrufen, um eine neue zu erstellen. Zum Entsperren des Volumes in Wiederherstellungs Szenarien, in denen der Zugriff auf den Verschlüsselungsschlüssel des Volumes nicht abgerufen werden kann, müssen zusätzliche Schlüssel Schutzvorrichtungen angegeben werden. Dies ist beispielsweise der Fall, wenn das TPM nicht mit dem Platt Form Validierungs Profil überprüft werden kann oder wenn der USB-Speicher, der den externen Schlüssel enthält, verloren geht

Verwenden Sie [**protectkeywithexternalkey**](protectkeywithexternalkey-win32-encryptablevolume.md) oder [**protectkeywithnumericalpassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) , um eine oder mehrere Schlüssel Schutzvorrichtungen für die Wiederherstellung eines anderweitig gesperrten Volumes zu erstellen.

Obwohl es möglich ist, sowohl eine Schlüssel Schutzvorrichtung vom Typ "TPM" als auch einen anderen Typ "TPM und Systemstart Schlüssel" zu haben, negiert das vorhanden sein des TPM-schlüsselschutzschutztyps die Auswirkungen anderer TPM-basierter Schlüssel Schutzvorrichtungen.

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ verschlüsseltablevolume. MOF</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ verschlüsseltablevolume**](win32-encryptablevolume.md)
</dt> <dt>

[**Win32- \_ TPM**](win32-tpm.md)
</dt> </dl>

 

 
