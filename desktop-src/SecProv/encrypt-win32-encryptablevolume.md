---
description: Startet die Verschlüsselung eines vollständig entschlüsselten Volumes oder nimmt die Verschlüsselung eines teilweise verschlüsselten Volumes wieder auf.
ms.assetid: bba8b800-309b-4268-8278-db69827bbdf6
title: Methode Verschlüsseln der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Encrypt
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 463f13c250404e9a66095144166e74dbfae933ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050472"
---
# <a name="encrypt-method-of-the-win32_encryptablevolume-class"></a>Methode Verschlüsseln der Win32- \_ Klasse "verschlüsseltablevolume"

Die **Verschlüsselungsmethode der** Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " beginnt mit der Verschlüsselung eines vollständig entschlüsselten Volumes oder nimmt die Verschlüsselung eines teilweise verschlüsselten Volumes wieder auf. Wenn die Verschlüsselung angehalten oder ausgeführt wird, verhält sich diese Methode genauso wie " [**resumeconversion**](resumeconversion-win32-encryptablevolume.md)". Wenn die Entschlüsselung angehalten oder in Bearbeitung ist, beendet diese Methode das Entschlüsseln und beginnt mit der Verschlüsselung.

> [!Note]  
> Wenn das Laufwerk Hardware verschlüsselt ist, werden die Daten von dieser Methode nicht verschlüsselt. Stattdessen wird der Band Status von "immer entsperrt" auf "nicht gesperrt" festgelegt. Wenn das Band gesperrt ist, entsperrt oder schreibgeschützt ist, wird das Laufwerk als verschlüsselt eingestuft.

 

**Windows Vista:** Die Verschlüsselung eines anderen Volumes als dem aktuell aktuell laufenden Betriebssystem Volume wird nicht unterstützt.

## <a name="syntax"></a>Syntax


