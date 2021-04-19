---
description: Verwendet die Passphrase zum Abrufen des abgeleiteten Schlüssels.
ms.assetid: 09b4ae7f-7084-42bd-8bbe-da686d6280e9
title: Unlockwithpasspphrase-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithPassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 75c5522a0781b1cd229bf97d2549433a426fbfc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360809"
---
# <a name="unlockwithpassphrase-method-of-the-win32_encryptablevolume-class"></a>Unlockwithpasspphrase-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **unlockwithpasspphrase** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " verwendet die Passphrase zum Abrufen des abgeleiteten Schlüssels. Nachdem der abgeleitete Schlüssel berechnet wurde, wird der abgeleitete Schlüssel verwendet, um den Hauptschlüssel des verschlüsselten Volumes zu entsperren.

> [!Note]  
> Wenn die Festplatte Hardware Verschlüsselung unterstützt, legt diese Funktion den Bandstatus auf "entsperrt" fest.

 

## <a name="syntax"></a>Syntax


```mof
uint32 UnlockWithPassphrase(
  [in] string Passphrase
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Passphrase* \[ in\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die die Passphrase angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                                       | BESCHREIBUNG                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                       | Die Methode war erfolgreich.<br/>                                                                                     |
| <dl> <dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt> </dl>                      | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu. <br/>                              |
| <dl> <dt>**F \_ E-fi-Kenn \_ \_ \_ Wörter verhindern Passphrase**</dt> <dt>2150695020 (0x8031006c)</dt> </dl>          | Die Gruppenrichtlinien Einstellung, die die Kompatibilität mit der Konformität erfordert, verhindert, dass die Passphrase generiert oder verwendet wird. <br/> |
| <dl> <dt>**F \_ E \_ Richtlinie \_ ungültige \_ Passphrasen \_ Länge**</dt> <dt>2150695040 (0x80310080)</dt> </dl> | Die angegebene Passphrase entspricht nicht den Anforderungen an die minimale oder maximale Länge.<br/>                              |
| <dl> <dt>**F \_ E \_ - \_ richtlinienpass Phrase \_ zu \_ einfach**</dt> <dt>2150695041 (0x80310081)</dt> </dl>     | Die Passphrase erfüllt nicht die Komplexitäts Anforderungen, die vom Administrator in der Gruppenrichtlinie festgelegt werden.<br/>             |
| <dl> <dt>**F \_ E \_ \_**</dt> -Fehler bei Authentifizierung <dt>2150694951 (0x80310027)</dt> </dl>              | Das Volume kann mit den bereitgestellten Informationen nicht entsperrt werden. <br/>                                                  |
| <dl> <dt>**F \_ E \_ Protector \_ nicht \_ gefunden**</dt> <dt>2150694963 (0x80310033)</dt> </dl>               | Die angegebene Schlüssel Schutzvorrichtung ist auf dem Volume nicht vorhanden. Sie müssen eine andere Schlüssel Schutzvorrichtung eingeben.<br/>                 |



 

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

 

 




