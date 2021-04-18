---
description: Ein "taubemnamedvalueset"-Objekt ist eine Sammlung von "taubemnamedvalue"-Objekten.
ms.assetid: 7d1c3a28-d0d3-4108-9628-74ad483e328e
ms.tgt_platform: multiple
title: Taubemnamedvalueset-Objekt (wbemdisp. h)
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
ms.openlocfilehash: 2b3048b8589666a07958251ed4c0d56100132fd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343411"
---
# <a name="swbemnamedvalueset-object"></a>Swap-namedvalueset-Objekt

Ein " **taubemnamedvalueset** "-Objekt ist eine Sammlung von " [**taubemnamedvalue**](swbemnamedvalue.md) "-Objekten. Die Methoden und Eigenschaften von " **Austausch Name** " werden im Wesentlichen verwendet, um weitere Informationen an Anbieter zu senden, wenn bestimmte WMI-Aufrufe übermittelt werden. Alle Aufrufe in " [**Swap Services**](swbemservices.md)" und einige Aufrufe in " [**errbemujeject**](swbemobject.md)" akzeptieren einen optionalen Parameter, bei dem es sich um ein Objekt dieses Typs handelt. Ein Client kann einem "Swap- **namedvalueset** "-Objektinformationen hinzufügen und das " **austaubemnamedvalueset** "-Objekt mit dem-Parameter als einen der-Parameter senden. Dieses Objekt kann durch den VBScript-Befehl "up- **Object** " erstellt werden.

Weitere Informationen finden Sie unter [zugreifen auf eine Sammlung](accessing-a-collection.md).

> [!Note]  
> Wichtig: Wenn möglich, verwenden Sie diesen Mechanismus nicht, da er das einheitliche Zugriffs Modell, das die Basis von WMI ist, unterbrechen kann. Wenn ein Anbieter diesen Mechanismus verwendet, ist es wichtig, dass dieser Mechanismus so sparsam wie möglich verwendet wird. Wenn ein Anbieter eine große Menge hochspezifischer Kontextinformationen erfordert, um auf eine Anforderung zu reagieren, müssen alle Clients so codiert sein, dass diese Informationen bereitgestellt werden. Mit diesem Mechanismus können Sie bei Bedarf auf solche Anbieter zugreifen.

 

Ein " **taubemnamedvalueset** "-Objekt ist eine Sammlung von " [**taubemnamedvalue**](swbemnamedvalue.md) "-Elementen. Diese Elemente werden der Auflistung mithilfe der Methode " [**Swap. Add**](swbemnamedvalueset-add.md) " hinzugefügt. Sie werden mithilfe der Methode " [**Swap Name. Remove**](swbemnamedvalueset-remove.md) " entfernt und mithilfe der Methode " [**Swap Name. Item**](swbemnamedvalueset-item.md) " abgerufen. Sie können auf die-Methoden zugreifen, um alle Kontextinformationen auszufüllen, die von einem dynamischen Anbieter benötigt werden. Nachdem Sie eine der Methode " [**Swap Services**](swbemservices.md) " aufgerufen haben, können Sie das Objekt " **taubemnamedvalueset** " für einen anderen-Befehl wieder verwenden.

Der zugrunde liegende Anbieter bestimmt die Informationen, die in einem " **Swap namedvalueset** "-Objekt enthalten sind. WMI verwendet die Informationen nicht, sondern leitet Sie einfach an den Anbieter weiter. Anbieter müssen die erforderlichen Kontextinformationen für die Dienst Anforderungen veröffentlichen.

## <a name="members"></a>Member

Das Objekt " **taubemnamedvalueset** " verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das Objekt " **Swap namedvalueset** " verfügt über diese Methoden.



| Methode                                            | BESCHREIBUNG                                                                                                                              |
|:--------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [**Eren**](swbemnamedvalueset-add.md)             | Fügt der Auflistung ein-Objekt mit dem [**Namen**](swbemnamedvalue.md) "-Objekt" hinzu.<br/>                                                  |
| [**Klon**](swbemnamedvalueset-clone.md)         | Erstellt eine Kopie dieser " **Swap namedvalueset** "-Auflistung.<br/>                                                                       |
| [**DeleteAll**](swbemnamedvalueset-deleteall.md) | Entfernt alle Elemente aus der Auflistung, sodass das Objekt " **taubemnamedvalueset** " leer ist.<br/>                                        |
| [**Element**](swbemnamedvalueset-item.md)           | Ruft [**ein-**](swbemnamedvalue.md) Objekt aus der-Auflistung ab. Dies ist die Standardmethode des-Objekts.<br/> |
| [**Aufgeh**](swbemnamedvalueset-remove.md)       | Entfernt ein " [**pulbemnamedvalue**](swbemnamedvalue.md) "-Objekt aus der Auflistung.<br/>                                             |



 

### <a name="properties"></a>Eigenschaften

Das Objekt " **Swap namedvalueset** " verfügt über diese Eigenschaften.



| Eigenschaft                                             | Zugriffstyp          | BESCHREIBUNG                                       |
|:-----------------------------------------------------|:---------------------|:--------------------------------------------------|
| [**Countdown**](swbemnamedvalueset-count.md)<br/> | Schreibgeschützt<br/> | Die Anzahl der Elemente in der Auflistung.<br/> |



 

## <a name="examples"></a>Beispiele

Das folgende VBScript-Beispiel veranschaulicht die Bearbeitung von benannten Wert Sätzen, falls der benannte Wert ein Arraytyp ist.


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



Das folgende perl-Beispiel veranschaulicht die Bearbeitung von benannten Wert Sätzen, falls der benannte Wert ein Arraytyp ist.


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
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Swap-namedvalueset<br/>                                                    |
| IID<br/>                      | IID \_ iswbemnamedvalueset<br/>                                                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[API-Skript Objekte](scripting-api-objects.md)
</dt> </dl>

 

 




