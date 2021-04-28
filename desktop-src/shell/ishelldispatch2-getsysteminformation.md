---
description: 'IShellDispatch2.GetSystemInformation-Methode: Ruft Systeminformationen ab.'
ms.assetid: 57c066e3-080f-4ecc-b56e-877f0569e901
title: IShellDispatch2.GetSystemInformation-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.GetSystemInformation
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a81ac091dc1905c1cbcd2c41575c907ce957e60c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117108"
---
# <a name="ishelldispatch2getsysteminformation-method"></a>IShellDispatch2.GetSystemInformation-Methode

Ruft Systeminformationen ab.

## <a name="syntax"></a>Syntax


```JScript
retVal = IShellDispatch2.GetSystemInformation(
  sName
)
```


```VB

IShellDispatch2.GetSystemInformation( _
  ByVal sName As BSTR _
) As Variant
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*sName* \[ In\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Eine **Zeichenfolge,** die die angeforderten Systeminformationen angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Typ: **Variant**

Gibt den Wert der angeforderten Systeminformationen zurück. Der Rückgabetyp hängt davon ab, welche Systeminformationen angefordert werden. Weitere Informationen finden Sie im Abschnitt Hinweise.

### <a name="vb"></a>VB

Typ: **Variant**

Gibt den Wert der angeforderten Systeminformationen zurück. Der Rückgabetyp hängt davon ab, welche Systeminformationen angefordert werden. Weitere Informationen finden Sie im Abschnitt Hinweise.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird implementiert und über die [**Shell.GetSystemInformation-Methode**](./shell-getsysteminformation.md) aufgerufen.

Diese Methode kann verwendet werden, um viele Systeminformationswerte an fordern. Die folgende Tabelle enthält den *sName-Wert,* der zum Anfordern der Informationen verwendet wird, und den zugeordneten Typ des zurückgegebenen Werts.



*sName*

Rückgabetyp

BESCHREIBUNG

DirectoryServiceAvailable

**Boolescher Wert**

Legen Sie auf **TRUE fest,** wenn der Verzeichnisdienst verfügbar ist. andernfalls **FALSE.**

DoubleClickTime

**Integer**

Die Doppelklickzeit in Millisekunden.

ProcessorLevel

**Integer**

**Windows Vista und höher.** Die Prozessorebene. Gibt für Prozessoren auf x386-, x486- und Pentium-Ebene 3, 4 oder 5 zurück.

ProcessorSpeed

**Integer**

Die Prozessorgeschwindigkeit in Megahertz (MHz).

ProcessorArchitecture

**Integer**

Die Prozessorarchitektur. Weitere Informationen finden Sie in der Erläuterung des **wProcessorArchitecture-Elements** der [**SYSTEM \_ INFO-Struktur.**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info)

PhysicalMemoryInstalled

**Integer**

Die Menge des installierten physischen Arbeitsspeichers in Bytes.

Die folgenden Sind nur unter Windows XP gültig.

IsOS \_ Professional

**Boolescher Wert**

Legen Sie diese Einstellung auf **TRUE** fest, wenn das Betriebssystem Windows XP Professional Edition ist. andernfalls **FALSE.**

IsOS \_ Personal

**Boolescher Wert**

Legen Sie diese Einstellung auf **TRUE** fest, wenn das Betriebssystem Windows XP Home Edition ist. andernfalls **FALSE.**

Folgendes ist nur unter Windows XP und höher gültig.

IsOS \_ DomainMember

**Boolescher Wert**

Wird auf **TRUE** festgelegt, wenn der Computer Mitglied einer Domäne ist. andernfalls **FALSE.**



 

Diese Methode ist derzeit in Microsoft Visual Basic nicht verfügbar.

## <a name="examples"></a>Beispiele

Die folgenden Beispiele zeigen die Verwendung von **GetSystemInformation** für JScript und VBScript.

Jscript:


```JScript
<script language="JavaScript">
    function fnGetSystemInformationJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;

        vReturn = objShell.GetSystemInformation("ProcessorLevel");
        document.write(vReturn);
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnGetSystemInformationVB()
        dim objShell
        dim vReturn

        set objShell = CreateObject("shell.application")

        vReturn = objShell.GetSystemInformation("ProcessorLevel")
        document.write(vReturn)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



 

 
