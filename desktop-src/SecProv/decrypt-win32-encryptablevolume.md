---
description: Startet die Entschlüsselung eines vollständig verschlüsselten Volumes oder setzt die Entschlüsselung eines teilweise verschlüsselten Volumes fort.
ms.assetid: 3cdbb1c1-1084-4ddb-ba8d-fc2e3ec75224
title: Decrypt-Methode der Win32_EncryptableVolume-Klasse (Infocard.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Decrypt
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e9018cfab8bea6c149c4771a54dbe55a62afafd447f4db2e162aa76d183c28ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004628"
---
# <a name="decrypt-method-of-the-win32_encryptablevolume-class"></a>Decrypt-Methode der Win32 \_ EncryptableVolume-Klasse

Die **Decrypt-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) beginnt mit der Entschlüsselung eines vollständig verschlüsselten Volumes oder setzt die Entschlüsselung eines teilweise verschlüsselten Volumes fort.

Wenn die Entschlüsselung angehalten wird oder in Bearbeitung ist, verhält sich diese Methode genauso wie [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md). Wenn die Verschlüsselung angehalten oder in Bearbeitung ist, setzt diese Methode die Verschlüsselung zurück und beginnt mit der Entschlüsselung. Nach Abschluss der Entschlüsselung werden alle Schlüsselschutzvorrichtungen auf diesem Volume aus dem System entfernt, und das Volume wird in ein NTFS-Standarddateisystem konvertiert.

> [!Note]  
> Wenn der Datenträger hardwareverschlüsselt ist, legt die **Decrypt-Methode** den Bandstatus auf "Immer entsperrt" fest, entfernt alle zugeordneten Metadaten und null die Sicherheits-ID für das Laufwerk.

 

## <a name="syntax"></a>Syntax


```mof
uint32 Decrypt();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn er fehlschlägt.

Diese Methode gibt sofort zurück. Wenn das Volume bereits vollständig entschlüsselt ist und keine anderen Fehler vorhanden sind, gibt diese Methode 0 zurück.



| Rückgabecode/-wert                                                                                                                                                                       | BESCHREIBUNG                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                       | Die Methode war erfolgreich.<br/>                                                                                                                                                                                                   |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl>      | Das Volume ist gesperrt.<br/>                                                                                                                                                                                                        |
| <dl> <dt>**FVE \_ E \_ AUTOUNLOCK \_ ENABLED**</dt> <dt>2150694953 (0x80310029)</dt> </dl> | Dieses Volume kann nicht entschlüsselt werden, da Schlüssel verfügbar sind, die zum automatischen Entsperren von Datenvolumes verwendet werden. <br/> Verwenden Sie [**ClearAllAutoUnlockKeys,**](clearallautounlockkeys-win32-encryptablevolume.md) um diese Schlüssel zu entfernen.<br/> |



 

## <a name="security-considerations"></a>Überlegungen zur Sicherheit

Wenn Sie die **Decrypt-Methode** aufrufen, bleiben die Daten ungeschützter.

Wenn der Schutzstatus des Volumes 1 (PROTECTION ON) lautet, bevor diese Methode verwendet wird, ändert der erfolgreiche Abschluss dieser Methode den Schutzstatus in 0 (PROTECTION OFF), da definitionsgemäß kein teilweise verschlüsseltes Volume geschützt ist.

## <a name="remarks"></a>Hinweise

Wenn das Volume noch nicht vollständig entschlüsselt ist, bewirkt das Ausführen von **Decrypt,** dass [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) angibt, dass die Entschlüsselung durchgeführt wird, und zeigt den Prozentsatz des Volumes an, das verschlüsselt bleibt.

Wenn der Schutzstatus des Volumes "ein" lautet, bevor diese Methode ausgeführt wird, ändert die Ausführung dieser Methode den Schutzstatus in "off", da definitionsgemäß ein teilweise verschlüsseltes Volume nicht geschützt ist.

Wenn diese Methode auf dem aktuell ausgeführten Betriebssystemvolume ausgeführt wird und dieses Betriebssystemvolume zum automatischen Entsperren von Datenvolumes verwendet wird (siehe [**Methode EnableAutoUnlock),**](enableautounlock-win32-encryptablevolume.md)müssen Sie zuerst die [**Methode ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md)aufrufen.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Enterprise, nur Windows Vista \[ Ultimate-Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\CIMV2-Stammsicherheit \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| Header<br/>                   | <dl> <dt>Infocard.h</dt> </dl>                   |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
