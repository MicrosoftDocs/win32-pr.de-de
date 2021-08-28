---
description: Startet die Verschlüsselung eines vollständig entschlüsselten Volumes oder setzt die Verschlüsselung eines teilweise verschlüsselten Volumes fort.
ms.assetid: bba8b800-309b-4268-8278-db69827bbdf6
title: Encrypt-Methode der Win32_EncryptableVolume-Klasse
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
ms.openlocfilehash: 968ff7f64a9a98a711210a4cfae64006c5a8f965
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481026"
---
# <a name="encrypt-method-of-the-win32_encryptablevolume-class"></a>Encrypt-Methode der Win32 \_ EncryptableVolume-Klasse

Die **Encrypt-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) beginnt mit der Verschlüsselung eines vollständig entschlüsselten Volumes oder setzt die Verschlüsselung eines teilweise verschlüsselten Volumes fort. Wenn die Verschlüsselung angehalten wird oder in Bearbeitung ist, verhält sich diese Methode genauso wie [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md). Wenn die Entschlüsselung angehalten oder in Bearbeitung ist, beendet diese Methode die Entschlüsselung und beginnt mit der Verschlüsselung.

> [!Note]  
> Wenn das Laufwerk hardwareverschlüsselt ist, verschlüsselt diese Methode keine Daten. Stattdessen wird der Bandstatus von "immer entsperrt" auf "entsperrt" festgelegt. Wenn das Band gesperrt, entsperrt oder schreibgeschützt ist, gilt das Laufwerk als verschlüsselt.

 

**Windows Vista:** Die Verschlüsselung eines anderen Volumes als dem derzeit ausgeführten Betriebssystemvolume wird nicht unterstützt.

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

Eine ganze Zahl ohne Vorzeichen, die den Verschlüsselungsalgorithmus und die Schlüsselgröße angibt, die zum Verschlüsseln des Volumes verwendet werden. Wenn dieser Parameter größer als 0 (null) ist und das Volume teilweise oder vollständig verschlüsselt ist, muss *EncryptionMethod* mit der vorhandenen Verschlüsselungsmethode des Volumes übereinstimmen. Wenn dieser Parameter größer als 0 (null) ist und die entsprechende Gruppenrichtlinie Einstellung mit einem gültigen Wert aktiviert ist, muss *EncryptionMethod* mit der einstellung Gruppenrichtlinie übereinstimmen.

Eine Liste der möglichen EncryptionMethod-Werte finden Sie in der [**GetEncryptionMethod-Methode.**](getencryptionmethod-win32-encryptablevolume.md)

Der Standardwert für Windows 7 oder darunter ist: 1 (AES \_ 128 \_ WITH \_ DIFFUSER).

Der Standardwert für Windows 8, Windows 8.1 oder Windows 10 Version 1507 lautet: 3 (AES \_ 128).

Standardwert für Windows 10, Version 1511 oder höher: 6 (XTS \_ AES \_ 128).

</dd> <dt>

*EncryptionFlags* \[ in, optional\]
</dt> <dd>

Typ: **uint32**

Flags, die das Verschlüsselungsverhalten beschreiben.

**Windows 7, Windows Server 2008 R2, Windows Vista Enterprise und Windows Server 2008:** Dieser Parameter ist nicht verfügbar.

Eine Kombination aus 32 Bits und den folgenden derzeit definierten Bits.



| Wert                                                                                  | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000001</dt> </dl>  | Durchführen der Volumeverschlüsselung im reinen Datenverschlüsselungsmodus beim Starten eines neuen Verschlüsselungsprozesses. Wenn die Verschlüsselung angehalten oder beendet wurde, setzt der Aufruf der **Encrypt-Methode** die Konvertierung effektiv fort, und der Wert dieses Bits wird ignoriert. Dieses Bit hat nur Dann Auswirkungen, wenn entweder die **Encrypt-** oder [**EncryptAfterHardwareTest-Methode**](encryptafterhardwaretest-win32-encryptablevolume.md) die Verschlüsselung aus dem vollständig entschlüsselten Zustand, dem Status der entschlüsselungsstatus oder dem angehaltenen Entschlüsselungsstatus startet. Wenn dieses Bit 0 (null) ist, was bedeutet, dass es nicht festgelegt ist, wird beim Starten eines neuen Verschlüsselungsprozesses die Konvertierung im vollständigen Modus ausgeführt.<br/> |
| <dl> <dt>0x00000002</dt> </dl>  | Führen Sie das bedarfsorientierte Zurücksetzen des freien Speicherplatzes auf dem Volume aus. Das Aufrufen der **Encrypt-Methode** mit diesem Bitsatz ist nur zulässig, wenn das Volume derzeit nicht konvertiert oder zurückgesetzt wird und sich in einem "verschlüsselten" Zustand befindet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>0x00010000 </dt> </dl> | Führen Sie den angeforderten Vorgang synchron aus. Der Aufruf wird blockiert, bis der angeforderte Vorgang abgeschlossen oder unterbrochen wurde. Dieses Flag wird nur mit der **Encrypt-Methode** unterstützt. Dieses Flag kann angegeben werden, wenn **Encrypt** aufgerufen wird, um die beendete oder unterbrochene Verschlüsselung oder das Zurücksetzen fortzusetzen oder wenn die Verschlüsselung oder das Zurücksetzen ausgeführt wird. Dadurch kann der Aufrufer synchron warten, bis der Prozess abgeschlossen oder unterbrochen wurde.<br/>                                                                                                                                                                                  |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn er fehlschlägt.

