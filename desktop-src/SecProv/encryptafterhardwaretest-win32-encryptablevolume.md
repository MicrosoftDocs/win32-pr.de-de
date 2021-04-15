---
description: Startet die Verschlüsselung eines vollständig entschlüsselten Betriebssystem Volume nach einem Hardware Test.
ms.assetid: 216c96bb-7737-4421-8b16-1ce295342266
title: Verschlüsseltashardwaretest-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EncryptAfterHardwareTest
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f356b9adda5e1b25fdd3d9fc39ace5cf8028da32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525688"
---
# <a name="encryptafterhardwaretest-method-of-the-win32_encryptablevolume-class"></a>Verschlüsseltaberterhardwaretest-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **verschlüsseltafterhardwaretest** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " beginnt nach einem Hardware Test mit der Verschlüsselung eines vollständig entschlüsselten Betriebssystem Volume. Zum Durchführen dieses Hardware Tests ist ein Neustart erforderlich. Verwenden Sie diese Methode anstelle der Methode " [**verschlüsseln**](encrypt-win32-encryptablevolume.md) ", um zu überprüfen, ob BitLocker erwartungsgemäß funktioniert.

> [!Note]  
> Wenn die Festplatte Hardware verschlüsselt ist, werden die Daten von dieser Methode nicht verschlüsselt. Stattdessen wird der Band Status von "dauerhaft entsperrt" auf "entsperrt" festgelegt. Wenn das Band gesperrt ist, entsperrt oder schreibgeschützt ist, wird das Laufwerk als verschlüsselt eingestuft.

 

## <a name="syntax"></a>Syntax


