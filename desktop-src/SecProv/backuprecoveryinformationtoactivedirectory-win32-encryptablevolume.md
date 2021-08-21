---
description: Sichern von Wiederherstellungsdaten in Active Directory
ms.assetid: 664562b3-5679-4185-8bbc-5d5350494707
title: BackupRecoveryInformationToActiveDirectory-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.BackupRecoveryInformationToActiveDirectory
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: bd24a13b7f41f2e87f48c2e5ba97a890d10df3245fcbc6e16f9291c1e0629d27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892958"
---
# <a name="backuprecoveryinformationtoactivedirectory-method-of-the-win32_encryptablevolume-class"></a>BackupRecoveryInformationToActiveDirectory-Methode der Win32 \_ EncryptableVolume-Klasse

Die **BackupRecoveryInformationToActiveDirectory-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) gesichert Wiederherstellungsdaten in Active Directory. Diese Methode erfordert, dass auf dem Volume eine numerische Kennwortschutzvorrichtung vorhanden ist. Gruppenrichtlinie muss auch so konfiguriert werden, dass die Sicherung von Wiederherstellungsinformationen in Active Directory aktiviert wird.

## <a name="syntax"></a>Syntax


```mof
uint32 BackupRecoveryInformationToActiveDirectory(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*VolumeKeyProtectorID* \[ In\]
</dt> <dd>

Typ: **Zeichenfolge**

Ein eindeutiger Zeichenfolgenbezeichner, der zum Verwalten einer verschlüsselten Volumeschlüsselschutzvorrichtung verwendet wird. Diese Schlüsselschutzvorrichtung muss eine numerische Kennwortschutzvorrichtung sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                            | Beschreibung                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                            | Die Methode war erfolgreich.<br/>                                                                                    |
| <dl> <dt>**S \_ FALSE**</dt> <dt>1 (0x1)</dt> </dl>                                         | Gruppenrichtlinie kann keine Wiederherstellungsinformationen in Active Directory speichern.<br/>                         |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüsselschutzvorrichtung hinzu, um BitLocker zu aktivieren. <br/>                             |
| <dl> <dt>**FVE \_ E \_ \_ UNGÜLTIGER \_ SCHUTZVORRICHTUNGSTYP**</dt> <dt>2150694970 (0x8031003A)</dt> </dl> | Die angegebene Schlüsselschutzvorrichtung ist keine numerische Schlüsselschutzvorrichtung. Sie müssen eine numerische Kennwortschutzvorrichtung eingeben. <br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Enterprise, Windows 7 \[ Ultimate-Desktop-Apps\]<br/>                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | \\CimV2-Stammsicherheit \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 




