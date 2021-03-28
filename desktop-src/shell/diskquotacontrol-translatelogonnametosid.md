---
description: Übersetzt einen Anmelde Namen in die entsprechende Benutzersicherheits-ID im Zeichen folgen Format.
title: Diskquotacontrol. translatelogonnametosid-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.TranslateLogonNameToSID
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3b6b0d03-e9ef-4575-bb67-f7b7b39d2a16
ms.openlocfilehash: ec5e6c0bbd013c8fbd3f6616671ee006109566d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042571"
---
# <a name="diskquotacontroltranslatelogonnametosid-method"></a>Diskquotacontrol. translatelogonnametosid-Methode

Übersetzt einen Anmelde Namen in die entsprechende Benutzersicherheits-ID im Zeichen folgen Format.

## <a name="syntax"></a>Syntax


```JScript
DiskQuotaControl.TranslateLogonNameToSID(
  logonname
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Anmelde Name* 
</dt> <dd>

Typ: **Zeichenfolge**

Ein Zeichen folgen Wert, der den Anmelde Namen des Benutzers angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Benutzer Sicherheits-ID (SID) im Zeichen folgen Format zurück, das dem angegebenen Anmelde Namen entspricht. Die zurückgegebene Zeichenfolge enthält die standardmäßigen schließenden geschweiften Klammern. Beispiel:

"{S-1-5-21-2127521184-1604012920-1887927527-19009}"

## <a name="remarks"></a>Bemerkungen

Die zurückgegebene SID-Zeichenfolge kann anstelle eines Anmelde namens an die [**FINDUSER**](diskquotacontrol-finduser.md) -Methode übergeben werden.

Wenn beim Aufrufen der Methode [**FINDUSER**](diskquotacontrol-finduser.md)( *Logonname*) ein Fehler auftritt, kann dies auf einen Konflikt zwischen dem Formular (z. b. dem Sicherheits Konto \[ -Manager SAM \] -kompatibel und dem Benutzer Prinzipal Namen- \[ UPN \] ) des angegebenen Anmelde namens und der im sid-Name-Cache gespeicherten Form zurückzuführen sein. In solchen Fällen kann der Anmelde Name in eine SID konvertiert werden, und der **FINDUSER** -Befehl wird wiederholt. **FINDUSER** erkennt eine SID-Zeichenfolge und umgeht die Cache Suche mit dem SID-Namen. Der folgende Microsoft Visual Basic Scripting Edition-Code (VBScript) veranschaulicht diese Vorgehensweise.


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



Die Namens-zu-sid-Übersetzung kann im Vergleich zu Such Vorgängen im Cache für sid-Namen ein langsamer Prozess sein. Daher wird empfohlen, dass [**FINDUSER**](diskquotacontrol-finduser.md) zuerst mit einem Anmelde Namen aufgerufen wird. Im obigen Beispiel wird diese Technik verwendet.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5,0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Diskquotacontrol-Objekt**](diskquotacontrol-object.md)
</dt> </dl>

 

 




