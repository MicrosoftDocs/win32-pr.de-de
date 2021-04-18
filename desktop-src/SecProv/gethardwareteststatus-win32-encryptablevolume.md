---
description: Stellt Statusinformationen zu einem Hardware Test eines vollständig entschlüsselten Betriebssystem Volumes bereit.
ms.assetid: d76bc266-3718-443e-94f9-dcaa0ec53151
title: Gethardwareteststatus-Methode der Win32_EncryptableVolume-Klasse
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
ms.openlocfilehash: 26d1984a79edef5f00f7687260fda7b211153863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350810"
---
# <a name="gethardwareteststatus-method-of-the-win32_encryptablevolume-class"></a>Gethardwareteststatus-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **gethardwareteststatus** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " stellt Statusinformationen über einen Hardware Test eines vollständig entschlüsselten Betriebssystem Volumes bereit.

Verwenden Sie diese Methode, um anzuzeigen, ob ein Hardware Test aussteht, sowie den Erfolg oder Misserfolg eines Hardware Tests, der beim letzten Neustart des Computers abgeschlossen wurde. Verwenden Sie die Methode " [**verschlüsseltafterhardwaretest**](encryptafterhardwaretest-win32-encryptablevolume.md) ", um einen Hardware Test anzufordern.

## <a name="syntax"></a>Syntax


