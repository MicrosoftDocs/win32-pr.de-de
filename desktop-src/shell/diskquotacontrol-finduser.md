---
description: Sucht den Eintrag eines Benutzers anhand des Namens in der Kontingentdatei des Volumes.
title: DiskQuotaControl.FindUser-Methode
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
ms.openlocfilehash: eab539a5ec5a360ae28fc87d5ffbb9dd4f9f1cc8
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841521"
---
# <a name="diskquotacontrolfinduser-method"></a>DiskQuotaControl.FindUser-Methode

Sucht den Eintrag eines Benutzers anhand des Namens in der Kontingentdatei des Volumes.

## <a name="syntax"></a>Syntax


```JScript
DiskQuotaControl.FindUser(
  sLogonName
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sLogonName* 
</dt> <dd>

Typ: **Zeichenfolge**

Ein Zeichenfolgenwert, der den Anmeldenamen des Benutzers enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Objektausdruck zurück, der das [**DIDiskQuotaUser-Objekt**](didiskquotauser-object.md) des Benutzers ergibt.

## <a name="remarks"></a>Hinweise

Diese Methode gibt ein [**DIDiskQuotaUser-Objekt**](didiskquotauser-object.md) zurück, auch wenn kein Eintrag für den Benutzer in der Kontingentdatei vorhanden ist. Für das zurückgegebene Benutzerobjekt sind warnungsschwellenwert und harte Kontingentgrenzen auf die Standardwerte des Volumes festgelegt.

Die von [**TranslateLogonNameToSID**](diskquotacontrol-translatelogonnametosid.md) zurückgegebene Zeichenfolge kann anstelle des *sLogonName-Parameters* übergeben werden. Wenn **FindUser** eine SID-Zeichenfolge empfängt, verwendet er die entsprechende SID für die direkte Suche des Kontingentdatensatzes des Benutzers auf dem Volume. Dadurch wird der SID-Name-Cache umgangen. In Fällen, in denen **FindUser** aufgrund eines Konflikts im Format (z. B. SAM-kompatibel und UPN) des angegebenen Anmeldenamens und des zwischengespeicherten Anmeldenamens fehlschlägt, kann der Anmeldename mit **TranslateLogonNameToSID** in eine SID-Zeichenfolge übersetzt und dann erneut an **FindUser** übergeben werden. Dies wird im folgenden VBScript-Code veranschaulicht.


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



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DiskQuotaControl-Objekt**](diskquotacontrol-object.md)
</dt> </dl>

 

 




