---
description: Gibt an, ob auf den Inhalt des Volumes von einem Windows.
ms.assetid: 54b2a41b-11c6-40ec-97fa-74996c15554e
title: GetLockStatus-Methode der Win32_EncryptableVolume Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetLockStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: caa213dbebc7db07851bc8df41b5d9379d3dfe97ee207f9b2578b0567fd9b65b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892016"
---
# <a name="getlockstatus-method-of-the-win32_encryptablevolume-class"></a>GetLockStatus-Methode der Win32 \_ EncryptableVolume-Klasse

Die **GetLockStatus-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) gibt an, ob auf den Inhalt des Volumes über die Windows.

## <a name="syntax"></a>Syntax


```mof
uint32 GetLockStatus(
  [out] uint32 LockStatus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*LockStatus* \[ out\]
</dt> <dd>

Typ: **uint32**

Gibt an, ob auf den Inhalt des Volumes über die Windows.



| Wert                                                                                                                                                                                                                           | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unlocked"></span><span id="unlocked"></span><span id="UNLOCKED"></span><dl> <dt>**Entsperrt**</dt> <dt>0</dt> </dl> | Für eine HDD Standard-Festplatte:<br/> Auf den vollständigen Inhalt des Volumes kann zugegriffen werden. Ein entsperrtes Volume ist entweder vollständig entschlüsselt oder verfügt über den Verschlüsselungsschlüssel, der auf dem Datenträger unverschlüsselt verfügbar ist. Auf das Volume mit dem aktuell ausgeführten Betriebssystem (z. B. das ausgeführte Windows) kann immer zugegriffen werden und kann nicht gesperrt werden.<br/> Für eine EHDD:<br/> Das Band ist unbefristet entsperrt.<br/> |
| <span id="Locked"></span><span id="locked"></span><span id="LOCKED"></span><dl> <dt>**Gesperrt**</dt> <dt>1</dt> </dl>         | Für eine HDD Standard-Festplatte:<br/> Auf alle oder einen Teil des Inhalts des Volumes kann nicht zugegriffen werden. Ein gesperrtes Volume muss teilweise oder vollständig verschlüsselt sein und darf nicht über den Verschlüsselungsschlüssel verfügen, der auf dem Datenträger in clear verfügbar ist.<br/> Für eine EHDD:<br/> Das Band ist entsperrt oder gesperrt.<br/>                                                                                                             |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                 | BESCHREIBUNG                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Die Methode war erfolgreich.<br/> |



 

## <a name="remarks"></a>Hinweise

Verwenden Sie [**unlockWithExternalKey und**](unlockwithexternalkey-win32-encryptablevolume.md) [**UnlockWithNumericalPassword,**](unlockwithnumericalpassword-win32-encryptablevolume.md) um Zugriff auf den Volumeinhalt zu erhalten. Verwenden [](lock-win32-encryptablevolume.md) Sie die Lock-Methode, um den Zugriff auf Volumeinhalte zu vererbn.

Auf das Volume, das das derzeit ausgeführte Betriebssystem enthält, kann immer zugegriffen werden und kann nicht gesperrt werden.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

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
</dt> </dl>

 

 
