---
description: Gibt den Verschlüsselungsalgorithmus und die Schlüsselgröße an, die auf dem Volume verwendet werden.
ms.assetid: 89df3dfc-4789-4d3c-b267-d8e26758e754
title: GetEncryptionMethod-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetEncryptionMethod
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f9f4a2ad20af7c5ee3ba3afd8e2d9e56d0720b38d7afc2b01042e440cc85bf33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892448"
---
# <a name="getencryptionmethod-method-of-the-win32_encryptablevolume-class"></a>GetEncryptionMethod-Methode der Win32 \_ EncryptableVolume-Klasse

Die **GetEncryptionMethod-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) gibt den Verschlüsselungsalgorithmus und die Schlüsselgröße an, die auf dem Volume verwendet werden.

## <a name="syntax"></a>Syntax


```mof
uint32 GetEncryptionMethod(
  [out] uint32 EncryptionMethod,
  [out] string SelfEncryptionDriveEncryptionMethod
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*EncryptionMethod* \[ out\]
</dt> <dd>

Typ: **uint32**

Eine ganze Zahl ohne Vorzeichen, die den Verschlüsselungsalgorithmus und die Schlüsselgröße angibt, die auf dem Volume verwendet werden.



| Wert                                                                                                                                                                                                                                          | Bedeutung                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="None"></span><span id="none"></span><span id="NONE"></span><dl> <dt>**Keine**</dt> <dt>0</dt> </dl>                                | Das Volume ist nicht verschlüsselt.<br/>                                                                                                                                                                                                                           |
| <span id="AES_128_WITH_DIFFUSER"></span><span id="aes_128_with_diffuser"></span><dl> <dt>**AES \_ 128 \_ MIT \_ DIFFUSER**</dt> <dt>1</dt> </dl> | Das Volume wurde vollständig oder teilweise mit dem AES-Algorithmus (Advanced Encryption Standard) verschlüsselt, der mit einer Diffusorebene mit einer AES-Schlüsselgröße von 128 Bits erweitert wurde. Diese Methode ist auf Geräten mit Windows 8.1 oder höher nicht mehr verfügbar.<br/> |
| <span id="AES_256_WITH_DIFFUSER"></span><span id="aes_256_with_diffuser"></span><dl> <dt>**AES \_ 256 \_ MIT \_ DIFFUSER**</dt> <dt>2</dt> </dl> | Das Volume wurde vollständig oder teilweise mit dem AES-Algorithmus (Advanced Encryption Standard) verschlüsselt, der mit einer Diffusorebene mit einer AES-Schlüsselgröße von 256 Bits erweitert wurde. Diese Methode ist auf Geräten mit Windows 8.1 oder höher nicht mehr verfügbar.<br/> |
| <span id="AES_128"></span><span id="aes_128"></span><dl> <dt>**AES \_ 128**</dt> <dt>3</dt> </dl>                                             | Das Volume wurde vollständig oder teilweise mit dem AES-Algorithmus (Advanced Encryption Standard) verschlüsselt, wobei eine AES-Schlüsselgröße von 128 Bits verwendet wurde.<br/>                                                                                                             |
| <span id="AES_256"></span><span id="aes_256"></span><dl> <dt>**AES \_ 256**</dt> <dt>4</dt> </dl>                                             | Das Volume wurde vollständig oder teilweise mit dem AES-Algorithmus (Advanced Encryption Standard) mit einer AES-Schlüsselgröße von 256 Bits verschlüsselt.<br/>                                                                                                             |
| <span id="HARDWARE_ENCRYPTION"></span><span id="hardware_encryption"></span><dl> <dt>**HARDWARE \_ ENCRYPTION**</dt> <dt>5</dt> </dl>         | Das Volume wurde vollständig oder teilweise mithilfe der Hardwarefunktionen des Laufwerks verschlüsselt.<br/>                                                                                                                                                      |
| <span id="XTS_AES_128"></span><span id="xts_aes_128"></span><dl> <dt>**XTS \_ AES \_ 128**</dt> <dt>6</dt> </dl>                                | Das Volume wurde mithilfe des Advanced Encryption Standard (AES) und einer AES-Schlüsselgröße von 128 Bit vollständig oder teilweise mit XTS verschlüsselt. Diese Methode ist nur auf Geräten verfügbar, auf denen Windows 10 Version 1511 oder höher ausgeführt wird.<br/>                          |
| <span id="XTS_AES_256"></span><span id="xts_aes_256"></span><dl> <dt>**XTS \_ AES \_ 256**</dt> <dt>7</dt> </dl>                                | Das Volume wurde mithilfe des Advanced Encryption Standard (AES) und einer AES-Schlüsselgröße von 256 Bit vollständig oder teilweise mit XTS verschlüsselt. Diese Methode ist nur auf Geräten verfügbar, auf denen Windows 10 Version 1511 oder höher ausgeführt wird.<br/>                          |
| <dl> <dt>(uint32)–1</dt> </dl>                                                                                                                                                          | UNBEKANNT<br/> Das Volume wurde vollständig oder teilweise mit einem unbekannten Algorithmus und einer unbekannten Schlüsselgröße verschlüsselt.<br/>                                                                                                                                            |



 

</dd> <dt>

*SelfEncryptionDriveEncryptionMethod* \[ out\]
</dt> <dd>

Typ: **Zeichenfolge**

Der Verschlüsselungsalgorithmus wird auf dem selbstverschlüsselnden Laufwerk konfiguriert. Eine NULL-Zeichenfolge bedeutet, dass entweder BitLocker Softwareverschlüsselung verwendet oder keine Verschlüsselungsmethode gemeldet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn er fehlschlägt.



| Rückgabecode/-wert                                                                                                                                 | BESCHREIBUNG                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Die Methode war erfolgreich.<br/> |



 

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Enterprise, nur Windows Vista \[ Ultimate-Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\CIMV2-Stammsicherheit \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
