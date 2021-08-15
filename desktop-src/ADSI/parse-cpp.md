---
title: Parse. Cpp
description: In der Beispielanbieterkomponente befindet sich ein Codebeispiel für den Verzeichnisdienstpfadparser in Parse.cpp.
ms.assetid: 5d68065b-0dab-41c9-baf1-f9610656bd6e
ms.tgt_platform: multiple
keywords:
- parse.cpp ADSI
- Pfadparser ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 544ab295318ac80ed19df39a7e5837b566615903a8d8bb963b6fdd5435efde8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023288"
---
# <a name="parsecpp"></a>Parse. Cpp

In der Beispielanbieterkomponente befindet sich ein Codebeispiel für den Verzeichnisdienstpfadparser in Parse.cpp. Der Pfadparser ist eine Schlüsselkomponente in ADs-Anbieterkomponenten. Es überprüft die syntaktische Gültigkeit eines an diesen Anbieter übergebenen ADs-Pfads. Wenn die Syntax gültig ist, wird eine **OBJECTINFO-Struktur** erstellt, die eine komponentenisierte Version des ADspath für dieses Objekt enthält.

Beachten Sie, dass dies nur eine Syntaxüberprüfung ist. Anstatt jede neue Iteration des Pfads in Sonderfällen zu verwenden, muss die gesamte Pfadüberprüfung den vom Parser festgelegten Grammatikregeln entsprechen.

In der folgenden Tabelle sind die in Parse.cpp implementierten Funktionen und Methoden aufgeführt.



| Element                      | BESCHREIBUNG                                                                                                                                                            |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ADsObject**             | Analysiert den an ihn übergebenen ADspath. Diese Funktion folgt den folgenden Grammatikregeln: <ADsObject>  ->  <ProviderName><SampleDSObject><br/>     |
| **SampleDSObject**        | Analysiert die folgenden Grammatikregeln: <SampleDSObject> -> " \\ \\ " " " <identifier> \\ "<Pathname><br/>                                            |
| **ProviderName**          | Fügt den syntaktisch korrekten Anbieternamen hinzu, wenn er nicht vorhanden ist.                                                                                                          |
| **PathName**              | Analysiert die folgenden Grammatikregeln: <Pathname>  ->  <Component> " \\ \\ " <Pathname> OR<br/> <Pathname> -> <Component><br/> |
| **Komponente**             | Analysiert die folgenden Grammatikregeln: <Identifier> OR<br/> <Identifier> "=" <Identifier><br/>                                              |
| **CLexer::CLexer**        | Standardkonstruktor.                                                                                                                                                  |
| **CLexer::~CLexer**       | Standard-Destruktor.                                                                                                                                                   |
| **CLexer::GetNextToken**  | Tokenizer.                                                                                                                                                             |
| **CLexer::NextChar**      | Ruft das nächste einzelne Zeichen ab.                                                                                                                                       |
| **CLexer::P ushBackToken** | Wird bis zum Anfang des letzten Tokens gesichert.                                                                                                                               |
| **CLexer::P ushbackChar**  | Sicherung eines Zeichens.                                                                                                                                                |
| **CLexer::IsKeyword**     | Überprüft die Schlüsselwortliste. Definiert in Globals.h).                                                                                                                          |
| **Addcomponent**          | Fügt diese Komponente dem Komponentenarray hinzu.                                                                                                                            |
| **AddProviderName**       | Fügt der **OBJECTINFO-Struktur** einen syntaktisch korrekten Anbieternamen hinzu.                                                                                            |
| **AddRootRDN**            | Fügt der **OBJECTINFO-Struktur** den syntaktisch korrekten RDN-Namen (Root Relative Distinguished Name) hinzu.                                                            |
| **SetType**               | Legt den Typ des Objekts fest.                                                                                                                                           |
| **Typ**                  | Analysiert Type-> "user" \| "group" usw.                                                                                                                          |



 

 

 





