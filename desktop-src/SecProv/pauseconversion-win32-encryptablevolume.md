---
description: Hält die Verschlüsselung oder Entschlüsselung eines Volumes an.
ms.assetid: 3c365299-f0e1-480e-ad96-c91bb4108bb2
title: PauseConversion-Methode der Win32_EncryptableVolume-Klasse
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
ms.openlocfilehash: 7612f7f587d13bb1dbe5fc96d29117d126b3a7166e0172abe98a0777d815effa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004448"
---
# <a name="pauseconversion-method-of-the-win32_encryptablevolume-class"></a>PauseConversion-Methode der Win32 \_ EncryptableVolume-Klasse

Die **PauseConversion-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) hält die Verschlüsselung oder Entschlüsselung eines Volumes an.

> [!Note]  
> Wenn der Datenträger die Hardwareverschlüsselung unterstützt, kann diese Funktion einen Abbruchvorgang anhalten, aber die hardwarebasierte Verschlüsselung nicht anhalten.

 

## <a name="syntax"></a>Syntax


```mof
uint32 PauseConversion();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.

Wenn diese Methode auf einem vollständig verschlüsselten oder vollständig entschlüsselten Volume verwendet wird oder die Verschlüsselung/Entschlüsselung bereits auf dem Volume angehalten wurde, wird 0 zurückgegeben, vorausgesetzt, es treten keine anderen Fehler auf.



| Rückgabecode/-wert                                                                                                                                                                  | BESCHREIBUNG                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Die Methode war erfolgreich.<br/> |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | Das Volume ist gesperrt.<br/>      |



 

## <a name="remarks"></a>Hinweise

Wenn diese Methode auf einem Volume verwendet wird, auf dem die Verschlüsselung/Entschlüsselung ausgeführt wird, bewirkt die erfolgreiche Ausführung dieser Methode, dass [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) darauf hinweist, dass die Verschlüsselung oder Entschlüsselung angehalten wurde.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Enterprise, Windows Vista \[ Ultimate-Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\CimV2-Stammsicherheit \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
