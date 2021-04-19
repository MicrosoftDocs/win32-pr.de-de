---
description: Verwendet die Passphrase zum Abrufen des abgeleiteten Schlüssels.
ms.assetid: 62b070ec-4788-47cc-bfa4-6811a712ddbd
title: Protectkeywithpasspphrase-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithPassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f97806652d86b104a0f333d40d299cfa9502cf3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356724"
---
# <a name="protectkeywithpassphrase-method-of-the-win32_encryptablevolume-class"></a>Protectkeywithpasspphrase-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **protectkeywithpasspphrase** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " verwendet die Passphrase zum Abrufen des abgeleiteten Schlüssels. Nachdem der abgeleitete Schlüssel berechnet wurde, wird der abgeleitete Schlüssel verwendet, um den Hauptschlüssel des verschlüsselten Volumes zu sichern.

## <a name="syntax"></a>Syntax


```mof
uint32 ProtectKeyWithPassphrase(
  [in, optional] string FriendlyName,
  [in]           string Passphrase,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FriendlyName* \[ in, optional\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die einen vom Benutzer zugewiesenen Zeichen folgen Bezeichner für diese Schlüssel Schutzvorrichtung angibt. Wenn dieser Parameter nicht angegeben wird, wird ein leerer Wert verwendet.

</dd> <dt>

*Passphrase* \[ in\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die die Passphrase angibt.

</dd> <dt>

*Volumekeyprotectorid* \[ vorgenommen\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die die erstellte Schlüssel Schutzvorrichtung eindeutig identifiziert.

Wenn das Laufwerk die Hardware Verschlüsselung unterstützt und BitLocker keinen bandbesitz hat, wird die ID-Zeichenfolge auf "BitLocker" festgelegt, und die Schlüssel Schutzvorrichtung wird in die pro-Band-Metadaten geschrieben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                                        | BESCHREIBUNG                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                        | Die Methode war erfolgreich.<br/>                                                                                    |
| <dl> <dt>**F \_ E ist im abgesicherten \_ \_ \_ \_ \_ Modus**</dt> <dt>2150694976 (0x80310040)</dt> nicht zulässig. </dl>         | BitLocker-Laufwerkverschlüsselung können nur für Wiederherstellungs Zwecke verwendet werden, wenn Sie im abgesicherten Modus verwendet werden.<br/>                     |
| <dl> <dt>**F \_ E \_ - \_ richtlinienpasspphrase \_ nicht \_ zulässig**</dt> <dt>2150695018 (0x8031006a)</dt> </dl>     | Die Erstellung einer Passphrase wird von der Gruppenrichtlinie nicht zugelassen.<br/>                                                    |
| <dl> <dt>**F \_ E-fi-Kenn \_ \_ \_ Wörter verhindern Passphrase**</dt> <dt>2150695020 (0x8031006c)</dt> </dl>           | Die Gruppenrichtlinien Einstellung, die die Kompatibilität mit der Konformität erfordert, verhindert, dass die Passphrase generiert oder verwendet wird.<br/> |
| <dl> <dt>**F \_ E \_ Richtlinie \_ ungültige \_ Passphrasen \_ Länge**</dt> <dt>2150695040 (0x80310080)</dt> </dl>  | Die angegebene Passphrase entspricht nicht den Anforderungen an die minimale oder maximale Länge.<br/>                             |
| <dl> <dt>**F \_ E \_ - \_ richtlinienpass Phrase \_ zu \_ einfach**</dt> <dt>2150695041 (0x80310081)</dt> </dl>      | Die Passphrase erfüllt nicht die Komplexitäts Anforderungen, die vom Administrator in der Gruppenrichtlinie festgelegt werden.<br/>            |
| <dl> <dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl>                       | Das Volume ist bereits durch BitLocker-Laufwerkverschlüsselung gesperrt. Das Laufwerk muss in der Systemsteuerung entsperrt werden.<br/>     |
| <dl> <dt>**F \_ E \_ überlappendes \_ Update**</dt> <dt>2150694948 (0x80310024)</dt> </dl>                   | Der Kontroll Block für das verschlüsselte Volume wurde von einem anderen Thread aktualisiert.<br/>                                     |
| <dl> <dt>**F \_ E \_ Key \_ Protector \_ \_ wird nicht unterstützt**</dt> <dt>2150695017 (0x80310069)</dt> </dl>       | Die Schlüssel Schutzvorrichtung wird von der Version von BitLocker-Laufwerkverschlüsselung, die sich aktuell auf dem Volume befindet, nicht unterstützt.<br/>      |
| <dl> <dt>**F \_ E \_ OS- \_ Volumen \_ Passphrase \_ nicht \_ zulässig**</dt> <dt>2150695021 (0x8031006d)</dt> </dl> | Die Passphrase kann dem Betriebssystem Volume nicht hinzugefügt werden. <br/>                                               |
| <dl> <dt>**F \_ E \_ Protector \_ vorhanden**</dt> <dt>2150694960 (0x80310030)</dt> </dl>                    | Die angegebene Schlüssel Schutzvorrichtung ist auf diesem Volume bereits vorhanden.<br/>                                                     |



 

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

 

 




