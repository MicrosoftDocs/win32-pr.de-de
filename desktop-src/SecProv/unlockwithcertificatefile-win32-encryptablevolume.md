---
description: Verwendet die bereitgestellte Zertifikatdatei, um den abgeleiteten Schlüssel abzurufen und das verschlüsselte Volume zu entsperren.
ms.assetid: 41811d38-5c89-4372-9dbc-3de45b05011f
title: UnlockWithCertificateFile-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithCertificateFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 576de5820e5b16b59a0b77659a4833a261ecd9ef8445306ce3d6f320c664f833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004228"
---
# <a name="unlockwithcertificatefile-method-of-the-win32_encryptablevolume-class"></a>UnlockWithCertificateFile-Methode der Win32 \_ EncryptableVolume-Klasse

Die **UnlockWithCertificateFile-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) verwendet die bereitgestellte [*Zertifikatdatei,*](../secgloss/c-gly.md) um den abgeleiteten Schlüssel abzurufen und das verschlüsselte Volume zu entsperren.

> [!Note]  
> Wenn der Datenträger Hardwareverschlüsselung unterstützt, legt diese Funktion den Bandstatus auf "entsperrt" fest.

 

## <a name="syntax"></a>Syntax


```mof
uint32 UnlockWithCertificateFile(
  [in] string FileName,
  [in] string PIN
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FileName* \[ In\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die den Speicherort und den Namen der CER-Datei angibt, die zum Abrufen des Zertifikatfingerabdrucks verwendet wird. Ein [*Verschlüsselungszertifikat*](../secgloss/e-gly.md) muss im CER-Format exportiert werden ([*Distinguished Encoding Rules*](../secgloss/d-gly.md) (DER)-codierte Binärdatei [*X.509*](../secgloss/x-gly.md) oder Base-64-codiertes X.509). Das Verschlüsselungszertifikat kann von microsoft-PKI, einer Drittanbieter-PKI oder selbstsigniert generiert werden.

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
| <dl> <dt>**FEHLER \_ DATEI \_ NICHT \_ GEFUNDEN**</dt> <dt>0000000002 (0x2)</dt> </dl>                 | Das System kann die angegebene Datei nicht erstellen.<br/>                                                                                                                                                                                                                    |
| <dl> <dt>**FVE \_ E \_ NICHT \_ AKTIVIERT**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüsselschutzvorrichtung hinzu, um BitLocker zu aktivieren. <br/>                                                                                                                                                                             |
| <dl> <dt>**FVE \_ E \_ FAILED \_ AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt> </dl>   | Das Volume kann nicht mit den bereitgestellten Informationen entsperrt werden. <br/>                                                                                                                                                                                                 |
| <dl> <dt>**FVE \_ \_E-SCHUTZVORRICHTUNG \_ NICHT \_ GEFUNDEN**</dt> <dt>2150694963 (0x80310033)</dt> </dl>    | Die bereitgestellte Schlüsselschutzvorrichtung ist auf dem Volume nicht vorhanden. Sie müssen eine andere Schlüsselschutzvorrichtung eingeben.<br/>                                                                                                                                                                |
| <dl> <dt>**FVE \_ E \_ PRIVATEKEY \_ AUTH \_ FAILED**</dt> <dt>2150695060 (0x80310094)</dt> </dl> | Der [*private Schlüssel,*](../secgloss/p-gly.md)der dem angegebenen Zertifikat zugeordnet ist, konnte nicht autorisiert werden. Die Autorisierung des privaten Schlüssels wurde entweder nicht bereitgestellt, oder die bereitgestellte Autorisierung war ungültig.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Enterprise, nur Windows 7 \[ Ultimate-Desktop-Apps\]<br/>                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | \\CIMV2-Stammsicherheit \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
