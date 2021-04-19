---
description: Verwendet einen bereitgestellten externen Schlüssel für den Zugriff auf den Inhalt eines Datenvolumens.
ms.assetid: e383767e-8557-469c-bc44-f67591c46f23
title: Unlockwithexternalkey-Methode der Win32_EncryptableVolume-Klasse
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
ms.openlocfilehash: 4b599f098856937ae5610156cba96a1deea1f64b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363363"
---
# <a name="unlockwithexternalkey-method-of-the-win32_encryptablevolume-class"></a>Unlockwithexternalkey-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **unlockwithexternalkey** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " verwendet einen bereitgestellten externen Schlüssel für den Zugriff auf den Inhalt eines Datenvolumens.

Der Verschlüsselungsschlüssel des Volumes muss mit einer oder mehreren Schlüssel Schutzvorrichtungen des Typs "externer Schlüssel" gesichert werden, indem die [**protectkeywithexternalkey**](protectkeywithexternalkey-win32-encryptablevolume.md) -Methode verwendet wird, um das Volume mit dieser Methode entsperren zu können.

> [!Note]  
> Wenn die Festplatte Hardware Verschlüsselung unterstützt, legt diese Funktion den Bandstatus auf "entsperrt" fest.

 

## <a name="syntax"></a>Syntax


```mof
uint32 UnlockWithExternalKey(
  [in] uint8 ExternalKey[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ExternalKey* \[ in\]
</dt> <dd>

Typ: **Uint8 \[ \]**

Ein Bytearray, das den externen 256-Bit-Schlüssel angibt, mit dem das Volume entsperrt wird. Dieser Schlüssel kann durch Aufrufen der [**getexternalkeyfromfile**](getexternalkeyfromfile-win32-encryptablevolume.md) -Methode abgerufen werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.

Wenn das Volume bereits entsperrt ist, gibt diese Methode 0 zurück.



| Rückgabecode/-wert                                                                                                                                                                  | BESCHREIBUNG                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Die Methode war erfolgreich.<br/>                                                                                                       |
| <dl> <dt>**Fehler \_ Es \_**</dt> wurde <dt>kein Wert gefunden (0x)</dt> . </dl>          | Das Volume weist keine Schlüssel Schutzvorrichtung vom Typ "externer Schlüssel" auf.<br/>                                                             |
| <dl> <dt>**Fehler \_ Ungültiges \_ Kennwort**</dt> <dt>kein Wert angegeben (0x)</dt> </dl>   | Mindestens eine Schlüssel Schutzvorrichtung des Typs "externer Schlüssel" ist vorhanden, aber der angegebene *ExternalKey* -Parameter kann das Volume nicht entsperren.<br/> |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | Der *ExternalKey* -Parameter ist kein Array der Größe 4.<br/>                                                                           |
| <dl> <dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu. <br/>                                                |



 

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

 

 
