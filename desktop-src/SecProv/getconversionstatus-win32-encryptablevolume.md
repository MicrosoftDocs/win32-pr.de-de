---
description: Gibt den Status der Verschlüsselung oder Entschlüsselung auf dem Volume an.
ms.assetid: b292a380-1b4a-4dff-948b-6494ec3b400b
title: Getkonversionstatus-Methode der Win32_EncryptableVolume-Klasse
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
ms.openlocfilehash: 9357db3397b04639329c1afd502d9da30cbb39be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862291"
---
# <a name="getconversionstatus-method-of-the-win32_encryptablevolume-class"></a>Getkonversionstatus-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **getkonversionstatus** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " gibt den Status der Verschlüsselung oder Entschlüsselung auf dem Volume an.

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

Configuration Manager- *Status* \[ vorgenommen\]
</dt> <dd>

Typ: **UInt32**

Volumeverschlüsselungs-oder Entschlüsselungs Status. Dies kann einer der folgenden Werte sein:



| Wert                                                                                                                                                                                                                                                                           | Bedeutung                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FullyDecrypted"></span><span id="fullydecrypted"></span><span id="FULLYDECRYPTED"></span><dl> <dt>**Fullydecrypted**</dt> <dt>0</dt> </dl>                         | Bei einer Standard Festplatte (HDD) wird das Volume vollständig entschlüsselt.<br/> Für eine Hardware verschlüsselte Festplatte (ehdd) wird das Volume dauerhaft entsperrt.<br/>     |
| <span id="FullyEncrypted"></span><span id="fullyencrypted"></span><span id="FULLYENCRYPTED"></span><dl> <dt>**Fullyverschlüsselt**</dt> <dt>1</dt> </dl>                         | Für eine Standard Festplatte (HDD) ist das Volume vollständig verschlüsselt.<br/> Für eine Hardware verschlüsselte Festplatte (ehdd) wird das Volume nicht dauerhaft entsperrt.<br/> |
| <span id="EncryptionInProgress"></span><span id="encryptioninprogress"></span><span id="ENCRYPTIONINPROGRESS"></span><dl> <dt>**Verschlüsselungsinprogress**</dt> <dt>2</dt> </dl> | Das Volume ist teilweise verschlüsselt.<br/>                                                                                                                             |
| <span id="DecryptionInProgress"></span><span id="decryptioninprogress"></span><span id="DECRYPTIONINPROGRESS"></span><dl> <dt>**Decryptioninprogress**</dt> <dt>3</dt> </dl> | Das Volume ist teilweise verschlüsselt.<br/>                                                                                                                             |
| <span id="EncryptionPaused"></span><span id="encryptionpaused"></span><span id="ENCRYPTIONPAUSED"></span><dl> <dt>**Verschlüsselter angehaltene**</dt> <dt>4</dt> </dl>                 | Das Volume wurde während des Verschlüsselungs Fortschritts angehalten. Das Volume ist teilweise verschlüsselt.<br/>                                                                  |
| <span id="DecryptionPaused"></span><span id="decryptionpaused"></span><span id="DECRYPTIONPAUSED"></span><dl> <dt>**Entschlüsselte**</dt> Ausführung <dt>5</dt> </dl>                 | Das Volume wurde während des Entschlüsselungs Fortschritts angehalten. Das Volume ist teilweise verschlüsselt.<br/>                                                                  |



 

</dd> <dt>

*Verschlüsselungs Prozentsatz* \[ vorgenommen\]
</dt> <dd>

Typ: **UInt32**

Prozentsatz des verschlüsselten Volumes. Dies ist eine ganze Zahl zwischen 0 und 100 einschließlich.

Aufgrund der Rundung von Zahlen weist der Verschlüsselungs Prozentsatz 0 oder 100 nicht notwendigerweise darauf hin, dass der Datenträger vollständig entschlüsselt oder vollständig verschlüsselt ist. Verwenden Sie immer "Configuration Manager *Status* ", um zu bestimmen, ob der Datenträger tatsächlich vollständig entschlüsselt oder vollständig verschlüsselt ist.

</dd> <dt>

*Verschlüsselungsflags* \[ vorgenommen\]
</dt> <dd>

Typ: **UInt32**

Flags, die das Verschlüsselungs Verhalten beschreiben.

Eine Kombination von 32 Bits mit folgenden Bits, die aktuell definiert sind.



