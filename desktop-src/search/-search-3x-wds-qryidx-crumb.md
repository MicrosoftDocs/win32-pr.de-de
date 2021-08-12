---
description: Erfahren Sie, wie Sie das CRUMB-Argument in Windows Search als Mittel zum Steuern des Bereichs einer Suche verwenden.
ms.assetid: b0b974ae-0573-45e4-888e-07138604b62e
title: CRUMB-Argument (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ec64fdcf9b15e0b7c87ea2ff0b122e22a8f8917bbacb9d9c3c3da274123f607
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118463242"
---
# <a name="crumb-argument-windows-search"></a>CRUMB-Argument (Windows Search)

Das `crumb` -Argument unterstützt vollständige AQS-Anweisungen (Advanced Query Syntax) und ist besonders nützlich, um den Bereich einer Suche zu steuern. Zusätzlich zu AQS-ements kann das -Argument einen speziellen Parameter für Windows Vista und die Parameter unter XP verwenden, wie weiter unten `crumb` `location` in diesem Thema `kind` `store` beschrieben.

Dieses Thema ist wie folgt organisiert:

-   [Crumb-Syntax](#crumb-syntax)
    -   [Allgemeine Beispiele](#general-examples)
-   [Verwenden von Crumb mit Vista (Standort)](#using-crumb-with-vista-location)
    -   [Vista-Beispiele](#vista-examples)
    -   [Konstanten für allgemeine Ordner](#constants-for-common-folders)
-   [Verwenden von crumb mit Windows XP (Art und Speicher)](#using-crumb-with-windows-xp-kind-and-store)
    -   [XP-Beispiele](#xp-examples)
-   [Zugehörige Themen](#related-topics)

 

## <a name="crumb-syntax"></a>Crumb-Syntax

Die Crumb-Syntax lautet wie folgt:


```
crumb=<column>:<value>[,<label>][,<column>:<value>[,<label>]]& 
```



Der <column> -Teil ist eine beliebige Eigenschaft im Eigenschaftensystem, und <value> portion ist ein gültiger Wert für diese Eigenschaft. Der <label> -Teil ist ein optionaler Alias für die Eigenschaft, die als Benutzeroberflächenhinweis angezeigt wird.

### <a name="general-examples"></a>Allgemeine Beispiele


```
crumb=System.Author:paolo&
crumb=store:mapi&
crumb=location:c%3a%5cMyVacationPix,Vacation&
```



 

## <a name="using-crumb-with-vista-location"></a>Verwenden von Crumb mit Vista (Standort)

Im crumb-Parameter unterstützt Windows Vista die vollständige AQS und auch die -Eigenschaft, die eine spezielle Implementierung enthält, die nur auf Windows `location` Vista verfügbar ist. Sie können entweder eine AQS-Zeichenfolge oder die -Eigenschaft innerhalb eines `location` einzelnen crumb-Parameters verwenden, aber nicht beide. Wenn der crumb-Parameter AQS enthält, wird alles andere in diesem crumb-Parameter ignoriert.

Mit `location` der -Eigenschaft können Sie einen Zu suchpfad angeben. Windows Vista kann den Indexer umgehen und das Verzeichnis direkt durchlaufen, wenn sich der Speicherort außerhalb des Indexer-Durchforstungsbereichs befindet. Folglich sind diese Suchvorgänge möglicherweise langsamer als Suchvorgänge, die den Indexer verwenden.

Wenn Sie eine Eigenschaft `location` angeben, werden zwei zusätzliche Parameter unterstützt und optional:



| Parameter | Werte                  | Beschreibung                                                                                                                                                                       |
|-----------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aufnahme | include, exclude        | Gibt an, ob die Abfrage Elemente in diesen Pfad ein- oder ausschließen soll. "Include" ist die Standardeinstellung. Windows Vista unterstützt keine Ausschlüsse ohne Einschlüsse. (Siehe Beispiel) |
| Rekursion | rekursiv, nicht rekursiv | Gibt an, ob bei der Suche alle Unterordner beginnend mit dem am Speicherort definierten Wert wiederholt werden sollen:<value>. "Rekursiv" ist die Standardeinstellung.                             |



 

Um einen Suchbereich mithilfe des Protokolls search-ms: zu erreichen, haben Sie je nach Ziel des Bereichs unterschiedliche Optionen.

Ordner auf einem lokalen Computer:

-   Verwenden Sie AQS (crumb=folder:<URL-codierten Pfad>)
-   Verwenden Sie das location-Argument (crumb=location:<URL-codierten Pfad>)

Ordner auf einem Remotecomputer/-netzwerk:

-   Verwenden Sie das location-Argument (crumb=location:<URL-codierten Pfad>)

Ordner, auf den über einen bekannten UNC-Protokollhandler zugegriffen wird:

-   Verwenden Sie AQS (crumb=store: <UNC protocol handler name> ).
-   Verwenden Sie das location-Argument (crumb=location:<URL-codierten Pfad>)

### <a name="vista-examples"></a>Vista-Beispiele


```
search-ms:query=vacation&crumb=location:shell%3aPersonal,include,recursive&

search-ms:crumb=location:c%3a%5cPictures&crumb=location:c%3a%5cPictures%5cDuplicates,,exclude& 

search-ms:crumb=location:c%3a%5cDocuments&crumb=kind:pics&
```



Im ersten Beispiel wird eine Suche nach "Vacation" ausgeführt, die am Shell://Personal-Speicherort beginnt (eine spezielle Verknüpfung zum Eigene Dokumente-Ordner des Benutzers), einschließlich dieses Ordners und aller Unterordner. Siehe dazu die folgende Tabelle.

Im zweiten Beispiel wird eine Suche in C: \\ Bilder ausgeführt, jedoch nicht in C: \\ \\ Bildduplizieren.

Im dritten Beispiel wird eine Suche in C: Dokumente ausgeführt, die auf Dateien beschränkt ist, deren \\ kind-Eigenschaft auf Pics festgelegt ist.

### <a name="constants-for-common-folders"></a>Konstanten für allgemeine Ordner

Windows Vista ermöglicht die Verwendung von [KNOWNFOLDERID-Werten,](/previous-versions//bb762584(v=vs.85)) die eine eindeutige systemunabhängige Möglichkeit bieten, spezielle Ordner zu identifizieren, die häufig von Anwendungen verwendet werden, aber möglicherweise nicht denselben Namen oder Speicherort auf einem bestimmten System haben. Der Systemordner kann beispielsweise "C: Windows" auf einem System und \\ "C: \\ Winnt" auf einem anderen System sein. Vor der Windows Vista wurden [CSIDLs](/windows/desktop/shell/csidl) verwendet.

Verwenden Sie diese Speicherorte mit dieser Syntax:


```
crumb=location:shell%3a<LocationName>&
```



 

## <a name="using-crumb-with-windows-xp-kind-and-store"></a>Verwenden von crumb mit Windows XP (Art und Speicher)

Für Windows Search on Windows XP (WDS 3.x) verfügen die AQS-Begriffe "kind" und "store" über eine spezielle Implementierung. Die "kind"-Werte sind dieselben [Werte, die in WDS 2.x verwendet werden.](../lwef/-search-2x-wds-perceivedtype.md) Die Werte für "store" umfassen Folgendes:

-   Mapi
-   file
-   outlookexpress
-   any

### <a name="xp-examples"></a>XP-Beispiele


```
search-ms:query=from:john&crumb=store:outlookexpress,OE%20Mail&
search-ms:query=from:john&crumb=kind:communications&
```



Im ersten Beispiel wird Microsoft Outlook Express-E-Mails von John mit der benutzerdefinierten Bezeichnung "OE Mail" zurückgegeben. Im zweiten Beispiel wird eine Suche nach einer beliebigen Kommunikation von John ausgeführt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte mit Parameter-Value Argumenten](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[Locale Identifier Arguments](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[SYNTAX-Argument](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[STACKEDBY-Argument](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[SUBQUERY-Argument](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 
