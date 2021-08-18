---
description: Löscht alle Schlüsselschutzvorrichtungen für das Volume.
ms.assetid: 46f61899-87ff-4e86-8409-635117cff4de
title: DeleteKeyProtectors-Methode der Win32_EncryptableVolume-Klasse
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
ms.openlocfilehash: 49884566a45bde4977d56baa3e83ae4c42fdd676447a3da1f3df528ec823c414
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004608"
---
# <a name="deletekeyprotectors-method-of-the-win32_encryptablevolume-class"></a>DeleteKeyProtectors-Methode der Win32 \_ EncryptableVolume-Klasse

Die **DeleteKeyProtectors-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) löscht alle Schlüsselschutzvorrichtungen für das Volume.

Wenn ein unverschlüsseltes Volume über Schlüsselschutzvorrichtungen verfügt, wird das Volume bei erfolgreicher Ausführung von **DeleteKeyProtectors** auf ein NTFS-Standarddateisystem zurückgesetzt.

Wenn das Volume noch nicht vollständig entschlüsselt ist, verwenden [**Sie DisableKeyProtectors,**](disablekeyprotectors-win32-encryptablevolume.md) bevor **Sie DeleteKeyProtectors** ausführen, um sicherzustellen, dass verschlüsselte Teile des Volumes weiterhin zugänglich sind.

## <a name="syntax"></a>Syntax


```mof
uint32 DeleteKeyProtectors();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn er fehlschlägt.



| Rückgabecode/-wert                                                                                                                                                                          | Beschreibung                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                          | Die Methode war erfolgreich.<br/>                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl>         | Das Volume ist gesperrt.<br/>                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**FVE \_ E \_ KEY \_ REQUIRED**</dt> <dt>2150694941 (0x8031001D)</dt> </dl>          | Die letzte Schlüsselschutzvorrichtung für ein teilweise oder vollständig verschlüsseltes Volume kann nicht entfernt werden, wenn Schlüsselschutzvorrichtungen aktiviert sind. Verwenden Sie [**DisableKeyProtectors,**](disablekeyprotectors-win32-encryptablevolume.md) bevor Sie diese letzte Schlüsselschutzvorrichtung entfernen, um sicherzustellen, dass verschlüsselte Teile des Volumes weiterhin zugänglich sind. <br/> |
| <dl> <dt>**FVE \_ E \_ VOLUME \_ BOUND \_ ALREADY**</dt> <dt>2150694943 (0x8031001F)</dt> </dl> | Schlüsselschutzvorrichtungen können nicht gelöscht werden, da eine davon verwendet wird, um das Volume automatisch zu entsperren. <br/> Verwenden Sie [**DisableAutoUnlock,**](disableautounlock-win32-encryptablevolume.md) um die automatische Entsperrung zu deaktivieren, bevor Sie diese Methode ausführen.<br/>                                                       |



 

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Enterprise, nur Windows Vista \[ Ultimate-Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\CIMV2-Stammsicherheit \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
