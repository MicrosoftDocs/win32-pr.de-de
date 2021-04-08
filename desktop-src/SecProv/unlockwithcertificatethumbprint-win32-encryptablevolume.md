---
description: Verwendet den angegebenen Zertifikat Fingerabdruck, um den abgeleiteten Schlüssel abzurufen und das verschlüsselte Volume zu entsperren.
ms.assetid: 41c25d17-db1b-427e-907b-a547483927e0
title: Unlockwithcertifitorethumschlag Print-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithCertificateThumbprint
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 5955334b6c147feea43d5e0a2c83a8e00050d900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750825"
---
# <a name="unlockwithcertificatethumbprint-method-of-the-win32_encryptablevolume-class"></a>Unlockwithcertifierethumschlag Print-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **unlockwithcertifi-** Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " verwendet den angegebenen Fingerabdruck des [*Zertifikats*](../secgloss/c-gly.md) , um den abgeleiteten Schlüssel abzurufen und das verschlüsselte Volume zu entsperren.

> [!Note]  
> Wenn die Festplatte Hardware Verschlüsselung unterstützt, legt diese Funktion den Bandstatus auf "entsperrt" fest.

 

## <a name="syntax"></a>Syntax


```mof
uint32 UnlockWithCertificateThumbprint(
  [in] string CertThumbprint,
  [in] string PIN
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Certthumbprint* \[ in\]
</dt> <dd>

Typ: **Zeichenfolge**

Der Fingerabdruck Wert 0 wird akzeptiert und führt zu einer Suche nach dem lokalen Speicher für das entsprechende Zertifikat. Wenn ein einzelnes BitLocker-Zertifikat gefunden wird, ist die Suche erfolgreich. Wenn keines oder mehrere Zertifikate gefunden werden, schlägt die Methode fehl.

</dd> <dt>

*Pin* \[ in\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine vom Benutzer angegebene persönliche Identifikations Zeichenfolge. Diese Zeichenfolge muss aus einer Sequenz von 4 bis 20 Ziffern bestehen. Diese Zeichenfolge wird verwendet, um den [*Schlüsselspeicher Anbieter*](../secgloss/k-gly.md) (KSP) im Hintergrund zu authentifizieren, wenn Sie mit einer [*Smartcard*](../secgloss/s-gly.md)verwendet werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                            | BESCHREIBUNG                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                            | Die Methode war erfolgreich.<br/>                                                                                                                                                                                                                                    |
| <dl> <dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu. <br/>                                                                                                                                                                             |
| <dl> <dt>**F \_ E \_ \_**</dt> -Fehler bei Authentifizierung <dt>2150694951 (0x80310027)</dt> </dl>   | Das Volume kann nicht mit den bereitgestellten Informationen entsperrt werden. <br/>                                                                                                                                                                                             |
| <dl> <dt>**F \_ E \_ Protector \_ nicht \_ gefunden**</dt> <dt>2150694963 (0x80310033)</dt> </dl>    | Die angegebene Schlüssel Schutzvorrichtung ist auf dem Volume nicht vorhanden. Sie müssen eine andere Schlüssel Schutzvorrichtung eingeben.<br/>                                                                                                                                                                |
| <dl> <dt>**F \_ E \_ PrivateKey-Authentifizierung ist \_ \_ fehlgeschlagen**</dt> <dt>2150695060 (0x80310094)</dt> </dl> | Der dem angegebenen Zertifikat zugeordnete [*private Schlüssel*](../secgloss/p-gly.md) konnte nicht autorisiert werden. Die Autorisierung für den privaten Schlüssel wurde entweder nicht bereitgestellt, oder die angegebene Autorisierung war nicht gültig.<br/> |



 

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

 

 
