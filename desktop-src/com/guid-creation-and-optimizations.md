---
title: GUID-Erstellung und-Optimierungen
description: GUID-Erstellung und-Optimierungen
ms.assetid: 698322f2-db89-4553-90c6-4278e96716dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc113675bae329d862c0b504851d4732243a84c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388706"
---
# <a name="guid-creation-and-optimizations"></a>GUID-Erstellung und-Optimierungen

Da eine CLSID, wie z. b. ein Schnittstellen Bezeichner (IID), eine GUID ist, hat keine andere Klasse, unabhängig von der Person, die Sie schreibt, eine doppelte CLSID. Server Implementierer erhalten CLSIDs in der Regel über die [**cokreateguid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) -Funktion. Mit dieser Funktion werden garantiert eindeutige CLSIDs erzeugt, sodass Server Implementierungen auf der ganzen Welt Ihre Software unabhängig entwickeln und bereitstellen können, ohne dass eine versehentliche Kollision mit von anderen geschriebenen Software besteht.

Durch die Verwendung eindeutiger CLSIDs wird die Möglichkeit von Namenskollisionen zwischen Klassen vermieden, weil CLSIDs in keiner Weise mit den in der zugrunde liegenden Implementierung verwendeten Namen verbunden sind. Beispielsweise können zwei verschiedene Lieferanten Klassen schreiben, die als "stackclass" bezeichnet werden, aber jede verfügt über eine eindeutige CLSID und kann daher nicht verwechselt werden.

COM muss häufig GUIDs (IIDs und CLSIDs) einem beliebig großen Satz an anderen Werten zuordnen. Als Anwendungsentwickler können Sie diese Suchvorgänge beschleunigen und dadurch die Systemleistung verbessern, indem Sie die GUIDs für Ihre Anwendung als Block von aufeinander folgenden Werten erstellen.

Die effizienteste Möglichkeit, einen Block von aufeinander folgenden GUIDs zu generieren, besteht darin, das Hilfsprogramm "" uuidgen "mithilfe der Schalter"-n "und"-x "auszuführen, die einen Block von UUIDs generieren, wobei jeder der ersten DWORD-Werte um eins erhöht wird.

Wenn Sie z. b. eingeben.

**"uuidgen-N5-x**

Das Hilfsprogramm "uuidgen würde einen Block von UUIDs generieren, der etwa wie folgt aussieht:

``` syntax
12340001-4980-1920-6788-123456789012
12340002-4980-1920-6788-123456789012
12340003-4980-1920-6788-123456789012
12340004-4980-1920-6788-123456789012
12340005-4980-1920-6788-123456789012
 
```

Eine Methode zum Erstellen und Nachverfolgen von GUIDs für ein gesamtes Projekt beginnt mit dem Erstellen eines Blocks einer beliebig großen Anzahl von UUIDs, z.b. 500. Wenn Sie z. b. eingeben.

**"uuidgen-N500-x > guids.txt**

Das Hilfsprogramm generiert 500 aufeinander folgende UUIDs und schreibt Sie in die angegebene Textdatei. Anschließend können Sie diese Datei in der Quell Struktur überprüfen und so ein einzelnes Repository für alle GUIDs bereitstellen, die in einem Projekt verwendet werden sollen. Da Benutzer GUIDs für ihre Teile des Projekts benötigen, können Sie die Datei Auschecken, aber viele GUIDs, die Sie benötigen, markieren, Sie als angenommen markieren und eine Notiz über den Speicherort im Code oder "Spezifikation" hinterlassen.

Zusätzlich zur Verbesserung der Systemleistung hat das Erstellen von Blöcken von aufeinander folgenden GUIDs auf diese Weise folgende Vorteile:

-   Eine zentrale Datei, in der alle GUIDs für eine Anwendung enthalten sind, macht es leicht nachzuverfolgen, welche GUIDs für was und welche Personen verwendet werden.
-   Ein Block von aufeinander folgenden GUIDs, die einer bestimmten Anwendung zugeordnet sind, hilft Entwicklern und Testern beim Debuggen beim Erkennen interner GUIDs und erleichtert die Suche in der Systemregistrierung, da Sie sequenziell gespeichert werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuständigkeiten von com-Servern](com-server-responsibilities.md)
</dt> </dl>

 

 




