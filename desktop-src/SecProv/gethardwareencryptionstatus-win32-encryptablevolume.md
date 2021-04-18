---
description: Bestimmt, ob sich das Volume auf einem Laufwerk befindet, das die Hardware Verschlüsselung unterstützt oder unterstützt.
ms.assetid: C6007BC4-71CD-404A-A0E9-D9662906151F
title: Gethardwareverschlüsseltionstatus-Methode der Win32_EncryptableVolume-Klasse
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
ms.openlocfilehash: 2f48bb7115d19779f437a849078238cee967f2d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345033"
---
# <a name="gethardwareencryptionstatus-method-of-the-win32_encryptablevolume-class"></a>Gethardwareverschlüsseltionstatus-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **gethardwareverschlüsseltionstatus** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " bestimmt, ob sich das Volume auf einem Laufwerk befindet, das die Hardware Verschlüsselung unterstützt oder unterstützt.

## <a name="syntax"></a>Syntax


```mof
uint32 GetHardwareEncryptionStatus(
  [out] uint32 HardwareEncryptionStatus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Hardwareverschlüsselungsstatus* \[ vorgenommen\]
</dt> <dd>

Gibt an, ob das Laufwerk die Hardware Verschlüsselung unterstützen kann. Dies kann einer der folgenden Werte sein:



| Wert                                                                                                                                                                                                                                               | Bedeutung                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="Not_supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span><dl> <dt>**Nicht unterstützt**</dt> <dt>0</dt> </dl> | Die Hardware Verschlüsselung wird nicht unterstützt.<br/>    |
| <span id="No_protection"></span><span id="no_protection"></span><span id="NO_PROTECTION"></span><dl> <dt>**Kein Schutz**</dt> <dt>1</dt> </dl> | Laufwerk Verschlüsselung wird nicht unterstützt.<br/>       |
| <span id="Uses_software"></span><span id="uses_software"></span><span id="USES_SOFTWARE"></span><dl> <dt>**Verwendet Software**</dt> <dt>2</dt> </dl> | Die Verschlüsselungsmethode ist Software basiert.<br/> |
| <span id="Uses_hardware"></span><span id="uses_hardware"></span><span id="USES_HARDWARE"></span><dl> <dt>**Verwendung von Hardware**</dt> <dt>3</dt> </dl> | Das Laufwerk unterstützt die Hardware Verschlüsselung.<br/>  |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt 0 (null) zurück, wenn das Volume mit der BitLocker-Hardware Verschlüsselung kompatibel ist. Andernfalls gibt die Funktion einen Fehler zurück.



| Rückgabecode/-wert                                                                                                                                 | BESCHREIBUNG                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Das Volume ist mit der BitLocker-Hardware Verschlüsselung kompatibel.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 Enterprise, Windows 8 pro \[ -Desktop-Apps\]<br/>                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ verschlüsseltablevolume. MOF</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ verschlüsseltablevolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 