Diese Methode gibt sofort zurück. Wenn das Volume bereits vollständig verschlüsselt ist und keine anderen Fehler zurückgegeben werden, gibt diese Methode 0 zurück.




| Rückgabecode/-wert | BESCHREIBUNG | 
|-------------------|-------------|
| <dl><dt><strong>S_OK</strong></dt><dt>0 (0x0)</dt></dl> | Die Methode war erfolgreich.<br /> | 
| <dl><dt><strong>E_INVALIDARG</strong></dt><dt>2147942487 (0x80070057)</dt></dl> | Der <em>EncryptionMethod-Parameter</em> wird bereitgestellt, liegt aber nicht innerhalb des bekannten Bereichs oder stimmt nicht mit der aktuellen einstellung Gruppenrichtlinie überein.<br /> | 
| <dl><dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt><dt>2150694958 (0x8031002E)</dt></dl> | Für das Volume ist kein Verschlüsselungsschlüssel vorhanden. Deaktivieren Sie schlüsselschutzvorrichtungen entweder mithilfe der <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors-Methode,</strong></a> oder verwenden Sie eine der folgenden Methoden, um Schlüsselschutzvorrichtungen für das Volume anzugeben:<br /><ul><li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li><li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li><li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li><li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li><li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></li><li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li></ul><strong>Windows Vista:</strong> Wenn kein Verschlüsselungsschlüssel für das Volume vorhanden ist, wird stattdessen ERROR_INVALID_OPERATION zurückgegeben. Der Dezimalwert ist 4317, und der Hexadezimalwert ist 0x10DD.<br /> | 
| <dl><dt><strong>FVE_E_CANNOT_SET_FVEK_ENCRYPTED</strong></dt><dt>2150694957 (0x8031002D)</dt></dl> | Die bereitgestellte Verschlüsselungsmethode stimmt nicht mit der des teilweise oder vollständig verschlüsselten Volumes überein. Lassen Sie den <em>Parameter EncryptionMethod</em> leer, oder verwenden Sie den Wert 0 (null), um die Verschlüsselung fortzusetzen.<br /> | 
| <dl><dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt><dt>2150694942 (0x8031001E)</dt></dl> | Das Volume kann nicht verschlüsselt werden, da dieser Computer als Teil eines Serverclusters konfiguriert ist.<br /> | 
| <dl><dt><strong>FVE_E_LOCKED_VOLUME</strong></dt><dt>2150694912 (0x80310000)</dt></dl> | Das Volume ist gesperrt.<br /> | 
| <dl><dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt><dt>2150694956 (0x8031002C)</dt></dl> | Es werden keine Schlüsselschutzvorrichtungen vom Typ "Numerisches Kennwort" angegeben. Die Gruppenrichtlinie erfordert eine Sicherung von Wiederherstellungsinformationen für Active Directory Domain Services. Um mindestens eine Schlüsselschutzvorrichtung dieses Typs hinzuzufügen, verwenden Sie die <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword-Methode.</strong></a><br /> | 




 

## <a name="remarks"></a>Hinweise

Wenn Sie diese Methode ohne den zweiten optionalen Parameter verwenden (gemäß Windows 7 und Windows Vista Enterprise Definition), initiiert die Methode immer die Konvertierung im vollständigen Modus, um abwärtskompatibel zu bleiben. Auf diese Weise wird die Sicherheitserwartung vorhandener Anwendungen und Skripts nicht durch hinzufügen des zweiten optionalen Parameters in Windows 8 und Windows Server 2012 unterbrochen.

Sie können [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) aufrufen, um zu bestimmen, ob die Verschlüsselung ausgeführt wird und welcher Prozentsatz des Volumes verschlüsselt wurde.

Nachdem das Volume vollständig verschlüsselt wurde und Schlüsselschutzvorrichtungen hinzugefügt und aktiviert wurden, ändert sich der Schutzstatus für das Volume in "Ein".

Managed Object Format -Dateien (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Enterprise, nur Windows Vista \[ Ultimate-Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
