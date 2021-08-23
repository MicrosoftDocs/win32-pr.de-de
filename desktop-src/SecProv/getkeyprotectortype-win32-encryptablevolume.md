---
description: Gibt den Typ einer bestimmten Schlüsselschutzvorrichtung an.
ms.assetid: 17cdde18-3979-4a19-b36e-aa71994148c9
title: GetKeyProtectorType-Methode der Win32_EncryptableVolume Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorType
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: d55603644c675d80341f1b82713ba66ae9ea310aadc19843dd724b233e34dc24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119667670"
---
# <a name="getkeyprotectortype-method-of-the-win32_encryptablevolume-class"></a>GetKeyProtectorType-Methode der Win32 \_ EncryptableVolume-Klasse

Die **GetKeyProtectorType-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) gibt den Typ einer bestimmten Schlüsselschutzvorrichtung an.

## <a name="syntax"></a>Syntax


```mof
uint32 GetKeyProtectorType(
  [in]  string VolumeKeyProtectorID,
  [out] uint32 KeyProtectorType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*VolumeKeyProtectorID* \[ In\]
</dt> <dd>

Typ: **Zeichenfolge**

Ein eindeutiger Zeichenfolgenbezeichner, der zum Verwalten einer verschlüsselten Volumeschlüsselschutzvorrichtung verwendet wird.

</dd> <dt>

*KeyProtectorType* \[ out\]
</dt> <dd>

Typ: **uint32**

Eine ganze Zahl ohne Vorzeichen, die den Typ der Schlüsselschutzvorrichtung angibt.



| Wert                                                                         | Bedeutung                                              |
|-------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  | Unbekannter oder anderer Schutzvorrichtungstyp<br/>           |
| <dl> <dt>1</dt> </dl>  | Trusted Platform Module (TPM)<br/>             |
| <dl> <dt>2</dt> </dl>  | Externer Schlüssel<br/>                              |
| <dl> <dt>3</dt> </dl>  | Numerisches Kennwort<br/>                        |
| <dl> <dt>4</dt> </dl>  | TPM und PIN<br/>                               |
| <dl> <dt>5</dt> </dl>  | TPM und Startschlüssel<br/>                       |
| <dl> <dt>6</dt> </dl>  | TPM und PIN und Startschlüssel<br/>               |
| <dl> <dt>7</dt> </dl>  | Öffentlicher Schlüssel<br/>                                |
| <dl> <dt>8</dt> </dl>  | Passphrase<br/>                                |
| <dl> <dt>9</dt> </dl>  | TPM-Zertifikat<br/>                           |
| <dl> <dt>10</dt> </dl> | CryptoAPI Next Generation -Schutzvorrichtung (CNG)<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                  | Beschreibung                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Die Methode war erfolgreich.<br/>                                                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | Der *VolumeKeyProtectorID-Parameter* bezieht sich nicht auf einen gültigen *KeyProtectorType.*<br/> |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüsselschutzvorrichtung hinzu, um BitLocker zu aktivieren. <br/>  |



 

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

 

 
