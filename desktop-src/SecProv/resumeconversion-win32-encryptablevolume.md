---
description: Setzt die Verschlüsselung oder Entschlüsselung eines Volumes fort.
ms.assetid: e37f3e32-5510-431e-9782-11908e65300d
title: ResumeConversion-Methode der Win32_EncryptableVolume-Klasse
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
ms.openlocfilehash: e1b3908f77b72f7f9a5ca0583193784ba054a50ab59aa63dad1c13b9f03317e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992670"
---
# <a name="resumeconversion-method-of-the-win32_encryptablevolume-class"></a>ResumeConversion-Methode der Win32 \_ EncryptableVolume-Klasse

Die **ResumeConversion-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) setzt die Verschlüsselung oder Entschlüsselung eines Volumes fort.

> [!Note]  
> Wenn der Datenträger die Hardwareverschlüsselung unterstützt, kann diese Funktion nur einen Zurücksetzungsvorgang fortsetzen. Weitere Informationen finden Sie unter [**PauseConversion**](pauseconversion-win32-encryptablevolume.md).

 

## <a name="syntax"></a>Syntax


```mof
uint32 ResumeConversion();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn er fehlschlägt.

Wenn diese Methode auf einem vollständig verschlüsselten oder vollständig entschlüsselten Volume verwendet wird oder die Verschlüsselung/Entschlüsselung auf dem Volume bereits ausgeführt wird, wird 0 zurückgegeben, sofern keine anderen Fehler auftreten.



| Rückgabecode/-wert                                                                                                                                                                  | BESCHREIBUNG                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Die Methode war erfolgreich.<br/> |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | Das Volume ist gesperrt.<br/>      |



 

## <a name="remarks"></a>Hinweise

Wenn diese Methode auf einem Volume mit angehaltener Verschlüsselung/Entschlüsselung verwendet wird, bewirkt die erfolgreiche Ausführung dieser Methode, dass [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) angibt, dass die Verschlüsselung oder Entschlüsselung ausgeführt wird.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Enterprise, nur Windows Vista \[ Ultimate-Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\CIMV2-Stammsicherheit \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
