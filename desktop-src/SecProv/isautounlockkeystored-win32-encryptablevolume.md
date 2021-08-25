---
description: Gibt an, ob externe Schlüssel oder zugehörige Informationen, die zum automatischen Entsperren von Datenvolumes verwendet werden können, auf dem aktuell ausgeführten Betriebssystemvolume vorhanden sind.
ms.assetid: 37e7fe85-312d-49ff-aa6b-8c76c4fc4bba
title: IsAutoUnlockKeyStored-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsAutoUnlockKeyStored
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: c28f8357edd88322f6f4498fd1e5b7156eeeff0b67d53b4d759c6935f4e9f9eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906310"
---
# <a name="isautounlockkeystored-method-of-the-win32_encryptablevolume-class"></a>IsAutoUnlockKeyStored-Methode der Win32 \_ EncryptableVolume-Klasse

Die **IsAutoUnlockKeyStored-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) gibt an, ob externe Schlüssel oder zugehörige Informationen, die zum automatischen Entsperren von Datenvolumes verwendet werden können, auf dem aktuell ausgeführten Betriebssystemvolume vorhanden sind.

## <a name="syntax"></a>Syntax


```mof
uint32 IsAutoUnlockKeyStored(
  [out] boolean IsAutoUnlockKeyStored
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IsAutoUnlockKeyStored* \[ out\]
</dt> <dd>

Typ: **boolescher Wert**

Ist **TRUE,** wenn Informationen, die zum automatischen Entsperren von Datenvolumes verwendet werden können, in der Registrierung des aktuell ausgeführten Betriebssystemvolumes gespeichert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn er fehlschlägt.



| Rückgabecode/-wert                                                                                                                                                                   | BESCHREIBUNG                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                   | Die Methode war erfolgreich.<br/>                                                        |
| <dl> <dt>**FVE \_ E \_ NICHT \_ AKTIVIERT**</dt> <dt>2150694920 (0x80310008)</dt> </dl>  | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüsselschutzvorrichtung hinzu, um BitLocker zu aktivieren. <br/> |
| <dl> <dt>**FVE \_ E \_ NOT \_ OS \_ VOLUME**</dt> <dt>2150694952 (0x80310028)</dt> </dl> | Die -Methode kann nur für das aktuell ausgeführte Betriebssystemvolume ausgeführt werden.<br/>     |



 

## <a name="remarks"></a>Hinweise

Verwenden Sie [**ClearAllAutoUnlockKeys,**](clearallautounlockkeys-win32-encryptablevolume.md) um alle Entsperrungsinformationen aus dem aktuell ausgeführten Betriebssystemvolume zu entfernen.

Informationen zum Entsperren eines Volumes werden gespeichert, wenn [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) für ein Datenvolume ausgeführt wird, während das aktuell ausgeführte Betriebssystemvolume ausgeführt wird.

**IsAutoUnlockKeyStored** unterscheidet sich von [**IsAutoUnlockEnabled**](isautounlockenabled-win32-encryptablevolume.md) darin, dass auch wenn die automatische Entsperrung für alle Datenvolumes deaktiviert ist, die derzeit mit dem Computer verbunden sind, möglicherweise weiterhin Entsperrinformationen im Zusammenhang mit getrennten Datenvolumes oder Datenvolumes vorhanden sind, die nicht mehr vorhanden sind.

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

 

 
