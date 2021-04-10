---
title: Verwenden von C/C++-Präprozessor mit mittlerer l
description: Der mittlerer l-Compiler führt keine Vorverarbeitung von Quelldateien aus.
ms.assetid: 0f62d2a4-cfc3-42a7-b3a6-4e5c67c7c849
keywords:
- Mittel l-compilermittell, C-Präprozessor
- C-präprozessormittell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5752bd64ee9a9b5fc26d586b5bc33c1a1fb96e83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309823"
---
# <a name="using-cc-preprocessor-with-midl"></a>Verwenden von C/C++-Präprozessor mit mittlerer l

Der mittlerer l-Compiler führt keine Vorverarbeitung von Quelldateien aus. Stattdessen verwendet der mittlerer l-Compiler einen verfügbaren Präprozessor, um den Eingabestream für die Verarbeitung vorzubereiten. In der Standardeinstellung verwendet die Mittel l den Präprozessor für den Microsoft C/C++-Compiler aus derselben Gebäudeumgebung wie die Mitte. Der Benutzer kann bei Bedarf einen anderen Präprozessor angeben, der von der Mittell verwendet werden soll.

In mittlerer l-Datei werden separate präprozessorausführungen für IDL-und ACF-Dateien der obersten Ebene und für jede mit der Anweisung "Mittel l Import" importierte Datei ausgeführt. Dateien, die in der **\# include** -Anweisung enthalten sind, werden vom Präprozessor direkt verarbeitet.

In den folgenden Themen werden verschiedene Aspekte von mittlerer l-präprozessorinteraktionen beschrieben:

-   [C-präprozessoranforderungen für die Mittel l](c-preprocessor-requirements-for-midl.md)
-   [Überprüfen von Präprozessoroptionen](verifying-preprocessor-options.md)
-   [Speichern der Präprozessorausgabe](saving-preprocessor-output.md)
-   [Umgang mit \# Definitionen in IDL-Dateien](dealing-with-defines-in-idl-files-2.md)

 

 




