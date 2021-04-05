---
description: Gibt an, ob das Volume und der zugehörige Verschlüsselungsschlüssel geschützt sind.
ms.assetid: bcd8fce5-da39-4aa8-93ff-0768deb900ec
title: Getschutzstatus-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetProtectionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 5f3fa2aaa019097a01a6e6d1628d7c4fe9b82710
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750841"
---
# <a name="getprotectionstatus-method-of-the-win32_encryptablevolume-class"></a>Getschutzstatus-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **getschutzstatus** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " gibt an, ob das Volume und der zugehörige Verschlüsselungsschlüssel (sofern vorhanden) gesichert sind.

Der Schutz ist deaktiviert, wenn ein Volume unverschlüsselt oder teilweise verschlüsselt ist, oder wenn der Verschlüsselungsschlüssel des Volumes im Klartext auf der Festplatte verfügbar ist.

## <a name="syntax"></a>Syntax


```mof
uint32 GetProtectionStatus(
  [out] uint32 ProtectionStatus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Schutz *Status* \[ vorgenommen\]
</dt> <dd>

Typ: **UInt32**

Gibt an, ob das Volume und der Verschlüsselungsschlüssel (sofern vorhanden) gesichert sind.



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
<td><span id="Unprotected"></span><span id="unprotected"></span><span id="UNPROTECTED"></span><dl> <dt><strong>Ungeschützt</strong></dt> <dt>0</dt> </dl></td>
<td>Schutz deaktiviert<br/> Für eine Standard-HDD:<br/> Das Volume ist unverschlüsselt, teilweise verschlüsselt, oder der Verschlüsselungsschlüssel des Volumes ist im Klartext auf der Festplatte verfügbar. Der Verschlüsselungsschlüssel ist im Klartext auf der Festplatte verfügbar, wenn die Schlüssel Schutzvorrichtungen mithilfe der <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>disablekeyprotector</strong></a> -Methode deaktiviert wurden oder wenn keine Schlüssel Schutzvorrichtungen mithilfe der folgenden Methoden angegeben wurden:
<ul>
<li><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>Protectkeywithcertificatefile</strong></a></li>
<li><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>Protectkeywithcertifierkeybibprint</strong></a></li>
<li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>Protectkeywithexternalkey</strong></a></li>
<li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>Protectkeywithnumericalpassword</strong></a></li>
<li><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>Protectkeywithpasspphrase</strong></a></li>
<li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>Protectkeywithtpm</strong></a></li>
<li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>Protectkeywithtpmandpin</strong></a></li>
<li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>Protectkeywithtpmandpinandstartupkey</strong></a></li>
<li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>Protectkeywithtpmandstartupkey</strong></a></li>
</ul>
<br/> Für einen ehdd:<br/> Das Band für das Volume ist dauerhaft entsperrt, verfügt über keinen Schlüssel Manager oder wird von einem Drittanbieter-Schlüssel-Manager verwaltet.<br/> Dies kann auch bedeuten, dass das Band von BitLocker verwaltet wird, aber die <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>disablekeyprotector</strong></a> -Methode aufgerufen wurde und das Laufwerk angehalten wird.<br/></td>
</tr>
<tr class="even">
<td><span id="Protected"></span><span id="protected"></span><span id="PROTECTED"></span><dl> <dt><strong>Geschützt</strong></dt> <dt>1</dt> </dl></td>
<td>Schutz für<br/> Für eine Standard-HDD:<br/> Das Volume ist vollständig verschlüsselt, und der Verschlüsselungsschlüssel für das Volume ist nicht im Klartext auf der Festplatte verfügbar.<br/> Für einen ehdd:<br/> BitLocker ist der Schlüssel-Manager für das Band. Das Laufwerk kann gesperrt oder entsperrt, aber nicht dauerhaft entsperrt werden.<br/></td>
</tr>
<tr class="odd">
<td><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt><strong>Unbekannt</strong></dt> <dt>2</dt> </dl></td>
<td>Der volumeschutzstatus kann nicht bestimmt werden. Dies kann dadurch verursacht werden, dass sich das Volume im gesperrten Zustand befindet.<br/> <strong>Windows Vista Ultimate, Windows Vista Enterprise und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt. Dieser Wert wird ab Windows 7 und Windows Server 2008 R2 unterstützt.<br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                 | BESCHREIBUNG                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Die Methode war erfolgreich.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Sie können ein Volume nur verschlüsseln, wenn Sie zuerst [**disablekeyprotector**](disablekeyprotectors-win32-encryptablevolume.md) oder eine der folgenden Methoden verwenden:

-   [**Protectkeywithcertificatefile**](protectkeywithcertificatefile-win32-encryptablevolume.md)
-   [**Protectkeywithcertifierkeybibprint**](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
-   [**Protectkeywithexternalkey**](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [**Protectkeywithnumericalpassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md)
-   [**Protectkeywithpasspphrase**](protectkeywithpassphrase-win32-encryptablevolume.md)
-   [**Protectkeywithtpm**](protectkeywithtpm-win32-encryptablevolume.md)
-   [**Protectkeywithtpmandpin**](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [**Protectkeywithtpmandpinandstartupkey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [**Protectkeywithtpmandstartupkey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

Wenn der Datenträger verschlüsselt ist und der Schutz *Status* NULL (Schutz deaktiviert) zurückgibt, werden die Schlüssel daher deaktiviert.

Verwenden Sie [**getkeyprotector**](getkeyprotectors-win32-encryptablevolume.md) , um die Schlüssel Schutzvorrichtungen aufzulisten, die angegeben wurden, um den Verschlüsselungsschlüssel des Volumes zu sichern. Wenn Schlüssel Schutzvorrichtungen vorhanden sind, der Schutz aber 0 (null) ist, verwenden Sie [**enablekeyprotector**](enablekeyprotectors-win32-encryptablevolume.md) , um den volumeschutz zu aktivieren.

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

 

 
