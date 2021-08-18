---
description: Startet die Verschlüsselung eines vollständig entschlüsselten Betriebssystemvolumes nach einem Hardwaretest.
ms.assetid: 216c96bb-7737-4421-8b16-1ce295342266
title: EncryptAfterHardwareTest-Methode der Win32_EncryptableVolume-Klasse
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
ms.openlocfilehash: f5365bd9aca023d42d9f2ab1d9de5d242497b8b21842004b2bb508f362752bd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004498"
---
# <a name="encryptafterhardwaretest-method-of-the-win32_encryptablevolume-class"></a>EncryptAfterHardwareTest-Methode der Win32 \_ EncryptableVolume-Klasse

Die **EncryptAfterHardwareTest-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) beginnt nach einem Hardwaretest mit der Verschlüsselung eines vollständig entschlüsselten Betriebssystemvolumes. Für diesen Hardwaretest ist ein Neustart erforderlich. Verwenden Sie diese [](encrypt-win32-encryptablevolume.md) Methode anstelle der Encrypt-Methode, um zu überprüfen, ob BitLocker erwartungsgemäß funktioniert.

> [!Note]  
> Wenn die Festplatte hardwareverschlüsselt ist, verschlüsselt diese Methode keine Daten. Stattdessen wird der Bandstatus auf entsperrt von "unbefristet entsperrt" festgelegt. Wenn das Band gesperrt, entsperrt oder schreibgeschützt ist, gilt das Laufwerk als verschlüsselt.

 

## <a name="syntax"></a>Syntax


