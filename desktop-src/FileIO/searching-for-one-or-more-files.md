---
description: Eine Anwendung kann das aktuelle Verzeichnis nach allen Dateinamen durchsuchen, die einem bestimmten Muster entsprechen, indem die Funktionen FindFirstFile, findfirstfileex, FindNextFile und FindClose verwendet werden.
ms.assetid: 7edd6c6e-7e8a-415c-866b-2283e5596a62
title: Suchen nach einer oder mehreren Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c5825b418221b1af429c6c0a731446d627701c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357396"
---
# <a name="searching-for-one-or-more-files"></a>Suchen nach einer oder mehreren Dateien

Eine Anwendung kann das aktuelle Verzeichnis nach allen Dateinamen durchsuchen, die einem bestimmten Muster entsprechen, indem die Funktionen [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**findfirstfileex**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)und [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) verwendet werden. Das Muster muss ein gültiger Dateiname sein und darf Platzhalter Zeichen enthalten.

Die Funktionen " [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) " und " [**findfirstfileex**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) " erstellen Handles, die von **findfirstfileex** verwendet werden, um nach anderen Dateien mit demselben Muster zu suchen. Alle Funktionen geben Informationen über die gefundene Datei zurück. Zu diesen Informationen gehören der Dateiname, die Größe, die Attribute und die Uhrzeit.

Die Funktion " [**findfirstfileex**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) " ermöglicht einer Anwendung auch das Suchen nach Dateien basierend auf zusätzlichen Suchkriterien. Mit der-Funktion können Suchvorgänge auf Gerätenamen oder Verzeichnisnamen beschränkt werden.

Die [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) -Funktion zerstört Handles, die von " [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) " und " [**findfirstfileex**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa)" erstellt wurden.

Eine Anwendung kann mithilfe der [**SearchPath**](/windows/win32/api/processenv/nf-processenv-searchpatha) -Funktion nach einer einzelnen Datei in einem bestimmten Pfad suchen.

 

 
