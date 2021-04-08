---
description: Der CAB-Datentyp muss in der CAB-Spalte der Medien Tabelle verwendet werden.
ms.assetid: 149c74ea-4342-45dd-8da4-4dfa7f4317a0
title: KEs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4814473ef4d21d5445b5b5319278a5e25a7f5540
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864423"
---
# <a name="cabinet"></a>KEs

Der CAB-Datentyp muss in der CAB-Spalte der [Medien Tabelle](media-table.md)verwendet werden.

Wenn dem CAB-Namen das Nummern Zeichen vorangestellt ist, wird die CAB-Datei als Datenstream innerhalb des Pakets gespeichert. Die Zeichenfolge, die auf folgt, \# ist ein [Bezeichner](identifier.md) für diesen Datenstrom. Beachten Sie Folgendes: Wenn die CAB-Datei als Datenstream gespeichert wird, wird bei einem CAB-Namen die Groß-/Kleinschreibung beachtet.

Wenn dem CAB-Namen nicht das Nummern Zeichen vorangestellt ist \# , wird die CAB-Datei in einer separaten Datei gespeichert, die sich im Stammverzeichnis der Quell Struktur befindet, die von der [Verzeichnis Tabelle](directory-table.md)angegeben wird. Die CAB-Datei muss die kurze Dateiname-Syntax verwenden, die aus einem acht Zeichennamen, einem Zeitraum und einer Erweiterung mit drei Zeichen besteht. Der CAB-Datentyp kann die kurze \| CPS-Syntax für Dateinamen nicht verwenden. Wenn die CAB-Datei als separate Datei gespeichert wird, wird bei dem Namen der CAB-Datei die Groß-/Kleinschreibung nicht beachtet.

Um Speicherplatz zu sparen, entfernt das Installationsprogramm alle in der MSI-Datei eingebetteten Schränke, bevor das Installationspaket auf dem Computer des Benutzers zwischengespeichert wird.

Weitere Informationen finden Sie [unter Einschließen einer CAB-Datei in eine Installation](including-a-cabinet-file-in-an-installation.md).

 

 



