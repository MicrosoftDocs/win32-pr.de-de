---
description: Übersetzt einen Anmeldenamen in die entsprechende Benutzersicherheits-ID im Zeichenfolgenformat.
title: DiskQuotaControl.TranslateLogonNameToSID-Methode
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
ms.openlocfilehash: 5f0a2591b0f5df6bc0f50994fcbf101b7bfbb36d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841561"
---
# <a name="diskquotacontroltranslatelogonnametosid-method"></a>DiskQuotaControl.TranslateLogonNameToSID-Methode

Übersetzt einen Anmeldenamen in die entsprechende Benutzersicherheits-ID im Zeichenfolgenformat.

## <a name="syntax"></a>Syntax


```JScript
DiskQuotaControl.TranslateLogonNameToSID(
  logonname
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Anmeldename* 
</dt> <dd>

Typ: **Zeichenfolge**

Ein Zeichenfolgenwert, der den Anmeldenamen des Benutzers angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Benutzersicherheits-ID (SID) im Zeichenfolgenformat zurück, das dem angegebenen Anmeldenamen entspricht. Die zurückgegebene Zeichenfolge enthält die standardmäßigen umschließenden geschweiften Klammern. Zum Beispiel:

"{S-1-5-21-2127521184-1604012920-1887927527-19009}"

## <a name="remarks"></a>Hinweise

Die zurückgegebene SID-Zeichenfolge kann statt eines Anmeldenamens an die [**FindUser-Methode**](diskquotacontrol-finduser.md) übergeben werden.

Wenn bei einem Aufruf der [**FindUser-Methode**](diskquotacontrol-finduser.md) *(logonname)* ein Fehler auftritt, kann dies auf einen Konflikt zwischen dem Formular (z. B. SAM-kompatibel mit dem Sicherheitskonto-Manager und dem \[ \] \[ Benutzerprinzipalnamen-UPN) des bereitgestellten Anmeldenamens und dem im SID-Namenscache gespeicherten Formular \] liegen. In solchen Fällen kann der Anmeldename in eine SID konvertiert und der Aufruf von **FindUser wiederholt** werden. **FindUser** erkennt eine SID-Zeichenfolge und umgeht die Cachesuche nach SID-Namen. Der folgende Code Visual Basic Scripting Edition (VBScript) von Microsoft veranschaulicht diese Technik.


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



Die Namens-zu-SID-Übersetzung kann im Vergleich zu Suchen im SID-Namenscache ein langsamer Prozess sein. Daher empfiehlt es sich, [**FindUser**](diskquotacontrol-finduser.md) zuerst mit einem Anmeldenamen auf zu nennen. Im obigen Beispiel wird diese Technik verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DiskQuotaControl-Objekt**](diskquotacontrol-object.md)
</dt> </dl>

 

 




