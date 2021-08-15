---
description: Gibt an, ob das Volume und sein Verschlüsselungsschlüssel gesichert sind.
ms.assetid: bcd8fce5-da39-4aa8-93ff-0768deb900ec
title: GetProtectionStatus-Methode der Win32_EncryptableVolume-Klasse
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
ms.openlocfilehash: 44fde17ee8e7d4d7bacd5c63743af045f89e16f840c193df8d883a5c80111659
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891872"
---
# <a name="getprotectionstatus-method-of-the-win32_encryptablevolume-class"></a>GetProtectionStatus-Methode der Win32 \_ EncryptableVolume-Klasse

Die **GetProtectionStatus-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) gibt an, ob das Volume und sein Verschlüsselungsschlüssel (sofern vorhanden) geschützt sind.

Der Schutz ist deaktiviert, wenn ein Volume unverschlüsselt oder teilweise verschlüsselt ist oder wenn der Verschlüsselungsschlüssel des Volumes auf der Festplatte unverschlüsselt verfügbar ist.

## <a name="syntax"></a>Syntax


```mof
uint32 GetProtectionStatus(
  [out] uint32 ProtectionStatus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ProtectionStatus* \[ out\]
</dt> <dd>

Typ: **uint32**

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
<td><span id="Unprotected"></span><span id="unprotected"></span><span id="UNPROTECTED"></span><dl> <dt><strong>Ungeschützte 0</strong></dt> <dt></dt> </dl></td>
<td>SCHUTZ AUS<br/> Für eine HDD-Standard-Festplatte:<br/> Das Volume ist unverschlüsselt, teilweise verschlüsselt, oder der Verschlüsselungsschlüssel des Volumes ist im Klartext auf der Festplatte verfügbar. Der Verschlüsselungsschlüssel ist auf der Festplatte im Klartext verfügbar, wenn Schlüsselschutzvorrichtungen mithilfe der <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors-Methode</strong></a> deaktiviert wurden oder wenn keine Schlüsselschutzvorrichtungen mithilfe der folgenden Methoden angegeben wurden:
<ul>
<li><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateFile</strong></a></li>
<li><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateThumbprint</strong></a></li>
<li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li>
<li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li>
<li><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>ProtectKeyWithPassphrase</strong></a></li>
<li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li>
<li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li>
<li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></li>
<li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li>
</ul>
<br/> Für eine EHDD:<br/> Das Band für das Volume wird unbefristet entsperrt, verfügt über keinen Schlüssel-Manager oder wird von einem Schlüssel-Manager eines Drittanbieters verwaltet.<br/> Dies kann auch bedeuten, dass das Band von BitLocker verwaltet wird, aber die <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors-Methode</strong></a> aufgerufen wurde und das Laufwerk angehalten wird.<br/></td>
</tr>
<tr class="even">
<td><span id="Protected"></span><span id="protected"></span><span id="PROTECTED"></span><dl> <dt><strong>Geschützt</strong></dt> <dt>1</dt> </dl></td>
<td>SCHUTZ EIN<br/> Für eine HDD-Standard-Festplatte:<br/> Das Volume ist vollständig verschlüsselt, und der Verschlüsselungsschlüssel für das Volume ist auf der Festplatte nicht im Klartext verfügbar.<br/> Für eine EHDD:<br/> BitLocker ist der Schlüssel-Manager für das Band. Das Laufwerk kann gesperrt oder entsperrt, aber nicht unbefristet entsperrt werden.<br/></td>
</tr>
<tr class="odd">
<td><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt><strong>Unbekannt</strong></dt> <dt>2</dt> </dl></td>
<td>Der Volumeschutzstatus kann nicht bestimmt werden. Dies kann darauf zurückzuführen sein, dass sich das Volume in einem gesperrten Zustand befindet.<br/> <strong>Windows Vista Ultimate, Windows Vista Enterprise und Windows Server 2008:</strong> Dieser Wert wird nicht unterstützt. Dieser Wert wird ab Windows 7 und Windows Server 2008 R2 unterstützt.<br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn er fehlschlägt.



| Rückgabecode/-wert                                                                                                                                 | BESCHREIBUNG                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Die Methode war erfolgreich.<br/> |



 

## <a name="remarks"></a>Hinweise

Sie können ein Volume nur verschlüsseln, wenn Sie entweder [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) zuerst aufrufen oder eine der folgenden Methoden verwenden:

-   [**ProtectKeyWithCertificateFile**](protectkeywithcertificatefile-win32-encryptablevolume.md)
-   [**ProtectKeyWithCertificateThumbprint**](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
-   [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md)
-   [**ProtectKeyWithPassphrase**](protectkeywithpassphrase-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPM**](protectkeywithtpm-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPIN**](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPINAndStartupKey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndStartupKey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

Wenn der Datenträger verschlüsselt ist und *ProtectionStatus* 0 (PROTECTION OFF) zurückgibt, werden Schlüssel daher deaktiviert.

Verwenden Sie [**GetKeyProtectors,**](getkeyprotectors-win32-encryptablevolume.md) um die Schlüsselschutzvorrichtungen aufzulisten, die zum Sichern des Verschlüsselungsschlüssels des Volumes angegeben wurden. Wenn Schlüsselschutzvorrichtungen vorhanden sind, aber der Schutz 0 (PROTECTION OFF) ist, verwenden [**Sie EnableKeyProtectors,**](enablekeyprotectors-win32-encryptablevolume.md) um den Volumeschutz zu aktivieren.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

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

 

 
