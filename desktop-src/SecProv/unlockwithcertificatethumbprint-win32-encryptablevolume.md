---
description: Verwendet den bereitgestellten Zertifikatfingerabdruck, um den abgeleiteten Schlüssel abzurufen und das verschlüsselte Volume zu entsperren.
ms.assetid: 41c25d17-db1b-427e-907b-a547483927e0
title: UnlockWithCertificateThumbprint-Methode der Win32_EncryptableVolume-Klasse
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
ms.openlocfilehash: 0ccf4a68f999bee1d32d8025759eb9625371b18fc5028b54e68e62df544bbd7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891365"
---
# <a name="unlockwithcertificatethumbprint-method-of-the-win32_encryptablevolume-class"></a>UnlockWithCertificateThumbprint-Methode der Win32 \_ EncryptableVolume-Klasse

Die **UnlockWithCertificateThumbprint-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) verwendet den bereitgestellten Zertifikatfingerabdruck, um den abgeleiteten Schlüssel abzurufen und das verschlüsselte Volume zu entsperren. [](../secgloss/c-gly.md)

> [!Note]  
> Wenn der Datenträger Hardwareverschlüsselung unterstützt, legt diese Funktion den Bandstatus auf "entsperrt" fest.

 

## <a name="syntax"></a>Syntax


```mof
uint32 UnlockWithCertificateThumbprint(
  [in] string CertThumbprint,
  [in] string PIN
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*CertThumbprint* \[ In\]
</dt> <dd>

Typ: **Zeichenfolge**

Der Fingerabdruckwert 0 wird akzeptiert und führt zu einer Suche im lokalen Speicher nach dem entsprechenden Zertifikat. Wenn ein einzelnes BitLocker-Zertifikat gefunden wird, ist die Suche erfolgreich. Wenn kein oder mehrere Zertifikate gefunden werden, schlägt die -Methode fehl.

</dd> <dt>

*PIN* \[ In\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine benutzerdefinierte persönliche Identifikationszeichenfolge. Diese Zeichenfolge muss aus einer Sequenz von 4 bis 20 Ziffern bestehen. Diese Zeichenfolge wird verwendet, um den [*Schlüsselspeicheranbieter (Key Storage Provider,*](../secgloss/k-gly.md) KSP) im Hintergrund zu authentifizieren, wenn er mit einer [*Smartcard*](../secgloss/s-gly.md)verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn er fehlschlägt.



| Rückgabecode/-wert                                                                                                                                                                            | BESCHREIBUNG                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                            | Die Methode war erfolgreich.<br/>                                                                                                                                                                                                                                    |
| <dl> <dt>**FVE \_ E \_ NICHT \_ AKTIVIERT**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüsselschutzvorrichtung hinzu, um BitLocker zu aktivieren. <br/>                                                                                                                                                                             |
| <dl> <dt>**FVE \_ E \_ FAILED \_ AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt> </dl>   | Das Volume kann nicht mithilfe der bereitgestellten Informationen entsperrt werden. <br/>                                                                                                                                                                                             |
| <dl> <dt>**FVE \_ \_E-SCHUTZVORRICHTUNG \_ NICHT GEFUNDEN \_ 2150694963**</dt> <dt>(0x80310033)</dt> </dl>    | Die bereitgestellte Schlüsselschutzvorrichtung ist auf dem Volume nicht vorhanden. Sie müssen eine andere Schlüsselschutzvorrichtung eingeben.<br/>                                                                                                                                                                |
| <dl> <dt>**FVE \_ E \_ PRIVATEKEY \_ AUTH \_ FAILED**</dt> <dt>2150695060 (0x80310094)</dt> </dl> | Der dem angegebenen Zertifikat zugeordnete [*private Schlüssel*](../secgloss/p-gly.md) konnte nicht autorisiert werden. Die Autorisierung des privaten Schlüssels wurde entweder nicht bereitgestellt, oder die bereitgestellte Autorisierung war ungültig.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Enterprise, nur Windows 7 \[ Ultimate-Desktop-Apps\]<br/>                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | \\CIMV2-Stammsicherheit \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
