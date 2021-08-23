---
description: Entfernt alle externen Schlüssel und zugehörigen Informationen, die auf dem aktuell ausgeführten Betriebssystemvolume gespeichert sind und zum automatischen Entsperren von Datenvolumes verwendet werden.
ms.assetid: a5fef793-0634-493d-b62d-cb842844b1e8
title: ClearAllAutoUnlockKeys-Methode der Win32_EncryptableVolume-Klasse
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
ms.openlocfilehash: 46ee3791425afafe63b0d566c3f4204fecc9195f4341b90caee4c95306afdeab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119668170"
---
# <a name="clearallautounlockkeys-method-of-the-win32_encryptablevolume-class"></a>ClearAllAutoUnlockKeys-Methode der Win32 \_ EncryptableVolume-Klasse

Die **ClearAllAutoUnlockKeys-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) entfernt alle externen Schlüssel und zugehörigen Informationen, die auf dem aktuell ausgeführten Betriebssystemvolume gespeichert sind und zum automatischen Entsperren von Datenvolumes verwendet werden.

## <a name="syntax"></a>Syntax


```mof
uint32 ClearAllAutoUnlockKeys();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn er fehlschlägt.



| Rückgabecode/-wert                                                                                                                                                                   | Beschreibung                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                   | Die Methode war erfolgreich.<br/>                                                        |
| <dl> <dt>**FVE \_ E \_ NICHT \_ AKTIVIERT**</dt> <dt>2150694920 (0x80310008)</dt> </dl>  | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüsselschutzvorrichtung hinzu, um BitLocker zu aktivieren. <br/> |
| <dl> <dt>**FVE \_ E \_ NOT \_ OS \_ VOLUME**</dt> <dt>2150694952 (0x80310028)</dt> </dl> | Die -Methode kann nur für das aktuell ausgeführte Betriebssystemvolume ausgeführt werden.<br/>     |



 

## <a name="remarks"></a>Hinweise

**ClearAllAutoUnlockKeys** erreicht die gleiche Funktionalität wie die Ausführung von [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) für jedes Datenvolume, das jemals dem aktuell ausgeführten Betriebssystem zugeordnet wurde, auch für Datenvolumes, die derzeit nicht mit dem Computer verbunden sind. Außerdem werden veraltete Entsperrinformationen entfernt, die nicht mehr vorhandenen Datenvolumes zugeordnet sind.

Verwenden Sie vor dem Aufrufen von [**Decrypt**](decrypt-win32-encryptablevolume.md) auf dem aktuell ausgeführten Betriebssystemvolume **ClearAllAutoUnlockKeys,** um sicherzustellen, dass auf dem Datenträger nicht auf Informationen zugegriffen werden kann, die in der Betriebssystemregistrierung zum automatischen Entsperren von Datenvolumes gespeichert sind.

Nachdem **ClearAllAutoUnlockKeys** erfolgreich ausgeführt wurde, können die Methoden [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) oder [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) verwendet werden, um alle Datenvolumes auf diesem Computer zu entsperren. Verwenden Sie [**EnableAutoUnlock,**](enableautounlock-win32-encryptablevolume.md) um das automatische Entsperren eines Datenvolumes erneut zu aktivieren.

Wenn keine anderen Fehler zurückgegeben werden, entfernt **ClearAllAutoUnlockKeys** alle Volumeschutzvorrichtungs-IDs und externen Schlüssel aus der Registrierung, die zum automatischen Entsperren aller Datenvolumes verwendet werden, die jemals dem aktuell ausgeführten Betriebssystemvolume zugeordnet wurden.

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

 

 
