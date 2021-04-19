---
description: Verwendet die neue Passphrase zum Abrufen eines neuen abgeleiteten Schlüssels.
ms.assetid: 89398bae-a2a2-466c-8a1e-a702018d679f
title: Changepasspphrase-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangePassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f28a78c6cb923b4f8934ec5cc8962b91b7f5139f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351423"
---
# <a name="changepassphrase-method-of-the-win32_encryptablevolume-class"></a>Changepasspphrase-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **changepasspphrase** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " verwendet die neue Passphrase zum Abrufen eines neuen abgeleiteten Schlüssels. Nachdem der abgeleitete Schlüssel berechnet wurde, wird der neue abgeleitete Schlüssel verwendet, um den Hauptschlüssel des verschlüsselten Volumes zu sichern.

## <a name="syntax"></a>Syntax


```mof
uint32 ChangePassphrase(
  [in]  string VolumeKeyProtectorID,
  [in]  string NewPassphrase,
  [out] string NewProtectorID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Volumekeyprotectorid* \[ in\]
</dt> <dd>

Typ: **Zeichenfolge**

Ein eindeutiger Zeichen folgen Bezeichner, der zum Verwalten einer verschlüsselten volumeschlüsselschutzvorrichtung verwendet wird.

</dd> <dt>

*Newpasspphrase* \[ in\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine aktualisierte Zeichenfolge, die die Passphrase angibt.

</dd> <dt>

*Newprotectorid* \[ vorgenommen\]
</dt> <dd>

Typ: **Zeichenfolge**

Ein aktualisierter eindeutiger Zeichen folgen Bezeichner zum Verwalten einer verschlüsselten volumeschlüsselschutzvorrichtung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                                       | BESCHREIBUNG                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                       | Die Methode war erfolgreich.<br/>                                                                                  |
| <dl> <dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl>                      | Das Volume ist bereits durch BitLocker-Laufwerkverschlüsselung gesperrt. Das Laufwerk muss in der Systemsteuerung entsperrt werden.<br/>   |
| <dl> <dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt> </dl>                      | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu. <br/>                           |
| <dl> <dt>**F \_ E \_ überlappendes \_ Update**</dt> <dt>2150694948 (0x80310024)</dt> </dl>                  | Der Kontroll Block für das verschlüsselte Volume wurde von einem anderen Thread aktualisiert.<br/>                                   |
| <dl> <dt>**F \_ E \_ ungültiger \_ \_ schutzschutztyp**</dt> <dt>2150694970 (0x8031003a)</dt> </dl>            | Die angegebene Schlüssel Schutzvorrichtung weist nicht den richtigen Typ auf. <br/>                                                    |
| <dl> <dt>**F \_ E \_ Richtlinie \_ ungültige \_ Passphrasen \_ Länge**</dt> <dt>2150695040 (0x80310080)</dt> </dl> | Die aktualisierte Passphrase entspricht nicht den Mindestanforderungen oder der maximalen Länge. <br/>                  |
| <dl> <dt>**F \_ E \_ - \_ richtlinienpass Phrase \_ zu \_ einfach**</dt> <dt>2150695041 (0x80310081)</dt> </dl>     | Die aktualisierte Passphrase erfüllt nicht die Komplexitäts Anforderungen, die vom Administrator in der Gruppenrichtlinie festgelegt wurden. <br/> |



 

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

 

 




