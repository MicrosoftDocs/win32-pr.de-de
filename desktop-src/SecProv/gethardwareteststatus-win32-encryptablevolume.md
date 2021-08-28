---
description: Stellt Statusinformationen zu einem Hardwaretest eines vollständig entschlüsselten Betriebssystemvolumes bereit.
ms.assetid: d76bc266-3718-443e-94f9-dcaa0ec53151
title: GetHardwareTestStatus-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetHardwareTestStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 32d0d477459dbc7352d1d8f6779c5c76cfbd537d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475356"
---
# <a name="gethardwareteststatus-method-of-the-win32_encryptablevolume-class"></a>GetHardwareTestStatus-Methode der Win32 \_ EncryptableVolume-Klasse

Die **GetHardwareTestStatus-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) stellt Statusinformationen zu einem Hardwaretest eines vollständig entschlüsselten Betriebssystemvolumes bereit.

Verwenden Sie diese Methode, um anzuzeigen, ob ein Hardwaretest aussteht, sowie den Erfolg oder Fehler eines Hardwaretests, der beim letzten Neustart des Computers abgeschlossen wurde. Um einen Hardwaretest anzufordern, verwenden Sie die [**EncryptAfterHardwareTest-Methode.**](encryptafterhardwaretest-win32-encryptablevolume.md)

## <a name="syntax"></a>Syntax


