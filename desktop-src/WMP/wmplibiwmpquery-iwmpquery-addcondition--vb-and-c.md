---
title: IWMPQuery addCondition-Methode
description: Die addCondition-Methode fügt der Verbundabfrage mithilfe der AND-Logik eine Bedingung hinzu.
ms.assetid: 4594ee6f-b153-4d53-b3ee-cd1718a4d5dc
keywords:
- addCondition-Windows Media Player
- addCondition-Methode Windows Media Player , IWMPQuery-Schnittstelle
- IWMPQuery-Schnittstelle Windows Media Player , addCondition-Methode
topic_type:
- apiref
api_name:
- IWMPQuery.addCondition
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe85999c60364827d483f81d14ff88602c9b2831c16e7cff8a3e17076b77671d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745705"
---
# <a name="iwmpqueryaddcondition-method"></a>IWMPQuery::addCondition-Methode

Die **addCondition-Methode** fügt der Verbundabfrage mithilfe der **AND-Logik eine Bedingung** hinzu.

## <a name="syntax"></a>Syntax


```CSharp
public void addCondition(
  System.String bstrAttribute,
  System.String bstrOperator,
  System.String bstrValue
);
```


```VB

Public Sub addCondition( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrOperator As System.String, _
  ByVal bstrValue As System.String _
)
Implements IWMPQuery.addCondition
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrAttribute* \[ In\]
</dt> <dd>

Eine **System.String,die** den Namen des Attributs angibt, das der Abfrage hinzugefügt werden soll.

</dd> <dt>

*bstrOperator* \[ In\]
</dt> <dd>

Eine **System.String,** die der Operator ist. Unterstützte Werte finden Sie unter Hinweise.

</dd> <dt>

*bstrValue* \[ In\]
</dt> <dd>

Eine **System.String,** die der Attributwert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Bedingungen, die in einer zusammengesetzten Abfrage enthalten sind, werden in Bedingungsgruppen organisiert. Mehrere Bedingungen innerhalb einer Bedingungsgruppe werden immer mithilfe der **AND-Logik verkettet.** Bedingungsgruppen werden immer mithilfe der **OR-Logik miteinander verkettet.** Um eine neue Bedingungsgruppe zu starten, rufen [Sie IWMPQuery.beginNextGroup auf.](wmplibiwmpquery-iwmpquery-beginnextgroup--vb-and-c.md)

Bei zusammengesetzten Abfragen, **die IWMPQuery verwenden,** wird die Kleinschreibung nicht beachtet.

Eine Liste der Werte für den *bstrAttribute-Parameter* finden Sie unter [Alphabetische Attributreferenz.](alphabetical-attribute-reference.md)

In der folgenden Tabelle sind die unterstützten Werte für *bstrOperator aufgeführt.*



| String              | Gilt für:     |
|---------------------|----------------|
| BeginsWith          | Zeichenfolgen        |
| Enthält            | Zeichenfolgen        |
| Ist gleich              | Alle Typen      |
| GreaterThan         | Zahlen, Datumsangaben |
| Größer als oder gleich | Zahlen, Datumsangaben |
| LessThan            | Zahlen, Datumsangaben |
| Kleiner als oder gleich    | Zahlen, Datumsangaben |
| NotBeginsWith       | Zeichenfolgen        |
| NotContains         | Zeichenfolgen        |
| NotEquals           | Alle Typen      |



 

## <a name="examples"></a>Beispiele

Das folgende Beispiel erstellt eine Abfrage, fügt ihr zwei Bedingungen hinzu und verwendet diese Abfrage, um die Ergebnisse der Abfrage als Zeichenfolgensammlung zu extrahieren. Die Ergebnisse werden dann in einem Listenfeld angezeigt. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


```CSharp
// Get a new Query interface.
WMPLib.IWMPMediaCollection2 mc = (WMPLib.IWMPMediaCollection2)player.mediaCollection;
WMPLib.IWMPQuery q = mc.createQuery();

// Add two conditions to the Query. 
q.addCondition("WM/Composer", "Equals", "Antonio Vivaldi");
q.addCondition("Title", "Contains", "Trio");

// Query the media collection and get a string collection containing the result.
// In this case, the string collection will contain the titles of all audio items that
// match the query.
WMPLib.IWMPStringCollection2 result = (WMPLib.IWMPStringCollection2)mc.getStringCollectionByQuery("Title", q, "audio", "", false);

// Display the results by adding them to a list box.
for (int i = 0; i < result.count; i++)
{
    queryResults.Items.Add(result.Item(i));
}
```


```VB

' Get a new Query interface.
Dim mc As WMPLib.IWMPMediaCollection2 = player.mediaCollection
Dim q As WMPLib.IWMPQuery = mc.createQuery()

&#39; Add two conditions to the Query. 
q.addCondition(&quot;WM/Composer&quot;, &quot;Equals&quot;, &quot;Antonio Vivaldi&quot;)
q.addCondition(&quot;Title&quot;, &quot;Contains&quot;, &quot;Trio&quot;)

&#39; Query the media collection and get a string collection containing the result.
&#39; In this case, the string collection will contain the titles of all audio items that
&#39; match the query.
Dim result As WMPLib.IWMPStringCollection2 = mc.getStringCollectionByQuery(&quot;Title&quot;, q, &quot;audio&quot;, &quot;&quot;, False)

&#39; Display the results by adding them to a list box.
For i As Integer = 0 To (result.count - 1)

    queryResults.Items.Add(result.Item(i))

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

[**Alphabetische Attributreferenz**](alphabetical-attribute-reference.md)
</dt> <dt>

[**IWMPMediaCollection2.createQuery (VB und C#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection2.getPlaylistByQuery (VB und C#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection2.getStringCollectionByQuery (VB und C#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[**IWMPQuery-Schnittstelle**](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





