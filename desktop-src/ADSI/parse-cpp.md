---
title: PARSE. CPP
description: In der Beispielanbieterkomponente befindet sich ein Codebeispiel für den Verzeichnisdienstpfadparser in Parse.cpp.
ms.assetid: 5d68065b-0dab-41c9-baf1-f9610656bd6e
ms.tgt_platform: multiple
keywords:
- parse.cpp ADSI
- Pfadparser ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 518db6857f9b7018a0dbf3e1e97ac60ed654447d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880289"
---
# <a name="parsecpp"></a>PARSE. CPP

In der Beispielanbieterkomponente befindet sich ein Codebeispiel für den Verzeichnisdienstpfadparser in Parse.cpp. Der Pfadparser ist eine Schlüsselkomponente in ADs-Anbieterkomponenten. Es überprüft die syntaktische Gültigkeit eines ADs-Pfads, der an diesen Anbieter übergeben wird. Wenn die Syntax gültig ist, wird eine **OBJECTINFO-Struktur** erstellt, die eine komponentenisierte Version des ADspath für dieses Objekt enthält.

Beachten Sie, dass dies nur eine Syntaxüberprüfung ist. Anstatt jede neue Iteration des Pfads in Sonderfall zu verwenden, muss jede Pfadüberprüfung den vom Parser festgelegten Grammatikregeln entsprechen.

In der folgenden Tabelle sind die Funktionen und Methoden aufgeführt, die in Parse.cpp implementiert sind.



| Element                      | Beschreibung                                                                                                                                                            |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ADsObject**             | Analysiert den an ihn übergebenen ADspath. Diese Funktion folgt den folgenden Grammatikregeln: &lt; ADsObject &gt;  ->  &lt; ProviderName &gt; &lt; SampleDSObject&gt;<br/>     |
| **SampleDSObject**        | Analysiert die folgenden Grammatikregeln: &lt; SampleDSObject &gt; -> \\ \\ " " identifier " &lt; " &gt; \\ &lt; Pathname&gt;<br/>                                            |
| **ProviderName**          | Fügt den syntaktisch korrekten Anbieternamen hinzu, falls er nicht dort ist.                                                                                                          |
| **PathName**              | Analysiert die folgenden Grammatikregeln: &lt; Pathname &gt;  ->  &lt; Component " &gt; " \\ \\ &lt; Pathname &gt; OR<br/> &lt;&gt;  ->  &lt; Pathname-Komponente&gt;<br/> |
| **Komponente**             | Analysiert die folgenden Grammatikregeln: &lt; Bezeichner &gt; OR<br/> &lt;Bezeichner &gt; "=" &lt; Bezeichner&gt;<br/>                                              |
| **CLexer::CLexer**        | Standardkonstruktor.                                                                                                                                                  |
| **CLexer::~CLexer**       | Standard-Destruktor.                                                                                                                                                   |
| **CLexer::GetNextToken**  | Tokenizer.                                                                                                                                                             |
| **CLexer::NextChar**      | Ruft das nächste einzelne Zeichen ab.                                                                                                                                       |
| **CLexer::P ushBackToken** | Wird bis zum Anfang des letzten Tokens sichern.                                                                                                                               |
| **CLexer::P ushbackChar**  | Sichern eines Zeichens.                                                                                                                                                |
| **CLexer::IsKeyword**     | Überprüft die Schlüsselwortliste. Definiert in Globals.h).                                                                                                                          |
| **Addcomponent**          | Fügt diese Komponente dem Komponentenarray hinzu.                                                                                                                            |
| **AddProviderName**       | Fügt der **OBJECTINFO-Struktur** einen syntaktisch korrekten Anbieternamen hinzu.                                                                                            |
| **AddRootRDN**            | Fügt der **OBJECTINFO-Struktur** den syntaktisch korrekten RDN-Namen (Root Relative Distinguished Name) hinzu.                                                            |
| **SetType**               | Legt den Typ des -Objekts fest.                                                                                                                                           |
| **Typ**                  | Analysiert typspezifische > "user" \| "group" und so weiter.                                                                                                                          |



 

 

 





