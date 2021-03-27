---
description: 'Das Search: Application-Protokoll ist eine erweiterbare Konvention zum Aufrufen der Desktop Suchanwendung unter Windows Vista mit Service Pack 1 (SP1) und höheren Versionen.'
title: Verwenden des Such Protokolls
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 91a1ec25-f6ab-4377-8478-20bc51a1d5df
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: a9223a2a30cab85f8e1b0dac0d0df2dc4fe8f80c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995030"
---
# <a name="using-the-search-protocol"></a>Verwenden des Such Protokolls

Das **Search:** [Application-Protokoll](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) ist eine erweiterbare Konvention zum Aufrufen der Desktop Suchanwendung unter Windows Vista mit Service Pack 1 (SP1) und höheren Versionen. Das Protokoll wurde in Windows Vista mit SP1 erstellt (Weitere Informationen finden Sie im Knowledge Base [-Artikelübersicht über Änderungen der Windows Vista-Desktop Suche in Windows Vista Service Pack 1](https://support.microsoft.com/kb/941946)), damit Windows eine Möglichkeit erhält, die standardmäßige Desktop Suchanwendung zu ermitteln und aufzurufen.

Die Protokoll Syntax bietet eine Reihe von Parametern, die für die Durchführung allgemeiner Desktop Suchvorgänge nützlich sind, wie z. b. vom Benutzer eingegebene Suchbegriffe oder den Speicherort der Suche. Wenn Benutzer von einem der beiden verfügbaren Such Einstiegspunkte (dem **Startmenü** oder Windows-Explorer) suchen, wird vom Betriebssystem das Such Protokoll verwendet, um die Standardanwendung für die Desktop Suche zu starten. Dies geschieht, indem die vom Benutzer eingegebenen Suchbegriffe der standardmäßigen Such Protokoll Syntax hinzugefügt und diese Informationen an die Anwendung übergeben werden, die als Standard Suchanwendung registriert ist.

Wenn keine anderen Desktop Suchanwendungen installiert sind, wird in einer in diese Einstiegspunkte eingegebenen Suche der Windows Search-Explorer gestartet. Entwickler von Drittanbietern können Ihre Anwendungen jedoch erstellen, installieren und registrieren, um das Such Protokoll und die Standard Suchanwendung zu verarbeiten. Solche Anwendungen müssen die Syntax des Suchprotokolls unterstützen und sich mit dem [Standardprogramm für Programme](default-programs.md) registrieren, um eine nahtlose Windows-Funktionalität zu gewährleisten.

Wenn Sie eine Anwendung entwickeln, die für eine bestimmte Desktop Suchanwendung verwendet oder erstellt werden soll, sollten Sie sich nicht ausschließlich auf das **Search:** -Protokoll verlassen. Da viele Anwendungen das **Search:** -Protokoll besitzen könnten, gibt es keine Garantie dafür, dass die Zielanwendung für die Desktop Suche Sie zu einem beliebigen Zeitpunkt übernimmt. Stattdessen sollten Sie ein privates Such Protokoll verwenden, das von der Zielanwendung für die Desktop Suche definiert wurde. Dies bedeutet, dass Desktop Suchanwendungen, die als Plattform für Anwendungen von Drittanbietern gedacht sind, sowohl das **Search:** -Protokoll als auch das eigene proprietäre Such Protokoll unterstützen sollten.

> [!Note]  
> Das **Search:** -Protokoll ersetzt nicht das proprietäre [Search-MS:-](../search/-search-3x-wds-qryidx-searchms.md) Protokoll. Anwendungen können weiterhin das **Search-MS:-** Protokoll verwenden, um den Fenster Such-Explorer zu starten oder den Windows Search-Indexer automatisch abzufragen.

 

In diesem Thema werden folgende Themen behandelt:

-   [Syntax](#syntax)
-   [Verwendung des Such Protokolls durch Windows Vista mit SP1](#windows-vista-with-sp1-use-of-the-search-protocol)
-   [Beispiele](#examples)
-   [Registrieren der Anwendung, die das Protokoll verarbeitet](#registering-the-application-that-handles-the-protocol)
    -   [Registrierungseinträge](#registry-entries)
-   [Zugehörige Themen](#related-topics)

## <a name="syntax"></a>Syntax

Das Such Protokoll verwendet die folgende standardmäßige URL-codierte Syntax:


```C++
search:parameter=value[&parameter=value]&
```



Die Syntax beginnt mit der Identifizierung des Protokolls selbst (**Search:**). Die Parameter/Wert-Paare sind Argumente, die an die Such-Engine übergeben werden, wie in der folgenden Tabelle beschrieben, in der alle möglichen Parameter für die Syntax des Suchprotokolls angezeigt werden.



| Parameter                                              | Wert                                                         | BESCHREIBUNG                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Abfrage                                                  | URL-codierter Text                                              | Der vom Benutzer eingegebene Abfragetext.                                                                                                                                                                                                                                                            |
| [InputLocale](search-protocol-localeidentifiers.md)   | Beliebiger gültiger Sprachcode Bezeichner (LCID)                     | Die LCID, die die Eingabe Sprache für die Abfrage identifiziert.                                                                                                                                                                                                                                     |
| [keywordlocale](search-protocol-localeidentifiers.md) | Eine beliebige gültige LCID                                                | Die LCID, die die Sprache der internationalen Version des Indexers identifiziert. Der Standardwert ist 1033 (en-US).                                                                                                                                                                                |
| [Breadcrumb)](search-protocol-crumb.md)                     | AQS-Anweisung                                                 | Dieses Argument schränkt den Bereich ein, der durchsucht wird. In Windows Vista unterstützt das Such Protokoll vollständige AQS und eine spezielle Implementierung für ein `location` Argument. In Windows XP unterstützt das Such Protokoll auch vollständige AQS, mit Ausnahme einer speziellen Implementierung von `kind` und `store` . |
| [Syntax](search-protocol-syntaxargument.md)           | NQS, AQS (Groß-/Kleinschreibung nicht beachtet)                                 | Die Abfrage Syntax, die zum Durchsuchen des Indexes verwendet werden soll: entweder natürliche Abfrage Syntax oder Erweiterte Abfrage Syntax (AQS). AQS ist die Standardeinstellung und wird immer als analysiert und unterstützt angenommen.                                                                                                                        |
| [stackedby](search-protocol-stackedby.md)             | Eine beliebige gültige Eigenschaft aus dem Eigenschaften System.                   | Eine-Eigenschaft, die die Spalte angibt, nach der die Ergebnisse gestapelt werden.                                                                                                                                                                                                                                      |
| [subquery](search-protocol-subquery.md)               | Ein vollständig angegebener Pfad für eine gespeicherte Suchdatei ( \* . Search-MS) | Die Ergebnisse der Unterabfrage werden als Quelle für die Abfrage verwendet. Das heißt, dass die Abfrage Begriffe anhand der Ergebnisse der Unterabfrage gesucht werden.                                                                                                                                               |
| displayname                                            | URL-codierte Zeichenfolge                                            | Der Name der aktuellen Suche.                                                                                                                                                                                                                                                                |



 

## <a name="windows-vista-with-sp1-use-of-the-search-protocol"></a>Verwendung des Such Protokolls durch Windows Vista mit SP1

Windows Vista mit SP1 verfügt über mehrere Einstiegspunkte, von denen das **Such** Protokoll aufgerufen wird. Diese Einstiegspunkte sind unten und die jeweils zugeordnete allgemeine Syntax aufgeführt.



| Such Protokoll-Einstiegspunkt | Standort         | Abfrage aufgerufen                                                         |
|-----------------------------|------------------|----------------------------------------------------------------------|
| **Überall suchen**       | **Startmenü**   | Search: Query =<*Suchbegriff*>                                   |
| **Überall suchen**       | Windows-Explorer | Suche: Abfrage =<*Suchbegriff*>&Crumb = Speicherort: <*Speicherort*> |
| WINDOWS-TASTE+F          | Überall         | Such                                                              |
| STRG+F                      | Windows-Explorer | Suche: Abfrage =<*Suchbegriff*>&Crumb = Speicherort: <*Speicherort*> |
| F3                          | **Startmenü**   | Such                                                              |
| F3                          | Windows-Explorer | Suche: Abfrage =<*Suchbegriff*>&Crumb = Speicherort: <*Speicherort*> |



 

Die Einstiegspunkte des Suchprotokolls von Windows Vista mit SP1 nutzen nicht alle möglichen Parameter im Such Protokoll. Anwendungen, die sich nur mit der Handhabung von Such Protokoll aufrufen von Windows Vista mit SP1 befassen, können die folgende Tabelle als Leitfaden für die Mindestanforderungen verwenden, die für die Implementierung erforderlich sind.



| Parameter                                              | Von Windows verwendet? | Verwendung durch Windows Vista mit SP1 beim Aufrufen der Suche:                                                                                                                                                                                                                     |
|--------------------------------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Abfrage                                                  | Ja              | Der vom Benutzer eingegebene Abfragetext.                                                                                                                                                                                                                                         |
| [Breadcrumb)](search-protocol-crumb.md)                     | Ja              | [Breadcrumb)](search-protocol-crumb.md) verwendet das- `location` Argument, um den Speicherort der Abfrage anzugeben.                                                                                                                                                                       |
| [subquery](search-protocol-subquery.md)               | Ja              | Die Ergebnisse des [Unterabfrage](search-protocol-subquery.md) Arguments werden als Bereich der zu durchsuchenden Elemente verwendet. Dies wird normalerweise verwendet, wenn ein Benutzer eine. Search-MS-Datei verwendet hat, um die standardmäßige Desktop Suchanwendung in dieser Suche zu suchen und anschließend aufzurufen. |
| [InputLocale](search-protocol-localeidentifiers.md)   | Nein               | Derzeit nicht verwendet.                                                                                                                                                                                                                                                         |
| [keywordlocale](search-protocol-localeidentifiers.md) | Nein               | Derzeit nicht verwendet.                                                                                                                                                                                                                                                         |
| [Syntax](search-protocol-syntaxargument.md)           | Nein               | Derzeit nicht verwendet.                                                                                                                                                                                                                                                         |
| [stackedby](search-protocol-stackedby.md)             | Nein               | Derzeit nicht verwendet.                                                                                                                                                                                                                                                         |
| displayname                                            | Nein               | Derzeit nicht verwendet.                                                                                                                                                                                                                                                         |



 

## <a name="examples"></a>Beispiele

Wenn ein Benutzer im **Startmenü** "Microsoft" eingibt und auf " **überall suchen**" klickt, wird der resultierende Such Protokoll Befehl durchgeführt:


```C++
search:query=microsoft&
```



Wenn ein Benutzer "Seattle" in Windows-Explorer innerhalb von "C: MyFolder" eingibt \\ und dann auf " **überall suchen**" klickt, wird der folgende Befehl durchgeführt, wobei Escapezeichen für ":" und "" verwendet werden \\ :


```C++
search:query=seattle&crumb=location:C%3A%5CMyFolder
```



## <a name="registering-the-application-that-handles-the-protocol"></a>Registrieren der Anwendung, die das Protokoll verarbeitet

Da sich mehrere Anwendungen mit dem Such Protokoll auseinandersetzen können, sollten Sie Ihre Anwendung bei der Installation mit der [Standardprogramm](default-programs.md) Funktion registrieren, damit der Benutzer den Standardwert leichter konfigurieren kann. Zusätzlich zu den Installations Prozeduren, die normalerweise unter Windows XP verwendet werden, muss eine auf Windows Vista basierende Anwendung mit der Standardprogramm Funktion registriert werden, damit die Anwendung und die Benutzer die Standardeinstellungen nahtlos konfigurieren können.

Nachdem Sie die erforderlichen Binärdateien auf dem Computer des Benutzers installiert haben, sollte die Installationsroutine die folgenden allgemeinen Aufgaben erfüllen:

1.  Schreiben Sie ProgIDs auf **\_ den lokalen \_ HKEY-Computer**, wie unten beschrieben. Beachten Sie, dass Anwendungen anwendungsspezifische ProgIDs für das Such Protokoll erstellen müssen.
2.  Die Such Protokoll Zuordnung auf Computer Ebene anfordern.
3.  Registrieren Sie die Anwendung bei [Standardprogrammen](default-programs.md)(wie unter [Registrieren einer Anwendung für die Verwendung mit Standardprogrammen](default-programs.md)erläutert) als Kandidat für das Such Protokoll.

### <a name="registry-entries"></a>Registrierungseinträge

Im folgenden finden Sie Beispiele für die erforderlichen Registrierungseinträge für eine fiktive Anwendung der Desktop Suche.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            URL Protocol = ""
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            DefaultIcon
               (Default) = %ProgramFiles%\Contoso\Search\contososearch.exe,-7
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Contoso\Search\contososearch.exe %1
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      RegisteredApplications
         Contoso Search = "Software\\Contoso\\Search\\Capabilities"
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         Search
            Capabilities
               ApplicationName = "Contoso Search Test App"
               ApplicationDescription = "Contoso search is a great new desktop search application"
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         Search
            Capabilities
               UrlAssociations
                  search = "contoso-search"
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweiterte Abfragesyntax](../search/-search-3x-advancedquerysyntax.md)
</dt> <dt>

[Standardprogramme](default-programs.md)
</dt> </dl>

 

 
