---
description: Ruft das Platt Form Validierungs Profil für eine angegebene Schlüssel Schutzvorrichtung des entsprechenden Typs ab.
ms.assetid: 45fa6ba7-169c-4753-8586-0029a7650acc
title: Getkeyprotectorplatformvalidationprofile-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorPlatformValidationProfile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: b9b951d3ce9eab52687730831f7052942fcbec93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373223"
---
# <a name="getkeyprotectorplatformvalidationprofile-method-of-the-win32_encryptablevolume-class"></a>Getkeyprotectorplatformvalidationprofile-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **getkeyprotectorplatformvalidationprofile** -Methode ruft das Platt Form Validierungs Profil für eine bestimmte Schlüssel Schutzvorrichtung des entsprechenden Typs ab.

Die schlüsselschutzschutzkennung muss auf eine Schlüssel Schutzvorrichtung vom Typ "TPM", "TPM und PIN", "TPM und PIN und Systemstart Schlüssel" oder "TPM und Systemstart Schlüssel" verweisen.

## <a name="syntax"></a>Syntax


```mof
uint32 GetKeyProtectorPlatformValidationProfile(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  PlatformValidationProfile[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Volumekeyprotectorid* \[ in\]
</dt> <dd>

Typ: **Zeichenfolge**

Ein eindeutiger Zeichen folgen Bezeichner zum Verwalten einer verschlüsselten volumeschlüsselschutzvorrichtung.

</dd> <dt>

*Platformvalidationprofile* \[ vorgenommen\]
</dt> <dd>

Typ: **Uint8 \[ \]**

Ein Array von ganzen Zahlen, das angibt, wie die Trusted Platform Module (TPM)-Sicherheits Hardware des Computers den Verschlüsselungsschlüssel des Datenträgervolumes sichert.



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



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                  | BESCHREIBUNG                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Die Methode war erfolgreich.<br/>                                                                                                                                        |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | Der *volumekeyprotectorid-* Parameter verweist nicht auf eine Schlüssel Schutzvorrichtung vom Typ "TPM", "TPM und PIN", "TPM und PIN und Systemstart Schlüssel" oder "TPM und Systemstart Schlüssel".<br/> |
| <dl> <dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu.<br/>                                                                                  |



 

## <a name="remarks"></a>Bemerkungen

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
</dt> </dl>

 

 
