---
title: IWMPMediaCollection2 createQuery-Methode
description: Die createQuery-Methode gibt eine IWMPQuery-Schnittstelle zurück, die eine neue Abfrage darstellt.
ms.assetid: a12da325-e77e-4e44-93d1-5e9c5733ea44
keywords:
- createQuery-Windows Media Player
- createQuery-Methode Windows Media Player , IWMPMediaCollection2-Schnittstelle
- IWMPMediaCollection2-Schnittstelle Windows Media Player , createQuery-Methode
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
ms.openlocfilehash: 1644748008e2b222fef0101a96892d480ad4723b9892b94e0e69c387b54e53d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000090"
---
# <a name="iwmpmediacollection2createquery-method"></a>IWMPMediaCollection2::createQuery-Methode

Die `createQuery` -Methode gibt eine **IWMPQuery-Schnittstelle** zurück, die eine neue Abfrage darstellt.

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

Eine **WMPLib.IWMPQuery-Schnittstelle,** die eine neue, leere Abfrage darstellt.

## <a name="remarks"></a>Hinweise

Das Erstellen einer neuen Abfrage ist der erste Schritt zum Erstellen einer zusammengesetzten Abfrage.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird `createQuery` verwendet, um eine **IWMPQuery-Schnittstelle** zu erhalten, die mit NULL initialisiert wird. Da dieser Abfrage keine Bedingungen hinzugefügt wurden, gibt die Methode eine Zeichenfolgensammlung zurück, die alle Medienelemente des angegebenen Medientyps enthält, wenn sie als Argument in der **getStringCollectionByQuery-Methode** verwendet wird. Die Zeichenfolgensammlung wird dann in einem Listenfeld angezeigt.


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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMPMediaCollection2-Schnittstelle (VB und C#)**](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[**IWMPQuery-Schnittstelle (VB und C#)**](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