```mof
uint32 GetHardwareTestStatus(
  [out] uint32 TestStatus,
  [out] uint32 TestError
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Teststatus* \[ vorgenommen\]
</dt> <dd>

Typ: **UInt32**

Gibt an, ob ein Hardware Test aussteht, sowie den Erfolg eines Fehlers eines Hardware Tests, der beim letzten Neustart des Computers abgeschlossen wurde.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Wert</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="NotFailed_and_NonePending"></span><span id="notfailed_and_nonepending"></span><span id="NOTFAILED_AND_NONEPENDING"></span><dl> <dt><strong>NotFailed_and_NonePending</strong></dt> <dt>0</dt> </dl></td>
<td>Wenn ein Test angefordert wurde, war der Test beim letzten Neustart des Computers erfolgreich, und die Volumeverschlüsselung wird jetzt ausgeführt. Den Verschlüsselungs Status finden Sie unter der <a href="getconversionstatus-win32-encryptablevolume.md"><strong>getkonversionstatus</strong></a> -Methode. Andernfalls wurde kein Test auf dem letzten Computer Neustart ausgeführt, und es ist kein ausstehend. <br/></td>
</tr>
<tr class="even">
<td><span id="Failed"></span><span id="failed"></span><span id="FAILED"></span><dl> <dt><strong></strong></dt> Fehler <dt>1</dt> </dl></td>
<td>Die Volumeverschlüsselung konnte nicht gestartet werden. Alle Schlüssel Schutzvorrichtungen wurden entfernt.<br/> So beheben Sie einen fehlgeschlagenen Test:<br/>
<ul>
<li>Überprüfen Sie die Informationen im <em>testerror</em> -Parameter.</li>
<li>Fügen Sie Schlüssel Schutzvorrichtungen hinzu, und verwenden Sie die Methode " <a href="encryptafterhardwaretest-win32-encryptablevolume.md"><strong>verschlüsseltafterhardwaretest</strong></a> " erneut.</li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="Pending"></span><span id="pending"></span><span id="PENDING"></span><dl> <dt><strong>Ausstehende</strong></dt> <dt>2</dt> </dl></td>
<td>Ein Test wurde angefordert und wird beim nächsten Neustart des Computers ausgeführt.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

" *Testerror* \[ " vorgenommen\]
</dt> <dd>

Typ: **UInt32**

Gibt den Fehler des letzten abgeschlossenen Hardware Tests an.



| Wert                                                                                               | Bedeutung                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>                        | Es sind keine Fehler aufgetreten, oder es wurde kein Hardware Test auf dem letzten Neustart des Computers ausgeführt.<br/>                                                                                                                                                                                                                                                                      |
| <dl> <dt> 2150694972 (0x8031003c)</dt> </dl> | f- \_ E- \_ KeyFile \_ nicht \_ gefunden<br/> Ein USB-Speicherstick mit einer externen Schlüsseldatei wurde nicht gefunden. Wenn dieser Fehler weiterhin auftritt, kann der Computer während des Neustarts keine USB-Laufwerke lesen. Möglicherweise können Sie externe Schlüssel nicht verwenden, um das Betriebssystem Volume während des Neustarts zu entsperren.<br/>                                                                |
| <dl> <dt> 2150694973 (0x8031003d)</dt> </dl> | \_ \_ ungültige E-Key-Datei \_<br/> Die externe Schlüsseldatei auf dem USB-Speicherstick war beschädigt. Probieren Sie einen anderen USB-Speicherstick zum Speichern der externen Schlüsseldatei aus.<br/>                                                                                                                                                                                 |
| <dl> <dt> 2150694975 (0x8031003f)</dt> </dl> | \_E \_ TPM \_ deaktiviert<br/> Das TPM ist entweder deaktiviert oder deaktiviert oder deaktiviert und deaktiviert. Um das TPM zu aktivieren, verwenden Sie den [**Win32- \_ TPM**](win32-tpm.md) -WMI-Anbieter, oder führen Sie das TPM-Verwaltungs-Snap-in (TPM. msc) aus.<br/>                                                                                                            |
| <dl> <dt> 2150694977 (0x80310041)</dt> </dl> | \_ \_ ungültige E TPM-Datei \_ \_<br/> Das TPM hat eine Änderung der Neustart Dienste des Betriebssystems im aktuellen Platt Form Validierungs Profil festgestellt. Entfernen Sie eine beliebige Start-CD oder DVD vom Computer. Wenn dieser Fehler weiterhin auftritt, überprüfen Sie, ob die neuesten Firmware-und BIOS-Upgrades installiert sind und ob das TPM andernfalls ordnungsgemäß funktioniert.<br/> |
| <dl> <dt>2150694979 (0x80310043)</dt> </dl>  | \_ \_ ungültige E-Pin \_<br/> Die angegebene PIN war falsch.<br/>                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

In der folgenden Tabelle sind einige der allgemeinen Rückgabecodes aufgeführt.



| Rückgabecode/-wert                                                                                                                                                                  | BESCHREIBUNG                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Die Methode wurde erfolgreich ausgeführt.<br/> |
| <dl> <dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | Das Volume ist gesperrt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die Methode " [**verschlüsseltafterhardwaretest**](encryptafterhardwaretest-win32-encryptablevolume.md) ", um einen Hardware Test anzufordern.

Führen Sie die folgenden Schritte aus, um einen Hardware Test auszuführen, wenn der Status "Ausstehend" lautet:

1.  Fügen Sie einen USB-Speicherstick, der eine externe Schlüsseldatei enthält, in den Computer ein. Dieser Schritt gilt nur, wenn das Volume über eine Schlüssel Schutzvorrichtung vom Typ "externer Schlüssel" oder "TPM und Systemstart Schlüssel" verfügt.
2.  Starten Sie den Computer neu. Beim Neustart des Computers wird der Hardware Test automatisch ausgeführt.

Verwenden Sie die Methode [**verschlüsseln**](encrypt-win32-encryptablevolume.md) , um den Hardware Test abzubrechen.

Ein erfolgreicher Test bestimmt Folgendes:

-   Das TPM kann das Volume entsperren, wenn eine TPM-bezogene Schlüssel Schutzvorrichtung vorhanden ist.
-   Der Computer kann einen USB-Speicherstick lesen, der eine externe Schlüsseldatei während des Starts enthält, wenn das Volume durch einen externen Schlüssel (einschließlich eines Systemstart Schlüssels) entsperrt werden kann.

Die Hardware Testergebnisse sind nach Änderungen an der Konvertierung oder nach dem nächsten Computer Neustart nicht verfügbar. Überprüfen Sie das System Ereignisprotokoll auf die Informationen zu Hardware Tests, die zuvor auf dem Computer ausgeführt wurden.

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

 

 
