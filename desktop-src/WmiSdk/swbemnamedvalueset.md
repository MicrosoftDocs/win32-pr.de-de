---
description: Ein SWbemNamedValueSet-Objekt ist eine Sammlung von SWbemNamedValue-Objekten.
ms.assetid: 7d1c3a28-d0d3-4108-9628-74ad483e328e
ms.tgt_platform: multiple
title: SWbemNamedValueSet-Objekt (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet
- ISWbemNamedValueSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cfdcc3ba2bde6dfdfd0cc732e4376ceb69ba60904f4d787d9030299c248ebb62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732670"
---
# <a name="swbemnamedvalueset-object"></a>SWbemNamedValueSet-Objekt

Ein **SWbemNamedValueSet-Objekt** ist eine Sammlung von [**SWbemNamedValue-Objekten.**](swbemnamedvalue.md) Die Methoden und Eigenschaften von **SWbemNamedValueSet** werden hauptsächlich verwendet, um weitere Informationen an Anbieter zu senden, wenn bestimmte Aufrufe an WMI gesendet werden. Alle Aufrufe in [**SWbemServices**](swbemservices.md)und einige Aufrufe in [**SWbemObject**](swbemobject.md)verwenden einen optionalen Parameter, der ein Objekt dieses Typs ist. Ein Client kann einem **SWbemNamedValueSet-Objekt** Informationen hinzufügen und das **SWbemNamedValueSet-Objekt** mit dem Aufruf als einen der Parameter senden. Dieses Objekt kann durch den VBScript **CreateObject-Aufruf erstellt** werden.

Weitere Informationen finden Sie unter [Zugreifen auf eine Auflistung.](accessing-a-collection.md)

> [!Note]  
> Wichtig: Verwenden Sie diesen Mechanismus nach Möglichkeit nicht, da er das einheitliche Zugriffsmodell, das die Grundlage von WMI ist, unterbricht. Wenn ein Anbieter diesen Mechanismus verwendet, ist es wichtig, dass dieser Mechanismus so wenig wie möglich verwendet wird. Wenn ein Anbieter eine große Menge hochspezifischer Kontextinformationen benötigt, um auf eine Anforderung zu reagieren, müssen alle Clients codiert werden, um diese Informationen bereitstellen zu können. Mit diesem Mechanismus können Sie bei Bedarf auf solche Anbieter zugreifen.

 

Ein **SWbemNamedValueSet-Objekt** ist eine Sammlung von [**SWbemNamedValue-Elementen.**](swbemnamedvalue.md) Diese Elemente werden der Auflistung mithilfe der [**SWbemNamedValueSet.Add-Methode**](swbemnamedvalueset-add.md) hinzugefügt. Sie werden mithilfe der [**SWbemNamedValueSet.Remove-Methode**](swbemnamedvalueset-remove.md) entfernt und mithilfe der [**SWbemNamedValueSet.Item-Methode**](swbemnamedvalueset-item.md) abgerufen. Sie können auf die Methoden zugreifen, um alle Kontextinformationen einfüllen zu können, die für einen dynamischen Anbieter erforderlich sind. Nachdem Sie eine der [**SWbemServices-Methoden**](swbemservices.md) aufrufen, können Sie das **SWbemNamedValueSet-Objekt** für einen anderen Aufruf wiederverwenden.

Der zugrunde liegende Anbieter bestimmt die Informationen, die in einem **SWbemNamedValueSet-Objekt enthalten** sind. WMI nutzt die Informationen nicht, sondern gibt sie einfach an den Anbieter weiter. Anbieter müssen die benötigten Kontextinformationen für Dienstanforderungen veröffentlichen.

## <a name="members"></a>Member

Das **SWbemNamedValueSet-Objekt** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **SWbemNamedValueSet-Objekt** verfügt über diese Methoden.



| Methode                                            | Beschreibung                                                                                                                              |
|:--------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [**Hinzufügen**](swbemnamedvalueset-add.md)             | Fügt der [**Auflistung ein SWbemNamedValue-Objekt**](swbemnamedvalue.md) hinzu.<br/>                                                  |
| [**Klon**](swbemnamedvalueset-clone.md)         | Erstellt eine Kopie dieser **SWbemNamedValueSet-Auflistung.**<br/>                                                                       |
| [**DeleteAll**](swbemnamedvalueset-deleteall.md) | Entfernt alle Elemente aus der Auflistung, wodurch das **SWbemNamedValueSet-Objekt** leer ist.<br/>                                        |
| [**Element**](swbemnamedvalueset-item.md)           | Ruft ein [**SWbemNamedValue-Objekt**](swbemnamedvalue.md) aus der Auflistung ab. Dies ist die Standardmethode des -Objekts.<br/> |
| [**Entfernen**](swbemnamedvalueset-remove.md)       | Entfernt ein [**SWbemNamedValue-Objekt**](swbemnamedvalue.md) aus der Auflistung.<br/>                                             |



 

### <a name="properties"></a>Eigenschaften

Das **SWbemNamedValueSet-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                             | Zugriffstyp          | Beschreibung                                       |
|:-----------------------------------------------------|:---------------------|:--------------------------------------------------|
| [**Anzahl**](swbemnamedvalueset-count.md)<br/> | Schreibgeschützt<br/> | Die Anzahl der Elemente in der Auflistung.<br/> |



 

## <a name="examples"></a>Beispiele

Das folgende VBScript-Beispiel veranschaulicht die Bearbeitung benannter Wertsätze, falls der benannte Wert ein Arraytyp ist.


```VB
Set Context = CreateObject("WbemScripting.SWbemNamedValueSet")

On Error Resume Next

Context.Add "n1", Array (1, 2, 3)
str = "The initial value of n1 is {"
for x=LBound(Context("n1")) to UBound(Context("n1"))
 str = str & Context("n1")(x)
 if x <> UBound(Context("n1")) Then
  str = str & ", "
 End if
next
str = str & "}"
WScript.Echo str

WScript.Echo ""

' report the value of an element of the context value
v = Context("n1")
WScript.Echo "By indirection the first element of n1 has value:",v(0)

' report the value directly
WScript.Echo "By direct access the first element of n1 has value:", Context("n1")(0)

' set the value of a single named value element
Context("n1")(1) = 11 
WScript.Echo "After direct assignment the first element of n1 has value:", Context("n1")(1)

' set the value of a single named value element
Set v = Context("n1")
v(1) = 345
WScript.Echo "After indirect assignment the first element of n1 has value:", Context("n1")(1)

' set the value of an entire context value
Context("n1") = Array (5, 34, 178871)
WScript.Echo "After direct array assignment the first element of n1 has value:", Context("n1")(1)

str = "After direct assignment the entire value of n1 is {"
for x=LBound(Context("n1")) to UBound(Context("n1"))
 str = str & Context("n1")(x)
 if x <> UBound(Context("n1")) Then
  str = str & ", "
 End if
next
str = str & "}"
WScript.Echo str

if Err <> 0 Then
 WScript.Echo Err.Description
 Err.Clear
End if
```



Das folgende Perl-Beispiel veranschaulicht die Bearbeitung benannter Wertsätze, falls der benannte Wert ein Arraytyp ist.


```
use strict;
use Win32::OLE;

my ( $Context, $str, $x, @v);

eval {$Context = new Win32::OLE 'WbemScripting.SWbemNamedValueSet'; };
unless($@)
{
 $Context->Add("n1", [1, 2, 3]);
 $str = "The initial value of n1 is {";
 for ($x = 0; $x < @{$Context->Item("n1")->{Value}}; $x++)
 {
  $str = $str.@{$Context->Item("n1")->{Value}}[$x];
  if ($x != (@{$Context->Item("n1")->{Value}}) - 1 )
  {
   $str = $str.", ";
  }
 }
 $str = $str."}";
 print $str,"\n\n";

 # report the value of an element of the context value
 @v = @{$Context->Item("n1")->{Value}};
 print "By indirection the first element of n1 has value:", $v[0], "\n";

 # report the value directly
 print "By direct access the first element of n1 has value:", @{$Context->Item("n1")->{Value}}[0], "\n";

 # set the value of a single named value element
 @{$Context->Item("n1")->{Value}}[1] = 11;
 print "After direct assignment the first element of n1 has value:", 
       @{$Context->Item("n1")->{Value}}[1], "\n";

 # set the value of a single named value element
 @v = @{$Context->Item("n1")->{Value}};
 $v[1] = 345;
 print "After indirect assignment the first element of n1 has value:", 
    @{$Context->Item("n1")->{Value}}[1], "\n";

 # set the value of an entire context value
 $Context->Item("n1")->{Value} = [5, 34, 178871];
 print "After direct array assignment the first element of n1 has value:", 
   @{$Context->Item("n1")->{Value}}[1], "\n";

 $str = "After direct assignment the entire value of n1 is {";
 for ($x = 0; $x < @{$Context->Item("n1")->{Value}}; $x++)
 {
  $str = $str.@{$Context->Item("n1")->{Value}}[$x];
  if ($x != (@{$Context->Item("n1")->{Value}}) - 1 )
  {
   $str = $str.", ";
  }
 }
 $str = $str."}";
 print $str,"\n";
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemNamedValueSet<br/>                                                    |
| IID<br/>                      | IID \_ ISWbemNamedValueSet<br/>                                                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Skripterstellung für API-Objekte](scripting-api-objects.md)
</dt> </dl>

 

 




