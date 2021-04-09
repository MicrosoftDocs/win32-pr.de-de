---
description: Das Breadcrumb)-Argument unterstützt vollständige Anweisungen der erweiterten Abfrage Syntax (AQS) und ist besonders nützlich, um den Suchbereich zu steuern.
ms.assetid: b0b974ae-0573-45e4-888e-07138604b62e
title: Crumb-Argument (Windows-Suche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51f36764174e0eecaedee4a9c360bb9d7dabca3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128596"
---
# <a name="crumb-argument-windows-search"></a>Crumb-Argument (Windows-Suche)

Das `crumb` -Argument unterstützt vollständige Anweisungen der erweiterten Abfrage Syntax (AQS) und ist besonders nützlich, um den Suchbereich zu steuern. Zusätzlich zu den AQS-Elementen kann das- `crumb` Argument einen speziellen `location` Parameter für Windows Vista und `kind` und `store` Parameter in XP verwenden, wie weiter unten in diesem Thema beschrieben.

Dieses Thema ist wie folgt organisiert:

-   [Crumb-Syntax](#crumb-syntax)
    -   [Allgemeine Beispiele](#general-examples)
-   [Verwenden von Breadcrumb) mit Vista (Speicherort)](#using-crumb-with-vista-location)
    -   [Vista-Beispiele](#vista-examples)
    -   [Konstanten für allgemeine Ordner](#constants-for-common-folders)
-   [Verwenden von Breadcrumb) mit Windows XP (Kind und Store)](#using-crumb-with-windows-xp-kind-and-store)
    -   [XP-Beispiele](#xp-examples)
-   [Zugehörige Themen](#related-topics)

 

## <a name="crumb-syntax"></a>Crumb-Syntax

Die Breadcrumb)-Syntax lautet wie folgt:


```
crumb=<column>:<value>[,<label>][,<column>:<value>[,<label>]]& 
```



Der <column> Teil ist eine beliebige Eigenschaft im Eigenschaften System, und der <value> "Teil" ist ein gültiger Wert für diese Eigenschaft. Der- <label> Teil ist ein optionaler Alias für die Eigenschaft, die als Benutzeroberflächen Hinweis angezeigt wird.

### <a name="general-examples"></a>Allgemeine Beispiele


```
crumb=System.Author:paolo&
crumb=store:mapi&
crumb=location:c%3a%5cMyVacationPix,Vacation&
```



 

## <a name="using-crumb-with-vista-location"></a>Verwenden von Breadcrumb) mit Vista (Speicherort)

Im Breadcrumb)-Parameter unterstützt Windows Vista vollständige AQS und auch die- `location` Eigenschaft, die über eine spezielle Implementierung verfügt, die nur unter Windows Vista verfügbar ist. Sie können entweder eine AQS-Zeichenfolge oder die- `location` Eigenschaft innerhalb eines einzelnen Breadcrumb)-Parameters verwenden, aber nicht beides. Wenn der Breadcrumb)-Parameter AQS enthält, wird alles andere in diesem Breadcrumb)-Parameter ignoriert.

Mit der- `location` Eigenschaft können Sie einen zu suchenden Pfad angeben. Windows Vista kann den Indexer umgehen und das Verzeichnis direkt durchlaufen, wenn der Speicherort außerhalb des Durchforstungs Bereichs des Indexers liegt. Folglich sind diese Suchvorgänge möglicherweise langsamer als Suchvorgänge, die den Indexer verwenden.

Wenn Sie eine `location` Eigenschaft angeben, werden zwei zusätzliche Parameter unterstützt und optional:



| Parameter | Werte                  | BESCHREIBUNG                                                                                                                                                                       |
|-----------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aufnahme | einschließen, ausschließen        | Gibt an, ob die Abfrage Elemente von diesem Pfad einschließen oder ausschließen soll. "Include" ist die Standardeinstellung. Windows Vista unterstützt keine Ausschlüsse ohne Inklusions. (Siehe Beispiel) |
| Rekursion | rekursiv, nicht rekursiv | Gibt an, ob bei der Suche alle Unterordner beginnend mit dem am Speicherort definierten Wert rekursiert werden sollen:<value>. Der Standardwert ist rekursiv.                             |



 

Wenn Sie den Bereich für eine Suche mithilfe des Such-MS:-Protokolls festlegen möchten, haben Sie je nach Ziel des Bereichs unterschiedliche Optionen.

Ordner auf einem lokalen Computer:

-   Verwenden Sie AQS (Crumb = Ordner: <URL-codierter Pfad>).
-   Use Location-Argument (Crumb = Speicherort: <URL-codierter Pfad>)

Ordner auf einem Remote Computer/Netzwerk:

-   Use Location-Argument (Crumb = Speicherort: <URL-codierter Pfad>)

Ordner, auf den über einen bekannten UNC-Protokollhandler zugegriffen wird:

-   Verwenden Sie AQS (Crumb = Store: <UNC protocol handler name> ).
-   Use Location-Argument (Crumb = Speicherort: <URL-codierter Pfad>)

### <a name="vista-examples"></a>Vista-Beispiele


```
search-ms:query=vacation&crumb=location:shell%3aPersonal,include,recursive&

search-ms:crumb=location:c%3a%5cPictures&crumb=location:c%3a%5cPictures%5cDuplicates,,exclude& 

search-ms:crumb=location:c%3a%5cDocuments&crumb=kind:pics&
```



Im ersten Beispiel wird eine Suche nach "Vacation" begonnen, beginnend an der Shell://Personal (eine besondere Verknüpfung zum Ordner "eigene Dateien" des Benutzers), einschließlich dieses Ordners und aller Unterordner. Siehe dazu die folgende Tabelle.

Im zweiten Beispiel wird eine Suche in c:- \\ Bildern ausgeführt, aber nicht in c: \\ Bilder \\ Duplikaten.

Im dritten Beispiel wird eine Suche innerhalb von C: \\ Documents ausgeführt, die auf Dateien beschränkt ist, deren Kind-Eigenschaft auf Bilder festgelegt ist.

### <a name="constants-for-common-folders"></a>Konstanten für allgemeine Ordner

Windows Vista ermöglicht die Verwendung von [KNOWNFOLDERID](/previous-versions//bb762584(v=vs.85)) -Werten, die eine eindeutige, systemunabhängige Möglichkeit zur Identifizierung spezieller Ordner bieten, die häufig von Anwendungen verwendet werden, aber nicht denselben Namen oder Speicherort auf einem beliebigen System haben. Der Systemordner kann z. b. "c: \\ Windows" auf einem System und "c: \\ Winnt" auf einem anderen System sein. Vor Windows Vista wurden [CSIDLs](/windows/desktop/shell/csidl) verwendet.

Verwenden Sie diese Speicherorte mit der folgenden Syntax:


```
crumb=location:shell%3a<LocationName>&
```



 

## <a name="using-crumb-with-windows-xp-kind-and-store"></a>Verwenden von Breadcrumb) mit Windows XP (Kind und Store)

Für Windows Search unter Windows XP (WDS 3. x) verfügen die AQS-Begriffe "Kind" und "Store" über eine besondere Implementierung. Die "Kind"-Werte entsprechen den [Werten, die in WDS 2. x verwendet](../lwef/-search-2x-wds-perceivedtype.md)werden. Die "Store"-Werte umfassen Folgendes:

-   MAPI
-   file
-   OutlookExpress
-   any

### <a name="xp-examples"></a>XP-Beispiele


```
search-ms:query=from:john&crumb=store:outlookexpress,OE%20Mail&
search-ms:query=from:john&crumb=kind:communications&
```



Im ersten Beispiel werden Microsoft Outlook Express-e-Mails von John mit der benutzerdefinierten Bezeichnung "OE Mail" zurückgegeben. Im zweiten Beispiel wird eine Suche nach einer beliebigen Kommunikation von John ausgeführt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Die ersten Schritte mit Parameter-Value Argumenten](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[Locale-bezeichnerargumente](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[Syntax Argument](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[Stackedby-Argument](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[Unterabfrage Argument](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 