```mof
uint32 EncryptAfterHardwareTest(
  [in, optional] uint32 EncryptionMethod,
  [in, optional] uint32 EncryptionFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Verschlüsselungsmethode* \[ in, optional\]
</dt> <dd>

Typ: **UInt32**

Gibt den Verschlüsselungsalgorithmus und die Schlüsselgröße an, die zum Verschlüsseln des Volumes verwendet werden. Lassen Sie diesen Parameter leer, um den Standardwert 0 (null) zu verwenden. Wenn das Volume teilweise oder vollständig verschlüsselt ist, muss der Wert dieses Parameters 0 sein oder mit der vorhandenen Verschlüsselungsmethode des Volumes identisch sein. Wenn die entsprechende Gruppenrichtlinie Einstellung mit einem gültigen Wert aktiviert wurde, muss der Wert dieses Parameters 0 sein oder mit der Gruppenrichtlinie Einstellung übereinstimmen.

Wenn die entsprechende Gruppenrichtlinie Einstellung ungültig ist, wird der Standardwert von AES 128 mit Diffuser verwendet.



| Wert                                                                                                                                                                                                                                       | Bedeutung                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span><dl> <dt>**Nicht angegeben**</dt> <dt>0</dt> </dl> | Verwenden Sie die aktuelle Gruppenrichtlinie Einstellung, falls verfügbar und gültig, oder andernfalls die Standard Verschlüsselungsmethode.<br/>                                                                              |
| <dl> <dt>1</dt> </dl>                                                                                                                                                                | AES 128 mit diffuser<br/> Verschlüsseln Sie das Volume mit dem Advanced Encryption Standard (AES)-Algorithmus, der mit einer diffuser-Schicht erweitert wurde, und verwenden Sie eine AES-Schlüsselgröße von 128 Bits.<br/> |
| <dl> <dt>2</dt> </dl>                                                                                                                                                                | AES 256 mit diffuser<br/> Verschlüsseln Sie das Volume mit dem Advanced Encryption Standard (AES)-Algorithmus, der mit einer diffuser-Schicht erweitert wurde, und verwenden Sie eine AES-Schlüsselgröße von 256 Bits.<br/> |
| <span id="AES_128"></span><span id="aes_128"></span><dl> <dt>**AES \_ 128**</dt> <dt>3</dt> </dl>                                          | Verschlüsseln Sie das Volume mit dem Advanced Encryption Standard-Algorithmus (AES) und mit einer AES-Schlüsselgröße von 128 Bits.<br/>                                                                 |
| <span id="AES_256"></span><span id="aes_256"></span><dl> <dt>**AES \_ 256**</dt> <dt>4</dt> </dl>                                          | Verschlüsseln Sie das Volume mit dem Advanced Encryption Standard-Algorithmus (AES) und mit einer AES-Schlüsselgröße von 256 Bits.<br/>                                                                 |



 

</dd> <dt>

*Verschlüsselungsflags* \[ in, optional\]
</dt> <dd>

Typ: **UInt32**

Flags, die das Verschlüsselungs Verhalten beschreiben.

**Windows 7, Windows Server 2008 R2, Windows Vista Enterprise und Windows Server 2008:** Dieser Parameter ist nicht verfügbar.

Eine Kombination von 32 Bits mit den folgenden Bits, die aktuell definiert sind.



| Wert                                                                                  | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000001</dt> </dl>  | Führen Sie die Volumeverschlüsselung im reinen Daten Verschlüsselungs Modus aus, wenn Sie den neuen Verschlüsselungsprozess starten. Wenn die Verschlüsselung angehalten oder beendet wurde, wird die Konvertierung durch Aufrufen der Methode " [**verschlüsseln**](encrypt-win32-encryptablevolume.md) " wirksam fortgesetzt, und der Wert dieses Bits wird ignoriert. Dieses Bit ist nur wirksam, wenn die Verschlüsselungs-oder **verschlüsseltafterhardwaretest** - **Methoden die Verschlüsselung** aus dem vollständig entschlüsselten Zustand, dem Entschlüsselungs Status oder dem Status der entschlüsselten Entschlüsselung starten. Wenn dieses Bit 0 (null) ist, was bedeutet, dass es beim Starten des neuen Verschlüsselungs Vorgangs nicht festgelegt ist, wird die vollständige Modus-Konvertierung ausgeführt.<br/> |
| <dl> <dt>0x00000002</dt> </dl>  | Ausführen einer bedarfsgesteuerten Löschung des freien Speicherplatzes auf dem Volume. Das Aufrufen der [**Verschlüsselungs**](encrypt-win32-encryptablevolume.md) Methode mit diesem Bitset ist nur zulässig, wenn das Volume derzeit nicht in den Status "verschlüsselt" versetzt wird und sich im Status "verschlüsselt" befindet.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>0x00010000 bis </dt> </dl> | Führt den angeforderten Vorgang synchron aus. Der-Befehl wird blockiert, bis der angeforderte Vorgang abgeschlossen ist oder unterbrochen wurde. Dieses Flag wird nur mit der Methode " [**verschlüsseln**](encrypt-win32-encryptablevolume.md) " unterstützt. Dieses Flag kann angegeben werden, wenn " **verschlüsseln** " aufgerufen wird, um die beendete oder unterbrochene Verschlüsselung oder das Zurücksetzen oder Löschen von Verschlüsselung oder Zurücksetzen zu beenden. Dies ermöglicht dem Aufrufer, synchron zu warten, bis der Prozess abgeschlossen oder unterbrochen wird.<br/>                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.

Diese Methode wird sofort zurückgegeben. Wenn das Volume bereits vollständig verschlüsselt ist und keine anderen Fehler zurückgegeben werden, gibt diese Methode 0 (null) zurück.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Rückgabecode/-wert</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </dl></td>
<td>Die Methode war erfolgreich.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>E_INVALIDARG</strong></dt> <dt>2147942487 (0x80070057)</dt> </dl></td>
<td>Der Parameter " <em>verschlüsselungmethod</em> " wird bereitgestellt, befindet sich jedoch nicht im bekannten Bereich oder entspricht nicht der aktuellen Gruppenrichtlinie Einstellung.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E)</dt> </dl></td>
<td>Für das Volume ist kein Verschlüsselungsschlüssel vorhanden.<br/> Deaktivieren Sie entweder die Schlüssel Schutzvorrichtungen mithilfe der <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>disablekeyprotector</strong></a> -Methode, oder verwenden Sie eine der folgenden Methoden, um Schlüssel Schutzvorrichtungen für das Volume anzugeben:
<ul>
<li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>Protectkeywithexternalkey</strong></a></li>
<li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>Protectkeywithnumericalpassword</strong></a></li>
<li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>Protectkeywithtpm</strong></a></li>
<li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>Protectkeywithtpmandpin</strong></a></li>
<li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>Protectkeywithtpmandpinandstartupkey</strong></a></li>
<li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>Protectkeywithtpmandstartupkey</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </dl></td>
<td>Das Volume kann nicht verschlüsselt werden, da dieser Computer als Teil eines Server Clusters konfiguriert ist.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_NO_PROTECTORS_TO_TEST</strong></dt> <dt>2150694971 (0x8031003b)</dt> </dl></td>
<td>Es wurden keine Schlüssel Schutzvorrichtungen für den Typ &quot; TPM &quot; , &quot; TPM und PIN &quot; , &quot; TPM und PIN sowie den Systemstart Schlüssel &quot; , das &quot; TPM und den Systemstart Schlüssel &quot; oder den &quot; externen Schlüssel &quot; gefunden. Der Hardware Test umfasst nur die vorherigen Schlüsselschutz Vorrichtungen.<br/> Wenn Sie trotzdem einen Hardware Test ausführen möchten, müssen Sie eine der folgenden Methoden verwenden, um die Schlüssel Schutzvorrichtungen für das Volume anzugeben:
<ul>
<li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>Protectkeywithexternalkey</strong></a></li>
<li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>Protectkeywithnumericalpassword</strong></a></li>
<li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>Protectkeywithtpm</strong></a></li>
<li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>Protectkeywithtpmandpin</strong></a></li>
<li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>Protectkeywithtpmandpinandstartupkey</strong></a></li>
<li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>Protectkeywithtpmandstartupkey</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>FVE_E_NOT_DECRYPTED</strong></dt> <dt>2150694969 (0x80310039)</dt> </dl></td>
<td>Das Volume ist teilweise oder vollständig verschlüsselt.<br/> Der Hardware Test wird angewendet, bevor die Verschlüsselung erfolgt. Wenn Sie den Test trotzdem ausführen möchten, verwenden Sie zunächst die <a href="decrypt-win32-encryptablevolume.md"><strong>Entschlüsselungsmethode</strong></a> , und verwenden Sie dann eine der folgenden Methoden, um Schlüssel Schutzvorrichtungen hinzuzufügen:
<ul>
<li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>Protectkeywithexternalkey</strong></a></li>
<li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>Protectkeywithnumericalpassword</strong></a></li>
<li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>Protectkeywithtpm</strong></a></li>
<li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>Protectkeywithtpmandpin</strong></a></li>
<li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>Protectkeywithtpmandstartupkey</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_NOT_OS_VOLUME</strong></dt> <dt>2150694952 (0x80310028)</dt> </dl></td>
<td>Das Volume ist ein Datenvolumen.<br/> Der Hardware Test gilt nur für Volumes, die das Betriebssystem starten können. Führen Sie diese Methode auf dem aktuell gestarteten Betriebssystem Volume aus.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002c)</dt> </dl></td>
<td>Es wurden keine Schlüssel Schutzvorrichtungen des &quot; typnumerischen Kennworts &quot; angegeben. Für den Gruppenrichtlinie ist eine Sicherung der Wiederherstellungs Informationen erforderlich, um Active Directory Domain Services. Um mindestens eine Schlüssel Schutzvorrichtung dieses Typs hinzuzufügen, verwenden Sie die <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>protectkeywithnumericalpassword</strong></a> -Methode.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Bemerkungen

Wenn Sie diese Methode ohne den zweiten optionalen Parameter verwenden (gemäß der Definition von Windows 7 und Windows Vista Enterprise), initiiert die Methode immer die Konvertierung im vollständigen Modus, um das abwärts kompatible Verhalten beizubehalten. Auf diese Weise wird die Sicherheits Erwartung vorhandener Anwendungen und Skripts nicht durch das Hinzufügen des zweiten optionalen Parameters in Windows 8 und Windows Server 2012 beschädigt.

Anders als bei der [**Verschlüsselungs**](encrypt-win32-encryptablevolume.md) Methode führt diese Methode Folgendes aus:

-   Testet, ob das TPM das Volume entsperren kann, wenn eine TPM-bezogene Schlüssel Schutzvorrichtung vorhanden ist.
-   Testet, ob der Computer einen USB-Speicherstick lesen kann, der eine externe Schlüsseldatei während des Starts enthält, wenn das Volume durch einen externen Schlüssel (einschließlich eines Systemstart Schlüssels) entsperrt wird.
-   Erfordert einen Computer Neustart, um den Hardware Test auszuführen.
-   Startet die Verschlüsselung nur dann, wenn der Hardware Test erfolgreich ist.
-   Kann nicht auf einem Daten Volume, auf einem teilweise oder vollständig verschlüsselten Volume oder zum Fortsetzen der Verschlüsselung verwendet werden.

Verwenden Sie vor dem Ausführen dieser Methode die folgenden Methoden, um die zugehörigen Schlüsselschutz Vorrichtungen zu erstellen:

-   [**Protectkeywithexternalkey**](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [**Protectkeywithtpm**](protectkeywithtpm-win32-encryptablevolume.md)
-   [**Protectkeywithtpmandpin**](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [**Protectkeywithtpmandpinandstartupkey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [**Protectkeywithtpmandstartupkey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

Führen Sie nach dem Ausführen dieser Methode die folgenden zusätzlichen Schritte aus:

1.  Fügen Sie einen USB-Speicherstick, der eine externe Schlüsseldatei enthält, in den Computer ein. Dieser Schritt gilt nur, wenn das Volume über eine Schlüssel Schutzvorrichtung vom Typ "externer Schlüssel" oder "TPM und Systemstart Schlüssel" verfügt.
2.  Starten Sie den Computer neu.

Beim Neustart des Computers wird der Hardware Test automatisch ausgeführt.

Die Verschlüsselung beginnt, wenn der Hardware Test erfolgreich ist. Versuchen Sie andernfalls, Hardwarefehler zu beheben. Führen Sie [**gethardwareteststatus**](gethardwareteststatus-win32-encryptablevolume.md) nach dem Neustart des Computers aus, um die Testergebnisse zu erhalten.

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

 

 
