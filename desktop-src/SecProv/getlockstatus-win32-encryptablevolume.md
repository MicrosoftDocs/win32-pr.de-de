---
description: Gibt an, ob der Inhalt des Volumes von Windows aus zugänglich ist.
ms.assetid: 54b2a41b-11c6-40ec-97fa-74996c15554e
title: Getlockstatus-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetLockStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3e81f77c37904f26e87f22b8e2b3b88763fe86cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342838"
---
# <a name="getlockstatus-method-of-the-win32_encryptablevolume-class"></a>Getlockstatus-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **getlockstatus** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " gibt an, ob der Inhalt des Volumes von Windows aus zugänglich ist.

## <a name="syntax"></a>Syntax


```mof
uint32 GetLockStatus(
  [out] uint32 LockStatus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Sperr Status* \[ vorgenommen\]
</dt> <dd>

Typ: **UInt32**

Gibt an, ob der Inhalt des Volumes von Windows aus zugänglich ist.



| Wert                                                                                                                                                                                                                           | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unlocked"></span><span id="unlocked"></span><span id="UNLOCKED"></span><dl> <dt>**Entsperrt**</dt> <dt>0</dt> </dl> | Für eine Standard-HDD:<br/> Der gesamte Inhalt des Volumes ist verfügbar. Ein entsperrtes Volume wird entweder vollständig entschlüsselt, oder der Verschlüsselungsschlüssel ist auf dem Datenträger Clear (Löschen) verfügbar. Das Volume mit dem aktuell ausgelaufenden Betriebssystem (z. b. dem ausgelaufenden Windows-Volume) ist immer verfügbar und kann nicht gesperrt werden.<br/> Für einen ehdd:<br/> Das Band ist dauerhaft entsperrt.<br/> |
| <span id="Locked"></span><span id="locked"></span><span id="LOCKED"></span><dl> <dt>**Gesperrt**</dt> <dt>1</dt> </dl>         | Für eine Standard-HDD:<br/> Auf alle oder einen Teil des Inhalts des Volumes kann nicht zugegriffen werden. Ein gesperrtes Volume muss teilweise oder vollständig verschlüsselt sein, und der Verschlüsselungsschlüssel darf nicht auf dem Datenträger "Clear on" verfügbar sein.<br/> Für einen ehdd:<br/> Das Band ist entsperrt oder gesperrt.<br/>                                                                                                             |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                 | BESCHREIBUNG                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Die Methode war erfolgreich.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Verwenden Sie [**unlockwithexternalkey**](unlockwithexternalkey-win32-encryptablevolume.md) und [**unlockwithnumericalpassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) , um Zugriff auf die volumeinhalte zu erhalten. Verwenden Sie die [**Lock**](lock-win32-encryptablevolume.md) -Methode, um den Zugriff auf den volumeinhalt zu

Das Volume mit dem aktuell ausgelaufenden Betriebssystem ist immer erreichbar und kann nicht gesperrt werden.

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

 

 
