---
description: .
ms.assetid: 0e5a633e-1703-4b72-8a04-6da71aec0ae2
title: Abfrageprozess in Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d92d868cb843e96b04d6b4bd575284638b6652ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750345"
---
# <a name="querying-process-in-windows-search"></a>Abfrageprozess in Windows Search

Dieses Thema ist wie folgt organisiert:

-   [Informationen zum Abfragen in Windows Search](#about-querying-in-windows-search)
    -   [Lokale Abfragen und Remote Abfragen](#local-and-remote-queries)
    -   [Übersicht über die strukturierte Abfrage-API](#structured-query-api-overview)
-   [Abfragen von Szenarien](#querying-scenarios)
    -   [Bedingungs Extraktion und Abfrage Verarbeitung](#condition-extraction-and-query-parsing)
    -   [Abfragen des Indexes](#querying-the-index)
-   [Zugehörige Themen](#related-topics)

## <a name="about-querying-in-windows-search"></a>Informationen zum Abfragen in Windows Search

Das Abfragen in Windows Search basiert auf den folgenden vier Ansätzen:

-   [Erweiterte Abfrage Syntax](-search-3x-advancedquerysyntax.md) (AQS)
-   Natürliche Abfrage Syntax (NQS)
-   Structured Query Language (SQL) (Structured Query Language, SQL)
-   Strukturierte Abfrageschnittstellen

AQS ist die Standard Abfrage Syntax, die von Windows Search verwendet wird, um den Index abzufragen und Suchparameter zu verfeinern und einzuschränken. AQS ist hauptsächlich für Benutzer sichtbar und kann von Benutzern verwendet werden, um AQS-Abfragen zu erstellen. Sie kann jedoch auch von Entwicklern verwendet werden, um Abfragen Programm gesteuert zu erstellen. In Windows 7 wurde die kanonische AQS eingeführt und muss zum programmgesteuerten Generieren von AQS-Abfragen verwendet werden. In Windows 7 und höher kann eine Kontextmenü Option basierend darauf verfügbar sein, ob eine AQS-Bedingung erfüllt ist. Weitere Informationen finden Sie unter "erzielen von dynamischen Verhalten bei statischen Verben mithilfe der erweiterten Abfrage Syntax" unter [Erstellen von Kontextmenü Handlern](../shell/context-menu-handlers.md). AQS-Abfragen können auf bestimmte Typen von Dateien beschränkt werden, die als Dateitypen bezeichnet werden. Weitere Informationen finden Sie unter [Dateitypen und Zuordnungen](../shell/fa-intro.md). Eine Referenz Dokumentation zu den relevanten Eigenschaften finden Sie unter [System. Kind](../properties/props-system-kind.md)und [System. kindtext](../properties/props-system-kindtext.md).

NQS ist eine Abfrage Syntax, die einfacher als AQS ist und der menschlichen Sprache ähnelt. NQS kann von Windows Search verwendet werden, um den Index abzufragen, wenn NQS anstelle der standardmäßigen AQS ausgewählt wird.

SQL ist eine Text Sprache, mit der Abfragen definiert werden. SQL ist in vielen verschiedenen Datenbanktechnologien üblich. Windows Search verwendet SQL, implementiert eine Teilmenge davon und erweitert Sie durch Hinzufügen von Elementen zur Sprache. Windows Search SQL erweitert die Standard Abfrage Syntax von SQL-92 und SQL-99, um die Nützlichkeit durch textbasierte Suchvorgänge zu verbessern. Alle Features von Windows Search SQL sind mit Windows Search unter Windows XP und Windows Server 2003 und höher kompatibel. Weitere Informationen zu Windows Search SQL finden Sie unter [Abfragen des Indexes mit der SQL-Syntax von Windows Search](-search-sql-windowssearch-entry.md)und [Übersicht über die SQL-Syntax von Windows Search](-search-sql-ovwofsearchquery.md).

Die APIs für strukturierte Abfragen werden weiter unten in diesem Thema beschrieben. Eine Referenz Dokumentation zu den APIs für strukturierte Abfragen finden Sie unter [Abfragen von Schnittstellen](-search-querying-interfaces-entry-page.md). Schnittstellen wie [**isearchqueryhelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) helfen beim Erstellen von SQL-Zeichen folgen aus einem Satz von Eingabe Werten. Diese Schnittstelle konvertiert AQS-Benutzer Abfragen in Windows Search SQL und gibt Abfrage Einschränkungen an, die in SQL, aber nicht in AQS ausgedrückt werden können. [**Isearchqueryhelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) erhält auch eine OLE DB Verbindungs Zeichenfolge, um eine Verbindung mit der Windows Search-Datenbank herzustellen.

### <a name="local-and-remote-queries"></a>Lokale Abfragen und Remote Abfragen

Sie können Ihre Abfragen entweder lokal oder Remote ausführen. Eine lokale Abfrage mit der [from-Klausel](-search-sql-from.md) wird im folgenden Beispiel gezeigt. Eine lokale Abfrage fragt nur den lokalen SystemIndex-Katalog ab.


```
FROM SystemIndex
```



Eine Remote Abfrage mit der [from-Klausel](-search-sql-from.md) wird im folgenden Beispiel gezeigt. Durch das Hinzufügen von Computername wird das vorherige Beispiel in eine Remote Abfrage transformiert.


```
FROM [<ComputerName>.]SystemIndex
```



In Windows XP und Windows Server 2003 ist Windows Search standardmäßig nicht installiert. Nur Windows Search 4 (WS4) bietet Unterstützung für Remote Abfragen. Frühere Versionen von Windows Desktop Search (WDS), wie z. b. 3,01 und früher, unterstützen keine Remote Abfragen. Mit Windows Explorer können Sie den lokalen Index eines Remote Computers für Dateisystem Elemente (Elemente, die vom Protokoll "file:" behandelt werden) Abfragen.

Zum Abrufen eines Elements nach Remote Abfrage muss das Element die folgenden Anforderungen erfüllen:

-   Kann über Universal Naming Convention (UNC)-Pfad aufgerufen werden.
-   Vorhanden auf dem Remote Computer, auf den der Client Zugriff hat.
-   Die Sicherheit muss festgelegt sein, damit der Client über Lesezugriff verfügen kann.

Windows-Explorer verfügt über Features zum Freigeben von Elementen, einschließlich einer öffentlichen Freigabe ( \\ \\ \\ Public \\ ...) im **Netzwerk-und Freigabe Center** und einer "Benutzer Freigabe" ( \\ \\ Computer \\ Benutzer.. \\ .) für Elemente, die über den Freigabe-Assistenten freigegeben werden. Nachdem Sie die Ordner freigegeben haben, können Sie den lokalen Index Abfragen, indem Sie den Computernamen des Remote Computers in der from-Klausel und einen UNC-Pfad auf dem Remote Computer in der Scope-Klausel angeben. Eine Remote Abfrage mit der from-Klausel und der Scope-Klausel ist im folgenden Beispiel dargestellt.


```
SELECT System.ItemName FROM MachineName.SystemIndex WHERE SCOPE='file://MachineName/<path>' 
```



In den hier bereitgestellten Beispielen wird SQL verwendet.

### <a name="structured-query-api-overview"></a>Übersicht über die strukturierte Abfrage-API

Eine strukturierte Abfrage bietet die Möglichkeit, anhand von booleschen Kombinationen von Abfragen über einzelne Eigenschaften nach Informationen zu suchen. In diesem Thema werden die Funktionen der wichtigsten strukturierten Abfrage-APIs und-Methoden erläutert. Eine Referenz Dokumentation zu den APIs für strukturierte Abfragen finden Sie unter [Abfragen von Schnittstellen](-search-querying-interfaces-entry-page.md).

### <a name="iqueryparser"></a>Iqueryparser

Die [**iqueryparser::P Arse**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-parse) -Methode analysiert eine Benutzereingabe Zeichenfolge und erzeugt eine Interpretation in Form einer [**iquerysolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution). Wenn der *pcustomproperties* -Parameter dieser Methode nicht NULL ist, handelt es sich um eine Enumeration von [**irichchunk**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk) -Objekten (eine für jede erkannte benutzerdefinierte Eigenschaft). Die anderen [**iqueryparser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) -Methoden ermöglichen es der Anwendung, mehrere Optionen wie locale, ein Schema, eine Wörter Trennung und Handler für verschiedene Typen von benannten Entitäten festzulegen. [**Iqueryparser:: getschemaprovider**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-getschemaprovider) gibt eine [**ischemaprovider**](/windows/desktop/api/Structuredquery/nn-structuredquery-ischemaprovider) -Schnittstelle zum Durchsuchen des geladenen Schemas zurück.

### <a name="iquerysolution--iconditionfactory"></a>Iquerysolution: iconditionfactory

Die [**iquerysolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution) -Schnittstelle stellt alle Informationen über das Ergebnis der Verarbeitung einer Eingabe Zeichenfolge bereit. Da **iquerysolution** auch eine [**iconditionfactory**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory) -Schnittstelle ist, können zusätzliche Bedingungs Struktur Knoten erstellt werden. Die [**iquerysolution:: GetQuery**](/windows/desktop/api/Structuredquery/nf-structuredquery-iquerysolution-getquery) -Methode erzeugt eine Bedingungs Struktur für die Interpretation. **Iquerysolution:: GetQuery** gibt auch den Semantik Typ zurück.

### <a name="iconditionfactory"></a>Iconditionfactory

[**Iconditionfactory**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory) erstellt Bedingungs Struktur Knoten. Wenn der *vereinfachte Parameter* von [**iconditionfactory:: makenot**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makenot) **Variant \_ true** ist, wird die resultierende [**icondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) -Eigenschaft vereinfacht und muss kein Negations Knoten sein. Wenn der *psubconditions* -Parameter von [**iconditionfactory:: makeandor**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makeandor) nicht NULL ist, sollte dieser Parameter eine Enumeration von [**icondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) -Objekten sein und zu Unterstrukturen werden. [**Iconditionfactory:: makeleaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makeleaf) erstellt einen Blattknoten mit einem angegebenen Eigenschaftsnamen,-Vorgang und-Wert. Die Zeichenfolge im *pvaluetype* -Parameter sollte der Name eines Semantik Typs aus dem Schema sein. Wenn der *Erweiterungs Parameter* **Variant \_ true** und die-Eigenschaft virtuell ist, ist die resultierende Bedingungs Struktur in der Regel eine Disjunktion, die sich aus der Erweiterung der-Eigenschaft auf die definierten-Bestandteile ergibt. Wenn der Wert nicht NULL ist, sollten die Parameter *ppropertynameterm*, *poperatorterm* und *pvalueterm* Begriffe identifizieren, die die Eigenschaft, den Vorgang und den Wert angeben.

### <a name="icondition--ipersiststream"></a>Icondition: IPersistStream

Die [**icondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) -Schnittstelle ist ein einzelner Knoten in einer Bedingungs Struktur. Der Knoten kann ein Negation-Knoten, ein Knoten, ein Knoten oder ein Blattknoten sein. Für einen nicht Blattknoten gibt [**icondition:: getsubconditions**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getsubconditions) eine Enumeration der Teil Strukturen zurück. Bei einem Blattknoten geben die folgenden Methoden von [**icondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) die folgenden Werte zurück:

-   [**Getcomparisoninfo**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getcomparisoninfo) gibt den Eigenschaftsnamen, den Vorgang und den Wert zurück.
-   [**Getvaluetype**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getvaluetype) gibt den semantischen Typ des Werts zurück, der im *pszvaluetype* -Parameter von [**iconditionfactory:: makeleaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makeleaf)angegeben wurde.
-   [**GetValueNormalization**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getvaluenormalization) gibt eine Zeichen folgen Form des Werts zurück. (Wenn der Wert bereits eine Zeichenfolge ist, wird dieses Formular in Bezug auf Groß-/Kleinschreibung, Akzente usw. normalisiert.)
-   [**Getinputterms**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getinputterms) gibt Informationen darüber zurück, welche Teile des Eingabe Satzes den Eigenschaftsnamen, den Vorgang und den Wert generiert haben.
-   [**Clone**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-clone) gibt eine tiefe Kopie einer Bedingungs Struktur zurück.

### <a name="irichchunk"></a>Irichchunk

Jedes [**irichchunk**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk) -Objekt identifiziert eine tokenspanne und eine Zeichenfolge. **Irichchunk** ist eine hilfsprogrammschnittstelle, die Informationen über eine Spanne (in der Regel eine Spanne von Token) darstellt, die durch eine Anfangsposition und-Länge gekennzeichnet wird. Diese Spannen Informationen beinhalten eine Zeichenfolge und/oder eine **Variante**.

### <a name="iconditiongenerator"></a>Iconditiongenerator

Die [**iconditiongenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) -Schnittstelle wird von der Anwendung bereitgestellt, um die Generierung von Erkennungs-und Bedingungs Strukturen für einen benannten Entitätstyp zu verarbeiten. Ein Bedingungs Generator wird an [**iqueryparser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) über [**iqueryparser:: setmultioption**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-setmultioption)übergeben. [**Iqueryparser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) ruft [**iconditiongenerator:: Initialize**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-initialize) mit einem [**ischemaprovider**](/windows/desktop/api/Structuredquery/nn-structuredquery-ischemaprovider) für das aktuell geladene Schema auf. Auf diese Weise kann [**iconditiongenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) alle erforderlichen Schema Informationen abrufen. Beim Parsen einer Eingabe Zeichenfolge ruft **iqueryparser** die [**iconditiongenerator:: erkenzenamedentities**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-recognizenamedentities) -Methode jedes [**iconditiongenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator)auf, sodass das Vorkommen von benannten Entitäten, das in der Eingabe Zeichenfolge erkannt wird, gemeldet werden kann. **Iqueryparser** kann das aktuelle Gebiets Schema verwenden und sollte die Tokenisierung der Eingabe verwenden, da es die tokenspannen von benannten Entitäten melden muss.

Wenn [**iqueryparser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) einen Blattknoten ausgibt und der Semantik Typ des Werts mit dem benannten Entitätstyp für einen [**iconditiongenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator)übereinstimmt, ruft **iqueryparser** [**iconditiongenerator:: generateforleaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-generateforleaf) mit den Informationen für den zu generierenden Knoten auf. Wenn der [**iconditiongenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) S OK zurückgibt \_ , sollte er eine Bedingungs Struktur zurückgeben (bei der es sich nicht um einen Endknoten handeln muss) und **iqueryparser** darüber informieren, ob die Alternative Zeichen folgen Interpretation unterdrückt werden soll, die normalerweise als Vorsichtsmaßnahme generiert würde.

### <a name="itokencollection"></a>Iabkencollection

Die [**itokencollection:: numoftokens**](/windows/desktop/api/Structuredquery/nf-structuredquery-itokencollection-numberoftokens) -Methode gibt die Anzahl der Token zurück. [**Itokencollection:: GetToken**](/windows/desktop/api/Structuredquery/nf-structuredquery-itokencollection-gettoken) gibt Informationen zum *i* Th-Token zurück. Der Anfang und die Länge sind Zeichen Positionen in der Eingabe Zeichenfolge. Der zurückgegebene Text ist nur ungleich NULL, wenn ein Text vorhanden ist, der die Zeichen aus der Eingabe Zeichenfolge überschreibt. Dies wird z. b. verwendet, um einen Bindestrich in der Eingabe Zeichenfolge zu überschreiben, und nicht, wenn sich dieser Bindestrich in einem Kontext befindet, in dem er als Negation interpretiert werden soll.

### <a name="inamedentitycollector"></a>Inamedentitycollector

[**Iconditiongenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) Ruft für jede erkannte benannte Entität [**inamedentitycollector:: Add**](/windows/desktop/api/Structuredquery/nf-structuredquery-inamedentitycollector-add) auf. Die Spannen sind tokenspannen. Dies muss immer die Groß-/Kleinschreibung *sein?* *beginactual*  <  *endactual* ? *endspan*. *beginspan* und *endspan* können von *beginactual* und *endactual* abweichen, wenn die benannte Entität beginnt und/oder mit semantisch unbedeutenden Token, wie z. b. Anführungszeichen, endet (die von der benannten Entität abgedeckt werden). Der Wert muss als Zeichenfolge ausgedrückt werden und wird anschließend in einem Aufrufen von [**iconditiongenerator:: generateforleaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-generateforleaf)angezeigt.

### <a name="ischemaprovider"></a>Ischemaprovider

Die [**ischemaprovider**](/windows/desktop/api/Structuredquery/nn-structuredquery-ischemaprovider) -Schnittstelle kann verwendet werden, um ein geladenes Schema nach Entitäten (Typen) und Beziehungen (Eigenschaften) zu durchsuchen. Im folgenden werden die einzelnen Methoden beschrieben:

-   [**Entitäten**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-entities) gibt eine Enumeration aller Entitäten ([**IEntity**](/windows/desktop/api/Structuredquery/nn-structuredquery-ientity)) im Schema zurück.
-   [**Rootentity**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-rootentity) gibt die Stamm Entität des Schemas zurück. Bei einem flachen Schema wird der Haupttyp jeder [**iquerysolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution) zurückgegeben.
-   [**GetEntity**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-getentity) sucht eine Entität anhand des Namens und gibt S false zurück, \_ Wenn keine solche Entität im Schema vorhanden ist.
-   [**Metadaten**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-metadata) gibt eine Enumeration von [**IMetadata**](/windows/desktop/api/Structuredquery/nn-structuredquery-imetadata) -Schnittstellen zurück.

### <a name="ientity"></a>IEntity

Die [**IEntity**](/windows/desktop/api/Structuredquery/nn-structuredquery-ientity) -Schnittstelle ist eine Schema Entität, die einen Typ mit einem Namen darstellt, eine Anzahl benannter Beziehungen zu anderen Typen (Eigenschaften) aufweist und von einer Basis Entität abgeleitet ist. Im folgenden werden die einzelnen Methoden beschrieben:

-   [**IEntity::**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-relationships) Relationship gibt eine Enumeration von [**IRelationship**](/windows/desktop/api/Structuredquery/nn-structuredquery-irelationship) -Objekten zurück, eine für jede ausgehende Beziehung dieses Typs. Jede ausgehende Beziehung einer Entität hat einen Namen.
-   [**IEntity:: GetRelationship**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-getrelationship) findet eine Beziehung nach Name und gibt S false zurück, \_ Wenn keine solche Beziehung für diese Entität vorhanden ist.
-   [**IEntity:: Metadata**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-metadata) gibt eine Enumeration von [**IMetadata**](/windows/desktop/api/Structuredquery/nn-structuredquery-imetadata) -Schnittstellen zurück, eine für jedes metadatenpaar dieser Entität.
-   [**IEntity::D efaultphrase**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-defaultphrase) gibt einen Standardausdruck zurück, um das Erstellen einer AQS-oder NQS-neuanweisung einer Bedingungs Struktur zu vereinfachen.

### <a name="irelationship"></a>IRelationship

Die [**IRelationship**](/windows/desktop/api/Structuredquery/nn-structuredquery-irelationship) -Schnittstelle stellt eine Beziehung zwischen zwei Entitäten dar: eine Quelle und ein Ziel. Im folgenden werden die einzelnen Methoden beschrieben:

-   [**IRelationship:: Isreal**](/windows/desktop/api/Structuredquery/nf-structuredquery-irelationship-isreal) meldet, ob eine Beziehung Real ist. Wenn z. B. Entität a von Entität B abgeleitet ist und eine Beziehung namens r von ihr erbt, hat eine möglicherweise noch eine eigene Beziehung namens r. Allerdings müssen die Beziehungen A und R den gleichen Zieltyp wie b aufweisen, und der einzige Grund dafür ist das Speichern von Metadaten, die für b spezifisch sind. Eine solche Beziehung von B ist nicht Real.
-   [**IRelationship:: medadata**](/windows/desktop/api/Structuredquery/nf-structuredquery-irelationship-metadata) gibt eine Enumeration von [**IMetadata**](/windows/desktop/api/Structuredquery/nn-structuredquery-imetadata) -Schnittstellen zurück, eine für jedes metadatenpaar dieser Entität.
-   [**IRelationship::D efaultphrase**](/windows/desktop/api/Structuredquery/nf-structuredquery-irelationship-defaultphrase) gibt den für diese Beziehung in Restatements zu verwendenden Standardausdruck zurück. Jede Beziehung verfügt über einen Standardausdruck, der die Erstellung einer AQS-oder NQS-neuanweisung einer Bedingungs Struktur erleichtert.

### <a name="imetadata"></a>IMetadata

Metadaten sind Schlüssel-Wert-Paare, die jeweils mit einer Entität, einer Beziehung oder dem gesamten Schema verknüpft sind. Da Schlüssel nicht notwendigerweise eindeutig sind, kann eine Auflistung von Metadaten als mehrfach Zuordnung betrachtet werden. [**IMetadata:: GetData**](/windows/desktop/api/Structuredquery/nf-structuredquery-imetadata-getdata) wird aufgerufen, um den Schlüssel und den Wert für ein metatdatenpaar abzurufen.

## <a name="querying-scenarios"></a>Abfragen von Szenarien

In den folgenden Szenarien wird die Verwendung von strukturierten Abfrage-APIs in Windows Search in allgemeinen Abfrage Szenarios beschrieben, wie z. b. das Erstellen einer Bedingungs Struktur und das Abfragen des Indexes.

### <a name="condition-extraction-and-query-parsing"></a>Bedingungs Extraktion und Abfrage Verarbeitung

Wenn eine Abfrage erstellt wird, wird der zugehörige Bereich definiert, indem dem System mitgeteilt wird, wo gesucht werden soll. Dadurch werden die Suchergebnisse eingeschränkt. Nachdem der Bereich definiert wurde, wird ein Filter angewendet, und es wird ein Filtersatz zurückgegeben. Die Suchergebnisse werden durch das Entwickeln einer Bedingungs Struktur mit Blattknoten, ähnlich einem Diagramm, eingeschränkt. Diese Bedingungen werden dann extrahiert. Eine Bedingungs Struktur ist eine boolesche Kombination (and, or, not) der Blatt Bedingungen, von denen jede eine Eigenschaft über einen Vorgang mit einem Wert verknüpft. Ein Blattknoten stellt eine Einschränkung für eine einzelne Eigenschaft zu einem Wert durch einige Vorgänge dar.

Eine Filter Einschränkung erfordert einen logischen Ausdruck, der die Einschränkung beschreibt. Die Definition dieses Ausdrucks beginnt mit der [**icondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) -Schnittstelle, die verwendet wird, um einen einzelnen Knoten in einer Bedingungs Struktur zu erstellen. Da im folgenden Beispiel nur eine Bedingung vorhanden ist, ändert sich die Struktur nicht.


```C++
    
    [
        object,
        uuid(0FC988D4-C935-4b97-A973-46282EA175C8),
        pointer_default(unique)
    ]
    interface ICondition : IPersistStream
    {
        HRESULT GetConditionType([out, retval] CONDITION_TYPE* pNodeType);
        HRESULT GetSubConditions([in] REFIID riid, [out, retval, iid_is(riid)] void** ppv);
        [local] HRESULT GetComparisonInfo([out, annotation("__deref_opt_out")] LPWSTR *ppszPropertyName, [out, annotation("__out_opt")] CONDITION_OPERATION *pOperation, [out, annotation("__out_opt")] PROPVARIANT *pValue);
        HRESULT GetValueType([out, retval] LPWSTR* ppszValueTypeName);
        HRESULT GetValueNormalization([out, retval] LPWSTR* ppszNormalization);
        [local] HRESULT GetInputTerms([out, annotation("__out_opt")] IRichChunk** ppPropertyTerm, [out, annotation("__out_opt")] IRichChunk** ppOperationTerm, [out, annotation("__out_opt")] IRichChunk** ppValueTerm);
        HRESULT Clone([out, retval] ICondition** ppc);
    };


```



Wenn mehrere Filterbedingungen vorhanden sind, werden und und andere boolesche Operatoren verwendet, um eine einzelne Struktur zu erzielen. -Strukturen und-Strukturen und-Strukturen stellen Zusammenhänge und Disjunktionen ihrer Teil Strukturen dar. Eine not-Tree-Struktur stellt die Negation der einzelnen Unterstruktur dar. AQS bietet einen Text Ansatz, mit dem logische Ausdrücke mit booleschen Operatoren erreicht werden können. Dies ist häufig einfacher.

Im nächsten Beispiel wird die Bedingungs Struktur ([**icondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition)) in das visuelle Formular konvertiert. Der Abfrage Parser konvertiert mithilfe der [**iqueryparser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) -Schnittstelle die [**icondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) in eine RTF-Abfrage Zeichenfolge (Rich Text formatiert). Die [**iqueryparser:: restateto String**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-restatetostring) -Methode gibt den Abfragetext zurück, während die [**iqueryparser::P Arse**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-parse) -Methode eine [**iquerysolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution) -Schnittstelle erzeugt. Das folgende Beispiel zeigt, wie Sie das tun.


```C++
    [
        object,
        uuid(2EBDEE67-3505-43f8-9946-EA44ABC8E5B0),
        pointer_default(unique)
    ]
    interface IQueryParser : IUnknown
    {
        HRESULT Parse([in] LPCWSTR pszInputString, [in] IEnumUnknown* pCustomProperties, [out, retval] IQuerySolution** ppSolution);
        HRESULT SetOption([in] STRUCTURED_QUERY_SINGLE_OPTION option, [in] PROPVARIANT const* pOptionValue);
        HRESULT GetOption([in] STRUCTURED_QUERY_SINGLE_OPTION option, [out, retval] PROPVARIANT* pOptionValue);
        HRESULT SetMultiOption([in] STRUCTURED_QUERY_MULTIOPTION option, [in] LPCWSTR pszOptionKey, [in] PROPVARIANT const* pOptionValue);
        HRESULT GetSchemaProvider([out, retval] ISchemaProvider** ppSchemaProvider);
        HRESULT RestateToString([in] ICondition* pCondition, [in] BOOL fUseEnglish, [out] LPWSTR* ppszQueryString);
        HRESULT ParsePropertyValue([in] LPCWSTR pszPropertyName, [in] LPCWSTR pszInputString, [out, retval] IQuerySolution** ppSolution);
        HRESULT RestatePropertyValueToString([in] ICondition* pCondition, [in] BOOL fUseEnglish, [out] LPWSTR* ppszPropertyName, [out] LPWSTR* ppszQueryString);
    };

```



Die Haupt Eingabe von [**iqueryparser::P Arse**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-parse) ist eine Benutzereingabe Zeichenfolge, die analysiert werden soll, aber die Anwendung kann den Abfrage Parser auch über alle Eigenschaften informieren, die er in der Eingabe erkannt hat (von anwendungsspezifischer Syntax). Die Ausgabe von **iqueryparser::P Arse** ist eine [**iquerysolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution), die alle Informationen zu diesem analysieren-Aufruf bereitstellt. Es gibt Methoden zum Abrufen der Eingabe Zeichenfolge, zur Tokenisierung der Eingabe Zeichenfolge, zu Analyse Fehlern und der analysierten Abfrage als Bedingungs Struktur, die durch eine [**icondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition)dargestellt wird. Das folgende Beispiel zeigt...


```C++
    [
        object,
        uuid(D6EBC66B-8921-4193-AFDD-A1789FB7FF57),
        pointer_default(unique)
    ]
    interface IQuerySolution : IConditionFactory
    {
        [local] HRESULT GetQuery([out, annotation("__out_opt")] ICondition** ppQueryNode, [out, annotation("__out_opt")] IEntity** ppMainType);
        HRESULT GetErrors([in] REFIID riid, [out, retval, iid_is(riid)] void** ppParseErrors);
        [local] HRESULT GetLexicalData([out, annotation("__deref_opt_out")] LPWSTR* ppszInputString, [out, annotation("__out_opt")] ITokenCollection** ppTokens, [out, annotation("__out_opt")] LCID* pLocale, [out, annotation("__out_opt")] IUnknown** ppWordBreaker);
    }    

    

```



Im vorherigen Beispiel konnte [**iquerysolution:: GetQuery**](/windows/desktop/api/Structuredquery/nf-structuredquery-iquerysolution-getquery) alle Informationen über die Abfrage abrufen, einschließlich des ursprünglichen Texts, der Token, die den Text umfassen, oder der Bedingungs Struktur. Beispiele für mögliche zurückgegebene Abfrage Werte sind in der folgenden Tabelle aufgeführt.



| Beispiele für zurückgegebene Abfrage Werte                        | BESCHREIBUNG                                                                                               |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| `  author:relja OR author:tyler`                         | Der Abfragetext, den [**iqueryparser:: restateto String**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-restatetostring) zurückgibt. |
| `?author?, ?:?, ?relja?, ?OR?, ?author?, ?:?, ?tyler?`   | Die Unterbrechung von Token                                                                                  |
| ![eine nicht aufgelöste Bedingungs Struktur](images/queryvalues1.png) | Eine nicht aufgelöste Bedingungs Struktur                                                                              |



 

Die ursprüngliche Bedingungs Struktur, die zurückgegeben wird, ist nicht aufgelöst. In einer nicht aufgelösten Bedingungs Struktur werden Datums-und Uhrzeit Verweise, wie z `date:yesterday` . b., nicht in die absolute Zeit konvertiert. Außerdem werden virtuelle Eigenschaften nicht erweitert. Virtuelle Eigenschaften sind Eigenschaften, die als Aggregate mehrerer Eigenschaften fungieren.

Die Abfrage `kind:email from:reljai` erzeugt z. b. die folgenden nicht aufgelösten und aufgelösten Bedingungs Strukturen. Die nicht aufgelöste Bedingungs Struktur befindet sich auf der linken Seite, und die aufgelöste Bedingungs Struktur befindet sich auf der rechten Seite.

![nicht aufgelöste und aufgelöste Bedingungs Strukturen](images/conditiontree.png)

Die aufgelöste Struktur kann durch Aufrufen von [**iconditionfactory:: Resolve**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-resolve)abgerufen werden. Durch die Übergabe von [**sqro nicht \_ Auflösen von \_ \_ DateTime**](/windows/desktop/api/Structuredquery/ne-structuredquery-structured_query_resolve_option) bleiben jedoch das Datum und die Uhrzeit nicht aufgelöst. Eine nicht aufgelöste Bedingungs Struktur hat Vorteile, da eine nicht aufgelöste Bedingungs Strukturinformationen zur Abfrage enthält. Jeder Blattknoten verweist auf die von [**iquerysolution:: getlexicaldata**](/windows/desktop/api/Structuredquery/nf-structuredquery-iquerysolution-getlexicaldata)zurückgegebenen Token, die der-Eigenschaft, dem-Operator und dem-Wert entsprechen, wenn die [**irichchunk**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk) -Schnittstelle verwendet wird. Das folgende Beispiel zeigt...


```C++
    interface ITokenCollection : IUnknown
    {
        HRESULT NumberOfTokens(ULONG* pCount);
        HRESULT GetToken([in] ULONG i, [out, annotation("__out_opt")] ULONG* pBegin, [out, annotation("__out_opt")] ULONG* pLength, [out, annotation("__deref_opt_out")] LPWSTR* ppsz);
    };

ICondition:: GetInputTerms([out, annotation("__out_opt")] 
IRichChunk** ppPropertyTerm, [out, annotation("__out_opt")] 
IRichChunk** ppOperationTerm, [out, annotation("__out_opt")] 
IRichChunk** ppValueTerm);

    interface IRichChunk : IUnknown
    {
        HRESULT GetData([out, annotation("__out_opt")] ULONG* pFirstPos, [out, annotation("__out_opt")] ULONG* pLength, [out, annotation("__deref_opt_out")] LPWSTR* ppsz, [out, annotation("__out_opt")] PROPVARIANT* pValue);
    }
```



### <a name="querying-the-index"></a>Abfragen des Indexes

Es gibt mehrere Ansätze zum Abfragen des Indexes. Einige basieren auf SQL, und andere basieren auf AQS. Mithilfe von Abfrage [Schnittstellen](./-search-querying-interfaces-entry-page.md)können Sie den Windows-Suchindex auch Programm gesteuert Abfragen. Es gibt drei Schnittstellen, die für das Abfragen des Indexes spezifisch sind: [**isearchqueryhelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper), [**irowsetprioritisierung**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)und [**irowsetevents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents). Konzeptionelle Informationen finden Sie unter [Programm gesteuertes Abfragen des Indexes](-search-3x-wds-qryidx-overview.md).

Sie können eine Komponente oder Hilfsklasse entwickeln, um den Index mithilfe der [**isearchqueryhelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) -Schnittstelle abzufragen. Diese Schnittstelle wird als Hilfsklasse in [**isearchcatalogmanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) (und [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)) implementiert und durch Aufrufen von [**isearchcatalogmanager:: getqueryhelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper)abgerufen. Konzeptionelle Informationen finden Sie unter [Abfragen des Indexes mit isearchqueryhelper](-search-3x-wds-qryidx-searchqueryhelper.md).

[**Isearchqueryhelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) ermöglicht Folgendes:

-   Rufen Sie eine OLE DB Verbindungs Zeichenfolge für die Verbindung mit der Windows Search-Datenbank ab.
-   Konvertieren Sie AQS-Benutzer Abfragen in Windows Search SQL.
-   Geben Sie Abfrage Einschränkungen an, die in SQL ausgedrückt werden können, aber nicht in AQS.

Indizierungs Priorisierung und rowsetereignisse werden in Windows 7 und höher unterstützt. Bei [**irowsetpriorisierung**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) gibt es einen Prioritäts Stapel, der es dem Client ermöglicht, anzufordern, dass die in einer bestimmten Abfrage verwendeten Bereiche höher als normale Priorität sind. [**Irowsetevents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents) ermöglicht das Benachrichtigen von Änderungen an Elementen in Rowsets, einschließlich der Addition neuer Elemente, dem Löschen von Elementen und der Änderung von Elementdaten. Durch die Verwendung von Rowset-Ereignis Benachrichtigungen wird sichergestellt, dass die Ergebnisse für vorhandene Abfragen so aktuell wie möglich sind. Konzeptionelle Informationen finden Sie unter [Indizieren von Priorisierung und rowsetereignissen in Windows 7](indexing-prioritization-and-rowset-events.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Indizierung, Abfragen und Benachrichtigungen in Windows Search](-search-3x-wds-included-in-index.md)
</dt> <dt>

[Was ist im Index enthalten?](-search-indexing-process-overview.md)
</dt> <dt>

[Indizierungsprozess in Windows Search](-search-indexing-process-overview.md)
</dt> <dt>

[Benachrichtigungs Prozess in Windows Search](-search-3x-wds-support.md)
</dt> <dt>

[URL-Formatierungs Anforderungen](url-formatting-requirements.md)
</dt> </dl>

 

 
