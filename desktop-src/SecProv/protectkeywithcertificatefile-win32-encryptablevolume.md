---
description: 'ProtectKeyWithCertificateFile-Methode der Win32_EncryptableVolume-Klasse: Überprüft den OID (Enhanced Key Usage)-Objektbezeichner (Enhanced Key Usage, erweiterte Schlüsselverwendung) des bereitgestellten Zertifikats.'
ms.assetid: cc716524-f976-4d75-84f3-693e277030e6
title: ProtectKeyWithCertificateFile-Methode der Win32_EncryptableVolume Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithCertificateFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: d61a0bd0d31c14f13edd9ef610e8f6d3ed20f037
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110563"
---
# <a name="protectkeywithcertificatefile-method-of-the-win32_encryptablevolume-class"></a>ProtectKeyWithCertificateFile-Methode der Win32 \_ EncryptableVolume-Klasse

Die **ProtectKeyWithCertificateFile-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) überprüft den EKU-Objektbezeichner [*(Enhanced*](../secgloss/o-gly.md) Key Usage) des bereitgestellten Zertifikats.

## <a name="syntax"></a>Syntax


```mof
uint32 ProtectKeyWithCertificateFile(
  [in, optional] string FriendlyName,
  [in]           string FileName,
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

*FileName* \[ In\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die den Speicherort und den Namen der CER-Datei angibt, die zum Aktivieren von BitLocker verwendet wird. Ein Verschlüsselungszertifikat muss im CER-Format exportiert werden ([*Distinguished Encoding Rules*](../secgloss/d-gly.md) (DER)-codierte binäre [*X.509-*](../secgloss/x-gly.md) oder Base-64-codierte X.509). Das Verschlüsselungszertifikat kann von Microsoft PKI, PKI eines Drittanbieters oder selbstsigniertem Zertifikat generiert werden.

</dd> <dt>

*VolumeKeyProtectorID* \[ out\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die die erstellte Schlüsselschutzvorrichtung eindeutig identifiziert, die zum Verwalten dieser Schlüsselschutzvorrichtung verwendet werden kann.

Wenn das Laufwerk hardwareverschlüsselung unterstützt und BitLocker keinen Bandbesitz übernommen hat, wird die ID-Zeichenfolge auf "BitLocker" festgelegt, und die Schlüsselschutzvorrichtung wird in die Metadaten pro Band geschrieben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                           | Die Methode war erfolgreich.<br/>                                                                                                                                                                                                                                                          |
| <dl> <dt>**FVE \_ E \_ NON \_ BITLOCKER \_ OID**</dt> <dt>2150695022 (0x8031006E)</dt> </dl>                     | Das EKU-Attribut des angegebenen Zertifikats lässt nicht zu, dass es für BitLocker-Laufwerkverschlüsselung verwendet wird. BitLocker erfordert nicht, dass ein Zertifikat über ein EKU-Attribut verfügt, aber wenn eines konfiguriert ist, muss es auf eine OID festgelegt werden, die der für BitLocker konfigurierten OID entspricht.<br/> |
| <dl> <dt>**FVE \_ E \_ POLICY USER CERTIFICATE NOT ALLOWED \_ \_ \_ \_**</dt> <dt>2150695026 (E POLICY USER CERTIFICATE NOT ALLOWED 2150695026 (E POLICY USER CERTIFICATE NOT ALLOWED 2150695026 (0X80310072))</dt> </dl> | Gruppenrichtlinie lässt nicht zu, dass Benutzerzertifikate wie Smartcards mit BitLocker verwendet werden.<br/>                                                                                                                                                                                     |
| <dl> <dt>**FVE \_ E \_ POLICY \_ USER \_ CERT MUST BE \_ \_ \_ HW**</dt> <dt>2150695028 (0x80310074)</dt> </dl>        | Gruppenrichtlinie erfordert, dass Sie eine Smartcard für die Verwendung von BitLocker bereitstellen.<br/>                                                                                                                                                                                                                |
| <dl> <dt>**FVE \_ E \_ POLICY \_ PROHIBITS \_ SELFSIGNED**</dt> <dt>2150695046 (0x80310086)</dt> </dl>           | Gruppenrichtlinie lässt die Verwendung von selbstsignieren Zertifikaten nicht zu.<br/>                                                                                                                                                                                                                   |
| <dl> <dt>**FEHLER \_ DATEI \_ NICHT \_ GEFUNDEN**</dt> <dt>00000000002 (0x2)</dt> </dl>                                | Das System kann die angegebene Datei nicht finden.<br/>                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Bemerkungen

Wenn die OID nicht mit der OID übereinstimmt, die dem Dienstcontroller in der Registrierung zugeordnet ist, schlägt diese Methode fehl. Dadurch wird verhindert, dass der Benutzer Schutzvorrichtungen für den Datenwiederherstellungs-Agent (Data Recovery Agent, DRA) manuell auf dem Volume festlegt. DRAs müssen nur vom Dienst festgelegt werden.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 Enterprise- und Windows 7 \[ Ultimate-Desktop-Apps\]<br/>                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ R2-Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
