---
description: Hiermit werden alle diesem Volume zugeordneten Schlüssel Schutzvorrichtungen deaktiviert oder angehalten.
ms.assetid: 19eed858-a116-4ec8-937a-2eea7aadbdc6
title: Disablekeyprotector-Methode der Win32_EncryptableVolume-Klasse
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
ms.openlocfilehash: 1de392c50f6665d793883582e2679cd502efbe37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359072"
---
# <a name="disablekeyprotectors-method-of-the-win32_encryptablevolume-class"></a>Disablekeyprotector-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Mit der **disablekeyprotector** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " werden alle diesem Volume zugeordneten Schlüssel Schutzvorrichtungen deaktiviert oder angehalten.

## <a name="syntax"></a>Syntax


```mof
uint32 DisableKeyProtectors(
  [in, optional] uint32 DisableCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Disablecount* \[ in, optional\]
</dt> <dd>

Typ: **UInt32**

Eine ganze Zahl, die die Anzahl der Neustarts angibt, für die die Schlüssel Schutzvorrichtungen deaktiviert werden. Dieser Parameter ist nur auf Betriebssystemvolumes verfügbar.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                  | BESCHREIBUNG                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Die Methode war erfolgreich.<br/> |
| <dl> <dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | Das Volume ist gesperrt.<br/>      |



 

## <a name="security-considerations"></a>Überlegungen zur Sicherheit

Diese Methode macht den Verschlüsselungsschlüssel des Volumes im Klartext auf der Festplatte verfügbar und deaktiviert den volumeschutz. Es wird davon abgeraten, ein Kennwort oder einen Verschlüsselungsschlüssel als Klartext anzugeben.

## <a name="remarks"></a>Bemerkungen

Neue Schlüssel Schutzvorrichtungen können auch dann hinzugefügt werden, wenn Schlüssel Schutzvorrichtungen deaktiviert oder angehalten wurden. Diese Schlüsselschutz Vorrichtungen bleiben deaktiviert, sofern [**enablekeyprotector**](enablekeyprotectors-win32-encryptablevolume.md) nicht aufgerufen wird.

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ verschlüsseltablevolume. MOF</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ verschlüsseltablevolume**](win32-encryptablevolume.md)
</dt> <dt>

[**Enablekeyprotector**](enablekeyprotectors-win32-encryptablevolume.md)
</dt> </dl>

 

 
