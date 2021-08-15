---
description: Aktualisiert ein Volume vom Windows Vista-Format auf das format Windows 7.
ms.assetid: d6654e92-8176-471b-b8e5-815dd9512240
title: UpgradeVolume-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UpgradeVolume
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 721676b0aa135903e0e139bf719e072c3af8b6af33118f168453880fb7329413
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891040"
---
# <a name="upgradevolume-method-of-the-win32_encryptablevolume-class"></a>UpgradeVolume-Methode der Win32 \_ EncryptableVolume-Klasse

Die **UpgradeVolume-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) aktualisiert ein Volume vom Windows Vista-Format auf das Windows 7-Format. Dies ist ein nicht umkehrbarer Vorgang.

## <a name="syntax"></a>Syntax


```mof
uint32 UpgradeVolume();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn er fehlschlägt.

Wenn das Volume bereits entsperrt ist und keine weiteren Fehler auftreten, gibt diese Methode 0 (null) zurück.



| Rückgabecode/-wert                                                                                                                                                                  | BESCHREIBUNG                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Die Methode war erfolgreich.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>214794287 (0xCCD802F)</dt> </dl>            | Mindestens ein Argument ist ungültig.<br/>                                       |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | Das Volume ist gesperrt.<br/>                                                             |
| <dl> <dt>**FVE \_ E \_ NICHT \_ AKTIVIERT**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüsselschutzvorrichtung hinzu, um BitLocker zu aktivieren. <br/> |



 

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

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

 

 
