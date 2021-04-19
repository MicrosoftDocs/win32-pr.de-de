---
description: Hält die Verschlüsselung oder Entschlüsselung eines Volumes an.
ms.assetid: 3c365299-f0e1-480e-ad96-c91bb4108bb2
title: Pauseconversion-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.PauseConversion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 1c9756da2339a6a3d8e87466651f61c8ff3f83a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363619"
---
# <a name="pauseconversion-method-of-the-win32_encryptablevolume-class"></a>Pauseconversion-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die Methode " **pauseconversion** " der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " hält die Verschlüsselung oder Entschlüsselung eines Volumes an.

> [!Note]  
> Wenn die Festplatte die Hardware Verschlüsselung unterstützt, kann diese Funktion einen Zurücksetzungs Vorgang anhalten, aber die hardwarebasierte Verschlüsselung nicht anhalten.

 

## <a name="syntax"></a>Syntax


```mof
uint32 PauseConversion();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.

Wenn diese Methode auf einem vollständig verschlüsselten oder vollständig entschlüsselten Volume verwendet wird oder wenn die Verschlüsselung/Entschlüsselung auf dem Volume bereits angehalten wurde, wird 0 zurückgegeben, wenn keine anderen Fehler auftreten.



| Rückgabecode/-wert                                                                                                                                                                  | BESCHREIBUNG                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Die Methode war erfolgreich.<br/> |
| <dl> <dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | Das Volume ist gesperrt.<br/>      |



 

## <a name="remarks"></a>Bemerkungen

Wenn diese Methode auf einem Volume mit verschlüsselter Verschlüsselung und Entschlüsselung verwendet wird, bewirkt die erfolgreiche Ausführung dieser Methode, dass " [**getkonversionstatus**](getconversionstatus-win32-encryptablevolume.md) " angibt, dass die Verschlüsselung oder Entschlüsselung angehalten wurde.

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ verschlüsseltablevolume. MOF</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ verschlüsseltablevolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
