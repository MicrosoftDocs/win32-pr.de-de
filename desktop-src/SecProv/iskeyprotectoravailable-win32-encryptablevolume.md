---
description: Gibt an, ob Schutzvorrichtungen für das Volume verfügbar sind.
ms.assetid: 92a959ea-27ec-4d38-a955-846bfd7b3a60
title: Iskeyprotectoravailable-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsKeyProtectorAvailable
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: a80f731bf77a39d1e16c7dfe9cca4884b80eec49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214512"
---
# <a name="iskeyprotectoravailable-method-of-the-win32_encryptablevolume-class"></a>Iskeyprotectoravailable-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **iskeyprotectoravailable** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " gibt an, ob Schutzvorrichtungen für das Volume verfügbar sind.

Wenn ein schutzschutztyp bereitgestellt wird, gibt die Methode an, ob Schutzvorrichtungen des angegebenen Typs für das Volume verfügbar sind.

## <a name="syntax"></a>Syntax


```mof
uint32 IsKeyProtectorAvailable(
  [in, optional] uint32  KeyProtectorType,
  [out]          boolean IsKeyProtectorAvailable
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Keyprotector Type* \[ in, optional\]
</dt> <dd>

Typ: **UInt32**

Eine ganze Zahl ohne Vorzeichen, die den Typ der abgefragten volumeschlüsselschutzvorrichtung angibt.

Wenn dieser Parameter nicht angegeben wird, werden alle verfügbaren Schlüssel Schutzvorrichtungen des Volumes abgefragt.



| Wert                                                                         | Bedeutung                                                          |
|-------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  | Alle Typen.<br/> Alle Schlüssel Schutzvorrichtungen werden abgefragt.<br/> |
| <dl> <dt>1</dt> </dl>  | Trusted Platform Module (TPM).<br/>                        |
| <dl> <dt>2</dt> </dl>  | Externer Schlüssel.<br/>                                         |
| <dl> <dt>3</dt> </dl>  | Numerisches Kennwort.<br/>                                   |
| <dl> <dt>4</dt> </dl>  | TPM und PIN.<br/>                                          |
| <dl> <dt>5</dt> </dl>  | TPM-und Systemstart Schlüssel.<br/>                                  |
| <dl> <dt>6</dt> </dl>  | TPM-und PIN-und Systemstart Schlüssel.<br/>                          |
| <dl> <dt>7</dt> </dl>  | Öffentlicher Schlüssel.<br/>                                           |
| <dl> <dt>8</dt> </dl>  | Passphrase.<br/>                                           |
| <dl> <dt>9</dt> </dl>  | TPM-Zertifikat<br/>                                       |
| <dl> <dt>10</dt> </dl> | Sicherheits-ID (SID)<br/>                             |



 

</dd> <dt>

*Iskeyprotector available* \[ vorgenommen\]
</dt> <dd>

Typ: **booleschen**

Ein boolescher Wert, der angibt, ob eine volumeschlüsselschutzvorrichtung des angegebenen Typs auf dem Volume vorhanden ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                         | BESCHREIBUNG                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                         | Die Methode war erfolgreich.<br/>                                                                      |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>2147942487 (0x80070057)</dt> </dl> | Der *keyprotectortype* -Parameter wird angegeben, verweist jedoch nicht auf einen gültigen schlüsselschutzschutztyp.<br/> |



 

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

 

 
