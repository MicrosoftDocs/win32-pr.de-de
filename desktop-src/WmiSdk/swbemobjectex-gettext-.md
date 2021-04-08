---
description: Gibt eine XML-Darstellung eines Objekts oder einer Instanz zurück. Die Textdatei wird im angegebenen XML-Format formatiert, wie in wbemubjecttextformatenum gezeigt.
ms.assetid: 98961d94-8360-4ed7-b1b1-20b4fca45d45
ms.tgt_platform: multiple
title: SWbemObjectEx.GetText_-Methode (wbemdisp. h)
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
ms.openlocfilehash: 6f174397b1ace85acd90ffe3def6b8122bf8d7f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050467"
---
# <a name="swbemobjectexgettext_-method"></a>Methode ' errbemubjectex. gettext ' \_

Die **gettext \_** -Methode des " [**errbemubjectex**](swbemobjectex.md) "-Objekts gibt eine XML-Darstellung eines Objekts oder einer Instanz zurück. Die Textdatei wird im angegebenen XML-Format formatiert, wie in [**wbemubjecttextformatenum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)gezeigt.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

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

*itextformat* \[ in\]
</dt> <dd>

Erforderlich. Ein Wert aus [**wbemubjecttextformatenum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum) , der das resultierende XML-Format angibt.

</dd> <dt>

*IFlags* \[ in, optional\]
</dt> <dd>

Reservierte Vorgangs-Flags. Der Standardwert ist 0 (null).

</dd> <dt>

*objwbemnamedvalueset* \[ in, optional\]
</dt> <dd>

Ein [**-**](swbemnamedvalueset.md) Objekt, das den Kontext für den Vorgang festlegt. Der Standardwert ist NULL. Weitere Informationen zu den zulässigen Name-Wert-Paaren finden Sie unten in den hinweisen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode hat keine Rückgabewerte.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **gettext \_** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)
</dt> <dd>

Das angeforderte Format wurde nicht gefunden.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Einer der Parameter für den Aufruf ist nicht korrekt.

</dd> <dt>

**wbemErrCriticalError** -2147749898 (0x8004100a)
</dt> <dd>

Ein interner, schwerwiegender und unerwarteter Fehler ist aufgetreten. Melden Sie diesen Fehler dem technischen Support von Microsoft.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Beim Erstellen des " [**Swap**](swbemnamedvalueset.md)Name/Value"-Paars sind nur die folgenden Name/Wert-Paare zulässig.



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
<td>LocalOnly</td>
<td><strong>VT_BOOL</strong><br/> <strong>True</strong>gibt an, dass nur lokal definierte Eigenschaften und Methoden im resultierenden XML-Code vorhanden sind. Der Standardwert ist <strong>false</strong>.<br/></td>
</tr>
<tr class="even">
<td>Includezqualifizierer</td>
<td><strong>VT_BOOL</strong><br/> <strong>True</strong>gibt an, dass Qualifizierer von Klassen, Instanzen, Eigenschaften und Methoden im resultierenden XML-Code enthalten sind. Der Standardwert ist <strong>false</strong>.<br/></td>
</tr>
<tr class="odd">
<td>Pathlevel</td>
<td><strong>VT-I4</strong><br/> Der Standardwert ist 0 (null). Dabei sind folgende Werte möglich:<br/>
<ul>
<li>0: abhängig davon, <CLASS> <INSTANCE> ob das Objekt eine Klasse oder eine Instanz ist, wird ein-oder-Element erstellt.</li>
<li>1: ein- <VALUE.NAMEDOBJECT> Element wird generiert.</li>
<li>2: ein- <VALUE.OBJECTWITHLOCALPATH> Element wird generiert.</li>
<li>3: ein- <VALUE.OBJECTWITHPATH> Element wird generiert.</li>
</ul></td>
</tr>
<tr class="even">
<td>Excludebug SystemProperties</td>
<td><strong>VT-bool</strong><br/> <strong>True</strong>gibt an, dass Systemeigenschaften wie __NAMESPACE aus der Ausgabe ausgeschlossen werden.<br/></td>
</tr>
<tr class="odd">
<td>Includeclassorigin</td>
<td><strong>VT_BOOL</strong><br/> Wenn <strong>true</strong>, wird das Klassen Ursprungs Attribut für das <PROPERTY> -Element und das-Element festgelegt <METHOD> . Der Standardwert ist <strong>false</strong>.<br/></td>
</tr>
</tbody>
</table>



 

Weitere Informationen zum Erstellen eines " [**taubemnamedvalueset**](swbemnamedvalueset.md)" finden [**Sie unter "austauschen von namedvalueset. Add**](swbemnamedvalueset-add.md)".

## <a name="examples"></a>Beispiele

Das folgende Skript zeigt, wie eine XML-Darstellung der [**Win32- \_ BIOS**](/windows/desktop/CIMWin32Prov/win32-bios) -Klassendefinition abgerufen wird. Wenn Sie eine bestimmte Instanz des **Win32- \_ BIOS** angeben, können Sie die Daten dieses Objekts in XML abrufen.


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
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Swap-Austausch<br/>                                                         |
| IID<br/>                      | IID \_ iswbejebjectex<br/>                                                          |



 