```mof
uint32 EncryptAfterHardwareTest(
  [in, optional] uint32 EncryptionMethod,
  [in, optional] uint32 EncryptionFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*EncryptionMethod* \[ in, optional\]
</dt> <dd>

Typ: **uint32**

Gibt den Verschlüsselungsalgorithmus und die Schlüsselgröße an, die zum Verschlüsseln des Volumes verwendet werden. Lassen Sie diesen Parameter leer, um den Standardwert 0 (null) zu verwenden. Wenn das Volume teilweise oder vollständig verschlüsselt ist, muss der Wert dieses Parameters 0 sein oder mit der vorhandenen Verschlüsselungsmethode des Volumes übereinstimmen. Wenn die entsprechende Gruppenrichtlinie Einstellung mit einem gültigen Wert aktiviert wurde, muss der Wert dieses Parameters 0 sein oder mit der einstellung Gruppenrichtlinie übereinstimmen.

Wenn die entsprechende Gruppenrichtlinie-Einstellung ungültig ist, wird der Standardwert AES 128 mit Diffusor verwendet.



| Wert                                                                                                                                                                                                                                       | Bedeutung                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span><dl> <dt>**Nicht angegeben**</dt> <dt>0</dt> </dl> | Verwenden Sie die aktuelle einstellung Gruppenrichtlinie , sofern verfügbar und gültig, oder die Standardverschlüsselungsmethode, andernfalls .<br/>                                                                              |
| <dl> <dt>1</dt> </dl>                                                                                                                                                                | AES 128 MIT DIFFUSER<br/> Verschlüsseln Sie das Volume mithilfe des AES-Algorithmus (Advanced Encryption Standard), der mit einer Diffusorebene erweitert wurde, und mithilfe einer AES-Schlüsselgröße von 128 Bits.<br/> |
| <dl> <dt>2</dt> </dl>                                                                                                                                                                | AES 256 MIT DIFFUSER<br/> Verschlüsseln Sie das Volume mithilfe des AES-Algorithmus (Advanced Encryption Standard), der mit einer Diffusorebene erweitert wurde, und mithilfe einer AES-Schlüsselgröße von 256 Bits.<br/> |
| <span id="AES_128"></span><span id="aes_128"></span><dl> <dt>**AES \_ 128**</dt> <dt>3</dt> </dl>                                          | Verschlüsseln Sie das Volume mit dem AES-Algorithmus (Advanced Encryption Standard) und einer AES-Schlüsselgröße von 128 Bits.<br/>                                                                 |
| <span id="AES_256"></span><span id="aes_256"></span><dl> <dt>**AES \_ 256**</dt> <dt>4</dt> </dl>                                          | Verschlüsseln Sie das Volume mit dem AES-Algorithmus (Advanced Encryption Standard) und einer AES-Schlüsselgröße von 256 Bits.<br/>                                                                 |



 

</dd> <dt>

*EncryptionFlags* \[ in, optional\]
</dt> <dd>

Typ: **uint32**

Flags, die das Verschlüsselungsverhalten beschreiben.

**Windows 7, Windows Server 2008 R2, Windows Vista Enterprise und Windows Server 2008:** Dieser Parameter ist nicht verfügbar.

Eine Kombination aus 32 Bits und den folgenden derzeit definierten Bits.



| Wert                                                                                  | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000001</dt> </dl>  | Durchführen der Volumeverschlüsselung im reinen Datenverschlüsselungsmodus beim Starten eines neuen Verschlüsselungsprozesses. Wenn die Verschlüsselung angehalten oder beendet wurde, setzt der Aufruf der [**Encrypt-Methode**](encrypt-win32-encryptablevolume.md) die Konvertierung effektiv fort, und der Wert dieses Bits wird ignoriert. Dieses Bit hat nur Dann Auswirkungen, wenn entweder die **Encrypt-** oder **EncryptAfterHardwareTest-Methode** die Verschlüsselung aus dem vollständig entschlüsselten Zustand, dem Status der entschlüsselungsstatus oder dem angehaltenen Entschlüsselungsstatus startet. Wenn dieses Bit 0 (null) ist, was bedeutet, dass es nicht festgelegt ist, wird beim Starten eines neuen Verschlüsselungsprozesses die Konvertierung im vollständigen Modus durchgeführt.<br/> |
| <dl> <dt>0x00000002</dt> </dl>  | Führen Sie das bedarfsorientierte Zurücksetzen des freien Speicherplatzes auf dem Volume aus. Das Aufrufen der [**Encrypt-Methode**](encrypt-win32-encryptablevolume.md) mit diesem Bitsatz ist nur zulässig, wenn das Volume derzeit nicht konvertiert oder zurückgesetzt wird und sich in einem "verschlüsselten" Zustand befindet.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>0x00010000 </dt> </dl> | Führen Sie den angeforderten Vorgang synchron aus. Der Aufruf wird blockiert, bis der angeforderte Vorgang abgeschlossen oder unterbrochen wurde. Dieses Flag wird nur mit der [**Encrypt-Methode**](encrypt-win32-encryptablevolume.md) unterstützt. Dieses Flag kann angegeben werden, wenn **Encrypt** aufgerufen wird, um die beendete oder unterbrochene Verschlüsselung oder das Zurücksetzen fortzusetzen oder wenn die Verschlüsselung oder das Zurücksetzen ausgeführt wird. Dadurch kann der Aufrufer synchron warten, bis der Prozess abgeschlossen oder unterbrochen wurde.<br/>                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn er fehlschlägt.

Diese Methode gibt sofort zurück. Wenn das Volume bereits vollständig verschlüsselt ist und keine anderen Fehler zurückgegeben werden, gibt diese Methode 0 (null) zurück.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Rückgabecode/-wert</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </dl></td>
<td>Die Methode war erfolgreich.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>E_INVALIDARG</strong></dt> <dt>2147942487 (0x80070057)</dt> </dl></td>
<td>Der <em>EncryptionMethod-Parameter</em> wird bereitgestellt, liegt aber nicht innerhalb des bekannten Bereichs oder stimmt nicht mit der aktuellen einstellung Gruppenrichtlinie überein.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E)</dt> </dl></td>
<td>Für das Volume ist kein Verschlüsselungsschlüssel vorhanden.<br/> Deaktivieren Sie entweder Schlüsselschutzvorrichtungen mithilfe der <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors-Methode,</strong></a> oder verwenden Sie eine der folgenden Methoden, um Schlüsselschutzvorrichtungen für das Volume anzugeben:
<ul>
<li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li>
<li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li>
<li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li>
<li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li>
<li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></li>
<li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </dl></td>
<td>Das Volume kann nicht verschlüsselt werden, da dieser Computer als Teil eines Serverclusters konfiguriert ist.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_NO_PROTECTORS_TO_TEST</strong></dt> <dt>2150694971 (0x8031003B)</dt> </dl></td>
<td>Es können keine Schlüsselschutzvorrichtungen vom Typ &quot; &quot; TPM, &quot; TPM und &quot; PIN, TPM und PIN und &quot; &quot; Startschlüssel, TPM und &quot; Startschlüssel oder Externer Schlüssel &quot; gefunden &quot; &quot; werden. Der Hardwaretest umfasst nur die vorherigen Schlüsselschutzvorrichtungen.<br/> Wenn Sie weiterhin einen Hardwaretest ausführen möchten, müssen Sie eine der folgenden Methoden verwenden, um Schlüsselschutzvorrichtungen für das Volume anzugeben:
<ul>
<li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li>
<li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li>
<li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li>
<li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li>
<li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></li>
<li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>FVE_E_NOT_DECRYPTED</strong></dt> <dt>2150694969 (0x80310039)</dt> </dl></td>
<td>Das Volume ist teilweise oder vollständig verschlüsselt.<br/> Der Hardwaretest wird angewendet, bevor die Verschlüsselung erfolgt. Wenn Sie den Test weiterhin ausführen möchten, verwenden Sie zuerst die <a href="decrypt-win32-encryptablevolume.md"><strong>Decrypt-Methode</strong></a> und dann eine der folgenden Methoden, um Schlüsselschutzvorrichtungen hinzuzufügen:
<ul>
<li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li>
<li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li>
<li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li>
<li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li>
<li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_NOT_OS_VOLUME</strong></dt> <dt>2150694952 (0x80310028)</dt> </dl></td>
<td>Das Volume ist ein Datenvolume.<br/> Der Hardwaretest gilt nur für Volumes, die das Betriebssystem starten können. Führen Sie diese Methode auf dem aktuell gestarteten Betriebssystemvolume aus.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C)</dt> </dl></td>
<td>Es werden keine Schlüsselschutzvorrichtungen vom Typ &quot; Numerisches Kennwort &quot; angegeben. Die Gruppenrichtlinie erfordert eine Sicherung von Wiederherstellungsinformationen für Active Directory Domain Services. Um mindestens eine Schlüsselschutzvorrichtung dieses Typs hinzuzufügen, verwenden Sie die <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword-Methode.</strong></a><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Hinweise

Wenn Sie diese Methode ohne den zweiten optionalen Parameter verwenden (gemäß Windows 7 und Windows Vista Enterprise Definition), initiiert die Methode immer die Konvertierung im vollständigen Modus, um das abwärtskompatible Verhalten beizubehalten. Auf diese Weise wird die Sicherheitserwartung vorhandener Anwendungen und Skripts nicht durch hinzufügen des zweiten optionalen Parameters in Windows 8 und Windows Server 2012 unterbrochen.

Im Gegensatz zur [**Encrypt-Methode**](encrypt-win32-encryptablevolume.md) führt diese Methode Folgendes aus:

-   Testet, ob das TPM das Volume entsperren kann, wenn eine TPM-bezogene Schlüsselschutzvorrichtung vorhanden ist.
-   Testet, ob der Computer während des Starts einen USB-Speicherstick lesen kann, der eine externe Schlüsseldatei enthält, wenn das Volume durch einen externen Schlüssel (einschließlich eines Startschlüssels) entsperrt wird.
-   Erfordert einen Neustart des Computers, um den Hardwaretest auszuführen.
-   Beginnt die Verschlüsselung nur, wenn der Hardwaretest erfolgreich ist.
-   Kann nicht auf einem Datenvolume, auf einem teilweise oder vollständig verschlüsselten Volume oder zum Fortsetzen der Verschlüsselung verwendet werden.

Verwenden Sie vor dem Ausführen dieser Methode die folgenden Methoden, um die zugehörigen Schlüsselschutzvorrichtungen zu erstellen:

-   [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPM**](protectkeywithtpm-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPIN**](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPINAndStartupKey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndStartupKey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

Führen Sie nach dem Ausführen dieser Methode die folgenden zusätzlichen Schritte aus:

1.  Fügen Sie auf dem Computer einen USB-Speicherstick ein, der eine externe Schlüsseldatei enthält. Dieser Schritt gilt nur, wenn das Volume über eine Schlüsselschutzvorrichtung vom Typ "Externer Schlüssel" oder "TPM und Startschlüssel" verfügt.
2.  Starten Sie den Computer neu.

Beim Neustart des Computers wird der Hardwaretest automatisch ausgeführt.

Die Verschlüsselung beginnt, wenn der Hardwaretest erfolgreich ist. Versuchen Sie andernfalls, Hardwarefehler zu beheben. Führen [**Sie GetHardwareTestStatus**](gethardwareteststatus-win32-encryptablevolume.md) nach dem Neustart des Computers aus, um Testergebnisse zu erhalten.

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

 

 
