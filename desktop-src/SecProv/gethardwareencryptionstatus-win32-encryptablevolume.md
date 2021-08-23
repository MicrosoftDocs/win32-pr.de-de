---
description: Bestimmt, ob sich das Volume auf einem Laufwerk befindet, das Hardwareverschlüsselung unterstützt oder unterstützen kann.
ms.assetid: C6007BC4-71CD-404A-A0E9-D9662906151F
title: GetHardwareEncryptionStatus-Methode der Win32_EncryptableVolume Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetHardwareEncryptionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 434c074260a07a251ac81148616c434cb9f7de74d799a42c71bd81451a1bd3b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119668000"
---
# <a name="gethardwareencryptionstatus-method-of-the-win32_encryptablevolume-class"></a>GetHardwareEncryptionStatus-Methode der Win32 \_ EncryptableVolume-Klasse

Die **GetHardwareEncryptionStatus-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) bestimmt, ob sich das Volume auf einem Laufwerk befindet, das Hardwareverschlüsselung unterstützt oder unterstützen kann.

## <a name="syntax"></a>Syntax


```mof
uint32 GetHardwareEncryptionStatus(
  [out] uint32 HardwareEncryptionStatus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HardwareEncryptionStatus* \[ out\]
</dt> <dd>

Gibt an, ob das Laufwerk Hardwareverschlüsselung unterstützen kann. Dies kann einer der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                               | Bedeutung                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="Not_supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span><dl> <dt>**Nicht unterstützt**</dt> <dt>0</dt> </dl> | Die Hardwareverschlüsselung wird nicht unterstützt.<br/>    |
| <span id="No_protection"></span><span id="no_protection"></span><span id="NO_PROTECTION"></span><dl> <dt>**Kein Schutz**</dt> <dt>1</dt> </dl> | Die Laufwerkverschlüsselung wird nicht unterstützt.<br/>       |
| <span id="Uses_software"></span><span id="uses_software"></span><span id="USES_SOFTWARE"></span><dl> <dt>**Verwendet Software**</dt> <dt>2</dt> </dl> | Die Verschlüsselungsmethode ist softwarebasierte Methode.<br/> |
| <span id="Uses_hardware"></span><span id="uses_hardware"></span><span id="USES_HARDWARE"></span><dl> <dt>**Verwendet Hardware**</dt> <dt>3</dt> </dl> | Das Laufwerk unterstützt die Hardwareverschlüsselung.<br/>  |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt null (0) zurück, wenn das Volume mit der BitLocker-Hardwareverschlüsselung kompatibel ist. Andernfalls gibt die Funktion einen Fehler zurück.



| Rückgabecode/-wert                                                                                                                                 | Beschreibung                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Das Volume ist mit der BitLocker-Hardwareverschlüsselung kompatibel.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 Enterprise, nur Windows 8 Pro \[ Desktop-Apps\]<br/>                                    |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\CimV2-Stammsicherheit \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 




