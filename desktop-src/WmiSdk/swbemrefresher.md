---
description: Das taubemrefresh Sher-Objekt ist ein Container Objekt, das die Daten für alle hinzugefügten Objekte aktualisieren kann. Der Satz von hinzugefügten Objekten, wobei jedes Element, das von einer-Instanz von einer-Instanz dargestellt wird, als Auflistung und Enumeration behandelt werden kann.
ms.assetid: cc5872a1-932b-4b68-9f5e-a91d35c8e117
ms.tgt_platform: multiple
title: Swap-Aktualisierungs Objekt (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher
- ISWbemRefresher
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f763ec4f738b612b9f2fef32871a63d6b170f96d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961177"
---
# <a name="swbemrefresher-object"></a>Swap-Aktualisierungs Objekt

Das **taubemrefresh Sher** -Objekt ist ein Container Objekt, das die Daten für alle hinzugefügten Objekte aktualisieren kann. Einzelne Instanzen und instanzenumeratoren können dem Container hinzugefügt oder daraus entfernt werden. Der Satz von hinzugefügten Objekten, wobei jedes Element, das [**von einer-**](swbemrefreshableitem.md) Instanz von einer-Instanz dargestellt wird, als Auflistung und Enumeration behandelt werden kann. WMI-Instanzen aus beliebigen Klassen können dem Objekt " **Swap** -Aktualisierungs Modul" hinzugefügt werden. Auch wenn es sich bei dem Anbieter für die Instanzdaten nicht um einen Hochleistungs Anbieter handelt, kann das Aktualisier Ende Objekt die Daten nach dem Aktualisierungs-und [**Update aktualisieren.**](swbemrefresher-refresh.md) Wenn die Daten über einen Hochleistungs Anbieter bereitgestellt werden und die [**autoreconnetct**](swbemrefresher-autoreconnect.md) -Eigenschaft den Wert **true** hat, versucht das Objekt " **Swap** -Aktualisierungs", eine unterbrochene Verbindung mit dem Datenanbieter wiederherzustellen. Dieses Objekt kann durch den VBScript-Befehl "up- **Object** " erstellt werden.

Der Aktualisierungs Vorgang kann durch Aufrufen der Methode " [**Swap. Refresh**](swbemrefresher-refresh.md) " oder der Methode " [**\_ errbemubjectex. Refresh**](swbemobjectex-refresh-.md) " durchgeführt werden.

## <a name="members"></a>Member

Das Objekt " **Swap** -Aktualisierungs Programm" verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **taubemaktualisierungs** -Objekt verfügt über diese Methoden.



| Methode                                        | BESCHREIBUNG                                                                                           |
|:----------------------------------------------|:------------------------------------------------------------------------------------------------------|
| [**Eren**](swbemrefresher-add.md)             | Fügt der Auflistung im Aktualisierungs Objekt ein neues Aktualisier bares Objekt hinzu.<br/>                   |
| [**AddEnum**](swbemrefresher-addenum.md)     | Fügt dem Aktualisierungs Objekt einen neuen Enumerator hinzu.<br/>                                             |
| [**DeleteAll**](swbemrefresher-deleteall.md) | Entfernt alle Elemente aus der Auflistung im Aktualisierungs-Objekt.<br/>                             |
| [**Element**](swbemrefresher-item.md)           | Gibt ein angegebenes Aktualisierungs Element aus der Auflistung zurück.<br/>                                    |
| [**Aktualisieren**](swbemrefresher-refresh.md)     | Aktualisiert alle Elemente, die im Aktualisierungs Objekt enthalten sind.<br/>                          |
| [**Aufgeh**](swbemrefresher-remove.md)       | Entfernt das Aktualisierungs Element Objekt oder den Objekt Satz mit einem angegebenen Index aus dem Aktualisierungs Programm.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **taubemaktualisierungs** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                         | Zugriffstyp          | BESCHREIBUNG                                                                                                           |
|:-----------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**Automatische**](swbemrefresher-autoreconnect.md)<br/> | Schreibgeschützt<br/> | Gibt an, ob das Aktualisierungs Programm automatisch erneut eine Verbindung mit einem Remote Anbieter herstellt, wenn die Verbindung getrennt ist.<br/> |
| [**Countdown**](swbemrefresher-count.md)<br/>                 | Schreibgeschützt<br/> | Enthält die Anzahl der Elemente im Aktualisierungs Objekt.<br/>                                                      |



 

## <a name="examples"></a>Beispiele

Das folgende Beispiel veranschaulicht das Erstellen eines slibemaktualisierungs-Objekts mithilfe der [**Add**](swbemrefresher-add.md) -Methode und der [**AddEnum**](swbemrefresher-addenum.md) -Methode, um eine einzelne Instanz und eine Enumerationsinstanz zu speichern, die Aktualisierung der Daten und die Verwendung der Item-Eigenschaft zum Abrufen der " [**slibemfreshableitem**](swbemrefreshableitem.md) "-Objekte. 


```VB
' Get namespace connections
set objServicesCimv2 = GetObject("winmgmts:root\cimv2")
set objServicesDefault = GetObject("winmgmts:root\default")

' Create a refresher object
set objRefresher = CreateObject("WbemScripting.SWbemRefresher")

' Add a single object (SWbemObjectEx) to the refresher. The "@"
' is used because _CIMOMIdentification is a singleton class- only 
' one instance exists. Note that the
' SWbemRefreshableItem.Object property must 
' be specified or the SWbemRefresher.Refresh call will fail.

set objRefreshableItem1 = objRefresher. _
    Add (objServicesDefault, "__CIMOMIdentification=@").Object

' Add an enumerator (SWbemObjectSet object)
' to the refresher. Note that the
' SWbemRefreshableItem.ObjectSet property
' must be specified or the SWbemRefresher.Refresh call will fail. 
set objRefreshableItem2 = objRefresher. _
    AddEnum (objServicesCimv2, "Win32_Process").ObjectSet

' Display number of items in refresher and update the data.
MsgBox "Number of items in refresher = " & objRefresher.Count
objRefresher.Refresh

' Iterate through the refresher. SWbemRefreshable
' Item.IsSet checks for whether the item is an enumerator.
for each RefreshableItem in objRefresher
 if RefreshableItem.IsSet then  
    MsgBox "Item with index " & RefreshableItem.Index &_
    " is an enumerator containing "_
    & RefreshableItem.ObjectSet.Count & " processes"
 else  
      MsgBox "Item with index " & RefreshableItem.Index _
          & " is a single object containing WMI version "_
          &  objRefreshableItem1.VersionCurrentlyRunning
 end if
next
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Austauschprogramm<br/>                                                        |
| IID<br/>                      | IID \_ iswbemfreshsher<br/>                                                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Swap-aktuableitem**](swbemrefreshableitem.md)
</dt> <dt>

[**Austauschen von "errbemubjectex"**](swbemobjectex.md)
</dt> <dt>

[API-Skript Objekte](scripting-api-objects.md)
</dt> </dl>

 

 




