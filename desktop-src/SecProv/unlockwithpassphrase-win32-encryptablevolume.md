---
description: 'UnlockWithPassphrase-Methode der Win32_EncryptableVolume Klasse: Verwendet die Passphrase, um den abgeleiteten Schlüssel zu erhalten.'
ms.assetid: 09b4ae7f-7084-42bd-8bbe-da686d6280e9
title: UnlockWithPassphrase-Methode der Win32_EncryptableVolume-Klasse
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
ms.openlocfilehash: 0206bf7884ffa204bc768ddfcf5a4a590bf25b60
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116458"
---
# <a name="unlockwithpassphrase-method-of-the-win32_encryptablevolume-class"></a>UnlockWithPassphrase-Methode der Win32 \_ EncryptableVolume-Klasse

Die **UnlockWithPassphrase-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) verwendet die Passphrase, um den abgeleiteten Schlüssel zu erhalten. Nachdem der abgeleitete Schlüssel berechnet wurde, wird der abgeleitete Schlüssel verwendet, um den Hauptschlüssel des verschlüsselten Volumes zu entsperren.

> [!Note]  
> Wenn der Datenträger Hardwareverschlüsselung unterstützt, legt diese Funktion den Bandstatus auf "Entsperrt" fest.

 

## <a name="syntax"></a>Syntax


```mof
uint32 UnlockWithPassphrase(
  [in] string Passphrase
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Passphrase* \[ In\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die die Passphrase angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                                       | BESCHREIBUNG                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                       | Die Methode war erfolgreich.<br/>                                                                                     |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>                      | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüsselschutzvorrichtung hinzu, um BitLocker zu aktivieren. <br/>                              |
| <dl> <dt>**FVE \_ E \_ FIPS \_ VERHINDERT \_ PASSPHRASE**</dt> <dt>2150695020 (0x8031006C)</dt> </dl>          | Die Gruppenrichtlinieneinstellung, die FIPS-Konformität erfordert, hat verhindert, dass die Passphrase generiert oder verwendet wird. <br/> |
| <dl> <dt>**FVE \_ E \_ POLICY \_ INVALID \_ PASSPHRASE \_ LENGTH**</dt> <dt>2150695040 (0x80310080)</dt> </dl> | Die bereitgestellte Passphrase erfüllt nicht die Mindest- oder Höchstlängenanforderungen.<br/>                              |
| <dl> <dt>**FVE \_ E \_ POLICY \_ PASSPHRASE \_ TOO \_ SIMPLE**</dt> <dt>2150695041 (0x80310081)</dt> </dl>     | Die Passphrase erfüllt nicht die Komplexitätsanforderungen, die der Administrator in der Gruppenrichtlinie festgelegt hat.<br/>             |
| <dl> <dt>**FVE \_ E \_ FAILED \_ AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt> </dl>              | Das Volume kann nicht mit den bereitgestellten Informationen entsperrt werden. <br/>                                                  |
| <dl> <dt>**FVE \_ \_E-SCHUTZVORRICHTUNG \_ NICHT \_ GEFUNDEN**</dt> <dt>2150694963 (0x80310033)</dt> </dl>               | Die bereitgestellte Schlüsselschutzvorrichtung ist auf dem Volume nicht vorhanden. Sie müssen eine andere Schlüsselschutzvorrichtung eingeben.<br/>                 |



 

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

 

 




