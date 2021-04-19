---
title: Iwmpquery-addcondition-Methode
description: Die addcondition-Methode fügt der Verbund Abfrage mithilfe der-und der-Logik eine Bedingung hinzu.
ms.assetid: 4594ee6f-b153-4d53-b3ee-cd1718a4d5dc
keywords:
- addcondition-Methode (Windows Media Player)
- addcondition-Methode, Windows Media Player, iwmpquery-Schnittstelle
- Iwmpquery Interface, Windows Media Player, addcondition-Methode
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
ms.openlocfilehash: 9de3015ef0389fef82934cbd8e9326b6f9ec2307
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352030"
---
# <a name="iwmpqueryaddcondition-method"></a>Iwmpquery:: addcondition-Methode

Die **addcondition** -Methode fügt der Verbund Abfrage mithilfe der **-und der-** Logik eine Bedingung hinzu.

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

*bstrattribute* \[ in\]
</dt> <dd>

Ein **System. String** -Wert, der der Name des Attributs ist, das der Abfrage hinzugefügt werden soll.

</dd> <dt>

*bstroperator* \[ in\]
</dt> <dd>

Ein **System. String** -Operator, der der-Operator ist. Siehe Hinweise zu unterstützten Werten.

</dd> <dt>

*bstrauvalue* \[ in\]
</dt> <dd>

Ein **System. String** -Wert, der der Attribut Wert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

In einer Verbund Abfrage enthaltene Bedingungen werden in Bedingungs Gruppen organisiert. Mehrere Bedingungen innerhalb einer Bedingungs Gruppe werden immer mithilfe der **-und der-** Logik verkettet. Bedingungs Gruppen werden stets mithilfe der- **oder** -Logik miteinander verkettet. Um eine neue Bedingungs Gruppe zu starten, nennen Sie [iwmpquery. beginnextgroup](wmplibiwmpquery-iwmpquery-beginnextgroup--vb-and-c.md).

Bei Verbund Abfragen mit **iwmpquery** wird die Groß-/Kleinschreibung nicht beachtet

Eine Liste der Werte für den *bstrattribute* -Parameter finden Sie in der [alphabetischen Attribut Referenz](alphabetical-attribute-reference.md).

In der folgenden Tabelle sind die unterstützten Werte für *bstroperator* aufgeführt.



| String              | Gilt für:     |
|---------------------|----------------|
| BeginsWith          | Zeichenfolgen        |
| Enthält            | Zeichenfolgen        |
| Equals              | Alle Typen      |
| GreaterThan         | Zahlen, Datumsangaben |
| Größer als oder gleich | Zahlen, Datumsangaben |
| LessThan            | Zahlen, Datumsangaben |
| Kleiner als oder gleich    | Zahlen, Datumsangaben |
| Notbeginswith       | Zeichenfolgen        |
| NotContains         | Zeichenfolgen        |
| NotEquals           | Alle Typen      |



 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird eine Abfrage erstellt, zwei Bedingungen hinzugefügt und diese Abfrage verwendet, um die Ergebnisse der Abfrage als Zeichen folgen Auflistung zu extrahieren. Die Ergebnisse werden dann in einem Listenfeld angezeigt. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Alphabetische Attribut Referenz**](alphabetical-attribute-reference.md)
</dt> <dt>

[**IWMPMediaCollection2. kreatequery (VB und c#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection2. getplaylistbyquery (VB und c#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection2. getstringcollectionbyquery (VB und c#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[**Iwmpquery-Schnittstelle**](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





