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
ms.openlocfilehash: c0d87eb21ea505b13ce3aacfe8be6ff1fa9d266ba2a781d6b8e6fc4d77dac10b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004358"
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

Wenn das Laufwerk Hardwareverschlüsselung unterstützt und BitLocker keinen Bandbesitz übernommen hat, wird die ID-Zeichenfolge auf "BitLocker" festgelegt, und die Schlüsselschutzvorrichtung wird in die Metadaten pro Band geschrieben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                                        | Beschreibung                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                        | Die Methode war erfolgreich.<br/>                                                                                    |
| <dl> <dt>**FVE \_ E \_ IM \_ \_ ABGESICHERTEN MODUS NICHT \_ \_ 2150694976**</dt> <dt>(0x80310040)</dt> </dl>         | BitLocker-Laufwerkverschlüsselung kann nur zu Wiederherstellungszwecken verwendet werden, wenn sie im Tresor werden.<br/>                     |
| <dl> <dt>**FVE \_ E \_ POLICY \_ PASSPHRASE \_ NOT ALLOWED \_ 2150695018**</dt> <dt>(0x8031006A)</dt> </dl>     | Die Gruppenrichtlinie lässt die Erstellung einer Passphrase nicht zu.<br/>                                                    |
| <dl> <dt>**FVE \_ E \_ FIPS \_ VERHINDERT \_ PASSPHRASE-2150695020**</dt> <dt>(0x8031006C)</dt> </dl>           | Die Gruppenrichtlinieneinstellung, die FIPS-Konformität erfordert, hat verhindert, dass die Passphrase generiert oder verwendet wird.<br/> |
| <dl> <dt>**FVE \_ E \_ POLICY \_ INVALID \_ PASSPHRASE \_ LENGTH**</dt> <dt>2150695040 (0x80310080)</dt> </dl>  | Die bereitgestellte Passphrase erfüllt nicht die Mindest- oder Höchstlängenanforderungen.<br/>                             |
| <dl> <dt>**FVE \_ E \_ POLICY \_ PASSPHRASE \_ TOO \_ SIMPLE**</dt> <dt>2150695041 (0x80310081)</dt> </dl>      | Die Passphrase erfüllt nicht die Komplexitätsanforderungen, die der Administrator in der Gruppenrichtlinie festgelegt hat.<br/>            |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl>                       | Das Volume ist bereits durch die BitLocker-Laufwerkverschlüsselung. Sie müssen das Laufwerk von der Systemsteuerung.<br/>     |
| <dl> <dt>**FVE \_ E \_ OVERLAPED \_ UPDATE**</dt> <dt>2150694948 (0x80310024)</dt> </dl>                   | Der Steuerungsblock für das verschlüsselte Volume wurde von einem anderen Thread aktualisiert.<br/>                                     |
| <dl> <dt>**FVE \_ E \_ KEY PROTECTOR NOT \_ \_ \_ SUPPORTED**</dt> <dt>2150695017 (0x80310069)</dt> </dl>       | Die Schlüsselschutzvorrichtung wird von der Version von BitLocker-Laufwerkverschlüsselung derzeit auf dem Volume nicht unterstützt.<br/>      |
| <dl> <dt>**FVE \_ E \_ OS \_ VOLUME \_ PASSPHRASE \_ NOT ALLOWED \_ 2150695021**</dt> <dt>(0x8031006D)</dt> </dl> | Die Passphrase kann dem Betriebssystem-Volume nicht hinzugefügt werden. <br/>                                               |
| <dl> <dt>**FVE \_ E \_ PROTECTOR \_ EXISTS**</dt> <dt>2150694960 (0x80310030)</dt> </dl>                    | Die bereitgestellte Schlüsselschutzvorrichtung ist auf diesem Volume bereits vorhanden.<br/>                                                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Enterprise, Windows 7 \[ Ultimate-Desktop-Apps\]<br/>                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | \\CimV2-Stammsicherheit \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 




