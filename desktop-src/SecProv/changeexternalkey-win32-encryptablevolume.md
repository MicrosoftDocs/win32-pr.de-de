---
description: Ändert einen externen Schlüssel, der einem verschlüsselten Volume zugeordnet ist.
ms.assetid: 14c7e643-f685-40bb-be86-aabc5b883d7e
title: Changeexternalkey-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangeExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 7441666ded1acc2234df84fc98ce6d02a117167d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362861"
---
# <a name="changeexternalkey-method-of-the-win32_encryptablevolume-class"></a>Changeexternalkey-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **changeexternalkey** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " ändert einen externen Schlüssel, der einem verschlüsselten Volume zugeordnet ist.

## <a name="syntax"></a>Syntax


```mof
uint32 ChangeExternalKey(
  [in]           string VolumeKeyProtectorID,
  [in, optional] uint8   NewExternalKey[],
  [out]          string NewVolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Volumekeyprotectorid* \[ in\]
</dt> <dd>

Typ: **Zeichenfolge**

Ein eindeutiger Zeichen folgen Bezeichner zum Verwalten einer verschlüsselten volumeschlüsselschutzvorrichtung.

</dd> <dt>

 " *Netwexternalkey* \[ " in, optional\]
</dt> <dd>

Typ: **Uint8 \[ \]**

Ein Bytearray, das den externen 256-Bit-Schlüssel angibt, mit dem das Volume entsperrt wird.

</dd> <dt>

*Newvolumekeyprotectorid* \[ vorgenommen\]
</dt> <dd>

Typ: **Zeichenfolge**

Ein aktualisierter eindeutiger Zeichen folgen Bezeichner, der zum Verwalten einer verschlüsselten volumeschlüsselschutzvorrichtung verwendet wird

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                            | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                            | Die Methode war erfolgreich.<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                    | Der Parameter " *netwexternalkey* " ist kein Array der Größe 32.<br/>                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl>           | Das Volume ist gesperrt.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu. <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**F \_ E \_ Bootable \_ CDDVD**</dt> <dt>2150694960 (0x80310030)</dt> </dl>          | Auf diesem Computer wurde eine Start fähige CD/DVD gefunden. Entfernen Sie die CD/DVD, und starten Sie den Computer neu.<br/>                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**F \_ E \_ Protector \_ nicht \_ gefunden**</dt> <dt>2150694963 (0x80310033)</dt> </dl>    | Die angegebene Schlüssel Schutzvorrichtung ist auf dem Volume nicht vorhanden.<br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**F \_ E \_ ungültiger \_ \_ schutzschutztyp**</dt> <dt>2150694970 (0x8031003a)</dt> </dl> | Der *volumekeyprotectorid-* Parameter verweist nicht auf eine Schlüssel Schutzvorrichtung des Typs "numerisches Kennwort" oder "externer Schlüssel". Verwenden Sie entweder die [**protectkeywithnumericalpassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) -Methode oder die [**protectkeywithexternalkey**](protectkeywithexternalkey-win32-encryptablevolume.md) -Methode, um eine Schlüssel Schutzvorrichtung des entsprechenden Typs zu erstellen.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode kann verwendet werden, um den externen Schlüssel für jede Schlüssel Schutzvorrichtung zu ändern, die einen externen Schlüssel verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop-Apps\]<br/>                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ verschlüsseltablevolume. MOF</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ verschlüsseltablevolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 




