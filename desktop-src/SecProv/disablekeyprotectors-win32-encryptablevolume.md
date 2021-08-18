---
description: Deaktiviert oder unter suspendiert alle Schlüsselschutzvorrichtungen, die diesem Volume zugeordnet sind.
ms.assetid: 19eed858-a116-4ec8-937a-2eea7aadbdc6
title: DisableKeyProtectors-Methode der Win32_EncryptableVolume Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DisableKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 79b9db0043e04d3ab6399677a9e103961d5f1a9b5c5214558bcf53359bedc61a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892539"
---
# <a name="disablekeyprotectors-method-of-the-win32_encryptablevolume-class"></a>DisableKeyProtectors-Methode der Win32 \_ EncryptableVolume-Klasse

Die **DisableKeyProtectors-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) deaktiviert oder unter suspendiert alle Schlüsselschutzvorrichtungen, die diesem Volume zugeordnet sind.

## <a name="syntax"></a>Syntax


```mof
uint32 DisableKeyProtectors(
  [in, optional] uint32 DisableCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DisableCount* \[ in, optional\]
</dt> <dd>

Typ: **uint32**

Eine ganze Zahl, die die Anzahl der Neustarts angibt, für die die Schlüsselschutzvorrichtungen deaktiviert werden. Dieser Parameter ist nur auf Betriebssystemvolumes verfügbar.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                  | BESCHREIBUNG                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Die Methode war erfolgreich.<br/> |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | Das Volume ist gesperrt.<br/>      |



 

## <a name="security-considerations"></a>Überlegungen zur Sicherheit

Mit dieser Methode wird der Verschlüsselungsschlüssel des Volumes auf der Festplatte im Klarschalten verfügbar gemacht, und der Volumeschutz wird deaktiviert. Wir raten davon ab, ein Kennwort oder einen Verschlüsselungsschlüssel in Klartext zu verwenden.

## <a name="remarks"></a>Hinweise

Neue Schlüsselschutzvorrichtungen können hinzugefügt werden, auch wenn Schlüsselschutzvorrichtungen deaktiviert oder angehalten werden. Diese Schlüsselschutzvorrichtungen bleiben deaktiviert, es sei [**denn, EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) wird aufgerufen.

Managed Object Format (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | \\CimV2-Stammsicherheit \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> <dt>

[**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md)
</dt> </dl>

 

 
