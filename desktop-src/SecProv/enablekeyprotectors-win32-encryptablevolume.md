---
description: Aktiviert oder setzt alle deaktivierten oder angehaltenen Schlüsselschutz Vorrichtungen fort.
ms.assetid: 6f5a17a3-84f2-43a0-a85f-1037cd52439a
title: Enablekeyprotector-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EnableKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 78f8502ae141458f1ae46a48d21c110b9434acd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354451"
---
# <a name="enablekeyprotectors-method-of-the-win32_encryptablevolume-class"></a>Enablekeyprotector-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **enablekeyprotector** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " aktiviert oder setzt alle deaktivierten oder angehaltenen Schlüsselschutz Vorrichtungen fort. Mit dieser Methode können Sie den BitLocker-Schutz auf einem verschlüsselten Volume erneut aktivieren oder fortsetzen. Mit dieser Methode wird sichergestellt, dass der Verschlüsselungsschlüssel des Volumes nicht im Klartext auf der Festplatte verfügbar gemacht wird.

> [!Note]  
> Wenn die Festplatte die Hardware Verschlüsselung unterstützt, wechselt der Status des Bands von "immer entsperrt" in "entsperrt".

 

## <a name="syntax"></a>Syntax


```mof
uint32 EnableKeyProtectors();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.

Wenn die Schlüssel Schutzvorrichtungen bereits aktiviert sind und keine weiteren Fehler auftreten, gibt diese Methode 0 (null) zurück.



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
<td><dl> <dt><strong>FVE_E_SECURE_KEY_REQUIRED</strong></dt> <dt>2150694919 (0x80310007)</dt> </dl></td>
<td>Auf dem Volume sind keine Schlüssel Schutzvorrichtungen vorhanden. Verwenden Sie eine der folgenden Methoden, um Schlüssel Schutzvorrichtungen für das Volume anzugeben:<br/>
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
</ul></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_NOT_ACTIVATED</strong></dt> <dt>2150694920 (0x80310008)</dt> </dl></td>
<td>BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Bemerkungen

Wenn das Volume vollständig verschlüsselt ist, wird durch das erfolgreiche Ausführen dieser Methode sichergestellt, dass das Volume geschützt ist. Wenn das Volume teilweise verschlüsselt ist, bedeutet eine erfolgreiche Ausführung dieser Methode, dass das Volume geschützt wird, sobald es vollständig verschlüsselt wird. Weitere Informationen finden Sie unter der [**getschutzstatus**](getprotectionstatus-win32-encryptablevolume.md) -Methode.

Wenn TPM-basierte Schlüssel Schutzvorrichtungen für das Volume vorhanden sind, werden diese Schutzvorrichtungen beim erfolgreichen Ausführen dieser Methode ebenfalls aktualisiert, damit das TPM die aktuellen Start Dienste auf der Plattform überprüft. Anders ausgedrückt: Sie bestätigen, dass der Status des aktuellen Computers der richtige Zustand ist, den das TPM bei zukünftigen Neustarts des Computers prüft.

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
</dt> <dt>

[**Disablekeyprotector**](disablekeyprotectors-win32-encryptablevolume.md)
</dt> <dt>

[**Protectkeywithcertificatefile**](protectkeywithcertificatefile-win32-encryptablevolume.md)
</dt> <dt>

[**Protectkeywithcertifierkeybibprint**](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
</dt> <dt>

[**Protectkeywithexternalkey**](protectkeywithexternalkey-win32-encryptablevolume.md)
</dt> <dt>

[**Protectkeywithnumericalpassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md)
</dt> <dt>

[**Protectkeywithpasspphrase**](protectkeywithpassphrase-win32-encryptablevolume.md)
</dt> <dt>

[**Protectkeywithtpm**](protectkeywithtpm-win32-encryptablevolume.md)
</dt> <dt>

[**Protectkeywithtpmandpin**](protectkeywithtpmandpin-win32-encryptablevolume.md)
</dt> <dt>

[**Protectkeywithtpmandpinandstartupkey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
</dt> <dt>

[**Protectkeywithtpmandstartupkey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)
</dt> </dl>

 

 
