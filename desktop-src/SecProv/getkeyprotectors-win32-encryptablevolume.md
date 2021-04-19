---
description: Listet die Schutzvorrichtungen auf, mit denen der Verschlüsselungsschlüssel des Volumes geschützt wird.
ms.assetid: ea88f128-c835-49e3-a395-c5ba472fff4b
title: Getkeyprotector-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3a7d6a4110953d905b10eb4f7ef9a255af77897a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353036"
---
# <a name="getkeyprotectors-method-of-the-win32_encryptablevolume-class"></a>Getkeyprotector-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **getkeyprotector** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " listet die Schutzvorrichtungen auf, mit denen der Verschlüsselungsschlüssel des Volumes geschützt wird. Wenn ein schutzschutztyp bereitgestellt wird, werden nur volumeschlüsselschutzvorrichtungen des angegebenen Typs zurückgegeben.

## <a name="syntax"></a>Syntax


```mof
uint32 GetKeyProtectors(
  [in, optional] uint32 KeyProtectorType,
  [out]          string VolumeKeyProtectorID[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Keyprotector Type* \[ in, optional\]
</dt> <dd>

Typ: **UInt32**

Eine ganze Zahl ohne Vorzeichen, die den Typ der zurück zugebende Schlüssel Schutzvorrichtung angibt.

Wenn dieser Parameter nicht angegeben wird, werden alle verfügbaren Schlüssel Schutzvorrichtungen des Volumes zurückgegeben.



| Wert                                                                         | Bedeutung                                                           |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  | Alle Typen.<br/> Alle Schlüssel Schutzvorrichtungen werden zurückgegeben.<br/> |
| <dl> <dt>1</dt> </dl>  | Trusted Platform Module (TPM).<br/>                         |
| <dl> <dt>2</dt> </dl>  | Externer Schlüssel.<br/>                                          |
| <dl> <dt>3</dt> </dl>  | Numerisches Kennwort.<br/>                                      |
| <dl> <dt>4</dt> </dl>  | TPM und PIN.<br/>                                           |
| <dl> <dt>5</dt> </dl>  | TPM-und Systemstart Schlüssel.<br/>                                   |
| <dl> <dt>6</dt> </dl>  | TPM-und PIN-und Systemstart Schlüssel.<br/>                           |
| <dl> <dt>7</dt> </dl>  | Öffentlicher Schlüssel.<br/>                                            |
| <dl> <dt>8</dt> </dl>  | Passphrase.<br/>                                            |
| <dl> <dt>9</dt> </dl>  | TPM-Zertifikat<br/>                                        |
| <dl> <dt>10</dt> </dl> | Sicherheits-ID (SID)<br/>                              |



 

</dd> <dt>

*Volumekeyprotectorid* \[ vorgenommen\]
</dt> <dd>

Typ: **Zeichen \[ \] Folge**

Ein Array von Zeichen folgen, die die zum Schutz des Verschlüsselungsschlüssels des Volumes verwendeten Schlüssel Schutzvorrichtungen identifizieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                  | BESCHREIBUNG                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Die Methode war erfolgreich.<br/>                                                                          |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | Der *volumekeyprotectorid-* Parameter ist angegeben, verweist jedoch nicht auf einen gültigen *keyprotectortype*.<br/> |
| <dl> <dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu. <br/>                   |



 

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

 

 
