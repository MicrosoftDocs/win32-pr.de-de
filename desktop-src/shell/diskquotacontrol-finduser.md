---
description: Sucht den Eintrag eines Benutzers anhand des Namens in der Kontingent Datei des Volumes.
title: Diskquotacontrol. FINDUSER-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.FindUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e5767d28-4c0a-49bc-a1d3-ba809411456d
ms.openlocfilehash: af1bc9c0398d37f04e47515a2b85cb4520795b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977185"
---
# <a name="diskquotacontrolfinduser-method"></a>Diskquotacontrol. FINDUSER-Methode

Sucht den Eintrag eines Benutzers anhand des Namens in der Kontingent Datei des Volumes.

## <a name="syntax"></a>Syntax


```JScript
DiskQuotaControl.FindUser(
  sLogonName
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*slogonname* 
</dt> <dd>

Typ: **Zeichenfolge**

Ein Zeichen folgen Wert, der den Anmelde Namen des Benutzers enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Objekt Ausdruck zurück, der das [**didiskquotauser**](didiskquotauser-object.md) -Objekt des Benutzers ergibt.

## <a name="remarks"></a>Bemerkungen

Diese Methode gibt ein [**didiskquotauser**](didiskquotauser-object.md) -Objekt zurück, auch wenn in der Kontingent Datei kein Eintrag für den Benutzer vorhanden ist. Für das zurückgegebene Benutzerobjekt sind Warnungs Schwellenwert und feste Kontingent Limits auf die Standardwerte des Volumes festgelegt.

Die von [**translatelogonnametosid**](diskquotacontrol-translatelogonnametosid.md) zurückgegebene Zeichenfolge kann anstelle des *slogonname* -Parameters übergeben werden. Wenn **FINDUSER** eine SID-Zeichenfolge empfängt, wird die entsprechende sid für die direkte Suche des Kontingent Datensatzes des Benutzers auf dem Volume verwendet. Dadurch wird der SID-Name-Cache umgangen. In Fällen, in denen **FINDUSER** aufgrund eines Konflikts im Format (z. b. Sam-kompatibel und UPN) des bereitgestellten Anmelde namens und des zwischengespeicherten Anmelde namens ausfällt, kann der Anmelde Name mithilfe von **translatelogonnametosid** in eine SID-Zeichenfolge übersetzt werden und dann erneut an **FINDUSER** übergeben werden. Dieses Verfahren wird im folgenden VBScript-Code veranschaulicht.


```
Function Find(dqc, name)
    On Error Resume Next
    SET Find = dqc.FindUser(name)

    If Err.Number <> 0 Then
        Err.Clear
        SET Find = dqc.FindUser(dqc.TranslateLogonNameToSID(name))
    End If    

End Function
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5,0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Diskquotacontrol-Objekt**](diskquotacontrol-object.md)
</dt> </dl>

 

 




