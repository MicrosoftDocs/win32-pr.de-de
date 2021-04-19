---
description: Verwendet die angegebene Zertifikat Datei, um den abgeleiteten Schlüssel abzurufen und das verschlüsselte Volume zu entsperren.
ms.assetid: 41811d38-5c89-4372-9dbc-3de45b05011f
title: Unlockwithcertificatefile-Methode der Win32_EncryptableVolume-Klasse
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
ms.openlocfilehash: d7ce1705c0ec457f64eb825e49334e76a14c184c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369015"
---
# <a name="unlockwithcertificatefile-method-of-the-win32_encryptablevolume-class"></a>Unlockwithcertificatefile-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **unlockwithcertificatefile** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " verwendet die angegebene [*Zertifikat*](../secgloss/c-gly.md) Datei, um den abgeleiteten Schlüssel abzurufen und das verschlüsselte Volume zu entsperren.

> [!Note]  
> Wenn die Festplatte Hardware Verschlüsselung unterstützt, legt diese Funktion den Bandstatus auf "entsperrt" fest.

 

## <a name="syntax"></a>Syntax


```mof
uint32 UnlockWithCertificateFile(
  [in] string FileName,
  [in] string PIN
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dateiname* \[ in\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die den Speicherort und den Namen der CER-Datei angibt, die zum Abrufen des Zertifikat Fingerabdrucks verwendet wird. Ein [*Verschlüsselungs*](../secgloss/e-gly.md) Zertifikat muss im CER-Format ([*Distinguished Encoding Rules*](../secgloss/d-gly.md) (der)-codiertes binäres [*x. 509*](../secgloss/x-gly.md) -Format oder Base-64-codiertes x. 509-Format exportiert werden. Das Verschlüsselungs Zertifikat kann von Microsoft PKI, PKI von Drittanbietern oder selbst signiert generiert werden.

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
| <dl> <dt>**Fehler \_ Datei \_ nicht \_ gefunden**</dt> <dt>0000000002 (0x2)</dt> </dl>                 | Das System kann die angegebene Datei nicht ablegen.<br/>                                                                                                                                                                                                                    |
| <dl> <dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu. <br/>                                                                                                                                                                             |
| <dl> <dt>**F \_ E \_ \_**</dt> -Fehler bei Authentifizierung <dt>2150694951 (0x80310027)</dt> </dl>   | Das Volume kann mit den bereitgestellten Informationen nicht entsperrt werden. <br/>                                                                                                                                                                                                 |
| <dl> <dt>**F \_ E \_ Protector \_ nicht \_ gefunden**</dt> <dt>2150694963 (0x80310033)</dt> </dl>    | Die angegebene Schlüssel Schutzvorrichtung ist auf dem Volume nicht vorhanden. Sie müssen eine andere Schlüssel Schutzvorrichtung eingeben.<br/>                                                                                                                                                                |
| <dl> <dt>**F \_ E \_ PrivateKey-Authentifizierung ist \_ \_ fehlgeschlagen**</dt> <dt>2150695060 (0x80310094)</dt> </dl> | Der [*private Schlüssel*](../secgloss/p-gly.md), der dem angegebenen Zertifikat zugeordnet ist, konnte nicht autorisiert werden. Die Autorisierung für den privaten Schlüssel wurde entweder nicht bereitgestellt, oder die angegebene Autorisierung war ungültig.<br/> |



 

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

 

 
