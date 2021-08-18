---
description: Gibt den Status der Verschlüsselung oder Entschlüsselung auf dem Volume an.
ms.assetid: b292a380-1b4a-4dff-948b-6494ec3b400b
title: GetConversionStatus-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetConversionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: a93e52e0df7f4ab3fdc4c4686ee05e9c1bc9c2c3082604d922da56bc57cb94f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004482"
---
# <a name="getconversionstatus-method-of-the-win32_encryptablevolume-class"></a>GetConversionStatus-Methode der Win32 \_ EncryptableVolume-Klasse

Die **GetConversionStatus-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) gibt den Status der Verschlüsselung oder Entschlüsselung auf dem Volume an.

## <a name="syntax"></a>Syntax


```mof
uint32 GetConversionStatus(
  [out] uint32 ConversionStatus,
  [out] uint32 EncryptionPercentage,
  [out] uint32 EncryptionFlags,
  [out] uint32 WipingStatus,
  [out] uint32 WipingPercentage,
  [in]  uint32 PrecisionFactor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ConversionStatus* \[ out\]
</dt> <dd>

Typ: **uint32**

Status der Volumeverschlüsselung oder -entschlüsselung. Dies kann einer der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                                                           | Bedeutung                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FullyDecrypted"></span><span id="fullydecrypted"></span><span id="FULLYDECRYPTED"></span><dl> <dt>**FullyDecrypted**</dt> <dt>0</dt> </dl>                         | Bei einer Standard-Festplatte (HDD) ist das Volume vollständig entschlüsselt.<br/> Für eine hardware verschlüsselte Festplatte (Hard Encrypted Hard Drive, EHDD) wird das Volume unbefristet entsperrt.<br/>     |
| <span id="FullyEncrypted"></span><span id="fullyencrypted"></span><span id="FULLYENCRYPTED"></span><dl> <dt>**FullyEncrypted**</dt> <dt>1</dt> </dl>                         | Bei einer Standard-Festplatte (HDD) ist das Volume vollständig verschlüsselt.<br/> Für eine hardware verschlüsselte Festplatte (Hard Encrypted Hard Drive, EHDD) wird das Volume nicht unbefristet entsperrt.<br/> |
| <span id="EncryptionInProgress"></span><span id="encryptioninprogress"></span><span id="ENCRYPTIONINPROGRESS"></span><dl> <dt>**EncryptionInProgress**</dt> <dt>2</dt> </dl> | Das Volume ist teilweise verschlüsselt.<br/>                                                                                                                             |
| <span id="DecryptionInProgress"></span><span id="decryptioninprogress"></span><span id="DECRYPTIONINPROGRESS"></span><dl> <dt>**DecryptionInProgress**</dt> <dt>3</dt> </dl> | Das Volume ist teilweise verschlüsselt.<br/>                                                                                                                             |
| <span id="EncryptionPaused"></span><span id="encryptionpaused"></span><span id="ENCRYPTIONPAUSED"></span><dl> <dt>**EncryptionPaused**</dt> <dt>4</dt> </dl>                 | Das Volume wurde während des Verschlüsselungsfortschritts angehalten. Das Volume ist teilweise verschlüsselt.<br/>                                                                  |
| <span id="DecryptionPaused"></span><span id="decryptionpaused"></span><span id="DECRYPTIONPAUSED"></span><dl> <dt>**DecryptionPaused**</dt> <dt>5</dt> </dl>                 | Das Volume wurde während des Entschlüsselungsfortschritts angehalten. Das Volume ist teilweise verschlüsselt.<br/>                                                                  |



 

</dd> <dt>

*EncryptionPercentage* \[ out\]
</dt> <dd>

Typ: **uint32**

Prozentsatz des verschlüsselten Volumes. Dies ist eine ganze Zahl von 0 bis einschließlich 100.

Aufgrund der Rundung von Zahlen gibt ein Verschlüsselungsprozentsatz von 0 oder 100 nicht notwendigerweise an, dass der Datenträger vollständig entschlüsselt oder vollständig verschlüsselt ist. Verwenden Sie *conversionStatus immer,* um zu bestimmen, ob der Datenträger tatsächlich vollständig entschlüsselt oder vollständig verschlüsselt ist.

</dd> <dt>

*EncryptionFlags* \[ out\]
</dt> <dd>

Typ: **uint32**

Flags, die das Verschlüsselungsverhalten beschreiben.

Eine Kombination aus 32 Bits und den folgenden derzeit definierten Bits.



| Wert                                                                                  | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000001</dt> </dl>  | Führen Sie die Volumeverschlüsselung im Datenverschlüsselungsmodus aus, wenn Sie einen neuen Verschlüsselungsprozess starten. Wenn die Verschlüsselung angehalten oder beendet wurde, wird die Konvertierung durch Aufrufen der [**Encrypt-Methode**](encrypt-win32-encryptablevolume.md) effektiv fortgesetzt, und der Wert dieses Bit wird ignoriert. Dieses Bit hat nur Dann Auswirkungen, wenn die **Encrypt-** oder [**EncryptAfterHardwareTest-Methode**](encryptafterhardwaretest-win32-encryptablevolume.md) die Verschlüsselung vom vollständig entschlüsselten Zustand, der Entschlüsselung im Status "Wird durchgeführt" oder dem angehaltenen Entschlüsselungszustand aus startet. Wenn dieses Bit 0 (null) ist, was bedeutet, dass es nicht festgelegt ist, wird beim Starten eines neuen Verschlüsselungsprozesses die Konvertierung im vollständigen Modus durchgeführt.<br/> |
| <dl> <dt>0x00000002</dt> </dl>  | Führen Sie eine bedarfsbasierte Zurücksetzung des freien Speicherplatzes auf dem Volume durch. Das Aufrufen [**der Encrypt-Methode**](encrypt-win32-encryptablevolume.md) mit diesem Bitsatz ist nur zulässig, wenn das Volume derzeit nicht konvertiert oder zurückf wird und sich in einem "verschlüsselten" Zustand befindet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>0x00010000 </dt> </dl> | Führen Sie den angeforderten Vorgang synchron aus. Der Aufruf wird blockiert, bis der angeforderte Vorgang abgeschlossen oder unterbrochen wurde. Dieses Flag wird nur mit der [**Encrypt-Methode**](encrypt-win32-encryptablevolume.md) unterstützt. Dieses Flag kann angegeben werden, wenn **Encrypt** aufgerufen wird, um die beendete oder unterbrochene Verschlüsselung oder das Zurückschneiden fort aufzunehmen, oder wenn die Verschlüsselung oder das Zurückschneiden in Bearbeitung ist. Dadurch kann der Aufrufer synchron warten, bis der Prozess abgeschlossen oder unterbrochen wird.<br/>                                                                                                                                                                                  |



 

</dd> <dt>

*WipingStatus* \[ out\]
</dt> <dd>

Typ: **uint32**

Der Status des freien Speicherplatzes wird zurückdringt. Dies kann einer der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                                                                               | Bedeutung                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="FreeSpaceNotWiped"></span><span id="freespacenotwiped"></span><span id="FREESPACENOTWIPED"></span><dl> <dt>**FreeSpaceNotWiped**</dt> <dt>0</dt> </dl>                                 | Der freie Speicherplatz wurde nicht zurückgelöscht.<br/>          |
| <span id="FreeSpaceWiped"></span><span id="freespacewiped"></span><span id="FREESPACEWIPED"></span><dl> <dt>**FreeSpaceWiped**</dt> <dt>1</dt> </dl>                                             | Der freie Speicherplatz wurde zurückgelöscht.<br/>              |
| <span id="FreeSpaceWipingInProgress"></span><span id="freespacewipinginprogress"></span><span id="FREESPACEWIPINGINPROGRESS"></span><dl> <dt>**FreeSpaceWipingInProgress**</dt> <dt>2</dt> </dl> | Das Beschneiden des freien Speicherplatzes wird derzeit in Bearbeitung.<br/> |
| <span id="FreeSpaceWipingPaused"></span><span id="freespacewipingpaused"></span><span id="FREESPACEWIPINGPAUSED"></span><dl> <dt>**FreeSpaceWipingPaused**</dt> <dt>3</dt> </dl>                 | Das Beschneiden des freien Speicherplatzes wurde angehalten.<br/>          |



 

</dd> <dt>

*WipingPercentage* \[ out\]
</dt> <dd>

Typ: **uint32**

Ein Wert zwischen 0 und 100, der den Prozentsatz des freien Speicherplatzes angibt, der zurückgelöscht wurde.

</dd> <dt>

*PrecisionFactor* \[ In\]
</dt> <dd>

Typ: **uint32**

Ein Wert zwischen 0 und 4, der die Genauigkeitsstufe angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                  | BESCHREIBUNG                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Die Methode war erfolgreich.<br/> |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | Das Volume ist gesperrt.<br/>      |



 

## <a name="remarks"></a>Hinweise

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

 

 
