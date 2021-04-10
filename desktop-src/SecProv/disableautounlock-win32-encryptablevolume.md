---
description: Entfernt den externen Schlüssel, der auf dem momentan laufenden Betriebssystem Volume gespeichert ist.
ms.assetid: a8c4bb3b-6566-4173-b550-e89740f1cba6
title: Disableautounlock-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DisableAutoUnlock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 6dd4e11e2ff4906627c2d790987500062136d56d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865435"
---
# <a name="disableautounlock-method-of-the-win32_encryptablevolume-class"></a>Disableautounlock-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **disableautounlock** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " entfernt den externen Schlüssel, der auf dem momentan laufenden Betriebssystem Volume gespeichert ist, sodass ein Daten Volume bei der Bereitstellung nicht automatisch entsperrt wird, z. b. wenn Wechsel Speichergeräte mit dem Computer verbunden sind.

Wenn das automatische Entsperren deaktiviert oder angehalten wird, müssen die Methoden " [**unlockwithexternalkey**](unlockwithexternalkey-win32-encryptablevolume.md) " oder " [**unlockwithnumericalpassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) " verwendet werden, um das Volume zu entsperren.

## <a name="syntax"></a>Syntax


```mof
uint32 DisableAutoUnlock();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                       | BESCHREIBUNG                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                       | Die Methode war erfolgreich.<br/>                                                       |
| <dl> Laufwerk <dt> **\_ E \_ \_ nicht \_ gebunden**</dt> <dt>2150694935 (0x80310017)</dt> </dl> | Das automatische Entsperren auf dem Volume ist deaktiviert.<br/>                                   |
| <dl> <dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt> </dl>      | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu.<br/> |
| <dl> <dt>**F \_ E \_ Not \_ Data \_ Volume**</dt> <dt>2150694937 (0x80310019)</dt> </dl>   | Die Methode kann nicht für das aktuell laufende Betriebssystem Volume ausgeführt werden.<br/>      |



 

## <a name="remarks"></a>Bemerkungen

Wenn keine Fehler zurückgegeben werden, entfernt diese Methode alle volumeschutzvorrichtungen und externen Schlüssel aus der Registrierung, die zum automatischen Entsperren des Volumes verwendet werden.

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

 

 
