---
description: Beginnt mit der Verschlüsselung eines vollständig entschlüsselten Volumes oder setzt die Verschlüsselung eines teilweise verschlüsselten Volumes wieder ein.
ms.assetid: bba8b800-309b-4268-8278-db69827bbdf6
title: Encrypt-Methode der Win32_EncryptableVolume Klasse
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
ms.openlocfilehash: e6e2ed0eea4bb9c70949a3916733bf2777397fcb509ba0ce2f91633bf15a74d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892468"
---
# <a name="encrypt-method-of-the-win32_encryptablevolume-class"></a>Encrypt-Methode der Win32 \_ EncryptableVolume-Klasse

Die **Encrypt-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) beginnt mit der Verschlüsselung eines vollständig entschlüsselten Volumes oder setzt die Verschlüsselung eines teilweise verschlüsselten Volumes wieder ein. Wenn die Verschlüsselung angehalten oder in Bearbeitung ist, verhält sich diese Methode genauso wie [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md). Wenn die Entschlüsselung angehalten oder in Bearbeitung ist, beendet diese Methode die Entschlüsselung und beginnt mit der Verschlüsselung.

> [!Note]  
> Wenn das Laufwerk hardware verschlüsselt ist, verschlüsselt diese Methode keine Daten. Stattdessen wird der Bandstatus von "immer entsperrt" auf "Entsperrt" fest. Wenn das Band gesperrt, entsperrt oder schreibgeschützt ist, gilt das Laufwerk als verschlüsselt.

 

**Windows Vista:** Die Verschlüsselung eines anderen Volumes als des derzeit ausgeführten Betriebssystem-Volumes wird nicht unterstützt.

## <a name="syntax"></a>Syntax


