---
description: Ruft den externen Schlüssel für eine bestimmte Schlüsselschutzvorrichtung ab.
ms.assetid: d2b5e7d4-97c1-4d7f-a155-b5cdca2b552e
title: GetKeyProtectorExternalKey-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f6db531e28880c6b47cb41d87769917a524965984e2a2fc1099f0d0aa65095f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119667890"
---
# <a name="getkeyprotectorexternalkey-method-of-the-win32_encryptablevolume-class"></a>GetKeyProtectorExternalKey-Methode der Win32 \_ EncryptableVolume-Klasse

Die **GetKeyProtectorExternalKey-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) ruft den externen Schlüssel für eine bestimmte Schlüsselschutzvorrichtung des entsprechenden Typs ab.

Der Schlüsselschutzvorrichtungsbezeichner muss auf eine Schlüsselschutzvorrichtung vom Typ "Externer Schlüssel", "TPM und PIN und Startschlüssel" oder "TPM und Startschlüssel" verweisen.

## <a name="syntax"></a>Syntax


```mof
uint32 GetKeyProtectorExternalKey(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  ExternalKey[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*VolumeKeyProtectorID* \[ In\]
</dt> <dd>

Typ: **Zeichenfolge**

Ein eindeutiger Zeichenfolgenbezeichner, der zum Verwalten einer verschlüsselten Volumeschlüsselschutzvorrichtung verwendet wird.

</dd> <dt>

*ExternalKey* \[ out\]
</dt> <dd>

Typ: **uint8 \[ \]**

Ein Bytearray, das den externen 256-Bit-Schlüssel angibt, der zum Entsperren des entsprechenden Volumes verwendet werden kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn er fehlschlägt.



| Rückgabecode/-wert                                                                                                                                                                  | Beschreibung                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Die Methode war erfolgreich.<br/>                                                                                                                                  |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | Das Volume ist gesperrt.<br/>                                                                                                                                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | Der *Parameter VolumeKeyProtectorID* verweist nicht auf eine Schlüsselschutzvorrichtung vom Typ "Externer Schlüssel", "TPM und PIN und Startschlüssel" oder "TPM und Startschlüssel".<br/> |
| <dl> <dt>**FVE \_ E \_ NICHT \_ AKTIVIERT**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüsselschutzvorrichtung hinzu, um BitLocker zu aktivieren. <br/>                                                                           |



 

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

 

 