| Wert                                                                                  | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000001</dt> </dl>  | Führen Sie die Volumeverschlüsselung im reinen Daten Verschlüsselungs Modus aus, wenn Sie den neuen Verschlüsselungsprozess starten. Wenn die Verschlüsselung angehalten oder beendet wurde, wird die Konvertierung durch Aufrufen der Methode " [**verschlüsseln**](encrypt-win32-encryptablevolume.md) " wirksam fortgesetzt, und der Wert dieses Bits wird ignoriert. Dieses Bit ist nur wirksam, wenn die Verschlüsselungs-oder [**verschlüsseltafterhardwaretest**](encryptafterhardwaretest-win32-encryptablevolume.md) - **Methoden die Verschlüsselung** aus dem vollständig entschlüsselten Zustand, dem Entschlüsselungs Status oder dem Status der entschlüsselten Entschlüsselung starten. Wenn dieses Bit 0 (null) ist, was bedeutet, dass es beim Starten des neuen Verschlüsselungs Vorgangs nicht festgelegt ist, wird die vollständige Modus-Konvertierung ausgeführt.<br/> |
| <dl> <dt>0x00000002</dt> </dl>  | Ausführen einer bedarfsgesteuerten Löschung des freien Speicherplatzes auf dem Volume. Das Aufrufen der [**Verschlüsselungs**](encrypt-win32-encryptablevolume.md) Methode mit diesem Bitset ist nur zulässig, wenn das Volume derzeit nicht in den Status "verschlüsselt" versetzt wird und sich im Status "verschlüsselt" befindet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>0x00010000 bis </dt> </dl> | Führt den angeforderten Vorgang synchron aus. Der-Befehl wird blockiert, bis der angeforderte Vorgang abgeschlossen ist oder unterbrochen wurde. Dieses Flag wird nur mit der Methode " [**verschlüsseln**](encrypt-win32-encryptablevolume.md) " unterstützt. Dieses Flag kann angegeben werden, wenn " **verschlüsseln** " aufgerufen wird, um die beendete oder unterbrochene Verschlüsselung oder das Zurücksetzen oder Löschen von Verschlüsselung oder Zurücksetzen zu beenden. Dies ermöglicht dem Aufrufer, synchron zu warten, bis der Prozess abgeschlossen oder unterbrochen wird.<br/>                                                                                                                                                                                  |



 

</dd> <dt>

*Wipingstatus* \[ vorgenommen\]
</dt> <dd>

Typ: **UInt32**

Status der Freigabe für freien Speicherplatz. Dies kann einer der folgenden Werte sein:



| Wert                                                                                                                                                                                                                                                                                               | Bedeutung                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="FreeSpaceNotWiped"></span><span id="freespacenotwiped"></span><span id="FREESPACENOTWIPED"></span><dl> <dt>**Freespacenotgelöschte**</dt> <dt>0</dt> </dl>                                 | Der freie Speicherplatz wurde nicht zurückgesetzt.<br/>          |
| <span id="FreeSpaceWiped"></span><span id="freespacewiped"></span><span id="FREESPACEWIPED"></span><dl> <dt>**Freespacewipt**</dt> <dt>1</dt> </dl>                                             | Der freie Speicherplatz wurde zurückgesetzt.<br/>              |
| <span id="FreeSpaceWipingInProgress"></span><span id="freespacewipinginprogress"></span><span id="FREESPACEWIPINGINPROGRESS"></span><dl> <dt>**Freespacewipinginprogress**</dt> <dt>2</dt> </dl> | Der freie Speicherplatz wird zurzeit ausgeführt.<br/> |
| <span id="FreeSpaceWipingPaused"></span><span id="freespacewipingpaused"></span><span id="FREESPACEWIPINGPAUSED"></span><dl> <dt>**Freespacewipingangeh**</dt> alten <dt>3</dt> </dl>                 | Der freie Speicherplatz wurde angehalten.<br/>          |



 

</dd> <dt>

*Wipingprozentsatz* \[ vorgenommen\]
</dt> <dd>

Typ: **UInt32**

Ein Wert zwischen 0 und 100, der den Prozentsatz des freien Speicherplatzes angibt, der zurückgesetzt wurde.

</dd> <dt>

*Precisionfactor* \[ in\]
</dt> <dd>

Typ: **UInt32**

Ein Wert zwischen 0 und 4, der die Genauigkeits Ebene angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                  | BESCHREIBUNG                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Die Methode war erfolgreich.<br/> |
| <dl> <dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | Das Volume ist gesperrt.<br/>      |



 

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

 

 
