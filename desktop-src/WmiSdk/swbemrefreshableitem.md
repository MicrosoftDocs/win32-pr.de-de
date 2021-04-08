---
description: Stellt ein einzelnes Element in einem "Swap-Aktualisierungs"-Objekt dar.
ms.assetid: 6a12c8eb-3ef9-4292-810c-6954294fc8c7
ms.tgt_platform: multiple
title: Taubemerfrischendes ableitem-Objekt (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem
- ISWbemRefreshableItem
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4bc4f85145926aba2bd050052c33eb5669dfee8a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761412"
---
# <a name="swbemrefreshableitem-object"></a>Taubemerfrischendes ableitem-Objekt

Das **taubemfreshableitem** -Objekt stellt ein einzelnes Element in einem " [**Swap**](swbemrefresher.md) "-Objekt dar. Ein " **slibemfreshableitem** "-Objekt wird durch die [**Add**](swbemrefresher-add.md) -und [**AddEnum**](swbemrefresher-addenum.md) -Methoden von " [**slibemaktusher**](swbemrefresher.md)" abgerufen. Dieses Objekt kann nicht durch den VBScript-Befehl "up- [Object](creating-an-object-using-vbscript.md) " erstellt werden.

## <a name="members"></a>Member

Das Objekt " **waybemerfrischendes ableitem** " verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das Objekt " **taubemerfrischendes ableitem** " verfügt über diese Methoden.



| Methode                                        | BESCHREIBUNG                                                                                                             |
|:----------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**Aufgeh**](swbemrefreshableitem-remove.md) | Entfernt das Objekt " **pulbemfreshableitem** " aus dem übergeordneten " [**pulbemaktusher**](swbemrefresher.md) "-Objekt.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das Objekt " **taubemerfrischendes ableitem** " verfügt über diese Eigenschaften.



| Eigenschaft                                                       | Zugriffstyp           | BESCHREIBUNG                                                                                                                          |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------|
| [**Sin**](swbemrefreshableitem-index.md)<br/>         | Lesen/Schreiben<br/> | Der Index des Elements in seinem übergeordneten " [**taubemaktusher**](swbemrefresher.md) "-Objekt.<br/>                                          |
| [**Isset**](swbemrefreshableitem-isset.md)<br/>         | Lesen/Schreiben<br/> | Gibt an, ob das Objekt " **Swap-ableitem** " ein einzelnes Objekt oder einen Objekt Satz darstellt.<br/>                        |
| [**Objekt**](swbemrefreshableitem-object.md)<br/>       | Lesen/Schreiben<br/> | Stellt ein einzelnes " [**errbemujejekt**](swbemobject.md) "-Objekt dar, das aktualisiert wird.<br/>                                          |
| [**ObjectSet**](swbemrefreshableitem-objectset.md)<br/> | Lesen/Schreiben<br/> | Stellt den zu aktualisierenden Objekt Satz dar.<br/>                                                                                |
| [**Aktualisierungs Programm**](swbemrefreshableitem-refresher.md)<br/> | Schreibgeschützt<br/>  | Stellt das übergeordnete " [**taubemaktualisierungs**](swbemrefresher.md) "-Objekt dar, das das Objekt " **Swap-ableitem** " enthält.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die VBScript-Methode " [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) " kann nicht verwendet werden, um " **Swap** "-Objekte direkt zu erstellen.

## <a name="examples"></a>Beispiele

Das folgende Skript veranschaulicht die Erstellung eines " [**Swap**](swbemrefresher.md) "-Objekts und das Hinzufügen eines einzelnen Objekts und des Enumerators " **austauschen** von".


```VB
' Get some namespace connections
set cimv2 = GetObject("winmgmts:root\cimv2")
set default = GetObject("winmgmts:root\default")    

' Create a refresher
set refresher = CreateObject("WbemScripting.SWbemRefresher")

' Add a single object to the refresher.
' The @ is used because this is a singleton 
' system class so only one instance exists.
set item1 = refresher.Add (default, "__CIMOMIdentification=@").Object
MsgBox "WMI Version " item1
' Add an enumerator to the refresher.
' Note that the SWbemRefreshableItem.ObjectSet 
' property must be used to designate
' this as an object set rather than a single object.
set item2 = refresher.AddEnum (cimv2, "Win32_Process").ObjectSet

' Loop three times, refreshing the items

For I= 1 To 3
MsgBox "Refresh number " & I
refresher.Refresh

' Iterate through the collection of
' processes in item2 with name of wscript
    For each process in item2
        If process.name = "wscript.exe" then
        MsgBox "Process " & process.Name & _
           " Page Faults " & process.PageFaults
        End If
    Next 
Next

' Clear out the refresher
refresher.DeleteAll 

' The following should return 0
MsgBox "Number of items in Refresher after DeleteAll " _
    & refresher.Count
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID, \_ Swap-ableitem<br/>                                                  |
| IID<br/>                      | IID \_ iswbemerfrischendes ableitem<br/>                                                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[API-Skript Objekte](scripting-api-objects.md)
</dt> </dl>

 

 




