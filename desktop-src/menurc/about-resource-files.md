---
title: Informationen zu Ressourcen Dateien
description: Hier wird beschrieben, wie Sie Ressourcen in die Windows-basierte Anwendung mit RC einbinden.
ms.assetid: af7c7aed-5d28-40ac-ad00-da0986fd89c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c43e9df59cf0b6507b6c6a53c42299b8792634f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036967"
---
# <a name="about-resource-files"></a>Informationen zu Ressourcen Dateien

Gehen Sie folgendermaßen vor, um Ressourcen in die Windows-basierte Anwendung mit RC einzuschließen:

1.  Erstellen Sie einzelne Dateien für Ihre Cursor, Symbole, Bitmaps, Dialogfelder und Schriftarten.
2.  Erstellen Sie ein Ressourcen Definitions Skript (RC-Datei), das die von der Anwendung verwendeten Ressourcen beschreibt.
3.  Kompilieren Sie das Skript mit RC. Weitere Informationen finden Sie unter [Verwenden von RC (RC-Befehlszeile)](using-rc-the-rc-command-line-.md).
4.  Verknüpfen Sie die kompilierte Ressourcen Datei (. res) mit dem Linker in der ausführbaren Datei der Anwendung.

Eine Ressourcen Datei ist eine Textdatei mit der Erweiterung. rc. Die Datei kann Einzel Byte-, Doppelbyte-oder Unicode-Zeichen verwenden. Die Syntax und die Semantik für den RC-Präprozessor ähneln denen des Microsoft C/C++-Compilers. RC unterstützt jedoch eine Teilmenge der Präprozessordirektiven, Definitionen und Pragmas in einem Skript.

Die Skriptdatei definiert Ressourcen. Für eine Ressource, die in einer separaten Datei vorhanden ist, z. b. ein Symbol oder einen Cursor, gibt das Skript die Ressource und die Datei an, in der Sie enthalten ist. Bei einigen Ressourcen, z. b. einem Menü, ist die gesamte Definition der Ressource im Skript vorhanden.

In den folgenden Themen werden die Informationen beschrieben, die eine Skriptdatei enthalten kann:

-   [Kommentare](comments.md), bei denen es sich um Notizen handelt, die von RC ignoriert werden.
-   [Vordefinierte Makros](predefined-macros.md), die keine Argumente annehmen und nicht neu definiert werden können.
-   [Präprozessordirektiven](preprocessor-directives.md), die RC anweisen, vor dem Kompilieren Aktionen für das Skript auszuführen.
-   [Präprozessoroperatoren](preprocessor-operators.md), die mit der **\# define** -Direktive verwendet werden.
-   [Pragma-Anweisungen](pragma-directives.md)
-   [Ressourcen Definitions Anweisungen](resource-definition-statements.md), die Ressourcen benennen und beschreiben.

 

 




