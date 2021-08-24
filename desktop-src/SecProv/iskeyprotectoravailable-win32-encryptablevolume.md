---
description: Gibt an, ob Schutzvorrichtungen für das Volume verfügbar sind.
ms.assetid: 92a959ea-27ec-4d38-a955-846bfd7b3a60
title: IsKeyProtectorAvailable-Methode der Win32_EncryptableVolume Klasse
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
ms.openlocfilehash: 8991d6b111efbcd94ee21414d1ffd899a1890f942d6b3c5d207c8092a817ad8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119667350"
---
# <a name="iskeyprotectoravailable-method-of-the-win32_encryptablevolume-class"></a>IsKeyProtectorAvailable-Methode der Win32 \_ EncryptableVolume-Klasse

Die **IsKeyProtectorAvailable-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) gibt an, ob Schutzvorrichtungen für das Volume verfügbar sind.

Wenn ein Schutzvorrichtungstyp angegeben wird, gibt die -Methode an, ob Schutzvorrichtungen des angegebenen Typs für das Volume verfügbar sind.

## <a name="syntax"></a>Syntax


```mof
uint32 IsKeyProtectorAvailable(
  [in, optional] uint32  KeyProtectorType,
  [out]          boolean IsKeyProtectorAvailable
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*KeyProtectorType* \[ in, optional\]
</dt> <dd>

Typ: **uint32**

Eine ganze Zahl ohne Vorzeichen, die den Typ der abgefragten Volumeschlüsselschutzvorrichtung angibt.

Wenn dieser Parameter nicht angegeben wird, werden alle verfügbaren Schlüsselschutzvorrichtungen des Volumes abgefragt.



| Wert                                                                         | Bedeutung                                                          |
|-------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  | Alle Typen.<br/> Alle Schlüsselschutzvorrichtungen werden abgefragt.<br/> |
| <dl> <dt>1</dt> </dl>  | Trusted Platform Module (TPM).<br/>                        |
| <dl> <dt>2</dt> </dl>  | Externer Schlüssel.<br/>                                         |
| <dl> <dt>3</dt> </dl>  | Numerisches Kennwort.<br/>                                   |
| <dl> <dt>4</dt> </dl>  | TPM und PIN.<br/>                                          |
| <dl> <dt>5</dt> </dl>  | TPM und Startschlüssel.<br/>                                  |
| <dl> <dt>6</dt> </dl>  | TPM und PIN und Startschlüssel.<br/>                          |
| <dl> <dt>7</dt> </dl>  | Öffentlicher Schlüssel.<br/>                                           |
| <dl> <dt>8</dt> </dl>  | Passphrase.<br/>                                           |
| <dl> <dt>9</dt> </dl>  | TPM-Zertifikat<br/>                                       |
| <dl> <dt>10</dt> </dl> | Sicherheits-ID (SID)<br/>                             |



 

</dd> <dt>

*IsKeyProtectorAvailable* \[ out\]
</dt> <dd>

Typ: **boolescher Wert**

Ein boolescher Wert, der angibt, ob eine Volumeschlüsselschutzvorrichtung des angegebenen Typs auf dem Volume vorhanden ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                         | Beschreibung                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                         | Die Methode war erfolgreich.<br/>                                                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl> | Der *KeyProtectorType-Parameter* wird angegeben, bezieht sich aber nicht auf einen gültigen Schlüsselschutzvorrichtungstyp.<br/> |



 

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

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

 

 
