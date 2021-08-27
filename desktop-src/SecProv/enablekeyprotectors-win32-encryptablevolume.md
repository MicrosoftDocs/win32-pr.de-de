---
description: Aktiviert oder setzt alle deaktivierten oder angehaltenen Schlüsselschutzvorrichtungen wieder auf.
ms.assetid: 6f5a17a3-84f2-43a0-a85f-1037cd52439a
title: EnableKeyProtectors-Methode der Win32_EncryptableVolume Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EnableKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: d90e37f800a9c224abefb21253f7e74c2bc08401
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474926"
---
# <a name="enablekeyprotectors-method-of-the-win32_encryptablevolume-class"></a>EnableKeyProtectors-Methode der Win32 \_ EncryptableVolume-Klasse

Die **EnableKeyProtectors-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) aktiviert oder setzt alle deaktivierten oder angehaltenen Schlüsselschutzvorrichtungen wieder auf. Mit dieser Methode können Sie den BitLocker-Schutz auf einem verschlüsselten Volume erneut aktivieren oder fortsetzen. Mit dieser Methode wird sichergestellt, dass der Verschlüsselungsschlüssel des Volumes auf der Festplatte nicht im Klaro verfügbar gemacht wird.

> [!Note]  
> Wenn der Datenträger Hardwareverschlüsselung unterstützt, geht der Bandzustand von "immer entsperrt" in "entsperrt" über.

 

## <a name="syntax"></a>Syntax


```mof
uint32 EnableKeyProtectors();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.

Wenn Die Schlüsselschutzvorrichtungen bereits aktiviert sind und keine anderen Fehler auftreten, gibt diese Methode 0 (null) zurück.




| Rückgabecode/-wert | BESCHREIBUNG | 
|-------------------|-------------|
| <dl><dt><strong>S_OK</strong></dt><dt>0 (0x0)</dt></dl> | Die Methode war erfolgreich.<br /> | 
| <dl><dt><strong>FVE_E_SECURE_KEY_REQUIRED</strong></dt><dt>2150694919 (0x80310007)</dt></dl> | Auf dem Volume sind keine Schlüsselschutzvorrichtungen vorhanden. Verwenden Sie eine der folgenden Methoden, um Schlüsselschutzvorrichtungen für das Volume anzugeben:<br /><ul><li><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateFile</strong></a></li><li><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateThumbprint</strong></a></li><li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li><li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li><li><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>ProtectKeyWithPassphrase</strong></a></li><li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li><li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li><li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></li><li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li></ul> | 
| <dl><dt><strong>FVE_E_NOT_ACTIVATED</strong></dt><dt>2150694920 (0x80310008)</dt></dl> | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüsselschutzvorrichtung hinzu, um BitLocker zu aktivieren. <br /> | 




 

## <a name="remarks"></a>Hinweise

Wenn das Volume vollständig verschlüsselt ist, wird durch die erfolgreiche Ausführung dieser Methode sichergestellt, dass das Volume geschützt ist. Wenn das Volume teilweise verschlüsselt ist, bedeutet die erfolgreiche Ausführung dieser Methode, dass das Volume geschützt wird, wenn es vollständig verschlüsselt wird. Weitere Informationen finden Sie unter [**GetProtectionStatus-Methode.**](getprotectionstatus-win32-encryptablevolume.md)

Wenn TPM-basierte Schlüsselschutzvorrichtungen für das Volume vorhanden sind, aktualisiert die erfolgreiche Ausführung dieser Methode auch diese Schutzvorrichtungen, sodass das TPM anhand der aktuellen Startdienste auf der Plattform überprüft wird. Anders ausgedrückt: Sie stellen sicher, dass der aktuelle Computerstatus der richtige Zustand ist, den das TPM bei zukünftigen Neustarts des Computers überprüft.

Managed Object Format (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Enterprise, Windows Vista \[ Ultimate-Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\CimV2-Stammsicherheit \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> <dt>

[**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithCertificateFile**](protectkeywithcertificatefile-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithCertificateThumbprint**](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithPassphrase**](protectkeywithpassphrase-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithTPM**](protectkeywithtpm-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithTPMAndPIN**](protectkeywithtpmandpin-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithTPMAndPINAndStartupKey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithTPMAndStartupKey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)
</dt> </dl>

 

 
