---
description: Entfernt die Bereitstellung des Volumes und entfernt den Verschlüsselungsschlüssel des Volumes aus dem Systemspeicher.
ms.assetid: 8d6e42a0-7b43-46d2-aa5e-941567ef2842
title: Lock-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Lock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f5053fe027bbae51ce93feb11de5f95bde1d7b17c85a05df1386e5470b1b20fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867660"
---
# <a name="lock-method-of-the-win32_encryptablevolume-class"></a>Lock-Methode der Win32 \_ EncryptableVolume-Klasse

Die **Lock-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) entfernt die Bereitstellung des Volumes und entfernt den Verschlüsselungsschlüssel des Volumes aus dem Systemspeicher. Auf den Inhalt des Volumes kann erst zugegriffen werden, wenn es mit der [**UnlockWithExternalKey-Methode**](unlockwithexternalkey-win32-encryptablevolume.md) oder der [**UnlockWithNumericalPassword-Methode entsperrt**](unlockwithnumericalpassword-win32-encryptablevolume.md) wird. Diese Methode kann für das derzeit ausgeführte Betriebssystem-Volume nicht erfolgreich ausgeführt werden.

> [!Note]  
> Wenn der Datenträger Hardwareverschlüsselung unterstützt, wird das Band auf "gesperrt" festgelegt.

 

## <a name="syntax"></a>Syntax


```mof
uint32 Lock(
  [in, optional] boolean ForceDismount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ForceDismount* \[ in, optional\]
</dt> <dd>

Typ: **boolescher Wert**

Wenn **"true"** ist, wird die Datenträgerbeendigung aufgehoben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                           | BESCHREIBUNG                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                           | Die Methode war erfolgreich.<br/>                                                                                                                                     |
| <dl> <dt>**E \_ ZUGRIFF \_ VERWEIGERT 2147942405**</dt> <dt>(0x80070005)</dt> </dl>               | Anwendungen greifen auf dieses Volume zu. Wenn der zugriffslose Zugriff nicht möglich ist, kann die Methode erfolgreich ausgeführt werden, wenn sie den *ForceDismount-Parameter* als TRUE angibt.<br/> |
| <dl> <dt>**FVE \_ E \_ NOT \_ ENCRYPTED**</dt> <dt>2150694913 (0x80310001)</dt> </dl>          | Das Volume ist vollständig entschlüsselt und kann nicht gesperrt werden.<br/>                                                                                                            |
| <dl> <dt>**FVE \_ E \_ PROTECTION \_ DISABLED**</dt> <dt>2150694945 (0x80310021)</dt> </dl>    | Der Verschlüsselungsschlüssel des Volumes ist in der Clear-Datei auf dem Datenträger verfügbar, um zu verhindern, dass das Volume gesperrt wird.<br/>                                                    |
| <dl> <dt>**FVE \_ E \_ RECOVERY \_ KEY \_ REQUIRED**</dt> <dt>2150694946 (0x80310022)</dt> </dl> | Das Volume verfügt nicht über Schlüsselschutzvorrichtungen vom Typ "Numerisches Kennwort" oder "Externer Schlüssel", die zum Entsperren des Volumes erforderlich sind.<br/>                            |



 

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

 

 
