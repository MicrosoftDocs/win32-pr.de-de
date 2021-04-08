---
description: Ermöglicht das automatische Entsperren eines Datenvolumens, wenn das Volume eingebunden wird.
ms.assetid: ec77b17f-545b-40a7-91b2-ff0b32b8370d
title: Enableautounlock-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EnableAutoUnlock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 39456e9130081e52820cd91ba3e191ee40ab2374
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865424"
---
# <a name="enableautounlock-method-of-the-win32_encryptablevolume-class"></a>Enableautounlock-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **enableautounlock** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " ermöglicht das automatische Entsperren eines Datenvolumens, wenn das Volume eingebunden wird.

Bei der automatischen Entsperrung wird ein externer Schlüssel im Betriebssystem gespeichert, mit dem das Volume automatisch auf dem momentan laufenden Betriebssystem Volume entsperrt werden kann.

Um diese Methode verwenden zu können, muss das Betriebssystem Volume bereits durch BitLocker-Laufwerkverschlüsselung geschützt werden, oder es muss eine Verschlüsselung ausgeführt werden. Außerdem muss bereits ein externer Schlüssel für das Datenvolumen vorhanden sein. Verwenden Sie [**protectkeywithexternalkey**](protectkeywithexternalkey-win32-encryptablevolume.md) , um den externen Schlüssel zu erstellen, mit dem das Volume automatisch entsperrt werden kann.

## <a name="syntax"></a>Syntax


```mof
uint32 EnableAutoUnlock(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Volumekeyprotectorid* \[ in\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die die Schlüssel Schutzvorrichtung des Typs "externer Schlüssel" identifiziert, der zum automatischen Entsperren des Volumes verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                           | BESCHREIBUNG                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                           | Die Methode war erfolgreich.<br/>                                                                                                                                        |
| <dl> <dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl>          | Das Volume ist gesperrt.<br/>                                                                                                                                             |
| <dl> <dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt> </dl>          | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu. <br/>                                                                                 |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                   | Der *volumekeyprotectorid-* Parameter verweist nicht auf eine gültige Schlüssel Schutzvorrichtung vom Typ "externer Schlüssel".<br/>                                                          |
| <dl> <dt>**F \_ E \_ Not \_ Data \_ Volume**</dt> <dt>2150694937 (0x80310019)</dt> </dl>       | Die Methode kann nicht für das aktuell laufende Betriebssystem Volume ausgeführt werden.<br/>                                                                                       |
| <dl> <dt>**F \_ E \_ OS \_ nicht \_ geschützt**</dt> <dt>2150694944 (0x80310020)</dt> </dl>      | Die Methode kann nicht ausgeführt werden, wenn das derzeit ausgeführte Betriebssystem Volume nicht durch BitLocker-Laufwerkverschlüsselung geschützt ist oder keine Verschlüsselung ausgeführt wird.<br/> |
| <dl> Das <dt> **Volume \_ wurde \_ \_ \_ bereits**</dt> <dt>2150694943 (0x8031001f)</dt> gebunden. </dl> | Das automatische Entsperren auf dem Volume wurde bereits aktiviert.<br/>                                                                                                    |



 

## <a name="remarks"></a>Bemerkungen

Wenn eine gültige volumeschlüsselschutzvorrichtung vom Typ "externer Schlüssel" angegeben ist, wird der zugehörige externe 256-Bit-Schlüssel aus der Schutzvorrichtung extrahiert und in der Registrierung des aktuell ausgelaufenden Betriebssystems zusammen mit der volumeschlüsselschutzvorrichtung-ID gespeichert.

Wenn der der volumeschlüsselschutzkennung zugeordnete externe Schlüssel gelöscht wird, wird die Funktion zum automatischen Entsperren des Volumes deaktiviert oder angehalten.

> [!Note]  
> Wechselmedien werden zurzeit nicht unterstützt.

 

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

 

 
