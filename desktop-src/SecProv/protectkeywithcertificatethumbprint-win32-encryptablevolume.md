---
description: 'ProtectKeyWithCertificateThumbprint-Methode der Win32_EncryptableVolume-Klasse: Überprüft den EKU-Objektbezeichner (Enhanced Key Usage, erweiterte Schlüsselverwendung) des bereitgestellten Zertifikats.'
ms.assetid: 7096cead-c44a-404c-b1e1-3e0ab27070f8
title: ProtectKeyWithCertificateThumbprint-Methode der Win32_EncryptableVolume-Klasse
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
ms.openlocfilehash: 900138c611198114397caa94894a3802475e2bebe5138629c0f2b9bd2c58c220
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891526"
---
# <a name="protectkeywithcertificatethumbprint-method-of-the-win32_encryptablevolume-class"></a>ProtectKeyWithCertificateThumbprint-Methode der Win32 \_ EncryptableVolume-Klasse

Die **ProtectKeyWithCertificateThumbprint-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) überprüft den EKU-Objektbezeichner [*(Enhanced*](../secgloss/o-gly.md) Key Usage) des bereitgestellten Zertifikats.

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

Eine Zeichenfolge, die einen vom Benutzer zugewiesenen Zeichenfolgenbezeichner für diese Schlüsselschutzvorrichtung angibt. Wenn dieser Parameter nicht angegeben wird, wird *der FriendlyName-Parameter* mithilfe des Betreffnamens im Zertifikat erstellt.

</dd> <dt>

*CertThumbprint* \[ In\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die den Zertifikatfingerabdruck angibt.

</dd> <dt>

*VolumeKeyProtectorID* \[ out\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die die erstellte Schlüsselschutzvorrichtung eindeutig identifiziert, die zum Verwalten dieser Schlüsselschutzvorrichtung verwendet werden kann.

Wenn das Laufwerk Hardwareverschlüsselung unterstützt und BitLocker keinen Bandbesitz übernommen hat, wird die ID-Zeichenfolge auf "BitLocker" festgelegt, und die Schlüsselschutzvorrichtung wird in die Metadaten pro Band geschrieben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                           | Die Methode war erfolgreich.<br/>                                                                                                                                                                                                                                                          |
| <dl> <dt>**FEHLER \_ UNGÜLTIGE \_ DATEN**</dt> <dt>13 (0xD)</dt> </dl>                                           | Die Daten sind ungültig.<br/>                                                                                                                                                                                                                                                              |
| <dl> <dt>**FVE \_ E \_ NON \_ BITLOCKER \_ OID**</dt> <dt>2150695022 (0x8031006E)</dt> </dl>                     | Das EKU-Attribut des angegebenen Zertifikats lässt nicht zu, dass es für die BitLocker-Laufwerkverschlüsselung. BitLocker erfordert nicht, dass ein Zertifikat über ein EKU-Attribut verfügt. Wenn eines konfiguriert ist, muss es jedoch auf eine OID festgelegt werden, die der für BitLocker konfigurierten OID entspricht.<br/> |
| <dl> <dt>**FVE \_ E \_ POLICY USER CERTIFICATE NOT ALLOWED \_ \_ \_ \_ 2150695026**</dt> <dt>(0x80310072)</dt> </dl> | Gruppenrichtlinie lässt nicht zu, dass Benutzerzertifikate, z. B. Smartcards, mit BitLocker verwendet werden können.<br/>                                                                                                                                                                                     |
| <dl> <dt>**FVE \_ E \_ POLICY \_ USER \_ CERT MUST BE \_ \_ \_ HW**</dt> <dt>2150695028 (0x80310074)</dt> </dl>        | Gruppenrichtlinie müssen Sie eine Smartcard für die Verwendung von BitLocker verwenden.<br/>                                                                                                                                                                                                                |
| <dl> <dt>**FVE \_ E \_ POLICY \_ PROHIBITS \_ SELFSIGNED**</dt> <dt>2150695046 (0x80310086)</dt> </dl>           | Gruppenrichtlinie nicht die Verwendung selbstsignierter Zertifikate.<br/>                                                                                                                                                                                                                   |



 

## <a name="remarks"></a>Hinweise

Wenn die OID nicht mit der OID übereinstimmen, die dem Dienstcontroller in der Registrierung zugeordnet ist, schlägt diese Methode fehl. Dadurch wird verhindert, dass der Benutzer Schutzvorrichtungen des Datenwiederherstellungs-Agents (DRA) manuell auf dem Volume festlegen kann. DRAs müssen nur vom Dienst festgelegt werden.

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

 

 
