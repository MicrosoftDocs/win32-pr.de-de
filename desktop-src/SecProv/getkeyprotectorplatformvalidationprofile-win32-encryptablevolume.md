---
description: Ruft das Plattformvalidierungsprofil für eine bestimmte Schlüsselschutzvorrichtung des entsprechenden Typs ab.
ms.assetid: 45fa6ba7-169c-4753-8586-0029a7650acc
title: GetKeyProtectorPlatformValidationProfile-Methode der Win32_EncryptableVolume-Klasse
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
ms.openlocfilehash: 9563fc306bd8d50ce4f0c13164640ecee8e99d441b1b923df35cce8615097c8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119667790"
---
# <a name="getkeyprotectorplatformvalidationprofile-method-of-the-win32_encryptablevolume-class"></a>GetKeyProtectorPlatformValidationProfile-Methode der Win32 \_ EncryptableVolume-Klasse

Die **GetKeyProtectorPlatformValidationProfile-Methode** ruft das Plattformvalidierungsprofil für eine bestimmte Schlüsselschutzvorrichtung des entsprechenden Typs ab.

Der Schlüsselschutzbezeichner muss auf eine Schlüsselschutzvorrichtung vom Typ "TPM", "TPM und PIN", "TPM und PIN und Startschlüssel" oder "TPM und Startschlüssel" verweisen.

## <a name="syntax"></a>Syntax


```mof
uint32 GetKeyProtectorPlatformValidationProfile(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  PlatformValidationProfile[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*VolumeKeyProtectorID* \[ In\]
</dt> <dd>

Typ: **Zeichenfolge**

Ein eindeutiger Zeichenfolgenbezeichner, der zum Verwalten einer verschlüsselten Volumeschlüsselschutzvorrichtung verwendet wird.

</dd> <dt>

*PlatformValidationProfile* \[ out\]
</dt> <dd>

Typ: **uint8 \[ \]**

Ein Array von ganzen Zahlen, das angibt, wie die Trusted Platform Module -Sicherheitshardware (TPM) des Computers den Verschlüsselungsschlüssel des Datenträgervolumens sichert.



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



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                  | Beschreibung                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Die Methode war erfolgreich.<br/>                                                                                                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | Der *Parameter VolumeKeyProtectorID* bezieht sich nicht auf eine Schlüsselschutzvorrichtung vom Typ "TPM", "TPM und PIN", "TPM und PIN und Startschlüssel" oder "TPM und Startschlüssel".<br/> |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüsselschutzvorrichtung hinzu, um BitLocker zu aktivieren.<br/>                                                                                  |



 

## <a name="remarks"></a>Hinweise

Managed Object Format (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Enterprise, Windows Vista \[ Ultimate-Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\CimV2-Stammsicherheit \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
