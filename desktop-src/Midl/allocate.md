---
title: Attribut zuordnen
description: Mit dem Attribut \ zuordnen \ ACF können Sie die Speicher Belegung und die Freigabe Zuordnung für einen Typ anpassen, der in der IDL-Datei definiert ist.
ms.assetid: 1956b11f-bafa-41c3-9025-5fcbb890d1a2
keywords:
- Attribut-Mittel l zuordnen
topic_type:
- apiref
api_name:
- allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ff902e34e07ebd34edcb73797baa131eec8b222
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857271"
---
# <a name="allocate-attribute"></a>Attribut zuordnen

Mit dem Attribut " **\[ zuordnen \]** von ACF" können Sie die Speicher Belegung und die Zuordnung für einen in der IDL-Datei definierten Typ anpassen.

``` syntax
typedef [allocate (allocate-option-list) [, type-attribute-list] ] type-name;
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*zuordnen-Option-List* 
</dt> <dd>

Gibt eine oder mehrere Speicher Belegungs Optionen an. Wählen Sie entweder einen **einzelnen \_ Knoten** oder **alle \_ Knoten** aus, oder wählen Sie entweder " **frei** " oder " **nicht \_ frei**" oder eines der Paare aus. Wenn Sie mehr als eine Option angeben, trennen Sie die Optionen durch Kommas.

</dd> <dt>

*Type-Attribute-List* 
</dt> <dd>

Gibt andere optionale ACF-Typattribute an. Wenn Sie mehr als ein Type-Attribut angeben, trennen Sie die Optionen durch Kommas.

</dd> <dt>

*Typname* 
</dt> <dd>

Gibt einen Typ an, der in der IDL-Datei definiert ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das Attribut " **\[ zuordnen \]** " weist die folgenden gültigen Optionen auf.



| Option           | BESCHREIBUNG                                                           |
|------------------|-----------------------------------------------------------------------|
| **alle \_ Knoten**   | Führt einen-Rückruf aus, um Speicher für alle Knoten zuzuweisen und freizugeben.             |
| **einzelner \_ Knoten** | Führt viele einzelne Aufrufe aus, um jeden Knoten des Arbeitsspeichers zuzuordnen und freizugeben. |
| **free**         | Gibt Arbeitsspeicher bei Rückgabe vom Serverstub frei.                          |
| **nicht \_ kostenlos**   | Von wird vom Serverstub kein Arbeitsspeicher freigegeben.                  |



 

Standardmäßig kann der Stub Speicher für Daten, auf die durch einen eindeutigen oder einen vollständigen Zeiger verwiesen wird, zuordnen, indem er die Benutzer Zuordnungen für die [**\_ Benutzer \_**](midl-user-allocate-1.md) Zuordnungen und die [**mittlere \_ \_ Benutzer**](midl-user-free-1.md) Freigabe für jeden Zeiger aufrufen

Sie können die Geschwindigkeit der Anwendung optimieren, indem Sie die Option **alle \_ Knoten** angeben. Diese Option weist den Stub an, die Größe des gesamten Speichers zu berechnen, auf den über den Zeiger des angegebenen Typs verwiesen wird, und um einen einzelnen aufzurufenden [**Mittel l- \_ Benutzer \_ zuzuordnen**](midl-user-allocate-1.md). Der Stub gibt den Arbeitsspeicher frei, indem er einen [**\_ Benutzer \_ kostenlos**](midl-user-free-1.md)aufruft.

Die Option " **nicht \_ frei** gegeben" weist den Mittelwert Compiler an, einen Serverstub zu generieren, der für den angegebenen Typ keinen [**mittleren \_ Benutzer \_**](midl-user-free-1.md) Namen aufruft. Die **Option \_ nicht** verfügbar ermöglicht, dass die-Zeiger Strukturen für die Serveranwendung zugänglich bleiben, nachdem der Remote Prozedur Aufruf abgeschlossen und an den Client zurückgegeben wurde.

Das Attribut " **\[ zuordnen \]** " bewirkt, dass jeder **\[ in-, out \]** -Parameter, der ein Zeiger auf einen Typ ist, der mit der Option **alle \_ Knoten** qualifiziert ist, den Speicher neu zuordnen kann, wenn die Daten gemarshallt werden Es liegt in der Verantwortung der Anwendung, den zuvor zugeordneten Arbeitsspeicher für diesen Parameter freizugeben. Beispiel:

``` syntax
typedef struct thistype 
{ 
    [string] char * PTHISTYPE;  
} * PTHISTYPE
HRESULT proc1 ( [in,out] PTHISTYPE * ppthistype);
```

Der Datentyp "pthistype" wird vom Stub vor dem Aufheben des Marshalling erneut in der [**\[ out \]**](out-idl.md) -Richtung zugewiesen. Daher muss die Anwendung den Arbeitsspeicher freigeben, den Sie zuvor für die Daten dieses Parameters reserviert haben, oder es tritt ein Speicherplatz auf.

## <a name="examples"></a>Beispiele

``` syntax
/* ACF file */ 
typedef [allocate(all_nodes, dont_free)] PTYPE1; 
typedef [allocate(all_nodes)] PTYPE2; 
typedef [allocate(dont_free)] PTYPE3;
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Anwendungs Konfigurationsdatei (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**in**](in.md)
</dt> <dt>

[**mittlere Benutzer Zuordnungen \_ \_**](midl-user-allocate-1.md)
</dt> <dt>

[**mittlerer l- \_ Benutzer \_ kostenlos**](midl-user-free-1.md)
</dt> <dt>

[**vorgenommen**](out-idl.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 