```mof
uint32 Encrypt(
  [in, optional] uint32 EncryptionMethod,
  [in, optional] uint32 EncryptionFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Verschlüsselungsmethode* \[ in, optional\]
</dt> <dd>

Typ: **UInt32**

Eine ganze Zahl ohne Vorzeichen, die den Verschlüsselungsalgorithmus und die Schlüsselgröße angibt, die zum Verschlüsseln des Volumes verwendet werden. Wenn dieser Parameter größer als 0 (null) ist und das Volume teilweise oder vollständig verschlüsselt ist, muss " *verschlüsselungmethod* " der vorhandenen Verschlüsselungsmethode des Volumes entsprechen. Wenn dieser Parameter größer als 0 (null) ist und die entsprechende Gruppenrichtlinie Einstellung mit einem gültigen Wert aktiviert ist, muss " *verschlüsselungsmethod* " mit der Gruppenrichtlinie Einstellung übereinstimmen.

Eine Liste möglicher Verschlüsselungsmethoden Werte finden Sie unter der [**getencryptionmethod**](getencryptionmethod-win32-encryptablevolume.md) -Methode.

Der Standardwert für Windows 7 oder niedriger ist: 1 (AES \_ 128 \_ mit \_ diffuser).

Der Standardwert für Windows 8, Windows 8.1 oder Windows 10, Version 1507 ist: 3 (AES \_ 128).

Der Standardwert für Windows 10, Version 1511 oder höher, ist: 6 (XTS \_ AES \_ 128).

</dd> <dt>

*Verschlüsselungsflags* \[ in, optional\]
</dt> <dd>

Typ: **UInt32**

Flags, die das Verschlüsselungs Verhalten beschreiben.

**Windows 7, Windows Server 2008 R2, Windows Vista Enterprise und Windows Server 2008:** Dieser Parameter ist nicht verfügbar.

Eine Kombination von 32 Bits mit folgenden Bits, die aktuell definiert sind.



| Wert                                                                                  | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000001</dt> </dl>  | Führen Sie die Volumeverschlüsselung im reinen Daten Verschlüsselungs Modus aus, wenn Sie den neuen Verschlüsselungsprozess starten. Wenn die Verschlüsselung angehalten oder beendet wurde, wird die Konvertierung durch Aufrufen der Methode " **verschlüsseln** " wirksam fortgesetzt, und der Wert dieses Bits wird ignoriert. Dieses Bit ist nur wirksam, wenn die Verschlüsselungs-oder [**verschlüsseltafterhardwaretest**](encryptafterhardwaretest-win32-encryptablevolume.md) - **Methoden die Verschlüsselung** aus dem vollständig entschlüsselten Zustand, dem Entschlüsselungs Status oder dem Status der entschlüsselten Entschlüsselung starten. Wenn dieses Bit 0 (null) ist, was bedeutet, dass es beim Starten des neuen Verschlüsselungs Vorgangs nicht festgelegt ist, wird die vollständige Modus-Konvertierung ausgeführt.<br/> |
| <dl> <dt>0x00000002</dt> </dl>  | Ausführen einer bedarfsgesteuerten Löschung des freien Speicherplatzes auf dem Volume. Das Aufrufen der **Verschlüsselungs** Methode mit diesem Bitset ist nur zulässig, wenn das Volume derzeit nicht in den Status "verschlüsselt" versetzt wird und sich im Status "verschlüsselt" befindet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>0x00010000 bis </dt> </dl> | Führt den angeforderten Vorgang synchron aus. Der-Befehl wird blockiert, bis der angeforderte Vorgang abgeschlossen ist oder unterbrochen wurde. Dieses Flag wird nur mit der Methode " **verschlüsseln** " unterstützt. Dieses Flag kann angegeben werden, wenn " **verschlüsseln** " aufgerufen wird, um die beendete oder unterbrochene Verschlüsselung oder das Zurücksetzen oder Löschen von Verschlüsselung oder Zurücksetzen zu beenden. Dies ermöglicht dem Aufrufer, synchron zu warten, bis der Prozess abgeschlossen oder unterbrochen wird.<br/>                                                                                                                                                                                  |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.

Diese Methode wird sofort zurückgegeben. Wenn das Volume bereits vollständig verschlüsselt ist und keine anderen Fehler zurückgegeben werden, gibt diese Methode 0 zurück.



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
<td>Für das Volume ist kein Verschlüsselungsschlüssel vorhanden. Deaktivieren Sie entweder die Schlüssel Schutzvorrichtungen mithilfe der <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>disablekeyprotector</strong></a> -Methode, oder verwenden Sie eine der folgenden Methoden, um Schlüssel Schutzvorrichtungen für das Volume anzugeben:<br/>
<ul>
<li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>Protectkeywithexternalkey</strong></a></li>
<li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>Protectkeywithnumericalpassword</strong></a></li>
<li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>Protectkeywithtpm</strong></a></li>
<li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>Protectkeywithtpmandpin</strong></a></li>
<li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>Protectkeywithtpmandpinandstartupkey</strong></a></li>
<li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>Protectkeywithtpmandstartupkey</strong></a></li>
</ul>
<strong>Windows Vista:</strong> Wenn kein Verschlüsselungsschlüssel für das Volume vorhanden ist, wird stattdessen ERROR_INVALID_OPERATION zurückgegeben. Der Dezimalwert ist 4317, und der hexadezimale Wert ist 0x10dd.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>FVE_E_CANNOT_SET_FVEK_ENCRYPTED</strong></dt> <dt>2150694957 (0x8031002d)</dt> </dl></td>
<td>Die bereitgestellte Verschlüsselungsmethode entspricht nicht der des teilweise oder vollständig verschlüsselten Volumes. Wenn Sie die Verschlüsselung fortsetzen möchten, lassen Sie den Parameter " <em>verschlüsselungmethod</em> " leer, oder verwenden Sie den Wert 0<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </dl></td>
<td>Das Volume kann nicht verschlüsselt werden, da dieser Computer als Teil eines Server Clusters konfiguriert ist.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>FVE_E_LOCKED_VOLUME</strong></dt> <dt>2150694912 (0x80310000)</dt> </dl></td>
<td>Das Volume ist gesperrt.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002c)</dt> </dl></td>
<td>Es wurden keine Schlüssel Schutzvorrichtungen des &quot; typnumerischen Kennworts &quot; angegeben. Für den Gruppenrichtlinie ist eine Sicherung der Wiederherstellungs Informationen erforderlich, um Active Directory Domain Services. Um mindestens eine Schlüssel Schutzvorrichtung dieses Typs hinzuzufügen, verwenden Sie die <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>protectkeywithnumericalpassword</strong></a> -Methode.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Bemerkungen

Wenn Sie diese Methode ohne den zweiten optionalen Parameter verwenden (gemäß der Definition von Windows 7 und Windows Vista Enterprise), initiiert die Methode immer die Konvertierung im vollständigen Modus, um das abwärts kompatible Verhalten beizubehalten. Auf diese Weise wird die Sicherheits Erwartung vorhandener Anwendungen und Skripts nicht durch das Hinzufügen des zweiten optionalen Parameters in Windows 8 und Windows Server 2012 beschädigt.

Sie können [**getdeversionstatus**](getconversionstatus-win32-encryptablevolume.md) aufrufen, um zu bestimmen, ob die Verschlüsselung ausgeführt wird, und den Prozentsatz des Volumes, das verschlüsselt wurde.

Wenn das Volume vollständig verschlüsselt ist und Schlüssel Schutzvorrichtungen hinzugefügt und aktiviert wurden, ändert sich der Schutzstatus für das Volume in "ein".

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

 

 
