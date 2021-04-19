---
description: Löscht alle Schlüssel Schutzvorrichtungen für das Volume.
ms.assetid: 46f61899-87ff-4e86-8409-635117cff4de
title: Deletekeyprotector-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DeleteKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0195a89884dcd9f9288cab020d9804dcc81b7977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368773"
---
# <a name="deletekeyprotectors-method-of-the-win32_encryptablevolume-class"></a>Deletekeyprotector-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **deletekeyprotector** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " löscht alle Schlüssel Schutzvorrichtungen für das Volume.

Wenn ein unverschlüsseltes Volume über Schlüssel Schutzvorrichtungen verfügt, wird das Volume in einem standardmäßigen NTFS-Dateisystem wieder hergestellt, wenn **deletekeyprotector** erfolgreich ausgeführt wird.

Wenn das Volume noch nicht vollständig entschlüsselt ist, verwenden Sie [**disablekeyprotector**](disablekeyprotectors-win32-encryptablevolume.md) vor dem Ausführen von **deletekeyprotector** , um sicherzustellen, dass die verschlüsselten Teile des Volumes zugänglich bleiben.

## <a name="syntax"></a>Syntax


```mof
uint32 DeleteKeyProtectors();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                          | Die Methode war erfolgreich.<br/>                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl>         | Das Volume ist gesperrt.<br/>                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**F \_ E- \_ Taste \_ erforderlich**</dt> <dt>2150694941 (0x8031001d)</dt> </dl>          | Die letzte Schlüssel Schutzvorrichtung für ein teilweise oder vollständig verschlüsseltes Volume kann nicht entfernt werden, wenn Schlüssel Schutzvorrichtungen aktiviert sind. Verwenden Sie [**disablekeyprotector**](disablekeyprotectors-win32-encryptablevolume.md) , bevor Sie diese letzte Schlüssel Schutzvorrichtung entfernen, um sicherzustellen, dass die verschlüsselten Teile des Volumes zugänglich bleiben. <br/> |
| <dl> <dt>**F \_ E \_ Volume \_ \_ bereits**</dt> <dt>2150694943 (0x8031001f)</dt> </dl> | Schlüssel Schutzvorrichtungen können nicht gelöscht werden, da eine von Ihnen zum automatischen Entsperren des Volumes verwendet wird. <br/> Verwenden Sie [**disableautounlock**](disableautounlock-win32-encryptablevolume.md) , um das automatische Entsperren zu deaktivieren, bevor Sie diese Methode ausführen.<br/>                                                       |



 

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

 

 
