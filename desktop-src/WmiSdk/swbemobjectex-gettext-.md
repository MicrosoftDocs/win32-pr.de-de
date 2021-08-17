---
description: Gibt eine XML-Darstellung eines Objekts oder einer Instanz zurück. Die Textdatei ist im XML-Format formatiert, das in WbemObjectTextFormatEnum angegeben ist.
ms.assetid: 98961d94-8360-4ed7-b1b1-20b4fca45d45
ms.tgt_platform: multiple
title: SWbemObjectEx.GetText_ -Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.GetText_
- ISWbemObjectEx.GetText_
- ISWbemObjectEx.GetText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8feace72eeb51ed0904ad748892ca3c1b3adea9c8ca6c97ac7a76ea11890dd08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117922428"
---
# <a name="swbemobjectexgettext_-method"></a>SWbemObjectEx.GetText-Methode \_

Die **GetText-Methode \_** des [**SWbemObjectEx-Objekts**](swbemobjectex.md) gibt eine XML-Darstellung eines Objekts oder einer Instanz zurück. Die Textdatei ist im XML-Format formatiert, das in [**WbemObjectTextFormatEnum angegeben ist.**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
strObj = .GetText_( _
  ByVal iTextFormat, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*iTextFormat* \[ In\]
</dt> <dd>

Erforderlich. Ein Wert aus [**WbemObjectTextFormatEnum,**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum) der das resultierende XML-Format angibt.

</dd> <dt>

*iFlags* \[ in, optional\]
</dt> <dd>

Reservierte Vorgangsflags. Der Standardwert ist 0 (null).

</dd> <dt>

*objWbemNamedValueSet* \[ in, optional\]
</dt> <dd>

Ein [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) das den Kontext für den Vorgang fest legt. Der Standardwert ist NULL. Weitere Informationen zu den zulässigen Name-Wert-Paaren finden Sie weiter unten in den Anmerkungen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode verfügt über keine Rückgabewerte.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **GetText-Methode \_** kann das **Err-Objekt** einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrNotFound** – 2147749890 (0x80041002)
</dt> <dd>

Das angeforderte Format wurde nicht gefunden.

</dd> <dt>

**wbemErrInvalidParameter** – 2147749896 (0x80041008)
</dt> <dd>

Einer der Parameter für den Aufruf ist nicht korrekt.

</dd> <dt>

**wbemErrCriticalError** – 2147749898 (0x8004100A)
</dt> <dd>

Ein interner, schwerwiegender und unerwarteter Fehler ist aufgetreten. Melden Sie diesen Fehler dem technischen Support von Microsoft.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Beim Erstellen ihres [**SWbemNamedValueSet**](swbemnamedvalueset.md)sind nur die folgenden Name-Wert-Paare zulässig.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Name</th>
<th>Wert</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Localonly</td>
<td><strong>VT_BOOL</strong><br/> True <strong>gibt an,</strong>dass nur lokal definierte Eigenschaften und Methoden im resultierenden XML-Code vorhanden sind. Der Standardwert ist <strong>FALSE.</strong><br/></td>
</tr>
<tr class="even">
<td>IncludeQualifiers</td>
<td><strong>VT_BOOL</strong><br/> True <strong>gibt</strong>an, dass Qualifizierer von Klassen, Instanzen, Eigenschaften und Methoden im resultierenden XML-Code enthalten sind. Der Standardwert ist <strong>FALSE.</strong><br/></td>
</tr>
<tr class="odd">
<td>PathLevel</td>
<td><strong>VT-I4</strong><br/> Der Standardwert ist 0 (null). Mögliche Werte:<br/>
<ul>
<li>0: Ein <CLASS> - oder <INSTANCE> -Element wird erstellt, je nachdem, ob das Objekt eine Klasse oder Instanz ist.</li>
<li>1: Ein <VALUE.NAMEDOBJECT> -Element wird generiert.</li>
<li>2: Ein <VALUE.OBJECTWITHLOCALPATH> -Element wird generiert.</li>
<li>3: Ein <VALUE.OBJECTWITHPATH> -Element wird generiert.</li>
</ul></td>
</tr>
<tr class="even">
<td>ExcludeSystemProperties</td>
<td><strong>VT-BOOL</strong><br/> True <strong>gibt</strong>an, dass Systemeigenschaften wie __NAMESPACE aus der Ausgabe ausgeschlossen werden.<br/></td>
</tr>
<tr class="odd">
<td>IncludeClassOrigin</td>
<td><strong>VT_BOOL</strong><br/> True <strong>gibt an,</strong>dass das Ursprungsattribut der Klasse für die Elemente <PROPERTY> und festgelegt <METHOD> wird. Der Standardwert ist <strong>FALSE.</strong><br/></td>
</tr>
</tbody>
</table>



 

Weitere Informationen zum Erstellen eines [**SWbemNamedValueSet**](swbemnamedvalueset.md)finden Sie unter [**SWbemNamedValueSet.Add.**](swbemnamedvalueset-add.md)

## <a name="examples"></a>Beispiele

Das folgende Skript zeigt, wie Sie eine XML-Darstellung der [**Win32 \_ Bios-Klassendefinition**](/windows/desktop/CIMWin32Prov/win32-bios) abrufen. Durch Angeben einer bestimmten Instanz von **Win32 \_ Bios** können Sie die Daten dieses Objekts in XML abrufen.


```VB
' Connect to the default namespace (root\cimv2) with the default
' impersonation level ("impersonate") and obtain a Win32_Bios class
' object.
Set obj = GetObject("winmgmts:win32_bios")

' Use the value for the desired XML CIM DTD format. 
XMLDtd = 1
Text = obj.GetText_(XMLDtd)
wscript.echo Text
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectEx<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemObjectEx<br/>                                                          |



 

