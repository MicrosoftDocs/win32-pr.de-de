---
description: Entfernt alle externen Schlüssel und zugehörigen Informationen, die auf dem momentan laufenden Betriebssystem Volume gespeichert sind, das zum automatischen Entsperren von Datenvolumes verwendet wird.
ms.assetid: a5fef793-0634-493d-b62d-cb842844b1e8
title: Clearallautounlockkeys-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ClearAllAutoUnlockKeys
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: b7f7e68891865893c1444a2c5de2370799b74426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345034"
---
# <a name="clearallautounlockkeys-method-of-the-win32_encryptablevolume-class"></a>Clearallautounlockkeys-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **clearallautounlockkeys** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " entfernt alle externen Schlüssel und zugehörigen Informationen, die auf dem momentan ausgelaufenden Betriebssystem Volume gespeichert sind, das zum automatischen Entsperren von Datenvolumes verwendet wird.

## <a name="syntax"></a>Syntax


```mof
uint32 ClearAllAutoUnlockKeys();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                   | BESCHREIBUNG                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                   | Die Methode war erfolgreich.<br/>                                                        |
| <dl> <dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt> </dl>  | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu. <br/> |
| <dl> <dt>**F \_ E \_ Not \_ OS \_ Volume**</dt> <dt>2150694952 (0x80310028)</dt> </dl> | Die-Methode kann nur für das aktuell laufende Betriebssystem Volume ausgeführt werden.<br/>     |



 

## <a name="remarks"></a>Bemerkungen

**Clearallautounlockkeys** erreicht die gleiche Funktionalität wie das Ausführen von [**disableautounlock**](disableautounlock-win32-encryptablevolume.md) für jedes Daten Volume, das jemals dem aktuell ausgelaufenden Betriebssystem zugeordnet ist. Dies gilt auch für Datenvolumes, die derzeit nicht mit dem Computer verbunden sind. Außerdem werden alle veralteten entsperrinformationen entfernt, die Daten Volumes zugeordnet sind, die nicht mehr vorhanden sind.

Verwenden Sie vor dem Aufrufen von " [**entschlüsseln**](decrypt-win32-encryptablevolume.md) " auf dem derzeit ausgelaufenden Betriebssystem Volume " **clearallautounlockkeys** ", um sicherzustellen, dass die Informationen in der Registrierung des Betriebssystems zum automatischen Entsperren von Datenvolumes nicht auf der Festplatte zugänglich sind.

Nachdem **clearallautounlockkeys** erfolgreich ausgeführt wurde, können die Methoden " [**unlockwithexternalkey**](unlockwithexternalkey-win32-encryptablevolume.md) " oder " [**unlockwithnumericalpassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) " verwendet werden, um alle Datenvolumes auf diesem Computer zu entsperren. Verwenden Sie [**enableautounlock**](enableautounlock-win32-encryptablevolume.md) zum erneuten Aktivieren des automatischen Entsperrens eines Datenvolumens.

Wenn keine anderen Fehler zurückgegeben werden, entfernt **clearallautounlockkeys** alle volumeschutzvorrichtungen und externen Schlüssel aus der Registrierung, die zum automatischen Entsperren von Datenvolumen verwendet werden, die jemals dem aktuell ausgelaufenden Betriebssystem Volume zugeordnet wurden.

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

 

 
