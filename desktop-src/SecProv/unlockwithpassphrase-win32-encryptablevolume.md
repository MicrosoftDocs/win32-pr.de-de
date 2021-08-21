---
description: 'UnlockWithPassphrase-Methode der Win32_EncryptableVolume-Klasse: Verwendet die Passphrase, um den abgeleiteten Schlüssel abzurufen.'
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
ms.openlocfilehash: 7b8a1ef65fd1ca3e279631a1add00ad7c07e2ff870bc24c883fd1877a3800d52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004168"
---
# <a name="unlockwithpassphrase-method-of-the-win32_encryptablevolume-class"></a>UnlockWithPassphrase-Methode der Win32 \_ EncryptableVolume-Klasse

Die **UnlockWithPassphrase-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) verwendet die Passphrase, um den abgeleiteten Schlüssel abzurufen. Nachdem der abgeleitete Schlüssel berechnet wurde, wird der abgeleitete Schlüssel verwendet, um den Hauptschlüssel des verschlüsselten Volumes zu entsperren.

> [!Note]  
> Wenn der Datenträger Hardwareverschlüsselung unterstützt, legt diese Funktion den Bandstatus auf "entsperrt" fest.

 

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

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn er fehlschlägt.



| Rückgabecode/-wert                                                                                                                                                                                       | BESCHREIBUNG                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                       | Die Methode war erfolgreich.<br/>                                                                                     |
| <dl> <dt>**FVE \_ E \_ NICHT \_ AKTIVIERT**</dt> <dt>2150694920 (0x80310008)</dt> </dl>                      | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüsselschutzvorrichtung hinzu, um BitLocker zu aktivieren. <br/>                              |
| <dl> <dt>**FVE \_ E \_ FIPS \_ VERHINDERT \_ PASSPHRASE-2150695020**</dt> <dt>(0x8031006C)</dt> </dl>          | Die Gruppenrichtlinieneinstellung, die FIPS-Konformität erfordert, hat verhindert, dass die Passphrase generiert oder verwendet wird. <br/> |
| <dl> <dt>**FVE \_ E \_ POLICY \_ INVALID \_ PASSPHRASE \_ LENGTH**</dt> <dt>2150695040 (0x80310080)</dt> </dl> | Die angegebene Passphrase erfüllt nicht die Mindest- oder Höchstlängenanforderungen.<br/>                              |
| <dl> <dt>**FVE \_ E \_ POLICY \_ PASSPHRASE \_ TOO \_ SIMPLE**</dt> <dt>2150695041 (0x80310081)</dt> </dl>     | Die Passphrase erfüllt nicht die Komplexitätsanforderungen, die vom Administrator in der Gruppenrichtlinie festgelegt wurden.<br/>             |
| <dl> <dt>**FVE \_ E \_ FAILED \_ AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt> </dl>              | Das Volume kann nicht mit den bereitgestellten Informationen entsperrt werden. <br/>                                                  |
| <dl> <dt>**FVE \_ \_E-SCHUTZVORRICHTUNG \_ NICHT \_ GEFUNDEN**</dt> <dt>2150694963 (0x80310033)</dt> </dl>               | Die bereitgestellte Schlüsselschutzvorrichtung ist auf dem Volume nicht vorhanden. Sie müssen eine andere Schlüsselschutzvorrichtung eingeben.<br/>                 |



 

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

 

 




