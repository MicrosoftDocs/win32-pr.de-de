---
title: Informationen zu Ressourcendateien
description: Beschreibt, wie Ressourcen in Ihre Windows-basierte Anwendung mit RC einfingen.
ms.assetid: af7c7aed-5d28-40ac-ad00-da0986fd89c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24f351592c57cb628204ad6528a48bfa1a10507f5e7aad90a524ea2f6034f304
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034468"
---
# <a name="about-resource-files"></a>Informationen zu Ressourcendateien

Gehen Sie wie folgt vor, um ressourcen in Windows-basierte Anwendung mit RC ein beispielen:

1.  Erstellen Sie einzelne Dateien für Ihre Cursor, Symbole, Bitmaps, Dialogfelder und Schriftarten.
2.  Erstellen Sie ein Ressourcendefinitionsskript (RC-Datei), das die von Ihrer Anwendung verwendeten Ressourcen beschreibt.
3.  Kompilieren Sie das Skript mit RC. Weitere Informationen finden Sie unter [Verwenden von RC (RC-Befehlszeile).](using-rc-the-rc-command-line-.md)
4.  Verknüpfen Sie die kompilierte Ressourcendatei (RES) mit Ihrem Linker in die ausführbare Datei der Anwendung.

Eine Ressourcendatei ist eine Textdatei mit der Erweiterung .rc. Die Datei kann Einzel-Byte-, Doppel-Byte- oder Unicode-Zeichen verwenden. Die Syntax und Semantik für den RC-Präprozessor ähneln denen des Microsoft C/C++-Compilers. RC unterstützt jedoch eine Teilmenge der Präprozessordirektiven, -definitionen und -Pragmas in einem Skript.

Die Skriptdatei definiert Ressourcen. Für eine Ressource, die in einer separaten Datei vorhanden ist, z. B. ein Symbol oder ein Cursor, gibt das Skript die Ressource und die Datei an, in der sie enthalten ist. Für einige Ressourcen, z. B. ein Menü, ist die gesamte Definition der Ressource im Skript vorhanden.

In den folgenden Themen werden die Informationen beschrieben, die eine Skriptdatei enthalten kann:

-   [Kommentare](comments.md), bei denen es sich um Notizen handelt, die von RC ignoriert werden sollen.
-   [Vordefinierte Makros, die](predefined-macros.md)keine Argumente verwenden und nicht neu definiert werden können.
-   [Präprozessordirektiven](preprocessor-directives.md), die RC anweisen, Aktionen für das Skript auszuführen, bevor es kompiliert wird.
-   [Präprozessoroperatoren,](preprocessor-operators.md)die mit der **\# define-Direktive verwendet** werden.
-   [Pragma-Anweisungen](pragma-directives.md)
-   [Resource-Definition-Anweisungen,](resource-definition-statements.md)die Ressourcen benennen und beschreiben.

 

 