```mof
uint32 Encrypt(
  [in, optional] uint32 EncryptionMethod,
  [in, optional] uint32 EncryptionFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*EncryptionMethod* \[ in, optional\]
</dt> <dd>

Typ: **uint32**

Eine ganze Zahl ohne Vorzeichen, die den Verschlüsselungsalgorithmus und die Schlüsselgröße angibt, die zum Verschlüsseln des Volumes verwendet werden. Wenn dieser Parameter größer als 0 (null) ist und das Volume teilweise oder vollständig verschlüsselt ist, muss *EncryptionMethod* mit der vorhandenen Verschlüsselungsmethode des Volumes übereinstimmen. Wenn dieser Parameter größer als 0 (null) ist und die entsprechende Gruppenrichtlinie-Einstellung mit einem gültigen Wert aktiviert ist, muss *EncryptionMethod* mit der Gruppenrichtlinie übereinstimmen.

Eine Liste der möglichen EncryptionMethod-Werte finden Sie unter [**GetEncryptionMethod-Methode.**](getencryptionmethod-win32-encryptablevolume.md)

Der Standardwert für Windows 7 oder darunter ist: 1 (AES \_ 128 \_ WITH \_ DIFFUSER).

Der Standardwert für Windows 8, Windows 8.1 oder Windows 10 Version 1507 ist: 3 (AES \_ 128).

Der Standardwert für Windows 10 Version 1511 oder höher ist: 6 (XTS \_ AES \_ 128).

</dd> <dt>

*EncryptionFlags* \[ in, optional\]
</dt> <dd>

Typ: **uint32**

Flags, die das Verschlüsselungsverhalten beschreiben.

**Windows 7, Windows Server 2008 R2, Windows Vista Enterprise und Windows Server 2008:** Dieser Parameter ist nicht verfügbar.

Eine Kombination aus 32 Bits und den folgenden derzeit definierten Bits.



| Wert                                                                                  | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000001</dt> </dl>  | Führen Sie die Volumeverschlüsselung im Datenverschlüsselungsmodus aus, wenn Sie einen neuen Verschlüsselungsprozess starten. Wenn die Verschlüsselung angehalten oder beendet wurde, wird die Konvertierung durch Aufrufen der **Encrypt-Methode** effektiv fortgesetzt, und der Wert dieses Bit wird ignoriert. Dieses Bit hat nur Dann Auswirkungen, wenn die **Encrypt-** oder [**EncryptAfterHardwareTest-Methode**](encryptafterhardwaretest-win32-encryptablevolume.md) die Verschlüsselung vom vollständig entschlüsselten Zustand, der Entschlüsselung im Status "Wird durchgeführt" oder dem angehaltenen Entschlüsselungszustand aus startet. Wenn dieses Bit 0 (null) ist, was bedeutet, dass es nicht festgelegt ist, wird beim Starten eines neuen Verschlüsselungsprozesses die Konvertierung im vollständigen Modus durchgeführt.<br/> |
| <dl> <dt>0x00000002</dt> </dl>  | Führen Sie eine bedarfsbasierte Zurücksetzung des freien Speicherplatzes auf dem Volume durch. Das Aufrufen **der Encrypt-Methode** mit diesem Bitsatz ist nur zulässig, wenn das Volume derzeit nicht konvertiert oder zurückf wird und sich in einem "verschlüsselten" Zustand befindet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>0x00010000 </dt> </dl> | Führen Sie den angeforderten Vorgang synchron aus. Der Aufruf wird blockiert, bis der angeforderte Vorgang abgeschlossen oder unterbrochen wurde. Dieses Flag wird nur mit der **Encrypt-Methode** unterstützt. Dieses Flag kann angegeben werden, wenn **Encrypt** aufgerufen wird, um die beendete oder unterbrochene Verschlüsselung oder das Zurückschneiden fort aufzunehmen, oder wenn die Verschlüsselung oder das Zurückschneiden in Bearbeitung ist. Dadurch kann der Aufrufer synchron warten, bis der Prozess abgeschlossen oder unterbrochen wird.<br/>                                                                                                                                                                                  |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.

Diese Methode gibt sofort zurück. Wenn das Volume bereits vollständig verschlüsselt ist und keine anderen Fehler zurückgegeben werden, gibt diese Methode 0 zurück.



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
<td>Der <em>EncryptionMethod-Parameter</em> wird bereitgestellt, liegt aber nicht innerhalb des bekannten Bereichs oder passt nicht zur aktuellen Gruppenrichtlinie.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E)</dt> </dl></td>
<td>Für das Volume ist kein Verschlüsselungsschlüssel vorhanden. Deaktivieren Sie Schlüsselschutzvorrichtungen entweder mithilfe der <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors-Methode,</strong></a> oder verwenden Sie eine der folgenden Methoden, um Schlüsselschutzvorrichtungen für das Volume anzugeben:<br/>
<ul>
<li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li>
<li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li>
<li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li>
<li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li>
<li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></li>
<li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li>
</ul>
<strong>Windows Vista:</strong> Wenn kein Verschlüsselungsschlüssel für das Volume vorhanden ist, wird ERROR_INVALID_OPERATION zurückgegeben. Der Dezimalwert ist 4317, und der Hexadezimalwert ist 0x10DD.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>FVE_E_CANNOT_SET_FVEK_ENCRYPTED</strong></dt> <dt>2150694957 (0x8031002D)</dt> </dl></td>
<td>Die bereitgestellte Verschlüsselungsmethode ist nicht mit der des teilweise oder vollständig verschlüsselten Volumes übereinstimmen. Lassen Sie den <em>EncryptionMethod-Parameter</em> leer, oder verwenden Sie den Wert 0 (null), um die Verschlüsselung fortzufahren.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </dl></td>
<td>Das Volume kann nicht verschlüsselt werden, da dieser Computer als Teil eines Serverclusters konfiguriert ist.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>FVE_E_LOCKED_VOLUME</strong></dt> <dt>2150694912 (0x80310000)</dt> </dl></td>
<td>Das Volume ist gesperrt.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C)</dt> </dl></td>
<td>Es werden keine Schlüsselschutzvorrichtungen vom Typ &quot; Numerisches &quot; Kennwort angegeben. Der Gruppenrichtlinie erfordert eine Sicherung von Wiederherstellungsinformationen, um Active Directory Domain Services. Um mindestens eine Schlüsselschutzvorrichtung dieses Typs hinzuzufügen, verwenden Sie die <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword-Methode.</strong></a><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Hinweise

Wenn Sie diese Methode ohne den zweiten optionalen Parameter verwenden (gemäß der Windows 7- und Windows Vista Enterprise-Definition), initiiert die Methode immer die Konvertierung des vollständigen Modus, um abwärtskompatibles Verhalten zu erhalten. Auf diese Weise wird die Sicherheitserwartung vorhandener Anwendungen und Skripts nicht durch hinzufügen des zweiten optionalen Parameters in Windows 8 und Windows Server 2012.

Sie können [**GetConversionStatus aufrufen,**](getconversionstatus-win32-encryptablevolume.md) um zu bestimmen, ob die Verschlüsselung in Bearbeitung ist und wie hoch der Prozentsatz des verschlüsselten Volumes ist.

Nachdem das Volume vollständig verschlüsselt und Schlüsselschutzvorrichtungen hinzugefügt und aktiviert wurden, ändert sich der Schutzstatus für das Volume in "Ein".

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Enterprise, Windows Vista \[ Ultimate-Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\CimV2-Stammsicherheit \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
