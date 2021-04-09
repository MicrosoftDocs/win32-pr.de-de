---
description: Hebt die Bereitstellung des Volumes auf und entfernt den Verschlüsselungsschlüssel des Volumes aus dem System Arbeitsspeicher.
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
ms.openlocfilehash: 8fb6cd7b4134f4921cdaf57414843fb6522c5823
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862287"
---
# <a name="lock-method-of-the-win32_encryptablevolume-class"></a>Lock-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Mit der **Lock** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " wird das Volume getrennt, und der Verschlüsselungsschlüssel des Volumes wird aus dem Systemspeicher entfernt. Der Inhalt des Volumes bleibt so lange nicht zugänglich, bis er entweder durch die [**unlockwithexternalkey**](unlockwithexternalkey-win32-encryptablevolume.md) -Methode oder die [**unlockwithnumericalpassword-Methode entsperrt**](unlockwithnumericalpassword-win32-encryptablevolume.md) wird. Diese Methode kann für das aktuell laufende Betriebssystem Volume nicht erfolgreich ausgeführt werden.

> [!Note]  
> Wenn die Festplatte die Hardware Verschlüsselung unterstützt, wird das Band auf "gesperrt" festgelegt.

 

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

Typ: **booleschen**

**True** gibt an, dass die Bereitstellung des Datenträgers erzwungen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                           | BESCHREIBUNG                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                           | Die Methode war erfolgreich.<br/>                                                                                                                                     |
| <dl> <dt>**E \_ Zugriff \_ verweigert**</dt> <dt>2147942405 (0x80070005)</dt> </dl>               | Anwendungen greifen auf dieses Volume zu. Wenn der gesamte Zugriff nicht exklusiv ist, kann die-Methode erfolgreich ausgeführt werden, wenn der *ForceDismount* -Parameter als true angegeben wird.<br/> |
| <dl> <dt>**F \_ E \_ nicht \_ verschlüsselt**</dt> <dt>2150694913 (0x80310001)</dt> </dl>          | Das Volume wird vollständig entschlüsselt und kann nicht gesperrt werden.<br/>                                                                                                            |
| <dl> <dt>**F \_ E- \_ Schutz \_ deaktiviert**</dt> <dt>2150694945 (0x80310021)</dt> </dl>    | Der Verschlüsselungsschlüssel für das Volume ist auf dem Datenträger im Klartext verfügbar, sodass das Volume nicht gesperrt werden kann.<br/>                                                    |
| <dl> <dt>**F \_ E \_ Wiederherstellungs \_ Schlüssel \_ erforderlich**</dt> <dt>2150694946 (0x80310022)</dt> </dl> | Das Volume weist keine Schlüssel Schutzvorrichtungen des Typs "numerisches Kennwort" oder "externer Schlüssel" auf, die zum Entsperren des Volumes erforderlich sind.<br/>                            |



 

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

 

 
