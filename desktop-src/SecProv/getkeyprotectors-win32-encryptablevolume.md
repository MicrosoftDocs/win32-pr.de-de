---
description: Listet die Schutzvorrichtungen auf, die zum Sichern des Verschlüsselungsschlüssels des Volumes verwendet werden.
ms.assetid: ea88f128-c835-49e3-a395-c5ba472fff4b
title: GetKeyProtectors-Methode der Win32_EncryptableVolume-Klasse
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
ms.openlocfilehash: 01342b932e3a285870026ef57bfa0040d1659ca7af1165e6fb67f3af780896d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119667680"
---
# <a name="getkeyprotectors-method-of-the-win32_encryptablevolume-class"></a>GetKeyProtectors-Methode der Win32 \_ EncryptableVolume-Klasse

Die **GetKeyProtectors-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) listet die Schutzvorrichtungen auf, die zum Sichern des Verschlüsselungsschlüssels des Volumes verwendet werden. Wenn ein Schutzvorrichtungstyp bereitgestellt wird, werden nur Volumeschlüsselschutzvorrichtungen des angegebenen Typs zurückgegeben.

## <a name="syntax"></a>Syntax


```mof
uint32 GetKeyProtectors(
  [in, optional] uint32 KeyProtectorType,
  [out]          string VolumeKeyProtectorID[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*KeyProtectorType* \[ in, optional\]
</dt> <dd>

Typ: **uint32**

Eine ganze Zahl ohne Vorzeichen, die den Typ der zurückzugebenden Schlüsselschutzvorrichtung angibt.

Wenn dieser Parameter nicht angegeben ist, werden alle verfügbaren Schlüsselschutzvorrichtungen des Volumes zurückgegeben.



| Wert                                                                         | Bedeutung                                                           |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  | Alle Typen.<br/> Alle Schlüsselschutzvorrichtungen werden zurückgegeben.<br/> |
| <dl> <dt>1</dt> </dl>  | Trusted Platform Module (TPM).<br/>                         |
| <dl> <dt>2</dt> </dl>  | Externer Schlüssel.<br/>                                          |
| <dl> <dt>3</dt> </dl>  | Numerisches Kennwort.<br/>                                      |
| <dl> <dt>4</dt> </dl>  | TPM und PIN.<br/>                                           |
| <dl> <dt>5</dt> </dl>  | TPM und Startschlüssel.<br/>                                   |
| <dl> <dt>6</dt> </dl>  | TPM und PIN und Startschlüssel.<br/>                           |
| <dl> <dt>7</dt> </dl>  | Öffentlicher Schlüssel.<br/>                                            |
| <dl> <dt>8</dt> </dl>  | Passphrase.<br/>                                            |
| <dl> <dt>9</dt> </dl>  | TPM-Zertifikat<br/>                                        |
| <dl> <dt>10</dt> </dl> | Sicherheits-ID (SID)<br/>                              |



 

</dd> <dt>

*VolumeKeyProtectorID* \[ out\]
</dt> <dd>

Typ: **\[ \] Zeichenfolge**

Ein Array von Zeichenfolgen, die die Schlüsselschutzvorrichtungen identifizieren, die zum Sichern des Verschlüsselungsschlüssels des Volumes verwendet werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn er fehlschlägt.



| Rückgabecode/-wert                                                                                                                                                                  | Beschreibung                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Die Methode war erfolgreich.<br/>                                                                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | Der *VolumeKeyProtectorID-Parameter* wird angegeben, verweist jedoch nicht auf einen gültigen *KeyProtectorType.*<br/> |
| <dl> <dt>**FVE \_ E \_ NICHT \_ AKTIVIERT**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüsselschutzvorrichtung hinzu, um BitLocker zu aktivieren. <br/>                   |



 

## <a name="remarks"></a>Hinweise

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
</dt> </dl>

 

 
