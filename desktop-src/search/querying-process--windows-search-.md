---
description: Abfrageprozess in Windows Search
ms.assetid: 0e5a633e-1703-4b72-8a04-6da71aec0ae2
title: Abfrageprozess in Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3585f2cca2a6d5d8548a85ae8fac759ec94b4fa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117328"
---
# <a name="querying-process-in-windows-search"></a>Abfrageprozess in Windows Search

Dieses Thema ist wie folgt organisiert:

-   [Informationen zum Abfragen in Windows Search](#about-querying-in-windows-search)
    -   [Lokale und Remoteabfragen](#local-and-remote-queries)
    -   [Übersicht über die API für strukturierte Abfragen](#structured-query-api-overview)
-   [Abfrageszenarien](#querying-scenarios)
    -   [Bedingungsextraktion und Abfrageparsing](#condition-extraction-and-query-parsing)
    -   [Abfragen des Index](#querying-the-index)
-   [Zugehörige Themen](#related-topics)

## <a name="about-querying-in-windows-search"></a>Informationen zum Abfragen in Windows Search

Abfragen in Windows Search basieren auf den folgenden vier Ansätzen:

-   [Erweiterte Abfragesyntax](-search-3x-advancedquerysyntax.md) (AQS)
-   Syntax natürlicher Abfragen (Natural Query Syntax, NQS)
-   Structured Query Language (SQL) (Structured Query Language, SQL)
-   Strukturierte Abfrageschnittstellen

AQS ist die Standardabfragesyntax, die von Windows Search zum Abfragen des Indexes und zum Verfeinern und Einengen von Suchparametern verwendet wird. AQS steht hauptsächlich für Benutzer zur Verfügung und kann von Benutzern zum Erstellen von AQS-Abfragen verwendet werden, kann aber auch von Entwicklern verwendet werden, um Abfragen programmgesteuert zu erstellen. In Windows 7 wurde kanonische AQS eingeführt und muss zum programmgesteuerten Generieren von AQS-Abfragen verwendet werden. Unter Windows 7 und höher kann eine Kontextmenüoption verfügbar sein, je nach Erfüllt einer AQS-Bedingung. Weitere Informationen finden Sie unter "Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax" (Abrufen des dynamischen Verhaltens für statische Verben mit erweiterter Abfragesyntax) in [Erstellen von Kontextmenühandlern.](../shell/context-menu-handlers.md) AQS-Abfragen können auf bestimmte Dateitypen beschränkt werden, die als Dateiarten bezeichnet werden. Weitere Informationen finden Sie unter [Dateitypen und Zuordnungen.](../shell/fa-intro.md) Eine Referenzdokumentation zu den relevanten Eigenschaften finden Sie unter [System.Kind](../properties/props-system-kind.md)und [System.KindText](../properties/props-system-kindtext.md).

NQS ist eine Abfragesyntax, die gelockerter als AQS ist und der menschlichen Sprache ähnelt. NQS kann von Windows Search Indexabfrage verwendet werden, wenn NQS anstelle der Standardeinstellung AQS ausgewählt ist.

SQL ist eine Textsprache, die Abfragen definiert. SQL ist in vielen verschiedenen Datenbanktechnologien üblich. Windows Search SQL verwendet, implementiert eine Teilmenge davon und erweitert sie durch Hinzufügen von Elementen zur Sprache. Windows Search SQL erweitert die Standardmäßige Sql-92- und SQL-99-Datenbankabfragesyntax, um ihre Nützlichkeit mit textbasierten Suchvorgängen zu verbessern. Alle Features von Windows Search SQL sind mit Windows Search unter Windows XP und Windows Server 2003 und höher kompatibel. Weitere Informationen zu Windows Search SQL finden Sie unter [Querying the Index with Windows Search SQL Syntax](-search-sql-windowssearch-entry.md)und Overview of Windows Search SQL [Syntax](-search-sql-ovwofsearchquery.md).

Die strukturierten Abfrage-APIs werden weiter unten in diesem Thema beschrieben. Eine Referenzdokumentation zu den strukturierten Abfrage-APIs finden Sie unter [Abfragen von Schnittstellen.](-search-querying-interfaces-entry-page.md) Schnittstellen wie [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) helfen beim Erstellen von SQL-Zeichenfolgen aus einem Satz von Eingabewerten. Diese Schnittstelle konvertiert AQS-Benutzerabfragen in Windows Search SQL und gibt Abfrageeinschränkungen an, die in SQL, aber nicht in AQS ausgedrückt werden können. [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) erhält auch eine OLE DB Verbindungszeichenfolge, um eine Verbindung mit der Windows Search herzustellen.

### <a name="local-and-remote-queries"></a>Lokale und Remoteabfragen

Sie können Ihre Abfragen entweder lokal oder remote ausführen. Eine lokale Abfrage, die die [FROM-Klausel verwendet,](-search-sql-from.md) wird im folgenden Beispiel gezeigt. Eine lokale Abfrage fragt nur den lokalen SystemIndex-Katalog ab.


```
FROM SystemIndex
```



Eine Remoteabfrage mithilfe der [FROM-Klausel](-search-sql-from.md) wird im folgenden Beispiel gezeigt. Durch hinzufügen von ComputerName wird das vorherige Beispiel in eine Remoteabfrage transformiert.


```
FROM [<ComputerName>.]SystemIndex
```



Standardmäßig ist für Windows XP und Windows Server 2003 Windows Search nicht installiert. Nur Windows Search 4 (WS4) bietet Remoteabfrageunterstützung. Frühere Versionen von Windows Desktop Search (WDS), z.B. 3.01 und früher, unterstützen keine Remoteabfragen. Mit Windows-Explorer können Sie den lokalen Index eines Remotecomputers nach Dateisystemelementen abfragen (Elemente, die vom Protokoll "file:" verarbeitet werden).

Um ein Element per Remoteabfrage abzurufen, muss das Element die folgenden Anforderungen erfüllen:

-   Der Zugriff ist über Universal Naming Convention (UNC)-Pfad möglich.
-   Auf dem Remotecomputer vorhanden, auf den der Client Zugriff hat.
-   Lassen Sie die Sicherheit so festgelegt, dass der Client Lesezugriff hat.

Windows-Explorer verfügt über Funktionen für die Freigabe von Elementen, einschließlich einer "öffentlichen" Freigabe \\ \\ (Öffentliche \\ \\ Computerfreigabe ...) im **Netzwerk- und Freigabecenter** und einer Benutzerfreigabe \\ \\ \\ (Computerbenutzer ...) für \\ Elemente, die über den Freigabe-Assistenten freigegeben wurden. Nachdem Sie die Ordner freigegeben haben, können Sie den lokalen Index abfragen, indem Sie den Computernamen des Remotecomputers in der FROM-Klausel und einen UNC-Pfad auf dem Remotecomputer in der SCOPE-Klausel angeben. Eine Remoteabfrage mithilfe der FROM- und SCOPE-Klauseln wird im folgenden Beispiel gezeigt.


```
SELECT System.ItemName FROM MachineName.SystemIndex WHERE SCOPE='file://MachineName/<path>' 
```



In den hier bereitgestellten Beispielen wird SQL verwendet.

### <a name="structured-query-api-overview"></a>Übersicht über die API für strukturierte Abfragen

Eine strukturierte Abfrage bietet die Möglichkeit, nach Informationen nach booleschen Kombinationen von Abfragen für einzelne Eigenschaften zu suchen. In diesem Thema werden die Funktionen der wichtigsten strukturierten Abfrage-APIs und -Methoden beschrieben. Eine Referenzdokumentation zu den strukturierten Abfrage-APIs finden Sie unter [Abfragen von Schnittstellen.](-search-querying-interfaces-entry-page.md)

### <a name="iqueryparser"></a>IQueryParser

Die [**IQueryParser::P arse-Methode**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-parse) analysiert eine Benutzereingabezeichenfolge und erzeugt eine Interpretation in Form einer [**IQuerySolution.**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution) Wenn der *pCustomProperties-Parameter dieser* Methode nicht NULL ist, handelt es sich um eine Enumeration von [**IRichChunk-Objekten**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk) (eines für jede erkannte benutzerdefinierte Eigenschaft). Mit den [**anderen IQueryParser-Methoden**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) kann die Anwendung mehrere Optionen festlegen, z. B. ein Locale, ein Schema, eine Wörtertrenneinheit und Handler für verschiedene Typen benannter Entitäten. [**IQueryParser::GetSchemaProvider gibt**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-getschemaprovider) eine [**ISchemaProvider-Schnittstelle**](/windows/desktop/api/Structuredquery/nn-structuredquery-ischemaprovider) zum Durchsuchen des geladenen Schemas zurück.

### <a name="iquerysolution--iconditionfactory"></a>IQuerySolution: IConditionFactory

Die [**IQuerySolution-Schnittstelle**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution) stellt alle Informationen zum Ergebnis der Analyse einer Eingabezeichenfolge bereit. Da **IQuerySolution auch** eine [**IConditionFactory-Schnittstelle**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory) ist, können zusätzliche Bedingungsstrukturknoten erstellt werden. Die [**IQuerySolution::GetQuery-Methode**](/windows/desktop/api/Structuredquery/nf-structuredquery-iquerysolution-getquery) erzeugt eine Bedingungsstruktur für die Interpretation. **IQuerySolution::GetQuery** gibt auch den semantischen Typ zurück.

### <a name="iconditionfactory"></a>IConditionFactory

[**IConditionFactory erstellt**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory) Bedingungsstrukturknoten. Wenn der *simplify-Parameter* von [**IConditionFactory::MakeNot**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makenot) **VARIANT \_ TRUE** ist, wird die resultierende [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) vereinfacht und muss kein Negationsknoten sein. Wenn der *pSubConditions-Parameter* von [**IConditionFactory::MakeAndOr**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makeandor) nicht NULL ist, sollte dieser Parameter eine Enumeration von [**ICondition-Objekten**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) sein und zu Teilstruktur werden. [**IConditionFactory::MakeLeaf erstellt**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makeleaf) einen Blattknoten mit einem angegebenen Eigenschaftennamen, Vorgang und Wert. Die Zeichenfolge im *pValueType-Parameter* sollte der Name eines semantischen Typs aus dem Schema sein. Wenn der *expand-Parameter* **VARIANT \_ TRUE** ist und die Eigenschaft virtuell ist, ist die resultierende Bedingungsstruktur in der Regel eine Disjunktion, die sich aus dem Erweitern der Eigenschaft auf die definierten Bestandteile ergibt. Wenn nicht NULL, sollten die Parameter *pPropertyNameTerm,* *pOperatorTerm* und *pValueTerm* Begriffe identifizieren, die die Eigenschaft, den Vorgang und den Wert angeben.

### <a name="icondition--ipersiststream"></a>ICondition : IPersistStream

Die [**ICondition-Schnittstelle**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) ist ein einzelner Knoten in einer Bedingungsstruktur. Der Knoten kann ein Negationsknoten, AND-Knoten, OR-Knoten oder Blattknoten sein. Für einen Nicht-Blattknoten gibt [**ICondition::GetSubConditions**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getsubconditions) eine Enumeration der Unterstrukturen zurück. Für einen Blattknoten geben die folgenden Methoden von [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) die folgenden Werte zurück:

-   [**GetComparisonInfo**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getcomparisoninfo) gibt den Namen, den Vorgang und den Wert der Eigenschaft zurück.
-   [**GetValueType**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getvaluetype) gibt den semantischen Typ des Werts zurück, der im *pszValueType-Parameter* von [**IConditionFactory::MakeLeaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makeleaf)spezifisch war.
-   [**GetValueNormalization**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getvaluenormalization) gibt eine Zeichenfolgenform des Werts zurück. (Wenn es sich bei dem Wert bereits um eine Zeichenfolge handelt, wird dieses Formular hinsichtlich Groß-/Schreibung, Akzenten usw. normalisiert.)
-   [**GetInputTerms**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getinputterms) gibt Informationen darüber zurück, welche Teile des Eingabesatzes den Eigenschaftennamen, den Vorgang und den Wert generiert haben.
-   [**Clone**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-clone) gibt eine tiefe Kopie einer Bedingungsstruktur zurück.

### <a name="irichchunk"></a>IRichChunk

Jedes [**IRichChunk-Objekt**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk) identifiziert eine Tokenspanne und eine Zeichenfolge. **IRichChunk** ist eine Hilfsprogrammschnittstelle, die Informationen über eine Spanne (in der Regel eine Tokenspanne) darstellt, die durch eine Anfangsposition und Länge identifiziert wird. Diese Spanneninformationen umfassen eine Zeichenfolge und/oder eine **VARIANT -Datei.**

### <a name="iconditiongenerator"></a>IConditionGenerator

Die [**IConditionGenerator-Schnittstelle**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) wird von der Anwendung bereitgestellt, um die Erkennung und Bedingungsstrukturgenerierung für einen benannten Entitätstyp zu verarbeiten. Ein Bedingungsgenerator wird einem [**IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) über [**IQueryParser::SetMultiOption**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-setmultioption)übergeben. [**IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) ruft [**IConditionGenerator::Initialize**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-initialize) mit einem [**ISchemaProvider**](/windows/desktop/api/Structuredquery/nn-structuredquery-ischemaprovider) für das derzeit geladene Schema auf. Dadurch kann [**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) alle erforderlichen Schemainformationen abrufen. Beim Analyse einer Eingabezeichenfolge ruft **IQueryParser** die [**IConditionGenerator::RecognizeNamedEntities-Methode**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-recognizenamedentities) jedes [**IConditionGenerators**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator)auf, damit das Vorkommen benannter Entitäten, die es in der Eingabezeichenfolge erkennt, gemeldet werden kann. **IQueryParser** kann das aktuelle Locale verwenden und sollte die Tokenisierung der Eingabe nutzen, da er die Tokenspanne aller benannten Entitäten melden muss.

Wenn [**IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) einen Blattknoten aus geben möchte und der semantische Typ des Werts mit dem benannten Entitätstyp für einen [**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator)abschneidet, ruft **IQueryParser** [**IConditionGenerator::GenerateforLeaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-generateforleaf) mit den Informationen für den zu generierenden Knoten auf. Wenn [**der IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) S OK zurückgibt, sollte er eine Bedingungsstruktur zurückgeben (die kein Blattknoten sein muss) und \_ **IQueryParser** darüber informieren, ob die alternative Zeichenfolgeninterpretation unterdrückt werden soll, die normalerweise als Vorsichtsmaßnahme generiert wird.

### <a name="itokencollection"></a>ITokenCollection

Die [**ITokenCollection::NumberOfTokens-Methode**](/windows/desktop/api/Structuredquery/nf-structuredquery-itokencollection-numberoftokens) gibt die Anzahl der Token zurück. [**ITokenCollection::GetToken gibt**](/windows/desktop/api/Structuredquery/nf-structuredquery-itokencollection-gettoken) Informationen zum *ith-Token* zurück. Der Anfang und die Länge sind Zeichenpositionen in der Eingabezeichenfolge. Der zurückgegebene Text ist nur dann nicht NULL, wenn ein Text die Zeichen aus der Eingabezeichenfolge überschreiben muss. Dies wird beispielsweise verwendet, um einen Bindestrich in der Eingabezeichenfolge mit NOT zu überschreiben, wenn sich dieser Bindestrich in einem Kontext befindet, in dem er als Negation interpretiert werden soll.

### <a name="inamedentitycollector"></a>INamedEntityCollector

[**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) ruft [**INamedEntityCollector::Add für**](/windows/desktop/api/Structuredquery/nf-structuredquery-inamedentitycollector-add) jede erkannte benannte Entität auf. Die Spannen sind Tokenspanne. Es muss immer der Fall sein, dass *beginSpan* ? *beginActual*  <  *endActual* ? *endSpan*. *beginSpan* und *endSpan* können sich von *beginActual* und *endActual* unterscheiden, wenn die benannte Entität mit semantisch nicht signifikanten Token wie Anführungszeichen beginnt und/oder endet (die dennoch von der benannten Entität abgedeckt werden). Der Wert muss als Zeichenfolge ausgedrückt werden und wird anschließend in einem Aufruf von [**IConditionGenerator::GenerateForLeaf angezeigt.**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-generateforleaf)

### <a name="ischemaprovider"></a>ISchemaProvider

Die [**ISchemaProvider-Schnittstelle**](/windows/desktop/api/Structuredquery/nn-structuredquery-ischemaprovider) kann verwendet werden, um ein geladenes Schema nach Entitäten (Typen) und Beziehungen (Eigenschaften) zu durchsuchen. Dies sind die einzelnen Methoden:

-   [**Entitäten**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-entities) geben eine Enumeration jeder Entität ([**IEntity**](/windows/desktop/api/Structuredquery/nn-structuredquery-ientity)) im Schema zurück.
-   [**RootEntity gibt**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-rootentity) die Stammentität des Schemas zurück. Bei einem flachen Schema wird der Haupttyp jeder [**IQuerySolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution) zurückgegeben.
-   [**GetEntity sucht**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-getentity) nach einer Entität nach Namen und gibt S FALSE zurück, wenn im Schema keine entität \_ dieser Entität vorkommt.
-   [**MetaData gibt**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-metadata) eine Enumeration von [**IMetaData-Schnittstellen**](/windows/desktop/api/Structuredquery/nn-structuredquery-imetadata) zurück.

### <a name="ientity"></a>IEntity

Die [**IEntity-Schnittstelle**](/windows/desktop/api/Structuredquery/nn-structuredquery-ientity) ist eine Schemaentität, die einen Typ darstellt, der einen Namen hat, über eine Reihe benannter Beziehungen zu anderen Typen (Eigenschaften) verfügt und von einer Basisentität abstammt. Die einzelnen Methoden führen dies aus:

-   [**IEntity::Relationships gibt**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-relationships) eine Enumeration von [**IRelationship-Objekten**](/windows/desktop/api/Structuredquery/nn-structuredquery-irelationship) zurück, eine für jede ausgehende Beziehung dieses Typs. Jede ausgehende Beziehung einer Entität hat einen Namen.
-   [**IEntity::GetRelationship**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-getrelationship) sucht eine Beziehung anhand des Namens und gibt S FALSE zurück, wenn für diese Entität keine \_ solche Beziehung besteht.
-   [**IEntity::MetaData**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-metadata) gibt eine Enumeration von [**IMetaData-Schnittstellen**](/windows/desktop/api/Structuredquery/nn-structuredquery-imetadata) zurück, eine für jedes Metadatenpaar dieser Entität.
-   [**IEntity::D efaultPhrase**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-defaultphrase) gibt einen Standardbegriff zurück, um das Generieren einer AQS- oder NQS-Neukonfiguration einer Bedingungsstruktur zu erleichtern.

### <a name="irelationship"></a>IRelationship

Die [**IRelationship-Schnittstelle**](/windows/desktop/api/Structuredquery/nn-structuredquery-irelationship) stellt eine Beziehung zwischen zwei Entitäten dar: einer Quelle und einem Ziel. Einzelne Methoden haben folgende Möglichkeiten:

-   [**IRelationship::IsReal**](/windows/desktop/api/Structuredquery/nf-structuredquery-irelationship-isreal) meldet, ob eine Beziehung real ist. Wenn Entität A beispielsweise von Entität B abgeleitet ist und eine Beziehung mit dem Namen R erbt, verfügt A möglicherweise noch über eine eigene Beziehung mit dem Namen R. Die Beziehung zwischen A und R muss jedoch den gleichen Zieltyp wie B aufweisen, und der einzige Grund dafür ist das Speichern von Metadaten, die für B spezifisch sind. Eine solche Beziehung von B wird als nicht real bezeichnet.
-   [**IRelationship::Medadata**](/windows/desktop/api/Structuredquery/nf-structuredquery-irelationship-metadata) gibt eine Enumeration von [**IMetaData-Schnittstellen**](/windows/desktop/api/Structuredquery/nn-structuredquery-imetadata) zurück, eine für jedes Metadatenpaar dieser Entität.
-   [**IRelationship::D efaultPhrase**](/windows/desktop/api/Structuredquery/nf-structuredquery-irelationship-defaultphrase) gibt den Standardbegriff zurück, der für diese Beziehung in Neueinstellungen verwendet werden soll. Jede Beziehung verfügt über einen Standardphrasen, der sie bezeichnet, um das Generieren einer AQS- oder NQS-Neudarstellung einer Bedingungsstruktur zu vereinfachen.

### <a name="imetadata"></a>IMetaData

Metadaten sind Schlüssel-Wert-Paare, die jeweils einer Entität, einer Beziehung oder dem gesamten Schema zugeordnet sind. Da Schlüssel nicht unbedingt eindeutig sind, kann eine Sammlung von Metadaten als Mehrfachzuordnung bezeichnet werden. [**IMetaData::GetData**](/windows/desktop/api/Structuredquery/nf-structuredquery-imetadata-getdata) wird aufgerufen, um den Schlüssel und wert für ein Metadatenpaar abzurufen.

## <a name="querying-scenarios"></a>Abfragen von Szenarien

In den folgenden Szenarien wird die Verwendung strukturierter Abfrage-APIs in Windows Search in gängigen Abfrageszenarien beschrieben, z. B. beim Erstellen einer Bedingungsstruktur und beim Abfragen des Indexes.

### <a name="condition-extraction-and-query-parsing"></a>Bedingungsextraktion und Abfrageparsing

Wenn eine Abfrage erstellt wird, wird ihr Bereich definiert, indem dem System mitgeteilt wird, wo gesucht werden soll. Dies schränkt die Suchergebnisse ein. Nachdem der Bereich definiert wurde, wird ein Filter angewendet, und ein Filtersatz wird zurückgegeben. Suchergebnisse werden durch erstellen einer Bedingungsstruktur mit Blattknoten eingeschränkt, ähnlich wie ein Diagramm. Diese Bedingungen werden dann extrahiert. Eine Bedingungsstruktur ist eine boolesche Kombination (AND, OR, NOT) von Blattbedingungen, von denen jede eine Eigenschaft über einen Vorgang mit einem Wert verbindet. Ein Blattknoten stellt eine Einschränkung für eine einzelne Eigenschaft auf einen Wert durch einige Vorgänge dar.

Eine Filtereinschränkung erfordert einen logischen Ausdruck, der die Einschränkung beschreibt. Das Definieren dieses Ausdrucks beginnt mit der [**ICondition-Schnittstelle,**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) die zum Erstellen eines einzelnen Knotens in einer Bedingungsstruktur verwendet wird. Da es im folgenden Beispiel nur eine Bedingung gibt, ändert sich die Struktur nicht.


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



Wenn es mehrere Filterbedingung gibt, werden AND und andere boolesche Operatoren verwendet, um eine einzelne Struktur zu erreichen. AND-Strukturen und OR-Strukturen stellen Konjunktionen und Disjunktionen ihrer Teilstrukturen dar. Eine NOT-Struktur stellt die Negation ihrer einzelnen Teilstruktur dar. AQS bietet einen Textansatz zum Erreichen logischer Ausdrücke mit booleschen Operatoren und ist häufig einfacher.

Im nächsten Beispiel konvertieren wir die Bedingungsstruktur ([**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition)) in visuelle Form. Der Abfrageparser konvertiert mithilfe der [**IQueryParser-Schnittstelle**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) [**die ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) in eine RTF-Abfragezeichenfolge (Rich Text Formatted). Die [**IQueryParser::RestateToString-Methode**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-restatetostring) gibt den Abfragetext zurück, während die [**IQueryParser::P arse-Methode**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-parse) eine [**IQuerySolution-Schnittstelle**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution) erzeugt. Das folgende Beispiel zeigt, wie Sie all dies tun.


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



Die Haupteingabe von [**IQueryParser::P arse**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-parse) ist eine zu analysierende Benutzereingabezeichenfolge, aber die Anwendung kann den Abfrageparser auch über alle Eigenschaften informieren, die er in der Eingabe erkannt hat (aus anwendungsspezifischer Syntax). Die Ausgabe von **IQueryParser::P arse** ist eine [**IQuerySolution,**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution)die alle Informationen zu diesem Analyseaufruf enthält. Es gibt Methoden zum Abrufen der Eingabezeichenfolge, zum Tokenisieren der Eingabezeichenfolge, zu Analysefehlern und zur analysierten Abfrage als Bedingungsstruktur, die durch [**eine ICondition dargestellt wird.**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) Das folgende Beispiel zeigt ...


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



Im vorherigen Beispiel konnte [**IQuerySolution::GetQuery**](/windows/desktop/api/Structuredquery/nf-structuredquery-iquerysolution-getquery) alle Informationen zur Abfrage abrufen, einschließlich des ursprünglichen Texts, token, die den Text bilden, oder der Bedingungsstruktur. Beispiele für mögliche zurückgegebene Abfragewerte sind in der folgenden Tabelle aufgeführt.



| Beispiele für zurückgegebene Abfragewerte                        | BESCHREIBUNG                                                                                               |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| `  author:relja OR author:tyler`                         | Der Abfragetext, den [**IQueryParser::RestateToString**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-restatetostring) zurückgibt |
| `?author?, ?:?, ?relja?, ?OR?, ?author?, ?:?, ?tyler?`   | Auflisten von Token                                                                                  |
| ![Eine nicht aufgelöste Bedingungsstruktur](images/queryvalues1.png) | Eine nicht aufgelöste Bedingungsstruktur                                                                              |



 

Die zurückgegebene Anfangsbedingungsstruktur ist nicht aufgelöst. In einer nicht aufgelösten Bedingungsstruktur werden Datums- und Uhrzeitverweise wie `date:yesterday` nicht in absolute Zeit konvertiert. Außerdem werden virtuelle Eigenschaften nicht erweitert. Virtuelle Eigenschaften sind Eigenschaften, die als Aggregate mehrerer Eigenschaften fungieren.

Die Abfrage erzeugt beispielsweise `kind:email from:reljai` die folgenden nicht aufgelösten und aufgelösten Bedingungsstrukturen. Die nicht aufgelöste Bedingungsstruktur befindet sich links, und die aufgelöste Bedingungsstruktur befindet sich rechts.

![Nicht aufgelöste und aufgelöste Bedingungsstrukturen](images/conditiontree.png)

Die aufgelöste Struktur kann durch Aufrufen von [**IConditionFactory::Resolve**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-resolve)abgerufen werden. Bei der Übergabe von [**SQRO \_ DONT \_ RESOLVE \_ DATETIME**](/windows/desktop/api/Structuredquery/ne-structuredquery-structured_query_resolve_option) bleiben Datum und Uhrzeit jedoch ungelöst. Eine nicht aufgelöste Bedingungsstruktur bietet Vorteile, da eine nicht aufgelöste Bedingungsstruktur Informationen über die Abfrage enthält. Jeder Blattknoten zeigt auf die von [**IQuerySolution::GetLexicalData**](/windows/desktop/api/Structuredquery/nf-structuredquery-iquerysolution-getlexicaldata)zurückgegebenen Token, die der Eigenschaft, dem Operator und dem Wert entsprechen, wenn die [**IRichChunk-Schnittstelle**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk) verwendet wird. Das folgende Beispiel zeigt ...


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



### <a name="querying-the-index"></a>Abfragen des Index

Es gibt mehrere Ansätze zum Abfragen des Indexes. Einige basieren auf SQL, andere auf AQS. Sie können den Index Windows Search auch programmgesteuert abfragen, indem Sie [Schnittstellen abfragen.](./-search-querying-interfaces-entry-page.md) Es gibt drei Schnittstellen, die für das Abfragen des Index spezifisch sind: [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper), [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)und [**IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents). Konzeptionelle Informationen finden Sie unter [Programmgesteuertes Abfragen des Indexes.](-search-3x-wds-qryidx-overview.md)

Sie können eine Komponente oder Hilfsklasse entwickeln, um den Index mithilfe der [**ISearchQueryHelper-Schnittstelle abfragen zu**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) können. Diese Schnittstelle wird als Hilfsklasse für [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) (und [**ISearchCatalogManager2)**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)implementiert und wird durch Aufrufen von [**ISearchCatalogManager::GetQueryHelper erhalten.**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper) Konzeptionelle Informationen finden Sie unter [Querying the Index with ISearchQueryHelper (Abfragen des Index mit ISearchQueryHelper).](-search-3x-wds-qryidx-searchqueryhelper.md)

[**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) ermöglicht Ihnen:

-   Abrufen einer OLE DB Verbindungszeichenfolge zum Herstellen einer Verbindung mit der Windows Search Datenbank.
-   Konvertieren Sie AQS-Benutzerabfragen in Windows Search SQL.
-   Geben Sie Abfrageeinschränkungen an, die in SQL, aber nicht in AQS ausgedrückt werden können.

Indizierungspriorisierungs- und Rowsetereignisse werden in Windows 7 und höher unterstützt. Mit [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) gibt es einen Prioritätsstapel, mit dem der Client anfordern kann, dass die in einer bestimmten Abfrage verwendeten Bereiche eine höhere Priorität als die normale Priorität erhalten. [**IRowsetEvents bietet**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents) Benachrichtigungen über Änderungen an Elementen in Rowsets, einschließlich des Hinzufügens neuer Elemente, des Löschens von Elementen und der Änderung von Elementdaten. Durch die Verwendung von Rowsetereignisbenachrichtigungen wird sichergestellt, dass die Ergebnisse für vorhandene Abfragen so aktuell wie möglich sind. Konzeptionelle Informationen finden Sie unter [Indizierungspriorisierung und Rowsetereignisse in Windows 7.](indexing-prioritization-and-rowset-events.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Indizierung, Abfrage und Benachrichtigungen in Windows Search](-search-3x-wds-included-in-index.md)
</dt> <dt>

[Was ist im Index enthalten?](-search-indexing-process-overview.md)
</dt> <dt>

[Indizierungsprozess in Windows Search](-search-indexing-process-overview.md)
</dt> <dt>

[Benachrichtigungsprozess in Windows Search](-search-3x-wds-support.md)
</dt> <dt>

[Anforderungen an die URL-Formatierung](url-formatting-requirements.md)
</dt> </dl>

 

 
