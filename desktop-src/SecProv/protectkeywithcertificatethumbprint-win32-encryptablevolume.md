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
ms.openlocfilehash: 8c71684bf66d8d14df60c9ff09083f507b114024
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110578"
---
# <a name="protectkeywithcertificatethumbprint-method-of-the-win32_encryptablevolume-class"></a>ProtectKeyWithCertificateThumbprint-Methode der Win32 \_ EncryptableVolume-Klasse

Die **ProtectKeyWithCertificateThumbprint-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) überprüft den EKU-Objektbezeichner (Enhanced Key Usage, erweiterte Schlüsselverwendung) des bereitgestellten Zertifikats. [](../secgloss/o-gly.md)

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

Eine Zeichenfolge, die einen vom Benutzer zugewiesenen Zeichenfolgenbezeichner für diese Schlüsselschutzvorrichtung angibt. Wenn dieser Parameter nicht angegeben ist, wird der *FriendlyName-Parameter* mithilfe des Antragstellernamens im Zertifikat erstellt.

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

Wenn das Laufwerk Hardwareverschlüsselung unterstützt und BitLocker keinen Bandbesitz übernommen hat, wird die ID-Zeichenfolge auf "BitLocker" festgelegt, und die Schlüsselschutzvorrichtung wird pro Bandmetadaten in geschrieben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn er fehlschlägt.



| Rückgabecode/-wert                                                                                                                                                                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                           | Die Methode war erfolgreich.<br/>                                                                                                                                                                                                                                                          |
| <dl> <dt>**FEHLER \_ INVALID \_ DATA**</dt> <dt>13 (0xD)</dt> </dl>                                           | Die Daten sind ungültig.<br/>                                                                                                                                                                                                                                                              |
| <dl> <dt>**FVE \_ E \_ NON \_ BITLOCKER \_ OID**</dt> <dt>2150695022 (0x8031006E)</dt> </dl>                     | Das EKU-Attribut des angegebenen Zertifikats lässt nicht zu, dass es für die BitLocker-Laufwerkverschlüsselung. BitLocker erfordert nicht, dass ein Zertifikat über ein EKU-Attribut verfügt, aber wenn eines konfiguriert ist, muss es auf eine OID festgelegt werden, die der für BitLocker konfigurierten OID entspricht.<br/> |
| <dl> <dt>**FVE \_ E \_ POLICY USER CERTIFICATE NOT ALLOWED \_ \_ \_ \_**</dt> <dt>2150695026 (0x80310072) (E POLICY USER CERTIFICATE NOT ALLOWED 2150695026 (0x80310072)</dt> </dl> | Gruppenrichtlinie lässt nicht zu, dass Benutzerzertifikate, z. B. Smartcards, mit BitLocker verwendet werden können.<br/>                                                                                                                                                                                     |
| <dl> <dt>**FVE \_ E \_ POLICY \_ USER \_ CERT MUSS \_ \_ \_ HW**</dt> <dt>2150695028 (0x80310074) SEIN.</dt> </dl>        | Gruppenrichtlinie müssen Sie eine Smartcard für die Verwendung von BitLocker verwenden.<br/>                                                                                                                                                                                                                |
| <dl> <dt>**FVE \_ E \_ POLICY VERHINDERT DIE \_ \_ SELBSTSIGNIERTE**</dt> <dt>2150695046 (0x80310086)</dt> </dl>           | Gruppenrichtlinie nicht die Verwendung selbstsignierter Zertifikate.<br/>                                                                                                                                                                                                                   |



 

## <a name="remarks"></a>Bemerkungen

Wenn die OID nicht mit der OID übereinstimmen, die dem Dienstcontroller in der Registrierung zugeordnet ist, schlägt diese Methode fehl. Dadurch wird verhindert, dass der Benutzer Schutzvorrichtungen des Datenwiederherstellungs-Agents (DRA) manuell auf dem Volume festlegen kann. DRAs müssen nur vom Dienst festgelegt werden.

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

 

 
