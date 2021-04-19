---
description: Überprüft die EKU-Objekt Kennung (Enhanced Key Usage, EKU) des angegebenen Zertifikats.
ms.assetid: 7096cead-c44a-404c-b1e1-3e0ab27070f8
title: Protectkeywithcertifitorethenumbprint-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithCertificateThumbprint
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e0b47aabccaacfb3ab81968b8a93037aad304f8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373188"
---
# <a name="protectkeywithcertificatethumbprint-method-of-the-win32_encryptablevolume-class"></a>Protectkeywithcertifitorethenumbprint-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **protectkeywithcertifigateethumbprint** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " überprüft die EKU- [*Objekt Kennung*](../secgloss/o-gly.md) (Enhanced Key Usage, EKU) des bereitgestellten Zertifikats.

## <a name="syntax"></a>Syntax


```mof
uint32 ProtectKeyWithCertificateThumbprint(
  [in, optional] string FriendlyName,
  [in]           string CertThumbprint,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FriendlyName* \[ in, optional\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die einen vom Benutzer zugewiesenen Zeichen folgen Bezeichner für diese Schlüssel Schutzvorrichtung angibt. Wenn dieser Parameter nicht angegeben wird, wird der *FriendlyName* -Parameter mit dem Antragsteller Namen im Zertifikat erstellt.

</dd> <dt>

*Certthumbprint* \[ in\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die den Zertifikat Fingerabdruck angibt.

</dd> <dt>

*Volumekeyprotectorid* \[ vorgenommen\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die die erstellte Schlüssel Schutzvorrichtung eindeutig identifiziert, die zum Verwalten dieser Schlüssel Schutzvorrichtung verwendet werden kann.

Wenn das Laufwerk die Hardware Verschlüsselung unterstützt und BitLocker keinen bandbesitz hat, wird die ID-Zeichenfolge auf "BitLocker" festgelegt, und die Schlüssel Schutzvorrichtung wird in die pro-Band-Metadaten geschrieben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                           | Die Methode war erfolgreich.<br/>                                                                                                                                                                                                                                                          |
| <dl> <dt>**Fehler \_ Ungültige \_ Daten**</dt> <dt>13 (0xD)</dt> </dl>                                           | Die Daten sind ungültig.<br/>                                                                                                                                                                                                                                                              |
| <dl> <dt>**F \_ E \_ nicht- \_ BitLocker- \_ OID**</dt> <dt>2150695022 (0x8031006e)</dt> </dl>                     | Das EKU-Attribut des angegebenen Zertifikats gestattet es nicht, für BitLocker-Laufwerkverschlüsselung zu verwenden. BitLocker erfordert nicht, dass ein Zertifikat ein EKU-Attribut aufweist. Wenn jedoch ein Zertifikat konfiguriert ist, muss es auf eine OID festgelegt werden, die mit der für BitLocker konfigurierten OID übereinstimmt.<br/> |
| <dl> <dt>**F \_ E \_ - \_ richtlinienbenutzerzertifikat \_ \_ nicht \_ zulässig**</dt> <dt>2150695026 (0x80310072)</dt> </dl> | In Gruppenrichtlinie können Benutzerzertifikate, z. b. Smartcards, nicht mit BitLocker verwendet werden.<br/>                                                                                                                                                                                     |
| <dl> <dt>**F \_ E \_ Policy \_ User \_ CERT \_ muss \_ \_ HW**</dt> <dt>2150695028 (0x80310074)</dt> sein. </dl>        | Gruppenrichtlinie müssen Sie für die Verwendung von BitLocker eine Smartcard angeben.<br/>                                                                                                                                                                                                                |
| <dl> <dt>**F \_ E- \_ Richtlinie \_ untersagt \_ selfsigned**</dt> <dt>2150695046 (0x80310086)</dt> </dl>           | Die Verwendung von selbst signierten Zertifikaten wird in Gruppenrichtlinie nicht zugelassen.<br/>                                                                                                                                                                                                                   |



 

## <a name="remarks"></a>Bemerkungen

Wenn die OID nicht mit der ID identisch ist, die dem Dienst Controller in der Registrierung zugeordnet ist, tritt bei dieser Methode ein Fehler auf. Dadurch wird verhindert, dass der Benutzer die Data Recovery Agent-Schutzvorrichtungen (DRA) manuell auf dem Volume festlegt. DRAs werden nur vom Dienst festgelegt.

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

 

 
