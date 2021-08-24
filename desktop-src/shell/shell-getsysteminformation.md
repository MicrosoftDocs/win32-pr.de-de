---
description: 'Shell.GetSystemInformation-Methode: Ruft Systeminformationen ab.'
ms.assetid: 94C10DD6-FE49-4dd4-AEED-69B73A75EDEF
title: Shell.GetSystemInformation-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.GetSystemInformation
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 23ad48c673fb0c5925e796f77bd43c77f3abd0afd4511864a5b840214861f792
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660650"
---
# <a name="shellgetsysteminformation-method"></a>Shell.GetSystemInformation-Methode

Ruft Systeminformationen ab.

## <a name="syntax"></a>Syntax


```JScript
retVal = Shell.GetSystemInformation(
  sName
)
```


```VB

Shell.GetSystemInformation( _
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

## <a name="remarks"></a>Hinweise

Diese Methode kann verwendet werden, um viele Systeminformationswerte anzufordern. Die folgende Tabelle enthält den *sName-Wert,* der verwendet wird, um die Informationen und den zugeordneten Typ des zurückgegebenen Werts anzufordern.



*sName*

Rückgabetyp

BESCHREIBUNG

DirectoryServiceAvailable

**Boolean**

Legen Sie auf **TRUE** fest, wenn der Verzeichnisdienst verfügbar ist. andernfalls **FALSE.**

DoubleClickTime

**Integer**

Die Doppelklickzeit in Millisekunden.

ProcessorLevel

**Integer**

**Windows Vista und höher.** Die Prozessorebene. Gibt 3, 4 oder 5 für x386-, x486- bzw. Pentium-Prozessoren zurück.

ProcessorSpeed

**Integer**

Die Prozessorgeschwindigkeit in Megahertz (MHz).

ProcessorArchitecture

**Integer**

Die Prozessorarchitektur. Weitere Informationen finden Sie in der Erläuterung des **wProcessorArchitecture-Elements** der [**SYSTEM \_ INFO-Struktur.**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info)

PhysicalMemoryInstalled

**Integer**

Die Menge des installierten physischen Arbeitsspeichers in Bytes.

Folgendes gilt nur für Windows XP.

IsOS \_ Professional

**Boolean**

Wird auf **TRUE** festgelegt, wenn das Betriebssystem Windows XP Professional Edition ist. andernfalls **FALSE.**

IsOS \_ Personal

**Boolean**

Wird auf **TRUE** festgelegt, wenn das Betriebssystem Windows XP Home Edition ist. andernfalls **FALSE.**

Folgendes gilt nur für Windows XP und höher.

IsOS \_ DomainMember

**Boolean**

Legen Sie diese Einstellung auf **TRUE** fest, wenn der Computer Mitglied einer Domäne ist. andernfalls **FALSE.**



 

Diese Methode ist derzeit in Microsoft Visual Basic nicht verfügbar.

## <a name="examples"></a>Beispiele

Die folgenden Beispiele zeigen die Verwendung von **GetSystemInformation** für JScript und VBScript.

JScript:


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



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



 

 
