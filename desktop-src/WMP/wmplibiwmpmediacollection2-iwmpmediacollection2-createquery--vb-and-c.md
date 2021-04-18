---
title: IWMPMediaCollection2-Methode "kreatequery"
description: Die Methode "Methode" gibt eine iwmpquery-Schnittstelle zurück, die eine neue Abfrage darstellt.
ms.assetid: a12da325-e77e-4e44-93d1-5e9c5733ea44
keywords:
- Windows Media Player der Methode "kreatequery"
- Methode "winatequery" Windows Media Player, IWMPMediaCollection2 Interface
- IWMPMediaCollection2 Interface, Windows Media Player, Methode "kreatequery"
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.createQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 318b27a20ba801e1fbed58ff79c5bed7841f8c29
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352153"
---
# <a name="iwmpmediacollection2createquery-method"></a>IWMPMediaCollection2:: kreatequery-Methode

Die- `createQuery` Methode gibt eine **iwmpquery** -Schnittstelle zurück, die eine neue Abfrage darstellt.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPQuery createQuery();
```


```VB

Public Function createQuery() As IWMPQuery
Implements IWMPMediaCollection2.createQuery
```





## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Eine **WMPLib. iwmpquery** -Schnittstelle, die eine neue, leere Abfrage darstellt.

## <a name="remarks"></a>Bemerkungen

Das Erstellen einer neuen Abfrage ist der erste Schritt, um eine Verbund Abfrage zu erstellen.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel `createQuery` wird verwendet, um eine **iwmpquery** -Schnittstelle zu erhalten, die mit NULL initialisiert wird. Da dieser Abfrage keine Bedingungen hinzugefügt werden, gibt die Methode eine Zeichen folgen Auflistung zurück, die alle Medienelemente des angegebenen Medientyps enthält, wenn Sie als Argument in der **getstringcollectionbyquery** -Methode verwendet wird. Die Zeichen folgen Sammlung wird dann in einem Listenfeld angezeigt.


```CSharp
// Get an IWMPMediaCollection2 interface so that you can access the createQuery and
// getStringCollectionByQuery methods.
WMPLib.IWMPMediaCollection2 mc = (WMPLib.IWMPMediaCollection2)player.mediaCollection;

// Create an IWMPQuery interface with no conditions added to it.
WMPLib.IWMPQuery nullQuery = mc.createQuery();

// Get a string collection that contains the titles of all the audio items in the media
// collection.
WMPLib.IWMPStringCollection2 allTitles = (WMPLib.IWMPStringCollection2)mc.getStringCollectionByQuery("Title", nullQuery, "audio", "", false);

// Display the titles by adding them to a list box.
for (int i = 0; i < allTitles.count; i++)
{
    queryResults.Items.Add(allTitles.Item(i));
}
```


```VB

' Get an IWMPMediaCollection2 interface so that you can access
&#39; the createQuery and getStringCollectionByQuery methods.
Dim mc As WMPLib.IWMPMediaCollection2 = player.mediaCollection

&#39; Create an IWMPQuery interface with no conditions added to it.
Dim nullQuery As WMPLib.IWMPQuery = mc.createQuery()

&#39; Get a string collection that contains the titles of all the audio items in the media
&#39; collection
Dim allTitles As WMPLib.IWMPStringCollection2 = mc.getStringCollectionByQuery(&quot;Title&quot;, nullQuery, &quot;audio&quot;, &quot;&quot;, False)

&#39; Display the titles by adding them to a ListBox
For i As Integer = 0 To (allTitles.count - 1)

    queryResults.Items.Add(allTitles.Item(i))

Next i
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPMediaCollection2-Schnittstelle (VB und c#)**](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[**Iwmpquery-Schnittstelle (VB und c#)**](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





