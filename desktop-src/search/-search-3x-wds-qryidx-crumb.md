---
description: Hier erfahren Sie, wie Sie das ARGUMENTS in Windows Search verwenden, um den Bereich einer Suche zu steuern.
ms.assetid: b0b974ae-0573-45e4-888e-07138604b62e
title: ARGUMENTS-Argument (Windows-Suche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2a1ae426881473a631a11b40ec8e567f600daa4
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886825"
---
# <a name="crumb-argument-windows-search"></a>ARGUMENTS-Argument (Windows-Suche)

Das `crumb` -Argument unterstützt vollständige AQS-Anweisungen (Advanced Query Syntax) und ist besonders nützlich, um den Bereich einer Suche zu steuern. Zusätzlich zu AQS-Ements kann das `crumb` Argument einen speziellen Parameter für Windows Vista und parameter für XP `location` `kind` `store` verwenden, wie weiter unten in diesem Thema beschrieben.

Dieses Thema ist wie folgt organisiert:

-   [Syntax der Verrenkung](#crumb-syntax)
    -   [Allgemeine Beispiele](#general-examples)
-   [Verwenden von "vererbte" mit Vista (Standort)](#using-crumb-with-vista-location)
    -   [Vista-Beispiele](#vista-examples)
    -   [Konstanten für allgemeine Ordner](#constants-for-common-folders)
-   [Verwenden von Krümmung mit Windows XP (Art und Speicher)](#using-crumb-with-windows-xp-kind-and-store)
    -   [XP-Beispiele](#xp-examples)
-   [Zugehörige Themen](#related-topics)

 

## <a name="crumb-syntax"></a>Syntax der Verrenkung

Die Syntax für die Unbrütlichung lautet wie folgt:


```
crumb=<column>:<value>[,<label>][,<column>:<value>[,<label>]]& 
```



Der &lt; &gt; Spaltenteil ist eine beliebige Eigenschaft im Eigenschaftensystem, und der &lt; &gt; Wertteil ist ein gültiger Wert für diese Eigenschaft. Der <label> -Teil ist ein optionaler Alias für die Eigenschaft, die als Benutzeroberflächenhinweis angezeigt wird.

### <a name="general-examples"></a>Allgemeine Beispiele


```
crumb=System.Author:paolo&
crumb=store:mapi&
crumb=location:c%3a%5cMyVacationPix,Vacation&
```



 

## <a name="using-crumb-with-vista-location"></a>Verwenden von "vererbte" mit Vista (Standort)

Im -Parameter wird von Windows Vista die vollständige AQS-Eigenschaft sowie die `location` -Eigenschaft unterstützt, die eine spezielle Implementierung nur auf Windows Vista zur Verfügung hat. Sie können entweder eine AQS-Zeichenfolge oder die `location` -Eigenschaft innerhalb eines einzigen Vererbeparameters verwenden, aber nicht beides. Wenn der Parameters zum Überschließen AQS enthält, wird alles andere in diesem Parameter ignoriert.

Mit `location` der -Eigenschaft können Sie einen Pfad für die Suche angeben. Windows Vista kann den Indexer umgehen und das Verzeichnis direkt durchlaufen, wenn sich der Speicherort außerhalb des Durchforstungsbereichs des Indexers befindet. Folglich sind diese Suchvorgänge möglicherweise langsamer als Suchvorgänge, die den Indexer verwenden.

Wenn Sie eine `location` Eigenschaft angeben, werden zwei zusätzliche Parameter unterstützt und optional:



| Parameter | Werte                  | Beschreibung                                                                                                                                                                       |
|-----------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aufnahme | Include, Exclude        | Gibt an, ob die Abfrage Elemente in diesen Pfad einschließen oder davon ausschließen soll. "Include" ist die Standardeinstellung. Windows Vista unterstützt keine Ausschlüsse ohne Einschlüsse. (Siehe Beispiel) |
| Rekursion | rekursiv, nicht rekursiv | Gibt an, ob die Suche alle Unterordner beginnend mit dem am Speicherort definierten Wert rekursiv durchgehen soll: &lt; value &gt; . "Rekursiv" ist die Standardeinstellung.                             |



 

Sie haben je nach Ziel des Bereichs verschiedene Optionen, um eine Suche mithilfe des Protokolls search-ms: zu ermöglichen.

Ordner auf einem lokalen Computer:

-   Verwenden Sie AQS (folder=folder:<URL-codierter Pfad>)
-   Verwenden Sie das Location-Argument (vererb=location:<URL-codierter Pfad>)

Ordner auf einem Remotecomputer/Netzwerk:

-   Verwenden Sie das Location-Argument (vererb=location:<URL-codierter Pfad>)

Ordner, auf den über einen bekannten UNC-Protokollhandler zugegriffen wird:

-   Verwenden Sie AQS (vererb=store: <UNC protocol handler name> ).
-   Verwenden Sie das Location-Argument (vererb=location:<URL-codierter Pfad>)

### <a name="vista-examples"></a>Vista-Beispiele


```
search-ms:query=vacation&crumb=location:shell%3aPersonal,include,recursive&

search-ms:crumb=location:c%3a%5cPictures&crumb=location:c%3a%5cPictures%5cDuplicates,,exclude& 

search-ms:crumb=location:c%3a%5cDocuments&crumb=kind:pics&
```



Im ersten Beispiel wird eine Suche nach "Vacation" am shell://Personal Speicherort (eine spezielle Verknüpfung zum Eigene Dokumente Ordner des Benutzers) ausgeführt, einschließlich dieses Ordners und aller Unterordner. Siehe dazu die folgende Tabelle.

Im zweiten Beispiel wird eine Suche in C: \\ Bilder ausgeführt, jedoch nicht in C: \\ \\ Bildduplikate.

Im dritten Beispiel wird eine Suche in C: \\ Dokumente ausgeführt, die auf Dateien beschränkt ist, deren kind-Eigenschaft auf Pics festgelegt ist.

### <a name="constants-for-common-folders"></a>Konstanten für allgemeine Ordner

Windows Vista ermöglicht die Verwendung von [KNOWNFOLDERID-Werten,](/previous-versions//bb762584(v=vs.85)) die eine eindeutige systemunabhängige Möglichkeit bieten, spezielle Ordner zu identifizieren, die häufig von Anwendungen verwendet werden, aber möglicherweise nicht den gleichen Namen oder Speicherort auf einem bestimmten System aufweisen. Beispielsweise kann der Systemordner auf einem System "C: \\ Windows" und auf einem anderen "C: \\ Winnt" sein. Vor Windows Vista wurden [CSIDLs](/windows/desktop/shell/csidl) verwendet.

Verwenden Sie diese Speicherorte mit dieser Syntax:


```
crumb=location:shell%3a<LocationName>&
```



 

## <a name="using-crumb-with-windows-xp-kind-and-store"></a>Verwenden von Krümmung mit Windows XP (Art und Speicher)

Für Windows Search on Windows XP (WDS 3.x) haben die AQS-Begriffe "kind" und "store" eine spezielle Implementierung. Die "kind"-Werte sind die gleichen Werte, die [in WDS 2.x verwendet werden.](../lwef/-search-2x-wds-perceivedtype.md) Die "store"-Werte umfassen Folgendes:

-   Mapi
-   file
-   outlookexpress
-   any

### <a name="xp-examples"></a>XP-Beispiele


```
search-ms:query=from:john&crumb=store:outlookexpress,OE%20Mail&
search-ms:query=from:john&crumb=kind:communications&
```



Im ersten Beispiel werden Microsoft Outlook Express-E-Mails von John mit der benutzerdefinierten Bezeichnung "OE Mail" zurückgegeben. Im zweiten Beispiel wird eine Suche nach jeglicher Kommunikation von John ausgeführt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte mit Parameter-Value Argumenten](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[Gebietsschemabezeichnerargumente](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[SYNTAX-Argument](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[STACKEDBY-Argument](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[SUBQUERY-Argument](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 
