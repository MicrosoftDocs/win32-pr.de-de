---
title: Query.addCondition-Methode
description: Die addCondition-Methode fügt dem Query-Objekt mithilfe der AND-Logik eine Bedingung hinzu.
ms.assetid: 29b5d372-eddf-4b70-882b-d2dde79d9287
keywords:
- addCondition-Windows Media Player
- addCondition-Methode Windows Media Player , Query-Klasse
- Abfrageklasse Windows Media Player , addCondition-Methode
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
ms.openlocfilehash: 53a3eed0a7923b93861eabc30d115a7726046d0595b7c57625d9a9afaf9c7523
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746589"
---
# <a name="queryaddcondition-method"></a>Query.addCondition-Methode

Die **addCondition-Methode** fügt  dem Query-Objekt mithilfe der AND-Logik eine Bedingung hinzu.

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

*Attribut* \[ In\]
</dt> <dd>

**Eine Zeichenfolge,** die den Attributnamen enthält.

</dd> <dt>

*Operator* \[ In\]
</dt> <dd>

**Eine Zeichenfolge,** die den Operator enthält. Unterstützte Werte finden Sie unter Hinweise.

</dd> <dt>

*value* \[ In\]
</dt> <dd>

**Eine Zeichenfolge,** die den Attributwert enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Bei zusammengesetzten Abfragen, die **Die Abfrage verwenden,** wird die Zwischenschreibung nicht beachtet.

Eine Liste der Werte für den *Attributparameter* finden Sie im Abschnitt [Alphabetische Attributreferenz.](alphabetical-attribute-reference.md)

In einem **Query-Objekt** enthaltene Bedingungen werden in Bedingungsgruppen organisiert. Mehrere Bedingungen innerhalb einer Bedingungsgruppe werden immer mithilfe der AND-Logik verkettet. Bedingungsgruppen werden immer mithilfe der OR-Logik miteinander verkettet. Um eine neue Bedingungsgruppe zu starten, rufen **Sie Query.beginNextGroup auf.**

In der folgenden Tabelle sind die unterstützten Werte für den *Operator aufgeführt.*



| Operator            | Gilt für:     |
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

Im folgenden beispiel JScript **Query.addCondition** und **Query.beginNextGroup** verwendet, um eine Beispielabfrage auszuführen.


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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MediaCollection.createQuery**](mediacollection-createquery.md)
</dt> <dt>

[**MediaCollection.getPlaylistByQuery**](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[**MediaCollection.getStringCollectionByQuery**](mediacollection-getstringcollectionbyquery.md)
</dt> <dt>

[**Abfrageobjekt**](query-object.md)
</dt> <dt>

[**Query.beginNextGroup**](query-beginnextgroup.md)
</dt> </dl>

 

 





