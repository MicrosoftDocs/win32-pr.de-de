---
description: Entfernt den externen Schlüssel, der auf dem aktuell ausgeführten Betriebssystem-Volume gespeichert ist.
ms.assetid: a8c4bb3b-6566-4173-b550-e89740f1cba6
title: DisableAutoUnlock-Methode der Win32_EncryptableVolume Klasse
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
ms.openlocfilehash: ce3a6bbb396136b128e084da0e64a79ad2f403217d8ac51dcf67b57941cc4a4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004558"
---
# <a name="disableautounlock-method-of-the-win32_encryptablevolume-class"></a>DisableAutoUnlock-Methode der Win32 \_ EncryptableVolume-Klasse

Die **DisableAutoUnlock-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) entfernt den externen Schlüssel, der auf dem aktuell ausgeführten Betriebssystemvolume gespeichert ist, sodass ein Datenvolume nicht automatisch entsperrt wird, wenn es bereitgestellt wird, z. B. wenn Wechselmedien mit dem Computer verbunden sind.

Wenn die automatische Entsperrung deaktiviert oder angehalten wird, müssen die Methoden [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) oder [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) verwendet werden, um das Volume zu entsperren.

## <a name="syntax"></a>Syntax


```mof
uint32 DisableAutoUnlock();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                       | BESCHREIBUNG                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                       | Die Methode war erfolgreich.<br/>                                                       |
| <dl> <dt> **FVE \_ E VOLUME NOT BOUND \_ \_ \_ 2150694935**</dt> <dt>(0x80310017)</dt> </dl> | Die automatische Entsperrung auf dem Volume ist deaktiviert.<br/>                                   |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>      | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüsselschutzvorrichtung hinzu, um BitLocker zu aktivieren.<br/> |
| <dl> <dt>**FVE \_ E \_ NOT \_ DATA \_ VOLUME**</dt> <dt>2150694937 (0x80310019)</dt> </dl>   | Die -Methode kann nicht für das derzeit ausgeführte Betriebssystem-Volume ausgeführt werden.<br/>      |



 

## <a name="remarks"></a>Hinweise

Wenn keine Fehler zurückgegeben werden, entfernt diese Methode alle Volumeschutz-IDs und externen Schlüssel, die zum automatischen Entsperren des Volumes verwendet werden, aus der Registrierung.

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

 

 
