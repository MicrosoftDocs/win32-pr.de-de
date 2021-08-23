---
description: Verwendet einen bereitgestellten externen Schlüssel für den Zugriff auf den Inhalt eines Datenvolumens.
ms.assetid: e383767e-8557-469c-bc44-f67591c46f23
title: UnlockWithExternalKey-Methode der Win32_EncryptableVolume Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: a61e85608e8ed0f3e5b014d015ce7d59c4f01c8d97ab9092864fe9bb338833ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004218"
---
# <a name="unlockwithexternalkey-method-of-the-win32_encryptablevolume-class"></a>UnlockWithExternalKey-Methode der Win32 \_ EncryptableVolume-Klasse

Die **UnlockWithExternalKey-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) verwendet einen bereitgestellten externen Schlüssel für den Zugriff auf den Inhalt eines Datenvolumes.

Der Verschlüsselungsschlüssel des Volumes muss mit einer oder mehrere Schlüsselschutzvorrichtungen des Typs "Externer Schlüssel" mithilfe der [**ProtectKeyWithExternalKey-Methode**](protectkeywithexternalkey-win32-encryptablevolume.md) gesichert worden sein, um das Volume mit dieser Methode entsperren zu können.

> [!Note]  
> Wenn der Datenträger Hardwareverschlüsselung unterstützt, legt diese Funktion den Bandstatus auf "Entsperrt" fest.

 

## <a name="syntax"></a>Syntax


```mof
uint32 UnlockWithExternalKey(
  [in] uint8 ExternalKey[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ExternalKey* \[ In\]
</dt> <dd>

Typ: **uint8 \[ \]**

Ein Bytearray, das den externen 256-Bit-Schlüssel angibt, der zum Entsperren des Volumes verwendet wird. Dieser Schlüssel kann durch Aufrufen der [**GetExternalKeyFromFile-Methode ermittelt**](getexternalkeyfromfile-win32-encryptablevolume.md) werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.

Wenn das Volume bereits entsperrt ist, gibt diese Methode 0 zurück.



| Rückgabecode/-wert                                                                                                                                                                  | BESCHREIBUNG                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Die Methode war erfolgreich.<br/>                                                                                                       |
| <dl> <dt>**FEHLER \_ NICHT \_ GEFUNDEN**</dt> <dt>Kein Wert angegeben (0x)</dt> </dl>          | Das Volume verfügt nicht über eine Schlüsselschutzvorrichtung vom Typ "Externer Schlüssel".<br/>                                                             |
| <dl> <dt>**FEHLER \_ UNGÜLTIGES \_ KENNWORT**</dt> <dt>Kein Wert angegeben (0x)</dt> </dl>   | Mindestens eine Schlüsselschutzvorrichtung vom Typ "Externer Schlüssel" ist vorhanden, aber der angegebene *ExternalKey-Parameter* kann das Volume nicht entsperren.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | Der *ExternalKey-Parameter* ist kein Array der Größe 4.<br/>                                                                           |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüsselschutzvorrichtung hinzu, um BitLocker zu aktivieren. <br/>                                                |



 

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

 

 
