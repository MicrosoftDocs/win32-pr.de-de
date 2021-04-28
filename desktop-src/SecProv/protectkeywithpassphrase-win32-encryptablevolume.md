---
description: 'ProtectKeyWithPassphrase-Methode der Win32_EncryptableVolume Klasse: Verwendet die Passphrase, um den abgeleiteten Schlüssel zu erhalten.'
ms.assetid: 62b070ec-4788-47cc-bfa4-6811a712ddbd
title: ProtectKeyWithPassphrase-Methode der Win32_EncryptableVolume Klasse
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
ms.openlocfilehash: 2a7772b1b65890fedbdbb8dcced1ad851f3845b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098348"
---
# <a name="protectkeywithpassphrase-method-of-the-win32_encryptablevolume-class"></a>ProtectKeyWithPassphrase-Methode der Win32 \_ EncryptableVolume-Klasse

Die **ProtectKeyWithPassphrase-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) verwendet die Passphrase, um den abgeleiteten Schlüssel zu erhalten. Nachdem der abgeleitete Schlüssel berechnet wurde, wird der abgeleitete Schlüssel verwendet, um den Hauptschlüssel des verschlüsselten Volumes zu sichern.

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

Eine Zeichenfolge, die einen vom Benutzer zugewiesenen Zeichenfolgenbezeichner für diese Schlüsselschutzvorrichtung angibt. Wenn dieser Parameter nicht angegeben wird, wird ein leerer Wert verwendet.

</dd> <dt>

*Passphrase* \[ In\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die die Passphrase angibt.

</dd> <dt>

*VolumeKeyProtectorID* \[ out\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die die erstellte Schlüsselschutzvorrichtung eindeutig identifiziert.

Wenn das Laufwerk hardwareverschlüsselung unterstützt und BitLocker keinen Bandbesitz übernommen hat, wird die ID-Zeichenfolge auf "BitLocker" festgelegt, und die Schlüsselschutzvorrichtung wird in die Metadaten pro Band geschrieben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                                        | BESCHREIBUNG                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                        | Die Methode war erfolgreich.<br/>                                                                                    |
| <dl> <dt>**FVE \_ E \_ \_ NICHT ZULÄSSIG IM \_ \_ ABGESICHERTEN \_ MODUS**</dt> <dt>2150694976 (0x80310040)</dt> </dl>         | BitLocker-Laufwerkverschlüsselung können nur zu Wiederherstellungszwecken verwendet werden, wenn sie im abgesicherten Modus verwendet werden.<br/>                     |
| <dl> <dt>**FVE \_ E \_ POLICY \_ PASSPHRASE NOT \_ \_ ALLOWED**</dt> <dt>2150695018 (0x8031006A) (E POLICY PASSPHRASE NOT ALLOWED 2150695018 (E POLICY PASSPHRASE NOT ALLOWED 2150695018 (E</dt> POLICY PASSPHRASE NOT ALLOWED 21 </dl>     | Die Gruppenrichtlinie lässt die Erstellung einer Passphrase nicht zu.<br/>                                                    |
| <dl> <dt>**FVE \_ E \_ FIPS \_ VERHINDERT \_ PASSPHRASE**</dt> <dt>2150695020 (0x8031006C)</dt> </dl>           | Die Gruppenrichtlinieneinstellung, die FIPS-Konformität erfordert, hat verhindert, dass die Passphrase generiert oder verwendet wird.<br/> |
| <dl> <dt>**FVE \_ E \_ POLICY \_ INVALID \_ PASSPHRASE \_ LENGTH**</dt> <dt>2150695040 (0x80310080)</dt> </dl>  | Die angegebene Passphrase erfüllt nicht die Mindest- oder Höchstlängenanforderungen.<br/>                             |
| <dl> <dt>**FVE \_ E \_ POLICY \_ PASSPHRASE \_ TOO \_ SIMPLE**</dt> <dt>2150695041 (0x80310081)</dt> </dl>      | Die Passphrase erfüllt nicht die Komplexitätsanforderungen, die der Administrator in der Gruppenrichtlinie festgelegt hat.<br/>            |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl>                       | Das Volume ist bereits durch BitLocker-Laufwerkverschlüsselung gesperrt. Sie müssen das Laufwerk aus Systemsteuerung entsperren.<br/>     |
| <dl> <dt>**FVE \_ E \_ OVERLAPPED \_ UPDATE**</dt> <dt>2150694948 (0x80310024)</dt> </dl>                   | Der Kontrollblock für das verschlüsselte Volume wurde von einem anderen Thread aktualisiert.<br/>                                     |
| <dl> <dt>**FVE \_ E KEY PROTECTOR NOT SUPPORTED 2150695017 (0X80310069) \_ (E-SCHLÜSSELSCHUTZVORRICHTUNG \_ WIRD NICHT \_ \_ UNTERSTÜTZT**</dt> <dt>2150695017 (0x80310069)</dt> </dl>       | Die Schlüsselschutzvorrichtung wird von der Version von BitLocker-Laufwerkverschlüsselung, die sich derzeit auf dem Volume befindet, nicht unterstützt.<br/>      |
| <dl> <dt>**FVE \_ E \_ \_ BETRIEBSSYSTEMVOLUME \_ PASSPHRASE \_ NICHT \_ ZULÄSSIG**</dt> <dt>2150695021 (0x8031006D)</dt> </dl> | Die Passphrase kann dem Betriebssystemvolume nicht hinzugefügt werden. <br/>                                               |
| <dl> <dt>**FVE \_ E \_ PROTECTOR \_ EXISTS**</dt> <dt>2150694960 (0x80310030)</dt> </dl>                    | Die bereitgestellte Schlüsselschutzvorrichtung ist auf diesem Volume bereits vorhanden.<br/>                                                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 Enterprise- und Windows 7 \[ Ultimate-Desktop-Apps\]<br/>                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ R2-Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | \\CimV2-Stammsicherheit \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 




