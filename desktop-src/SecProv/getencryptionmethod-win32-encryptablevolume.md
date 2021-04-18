---
description: Gibt den Verschlüsselungsalgorithmus und die Schlüsselgröße an, die auf dem Volume verwendet werden.
ms.assetid: 89df3dfc-4789-4d3c-b267-d8e26758e754
title: Getencryptionmethod-Methode der Win32_EncryptableVolume-Klasse
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
ms.openlocfilehash: 16fb9b00976b652bcc9643ab5ec4912029898424
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352627"
---
# <a name="getencryptionmethod-method-of-the-win32_encryptablevolume-class"></a>Getencryptionmethod-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **getencryptionmethod** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " gibt den Verschlüsselungsalgorithmus und die Schlüsselgröße an, die auf dem Volume verwendet werden.

## <a name="syntax"></a>Syntax


```mof
uint32 GetEncryptionMethod(
  [out] uint32 EncryptionMethod,
  [out] string SelfEncryptionDriveEncryptionMethod
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Verschlüsselungsmethode* \[ vorgenommen\]
</dt> <dd>

Typ: **UInt32**

Eine ganze Zahl ohne Vorzeichen, die den Verschlüsselungsalgorithmus und die Schlüsselgröße angibt, die auf dem Volume verwendet werden.



| Wert                                                                                                                                                                                                                                          | Bedeutung                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="None"></span><span id="none"></span><span id="NONE"></span><dl> <dt>**Keine**</dt> <dt>0</dt> </dl>                                | Das Volume ist nicht verschlüsselt.<br/>                                                                                                                                                                                                                           |
| <span id="AES_128_WITH_DIFFUSER"></span><span id="aes_128_with_diffuser"></span><dl> <dt>**AES \_ 128 \_ mit \_ diffuser**</dt> <dt>1</dt> </dl> | Das Volume wurde mithilfe einer AES-Schlüsselgröße von 128 Bits vollständig oder teilweise mit dem Advanced Encryption Standard (AES)-Algorithmus verschlüsselt, der durch eine diffuser-Schicht erweitert wurde. Diese Methode ist nicht mehr auf Geräten verfügbar, auf denen Windows 8.1 oder höher ausgeführt wird.<br/> |
| <span id="AES_256_WITH_DIFFUSER"></span><span id="aes_256_with_diffuser"></span><dl> <dt>**AES \_ 256 \_ mit \_ diffuser**</dt> <dt>2</dt> </dl> | Das Volume wurde mithilfe einer AES-Schlüsselgröße von 256 Bits vollständig oder teilweise mit dem Advanced Encryption Standard (AES)-Algorithmus verschlüsselt, der durch eine diffuser-Schicht erweitert wurde. Diese Methode ist nicht mehr auf Geräten verfügbar, auf denen Windows 8.1 oder höher ausgeführt wird.<br/> |
| <span id="AES_128"></span><span id="aes_128"></span><dl> <dt>**AES \_ 128**</dt> <dt>3</dt> </dl>                                             | Das Volume wurde mit dem Advanced Encryption Standard (AES)-Algorithmus vollständig oder teilweise verschlüsselt, wobei eine AES-Schlüsselgröße von 128 Bits verwendet wurde.<br/>                                                                                                             |
| <span id="AES_256"></span><span id="aes_256"></span><dl> <dt>**AES \_ 256**</dt> <dt>4</dt> </dl>                                             | Das Volume wurde mit dem Advanced Encryption Standard (AES)-Algorithmus vollständig oder teilweise verschlüsselt, wobei eine AES-Schlüsselgröße von 256 Bits verwendet wurde.<br/>                                                                                                             |
| <span id="HARDWARE_ENCRYPTION"></span><span id="hardware_encryption"></span><dl> <dt>**Hardware \_ Verschlüsselung**</dt> <dt>5</dt> </dl>         | Das Volume wurde mithilfe der Hardwarefunktionen des Laufwerks vollständig oder teilweise verschlüsselt.<br/>                                                                                                                                                      |
| <span id="XTS_AES_128"></span><span id="xts_aes_128"></span><dl> <dt>**XTS \_ AES \_ 128**</dt> <dt>6</dt> </dl>                                | Das Volume wurde mit XTS vollständig oder teilweise verschlüsselt, wobei die Advanced Encryption Standard (AES) und eine AES-Schlüsselgröße von 128 Bits verwendet werden. Diese Methode ist nur auf Geräten verfügbar, auf denen Windows 10, Version 1511 oder höher, ausgeführt wird.<br/>                          |
| <span id="XTS_AES_256"></span><span id="xts_aes_256"></span><dl> <dt>**XTS \_ AES \_ 256**</dt> <dt>7</dt> </dl>                                | Das Volume wurde mit XTS vollständig oder teilweise verschlüsselt, wobei die Advanced Encryption Standard (AES) und eine AES-Schlüsselgröße von 256 Bits verwendet werden. Diese Methode ist nur auf Geräten verfügbar, auf denen Windows 10, Version 1511 oder höher, ausgeführt wird.<br/>                          |
| <dl> <dt>(UInt32) – 1</dt> </dl>                                                                                                                                                          | UNBEKANNT<br/> Das Volume wurde vollständig oder teilweise mit einem unbekannten Algorithmus und Schlüsselgröße verschlüsselt.<br/>                                                                                                                                            |



 

</dd> <dt>

*Selfencryptiondriveverschlüsseltionmethod* \[ vorgenommen\]
</dt> <dd>

Typ: **Zeichenfolge**

Der Verschlüsselungsalgorithmus wird auf dem selbst verschlüsselnden Laufwerk konfiguriert. Eine NULL-Zeichenfolge bedeutet, dass entweder BitLocker Software Verschlüsselung verwendet oder keine Verschlüsselungsmethode gemeldet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                 | BESCHREIBUNG                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Die Methode war erfolgreich.<br/> |



 

## <a name="remarks"></a>Bemerkungen

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

 

 
