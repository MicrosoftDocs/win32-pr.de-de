---
title: IWMPQuery beginNextGroup-Methode
description: Die beginNextGroup-Methode startet eine neue Bedingungsgruppe. | IWMPQuery beginNextGroup-Methode
ms.assetid: 15d20c9f-2ce7-4a86-9054-b7317ebe1a0a
keywords:
- beginNextGroup-Methode Windows Media Player
- beginNextGroup-Methode Windows Media Player , IWMPQuery-Schnittstelle
- IWMPQuery-Schnittstelle Windows Media Player , beginNextGroup-Methode
topic_type:
- apiref
api_name:
- IWMPQuery.beginNextGroup
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56a5e0622140aacd2668b1ea145e6a36f7fb2b0ecd243adacc313301d5fb7220
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745725"
---
# <a name="iwmpquerybeginnextgroup-method"></a>IWMPQuery::beginNextGroup-Methode

Die **beginNextGroup-Methode** startet eine neue Bedingungsgruppe.

## <a name="syntax"></a>Syntax


```CSharp
public void beginNextGroup();
```


```VB

Public Sub beginNextGroup()
Implements IWMPQuery.beginNextGroup
```





## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn Sie eine neue Bedingungsgruppe beginnen, bedeutet dies, dass Sie die aktuelle Bedingungsgruppe abgeschlossen haben. Die neue Bedingungsgruppe wird immer mithilfe der **OR-Logik** mit der vorherigen Bedingungsgruppe verkettet.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird eine komplexe Abfrage erstellt, indem zwei Gruppen kombiniert werden, die jeweils eine Bedingung enthalten. Die Ergebnisse der Abfrage werden als Zeichenfolgenauflistung extrahiert und in einem Listenfeld angezeigt. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


```CSharp
// Get a new Query interface.
WMPLib.IWMPMediaCollection2 mc = (WMPLib.IWMPMediaCollection2)player.mediaCollection;
WMPLib.IWMPQuery q = mc.createQuery();

// Add a condition to the Query. 
q.addCondition("WM/Composer", "Equals", "Antonio Vivaldi");

// Begin another Query group.
q.beginNextGroup();

// Add a condition to the new group understanding that it will be combined with the
// first group using OR logic.
q.addCondition("Title", "Contains", "Capriol");

// Query the media collection and get a string collection containing the result.
// In this case, the string collection will contain the titles of all audio items that
// match the query.
WMPLib.IWMPStringCollection2 result = (WMPLib.IWMPStringCollection2)mc.getStringCollectionByQuery("Title", q, "audio", "", false);

// Display the results by adding them to a list box.
for (int i = 0; i < result.count; i++)
{
    complexQueryResults.Items.Add(result.Item(i));
}
```


```VB

' Get a new Query interface.
Dim mc As WMPLib.IWMPMediaCollection2 = player.mediaCollection
Dim q As WMPLib.IWMPQuery = mc.createQuery()

' Add a condition to the Query. 
q.addCondition("WM/Composer", "Equals", "Antonio Vivaldi")

' Begin another Query group.
q.beginNextGroup()

' Add a condition to the new group understanding that it will be combined with the
' first group using OR logic.
q.addCondition("Title", "Contains", "Capriol")

' Query the media collection and get a string collection containing the result.
' In this case, the string collection will contain the titles of all audio items that
' match the query.
Dim result As WMPLib.IWMPStringCollection2 = mc.getStringCollectionByQuery("Title", q, "audio", "", False)

' Display the results by adding them to a list box.
For i As Integer = 0 To (result.count - 1)

    complexQueryResults.Items.Add(result.Item(i))

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

[**IWMPMediaCollection2.createQuery (VB und C#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection2.getPlaylistByQuery (VB und C#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection2.getStringCollectionByQuery (VB und C#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[**IWMPQuery-Schnittstelle (VB und C#)**](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





