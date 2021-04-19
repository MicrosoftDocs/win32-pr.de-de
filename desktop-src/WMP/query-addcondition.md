---
title: Query. addcondition-Methode
description: Die addcondition-Methode fügt dem Query-Objekt mithilfe der-und der-Logik eine Bedingung hinzu.
ms.assetid: 29b5d372-eddf-4b70-882b-d2dde79d9287
keywords:
- addcondition-Methode (Windows Media Player)
- addcondition-Methode, Windows Media Player, Abfrage Klasse
- Query-Klasse, Windows Media Player, addcondition-Methode
topic_type:
- apiref
api_name:
- Query.addCondition
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4035d2877cf0081e9153277c88feb545a529568d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352893"
---
# <a name="queryaddcondition-method"></a>Query. addcondition-Methode

Die **addcondition** -Methode fügt dem **Query** -Objekt mithilfe der-und der-Logik eine Bedingung hinzu.

## <a name="syntax"></a>Syntax


```JScript
Query.addCondition(
  attribute,
  operator,
  value
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Attribut* \[ in\]
</dt> <dd>

**Zeichenfolge** , die den Attributnamen enthält.

</dd> <dt>

*Operator* \[ in\]
</dt> <dd>

**Zeichenfolge** , die den Operator enthält. Siehe Hinweise zu unterstützten Werten.

</dd> <dt>

*Wert* \[ in\]
</dt> <dd>

**Zeichenfolge** , die den Attribut Wert enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Bei Verbund Abfragen mit **Abfrage** wird die Groß-/Kleinschreibung nicht beachtet

Eine Liste der Werte für den *Attribut* Parameter finden Sie im Abschnitt " [alphabetische Attribut Verweis](alphabetical-attribute-reference.md) ".

Bedingungen, die in einem **Abfrage** Objekt enthalten sind, werden in Bedingungs Gruppen organisiert. Mehrere Bedingungen innerhalb einer Bedingungs Gruppe werden stets mithilfe der-und der-Logik verkettet. Bedingungs Gruppen werden mit der-oder der-Logik immer aufeinander verkettet. Zum Starten einer neuen Bedingungs Gruppe aufrufen Sie **Query. beginnextgroup**.

In der folgenden Tabelle sind die unterstützten Werte für den- *Operator* aufgeführt.



| Operator            | Gilt für:     |
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

Im folgenden JScript-Beispiel wird **Query. addcondition** und **Query. beginnextgroup** verwendet, um eine Beispiel Abfrage auszuführen.


```JScript
// Perform an example query for media for which:
// The genre contains "jazz"
// and the title begins with "a"
// OR the genre contains "jazz"
// and the author begins with "b".

// Create the query object.
var Query = Player.mediaCollection.createQuery();

// Add the first condition group.
Query.addCondition("WM/Genre", "Contains", "jazz");
Query.addCondition("Title", "BeginsWith", "a");

// Begin the new condition group ("or").
Query.beginNextGroup();

// Add the second condition group.
Query.addCondition("WM/Genre", "Contains", "jazz");
Query.addCondition("Author", "BeginsWith", "b");

// Perform the query on "audio" media.
var Playlist = Player.mediaCollection.getPlaylistByQuery(
    Query,      // query
    "audio",    // mediaType
    "",         // sortAttribute
    false);     // sortAscending
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mediacollection. kreatequery**](mediacollection-createquery.md)
</dt> <dt>

[**Mediacollection. getplaylistbyquery**](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[**Mediacollection. getstringcollectionbyquery**](mediacollection-getstringcollectionbyquery.md)
</dt> <dt>

[**Query-Objekt**](query-object.md)
</dt> <dt>

[**Query. beginnextgroup**](query-beginnextgroup.md)
</dt> </dl>

 

 





