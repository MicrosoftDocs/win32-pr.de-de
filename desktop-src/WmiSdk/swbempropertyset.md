---
description: Ein "taubempropertyset"-Objekt ist eine Sammlung von "Swap Property"-Objekten.
ms.assetid: 0edad17b-facc-4885-9ce4-561ca6f57a66
ms.tgt_platform: multiple
title: Taubempropertyset-Objekt (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet
- ISWbemPropertySet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 05ae5d5e0bfbc5ab0733e00e4649baa2849d3446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351096"
---
# <a name="swbempropertyset-object"></a>Swap-PropertySet-Objekt

Ein " **taubempropertyset** "-Objekt ist eine Sammlung von " [**Swap Property**](swbemproperty.md) "-Objekten. Sie können der Auflistung Elemente mithilfe der [**Add**](swbempropertyset-add.md) -Methode hinzufügen, Elemente aus der Auflistung mithilfe der- [**Element**](swbempropertyset-item.md) Methode abrufen und mithilfe der [**Remove**](swbempropertyset-remove.md) -Methode Elemente aus der Auflistung entfernen. Weitere Informationen finden Sie unter [zugreifen auf eine Sammlung](accessing-a-collection.md). Dieses Objekt kann nicht durch den VBScript-Befehl "up- [Object](creating-an-object-using-vbscript.md) " erstellt werden.

Die " [**Swap Property**](swbemproperty.md) "-Objekte, aus denen eine " **Swap PropertySet** "-Auflistung besteht, werden verwendet, um die Eigenschaften einer einzelnen WMI-Klasse oder-Instanz zu beschreiben.

## <a name="members"></a>Member

Das Objekt " **Swap PropertySet** " verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das Objekt " **Swap PropertySet** " verfügt über diese Methoden.



| Methode                                    | BESCHREIBUNG                                                                                                                     |
|:------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**Eren**](swbempropertyset-add.md)       | Fügt der Auflistung von " **gobempropertyset** " ein " [**gotenproperty**](swbemproperty.md) "-Objekt hinzu.<br/>                        |
| [**Element**](swbempropertyset-item.md)     | Ruft eine benannte " [**taubemproperty**](swbemproperty.md) " aus der Auflistung ab. Dies ist die Standardmethode für dieses Objekt.<br/> |
| [**Aufgeh**](swbempropertyset-remove.md) | Löscht ein [**-**](swbemproperty.md) Objekt aus der-Auflistung.<br/>                                        |



 

### <a name="properties"></a>Eigenschaften

Das Objekt " **Swap PropertySet** " verfügt über diese Eigenschaften.



| Eigenschaft                                           | Zugriffstyp          | BESCHREIBUNG                                                            |
|:---------------------------------------------------|:---------------------|:-----------------------------------------------------------------------|
| [**Countdown**](swbempropertyset-count.md)<br/> | Schreibgeschützt<br/> | Die Anzahl der Elemente in der **Swap** -Auflistung.<br/> |



 

## <a name="examples"></a>Beispiele

Das folgende VBScript-Beispiel veranschaulicht, wie " [**taubempropertyset. Remove**](swbempropertyset-remove.md) " **wbemErrResetToDefault** zurückgeben kann, wenn die Eigenschaft überschrieben wird.


```VB
on error resume next 

'Create a keyed class with a defaulted property
set service = GetObject("Winmgmts:")
set emptyclass = service.Get
emptyclass.path_.class = "REMOVETEST00"
set prop = emptyclass.properties_.add ("p", 19)

prop.qualifiers_.add "key", true
emptyclass.properties_.add ("q", 19).Value = 12

emptyclass.put_

'create an instance and override the property
set instance = service.get ("RemoveTest00").spawninstance_

instance.properties_("q").Value = 24
instance.properties_("p").Value = 1
instance.put_

'retrieve the instance and remove the property
set instance = service.get ("removetest00=1")
set property = instance.properties_ ("q")

WScript.echo "Overridden value of property is [24]:", property.value
WScript.echo ""

instance.properties_.remove "q"
set property = instance.properties_ ("q")
WScript.echo "Value of property after removal is [12]:", property.value
WScript.echo ""

if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
end if
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Swap-Eigenschaften Satz<br/>                                                      |
| IID<br/>                      | IID \_ iswbempropertyset<br/>                                                       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[API-Skript Objekte](scripting-api-objects.md)
</dt> </dl>

 

 




