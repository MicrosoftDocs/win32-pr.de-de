---
description: Ruft Systeminformationen ab.
ms.assetid: 94C10DD6-FE49-4dd4-AEED-69B73A75EDEF
title: Shell. getsysteminformation-Methode (Shldisp. h)
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
ms.openlocfilehash: 2ad7a865ba6ac5b62bc8a9b5ac105c0ef166d574
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980625"
---
# <a name="shellgetsysteminformation-method"></a>Shell. getsysteminformation-Methode

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

*sname* \[ in\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Eine **Zeichenfolge** , die die angeforderten Systeminformationen angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Typ: **Variant**

Gibt den Wert der angeforderten Systeminformationen zurück. Der Rückgabetyp hängt davon ab, welche Systeminformationen angefordert werden. Weitere Informationen finden Sie im Abschnitt Hinweise.

### <a name="vb"></a>VB

Typ: **Variant**

Gibt den Wert der angeforderten Systeminformationen zurück. Der Rückgabetyp hängt davon ab, welche Systeminformationen angefordert werden. Weitere Informationen finden Sie im Abschnitt Hinweise.

## <a name="remarks"></a>Bemerkungen

Diese Methode kann verwendet werden, um viele System Informationswerte anzufordern. In der folgenden Tabelle wird der *sname* -Wert, der zum Anfordern der Informationen verwendet wird, und der zugehörige Typ des zurückgegebenen Werts angezeigt.



*sName*

Rückgabetyp

BESCHREIBUNG

Director Service Available

**Boolescher Wert**

Auf " **true** " festgelegt, wenn der Verzeichnisdienst verfügbar ist. andernfalls **false**.

DoubleClickTime

**Integer**

Die Doppelklick Zeit in Millisekunden.

ProcessorLevel

**Integer**

**Windows Vista und** höher. Die Prozessor Ebene. Gibt 3, 4 oder 5 für Prozessoren der x386-, x486-und Pentium-Ebene zurück.

ProcessorSpeed

**Integer**

Die Prozessorgeschwindigkeit in Megahertz (MHz).

ProcessorArchitecture

**Integer**

Die Prozessorarchitektur. Weitere Informationen finden Sie in der Erörterung des **wprocessorarchitecture** -Members der [**System \_ Info**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) -Struktur.

Physicalmemoryinstalliert

**Integer**

Die Menge des installierten physischen Speichers in Bytes.

Folgendes gilt nur für Windows XP.

ISOS \_ Professional

**Boolescher Wert**

Auf " **true** " festgelegt, wenn das Betriebssystem Windows XP Professional Edition ist. andernfalls **false**.

ISOS \_ persönlich

**Boolescher Wert**

Auf " **true** " festgelegt, wenn das Betriebssystem Windows XP Home Edition ist. andernfalls **false**.

Folgendes gilt nur für Windows XP und höher.

ISOS- \_ domainmember

**Boolescher Wert**

Auf " **true** " festgelegt, wenn der Computer Mitglied einer Domäne ist. andernfalls **false**.



 

Diese Methode ist zurzeit nicht in Microsoft Visual Basic verfügbar.

## <a name="examples"></a>Beispiele

In den folgenden Beispielen wird die Verwendung von **getsysteminformation** für JScript und VBScript veranschaulicht.

JScript


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



VBScript


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



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5,0 oder höher)</dt> </dl> |



 

 
