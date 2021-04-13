---
description: Löscht eine angegebene Schlüssel Schutzvorrichtung für das Volume.
ms.assetid: fa6b89b0-83b6-4be2-8b7b-61b0501747d2
title: Deletekeyprotector-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DeleteKeyProtector
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: b1f539683bb76559d08066d01de6aeca0394ced3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343078"
---
# <a name="deletekeyprotector-method-of-the-win32_encryptablevolume-class"></a>Deletekeyprotector-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **deletekeyprotector** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " löscht eine bestimmte Schlüssel Schutzvorrichtung für das Volume.

Wenn ein unverschlüsseltes Volume über Schlüssel Schutzvorrichtungen verfügt und die letzte Schlüssel Schutzvorrichtung von **deletekeyprotector** entfernt wird, wird das Volume auf ein Standardmäßiges NTFS-Dateisystem zurückgesetzt.

Wenn ein Volume nie verschlüsselt wurde, wird das Löschen der Schlüssel Schutzvorrichtung auf NTFS zurückgesetzt.

Wenn das Volume noch nicht vollständig entschlüsselt ist, verwenden Sie [**disablekeyprotector**](disablekeyprotectors-win32-encryptablevolume.md) , bevor Sie die letzte Schlüssel Schutzvorrichtung des Volumes entfernen, um sicherzustellen, dass die verschlüsselten Teile des Volumes zugänglich bleiben.

## <a name="syntax"></a>Syntax


```mof
uint32 DeleteKeyProtector(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Volumekeyprotectorid* \[ in\]
</dt> <dd>

Typ: **Zeichenfolge**

Ein eindeutiger Zeichen folgen Bezeichner zum Verwalten einer verschlüsselten volumeschlüsselschutzvorrichtung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                          | Die Methode war erfolgreich.<br/>                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl>         | Das Volume ist gesperrt.<br/>                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt> </dl>         | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu. <br/>                                                                                                                                                                                                                              |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                  | Der *volumekeyprotectorid-* Parameter verweist nicht auf eine gültige Schlüssel Schutzvorrichtung.<br/>                                                                                                                                                                                                                                  |
| <dl> <dt>**F \_ E- \_ Taste \_ erforderlich**</dt> <dt>2150694941 (0x8031001d)</dt> </dl>          | Die letzte Schlüssel Schutzvorrichtung für ein teilweise oder vollständig verschlüsseltes Volume kann nicht entfernt werden, wenn Schlüssel Schutzvorrichtungen aktiviert sind. Verwenden Sie [**disablekeyprotector**](disablekeyprotectors-win32-encryptablevolume.md) , bevor Sie diese letzte Schlüssel Schutzvorrichtung entfernen, um sicherzustellen, dass die verschlüsselten Teile des Volumes zugänglich bleiben. <br/> |
| <dl> <dt>**F \_ E \_ Volume \_ \_ bereits**</dt> <dt>2150694943 (0x8031001f)</dt> </dl> | Diese Schlüssel Schutzvorrichtung kann nicht gelöscht werden, da Sie zum automatischen Entsperren des Volumes verwendet wird. <br/> Verwenden Sie [**disableautounlock**](disableautounlock-win32-encryptablevolume.md) , um das automatische Entsperren zu deaktivieren, bevor Sie diese Schlüssel Schutzvorrichtung löschen.<br/>                                                    |



 

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

 

 
