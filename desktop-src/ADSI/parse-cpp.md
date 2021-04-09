---
title: Analysieren. CPP
description: In der Beispiel Anbieter Komponente befindet sich ein Codebeispiel für den Verzeichnisdienst Pfad-Parser in "Parse. cpp".
ms.assetid: 5d68065b-0dab-41c9-baf1-f9610656bd6e
ms.tgt_platform: multiple
keywords:
- cpp-ADSI analysieren
- Pfad Parser ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ee4df5c1c709fde724385fdf5d5cddbafef338
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947335"
---
# <a name="parsecpp"></a>Analysieren. CPP

In der Beispiel Anbieter Komponente befindet sich ein Codebeispiel für den Verzeichnisdienst Pfad-Parser in "Parse. cpp". Der Pfad Parser ist eine Schlüsselkomponente in der ADS-Anbieter Komponente. Er überprüft die syntaktische Gültigkeit eines ADS, der an diesen Anbieter übermittelt wurde. Wenn die Syntax gültig ist, wird eine **objectinfo** -Struktur erstellt, die eine Komponenten entierte Version des ADsPath für dieses Objekt enthält.

Beachten Sie, dass es sich hierbei nur um eine Syntax Überprüfung handelt. Anstelle von Sonderfällen für jede neue Iterationspfad muss die gesamte Pfad Überprüfung den vom Parser festgelegten Grammatikregeln entsprechen.

In der folgenden Tabelle werden die in "cpp" implementierten Funktionen und Methoden aufgelistet.



| Element                      | BESCHREIBUNG                                                                                                                                                            |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **AdsObject**             | Analysiert den an ihn bestandenen ADsPath. Diese Funktion folgt den folgenden Grammatikregeln: <ADsObject>  ->  <ProviderName><SampleDSObject><br/>     |
| **Sampledsobject**        | Analysiert die folgenden Grammatikregeln: <SampleDSObject> -> " \\ \\ " <identifier> \\ ""<Pathname><br/>                                            |
| **ProviderName**          | Fügt den Namen des syntaktisch korrekten Anbieters hinzu, wenn dies nicht der Fall ist.                                                                                                          |
| **PathName**              | Analysiert die folgenden Grammatikregeln: <Pathname>  ->  <Component> " \\ \\ " <Pathname> oder<br/> <Pathname> -> <Component><br/> |
| **Komponente**             | Analysiert die folgenden Grammatikregeln: <Identifier> oder<br/> <Identifier> "=" <Identifier><br/>                                              |
| **Clexer:: clexer**        | Standardkonstruktor.                                                                                                                                                  |
| **Clexer:: ~ clexer**       | Standardedekonstruktor.                                                                                                                                                   |
| **Clexer:: GetNextToken**  | Tokenizer.                                                                                                                                                             |
| **Clexer:: nextchar**      | Ruft das nächste einzelne Zeichen ab.                                                                                                                                       |
| **Clexer::P ushbacktoken** | Sichert bis zum Anfang des letzten Tokens.                                                                                                                               |
| **Clexer::P ushbackchar**  | Sichert ein Zeichen.                                                                                                                                                |
| **Clexer:: IsKeyword**     | Überprüft die Schlüsselwort Liste. Definiert in Globals. h).                                                                                                                          |
| **AddComponent**          | Fügt diese Komponente zum Komponenten Array hinzu.                                                                                                                            |
| **Addprovidername**       | Fügt der **objectinfo** -Struktur einen syntaktisch korrekten Anbieter Namen hinzu.                                                                                            |
| **Addrootrdn**            | Fügt der **objectinfo** -Struktur den Namen des syntaktisch korrekten Stamm-Distinguished Name (RDN) hinzu.                                                            |
| **Settype**               | Legt den Typ des-Objekts fest.                                                                                                                                           |
| **Type**                  | Analysiert Type-> "User" \| "Group" usw.                                                                                                                          |



 

 

 





