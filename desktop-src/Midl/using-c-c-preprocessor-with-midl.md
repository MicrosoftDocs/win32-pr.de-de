---
title: Verwenden von C/C++-Preprocessor mit MIDL
description: Der MIDL-Compiler verarbeitet keine Quelldateien.
ms.assetid: 0f62d2a4-cfc3-42a7-b3a6-4e5c67c7c849
keywords:
- MIDL-Compiler MIDL , C-Präprozessor
- C-Präprozessor-MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac3952a342b101f0366d2bce8810426e758c4aa5b32fa267e685bc6d658f034
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382794"
---
# <a name="using-cc-preprocessor-with-midl"></a>Verwenden von C/C++-Preprocessor mit MIDL

Der MIDL-Compiler verarbeitet keine Quelldateien. Stattdessen verwendet der MIDL-Compiler einen verfügbaren Präprozessor, um den Eingabestream für die Analyse vorzubereiten. Standardmäßig verwendet MIDL den Präprozessor für den Microsoft C/C++-Compiler aus derselben Gebäudeumgebung wie MIDL. Der Benutzer kann bei Bedarf einen anderen Präprozessor angeben, der von MIDL verwendet werden soll.

MIDL führt separate Präprozessorläufe für IDL- und ACF-Dateien der obersten Ebene und für jede Datei aus, die mit der MIDL-Importdirektive importiert wurde. Dateien, die in der **\# include-Direktive** enthalten sind, werden direkt vom Präprozessor verarbeitet.

In den folgenden Themen werden verschiedene Aspekte von MIDL-Präprozessorinteraktionen beschrieben:

-   [C-Präprozessoranforderungen für MIDL](c-preprocessor-requirements-for-midl.md)
-   [Überprüfen von Präprozessoroptionen](verifying-preprocessor-options.md)
-   [Speichern der Präprozessorausgabe](saving-preprocessor-output.md)
-   [Umgang mit \# Definitionen in IDL-Dateien](dealing-with-defines-in-idl-files-2.md)

 

 