```mof
uint32 GetHardwareTestStatus(
  [out] uint32 TestStatus,
  [out] uint32 TestError
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*TestStatus* \[ out\]
</dt> <dd>

Typ: **uint32**

Gibt an, ob ein Hardwaretest aussteht, sowie der Erfolg eines Hardwaretests, der beim letzten Neustart des Computers abgeschlossen wurde.




| Wert | Bedeutung | 
|-------|---------|
| <span id="NotFailed_and_NonePending"></span><span id="notfailed_and_nonepending"></span><span id="NOTFAILED_AND_NONEPENDING"></span><dl><dt><strong>NotFailed_and_NonePending</strong></dt><dt>0</dt></dl> | Wenn ein Test angefordert wurde, war der Test beim letzten Neustart des Computers erfolgreich, und die Volumeverschlüsselung wird jetzt ausgeführt. Informationen zum Verschlüsselungsstatus finden Sie in der <a href="getconversionstatus-win32-encryptablevolume.md"><strong>GetConversionStatus-Methode.</strong></a> Andernfalls wurde kein Test auf dem letzten Computerneustart ausgeführt, und keiner steht aus. <br /> | 
| <span id="Failed"></span><span id="failed"></span><span id="FAILED"></span><dl><dt><strong>Fehler</strong></dt><dt>1</dt></dl> | Die Volumeverschlüsselung wurde nicht gestartet. Alle Schlüsselschutzvorrichtungen wurden entfernt.<br /> So beheben Sie einen fehlgeschlagenen Test:<br /><ul><li>Lesen Sie die Informationen im <em>TestError-Parameter.</em></li><li>Fügen Sie Schlüsselschutzvorrichtungen hinzu, und verwenden Sie erneut die <a href="encryptafterhardwaretest-win32-encryptablevolume.md"><strong>EncryptAfterHardwareTest-Methode.</strong></a></li></ul> | 
| <span id="Pending"></span><span id="pending"></span><span id="PENDING"></span><dl><dt><strong>Ausstehend</strong></dt><dt>2</dt></dl> | Ein Test wurde angefordert und wird auf dem nächsten Computerneustart ausgeführt.<br /> | 




 

</dd> <dt>

*TestError* \[ out\]
</dt> <dd>

Typ: **uint32**

Gibt den Fehler aus dem letzten abgeschlossenen Hardwaretest an.



| Wert                                                                                               | Bedeutung                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>                        | Beim letzten Neustart des Computers sind keine Fehler aufgetreten oder es wurde kein Hardwaretest ausgeführt.<br/>                                                                                                                                                                                                                                                                      |
| <dl> <dt> 2150694972 (0x8031003C)</dt> </dl> | FVE \_ E \_ KEYFILE NICHT \_ \_ GEFUNDEN<br/> Ein USB-Speicherstick mit einer externen Schlüsseldatei wurde nicht gefunden. Wenn dieser Fehler weiterhin auftritt, kann der Computer während des Neustarts keine USB-Laufwerke lesen. Möglicherweise können Sie während des Neustarts keine externen Schlüssel verwenden, um das Betriebssystemvolume zu entsperren.<br/>                                                                |
| <dl> <dt> 2150694973 (0x8031003D)</dt> </dl> | FVE \_ E \_ KEYFILE \_ UNGÜLTIG<br/> Die externe Schlüsseldatei auf dem USB-Speicherstick war beschädigt. Probieren Sie einen anderen USB-Speicherstick aus, um die externe Schlüsseldatei zu speichern.<br/>                                                                                                                                                                                 |
| <dl> <dt> 2150694975 (0x8031003F)</dt> </dl> | FVE \_ E \_ TPM \_ DEAKTIVIERT<br/> Das TPM ist entweder deaktiviert oder deaktiviert oder sowohl deaktiviert als auch deaktiviert. Um das TPM zu aktivieren, verwenden Sie den [**Win32 \_ Tpm**](win32-tpm.md) WMI-Anbieter, oder führen Sie das TPM-Verwaltungs-Snap-In (Tpm.msc) aus.<br/>                                                                                                            |
| <dl> <dt> 2150694977 (0x80310041)</dt> </dl> | FVE \_ E \_ TPM \_ INVALID \_ PCR<br/> Das TPM hat eine Änderung der Neustartdienste des Betriebssystems innerhalb des aktuellen Plattformvalidierungsprofils erkannt. Entfernen Sie alle Start-CD- oder DVD-Dateien vom Computer. Wenn dieser Fehler weiterhin auftritt, überprüfen Sie, ob die neuesten Firmware- und BIOS-Upgrades installiert sind und dass das TPM andernfalls ordnungsgemäß funktioniert.<br/> |
| <dl> <dt>2150694979 (0x80310043)</dt> </dl>  | FVE \_ E \_ PIN \_ UNGÜLTIG<br/> Die angegebene PIN war falsch.<br/>                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

In der folgenden Tabelle sind einige der allgemeinen Rückgabecodes aufgeführt.



| Rückgabecode/-wert                                                                                                                                                                  | BESCHREIBUNG                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Die Methode wurde erfolgreich ausgeführt.<br/> |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | Das Volume ist gesperrt.<br/> |



 

## <a name="remarks"></a>Hinweise

Um einen Hardwaretest anzufordern, verwenden Sie die [**EncryptAfterHardwareTest-Methode.**](encryptafterhardwaretest-win32-encryptablevolume.md)

Führen Sie die folgenden Schritte aus, um einen Hardwaretest auszuführen, wenn sein Status aussteht:

1.  Fügen Sie auf dem Computer einen USB-Speicherstick ein, der eine externe Schlüsseldatei enthält. Dieser Schritt gilt nur, wenn das Volume über eine Schlüsselschutzvorrichtung vom Typ "Externer Schlüssel" oder "TPM und Startschlüssel" verfügt.
2.  Starten Sie den Computer neu. Beim Neustart des Computers wird der Hardwaretest automatisch ausgeführt.

Um den Hardwaretest abzubrechen, verwenden Sie die [**Encrypt-Methode.**](encrypt-win32-encryptablevolume.md)

Bei einem erfolgreichen Test wird Festgestellt, dass:

-   Das TPM kann das Volume entsperren, wenn eine TPM-bezogene Schlüsselschutzvorrichtung vorhanden ist.
-   Der Computer kann während des Starts einen USB-Speicherstick lesen, der eine externe Schlüsseldatei enthält, wenn das Volume durch einen externen Schlüssel (einschließlich eines Startschlüssels) entsperrt werden kann.

Hardwaretestergebnisse sind nach Änderungen bei der Konvertierung oder nach dem nächsten Neustart des Computers nicht verfügbar. Überprüfen Sie das Systemereignisprotokoll auf Informationen zu Hardwaretests, die zuvor auf dem Computer ausgeführt wurden.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

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

 

 
