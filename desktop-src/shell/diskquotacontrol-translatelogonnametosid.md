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
ms.openlocfilehash: 6bcaa5ac4f7dff4be80763b0aa411b7f104ff786b21e422044bdc7198697d54c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111820"
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

Gibt die Benutzersicherheits-ID (SID) im Zeichenfolgenformat zurück, das dem angegebenen Anmeldenamen entspricht. Die zurückgegebene Zeichenfolge enthält die standardmäßig einschließenden geschweiften Klammern. Beispiel:

"{S-1-5-21-2127521184-1604012920-1887927527-19009}"

## <a name="remarks"></a>Hinweise

Die zurückgegebene SID-Zeichenfolge kann anstelle eines Anmeldenamens an die [**FindUser-Methode**](diskquotacontrol-finduser.md) übergeben werden.

Wenn bei einem Aufruf der [**FindUser**](diskquotacontrol-finduser.md)-Methode ( *Anmeldename*) ein Fehler auftritt, kann dies auf einen Konflikt zwischen dem Formular (z. B. SAM-kompatibel mit dem Sicherheitskonto-Manager \[ und dem \] Benutzerprinzipalnamen-UPN) \[ des \] angegebenen Anmeldenamens und dem im SID-Namencache gespeicherten Formular zurückzuführen sein. In solchen Fällen kann der Anmeldename in eine SID konvertiert und der Aufruf von **FindUser** wiederholt werden. **FindUser** erkennt eine SID-Zeichenfolge und umgeht die Cachesuche des SID-Namens. Dieses Verfahren wird im folgenden VbScript-Code (Microsoft Visual Basic Scripting Edition) veranschaulicht.


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



Die Übersetzung von Name zu SID kann im Vergleich zu Suchfunktionen im SID-Namencache ein langsamer Prozess sein. Aus diesem Grund wird empfohlen, [**findUser**](diskquotacontrol-finduser.md) zuerst mit einem Anmeldenamen aufzuweisen. Im obigen Beispiel wird diese Technik verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DiskQuotaControl-Objekt**](diskquotacontrol-object.md)
</dt> </dl>

 

 




