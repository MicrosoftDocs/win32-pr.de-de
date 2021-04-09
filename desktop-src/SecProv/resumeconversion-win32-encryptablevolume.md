---
description: Nimmt die Verschlüsselung oder Entschlüsselung eines Volumes wieder auf.
ms.assetid: e37f3e32-5510-431e-9782-11908e65300d
title: Resumeconversion-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ResumeConversion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: eafa700f86e51310096835e2f24b53a28e66f800
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750833"
---
# <a name="resumeconversion-method-of-the-win32_encryptablevolume-class"></a>Resumeconversion-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **resumeconversion** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " nimmt die Verschlüsselung oder Entschlüsselung eines Volumes wieder auf.

> [!Note]  
> Wenn die Festplatte die Hardware Verschlüsselung unterstützt, kann diese Funktion nur einen Zurücksetzungs Vorgang fortsetzen. Weitere Informationen finden Sie unter " [**pauseconversion**](pauseconversion-win32-encryptablevolume.md)".

 

## <a name="syntax"></a>Syntax


```mof
uint32 ResumeConversion();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.

Wenn diese Methode auf einem vollständig verschlüsselten oder vollständig entschlüsselten Volume verwendet wird, oder wenn auf dem Volume bereits eine Verschlüsselung/Entschlüsselung ausgeführt wird, wird 0 zurückgegeben, wenn keine anderen Fehler auftreten.



| Rückgabecode/-wert                                                                                                                                                                  | BESCHREIBUNG                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Die Methode war erfolgreich.<br/> |
| <dl> <dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | Das Volume ist gesperrt.<br/>      |



 

## <a name="remarks"></a>Bemerkungen

Wenn diese Methode auf einem Volume mit angehaltenen Verschlüsselung/Entschlüsselung verwendet wird, bewirkt die erfolgreiche Ausführung dieser Methode, dass [**getkonversionstatus**](getconversionstatus-win32-encryptablevolume.md) anzeigt, dass die Verschlüsselung oder Entschlüsselung ausgeführt wird.

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

 

 
