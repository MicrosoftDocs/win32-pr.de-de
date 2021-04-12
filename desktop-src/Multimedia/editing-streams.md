---
title: Bearbeiten von Streams
description: Bearbeiten von Streams
ms.assetid: 1653ff90-e96a-43fc-b509-6d8ad4ddcd2c
keywords:
- Funktion "deateeditablestream"
- Editstreamcut-Funktion
- Editstreamcopy-Funktion
- Editstreampaste-Funktion
- Editstreamclone-Funktion
- Editstreamabtinfo-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29eb687eb36ff9dfe0b1d3477bff095bdd78a135
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471461"
---
# <a name="editing-streams"></a>Bearbeiten von Streams

Sie können einen Stream erstellen, den Sie [**mit der Funktion**](/windows/desktop/api/Vfw/nf-vfw-createeditablestream) "-Funktion" in der Funktion "Funktion" bearbeiten können. Diese Funktion initialisiert die Umgebung zum Bearbeiten eines Streams. Dazu gehört das Erstellen einer Schnittstelle für den neuen Stream und interne Bearbeitungs Tabellen, die Änderungen am Stream nachverfolgen. " **Kreateeditablestream** " gibt einen Datenstrom Zeiger auf einen bearbeitbaren Datenstrom zurück, der für andere streambearbeitungs Funktionen erforderlich ist. Der bearbeitbare Streamzeiger kann auch von anderen avifile-Funktionen verwendet werden, die Streamzeiger akzeptieren.

Sie können ein oder mehrere Beispiele aus einem bearbeitbaren Stream mithilfe der [**editstreamcut**](/windows/desktop/api/Vfw/nf-vfw-editstreamcut) -Funktion Ausschneiden. Um Beispiele aus dem bearbeitbaren Stream zu entfernen, fügt diese Funktion einen Eintrag in die Bearbeitungs Tabelle ein. Die Funktion platziert dann eine Kopie der Ausschneide Proben in einem neuen temporären Stream, dessen Schnittstellen Zeiger in einer Variablen zurückgegeben wird.

Sie können ein oder mehrere Beispiele aus einem bearbeitbaren Datenstrom mithilfe der [**editstreamcopy**](/windows/desktop/api/Vfw/nf-vfw-editstreamcopy) -Funktion in einen temporären Stream kopieren. **Editstreamcopy** platziert Kopien der Beispiele in einem neuen temporären Stream, dessen Schnittstellen Zeiger in einer Variablen zurückgegeben wird.

Sie können ein oder mehrere Beispiele aus einem Stream kopieren und in einen bearbeitbaren Stream einfügen, indem Sie die [**editstreampaste**](/windows/desktop/api/Vfw/nf-vfw-editstreampaste) -Funktion verwenden. Um die Beispiele an der angegebenen Position einzufügen, fügt diese Funktion einen Eintrag in der Bearbeitungs Tabelle des bearbeitbaren Ziel Datenstroms hinzu.

Sie können einen bearbeitbaren Stream mithilfe der [**editstreamclone**](/windows/desktop/api/Vfw/nf-vfw-editstreamclone) -Funktion duplizieren. Diese Funktion gibt einen Zeiger auf die streamschnittstelle des neuen Streams zurück. Sie können diese Datenströme in die Zwischenablage kopieren oder Sie verwenden, um einen Pfad der an einen Stream vorgenommenen Änderungen beizubehalten.

Sie können mehrere der Merkmale eines bearbeitbaren Streams mithilfe der [**editstreamtstinfo**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetinfoa) -Funktion ändern. Diese Funktion aktualisiert die Prioritäts Einstellung, die Sprache, die Skala und die Rate, die Startzeit, die Qualitätseinstellung, die Abmessungen und Koordinaten des Ziel Rechtecks und die Textbeschreibung des Streams. Diese Elemente werden in der [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) -Struktur gespeichert, die dem bearbeitbaren Stream zugeordnet ist.

Sie können auch die Textbeschreibung eines bearbeitbaren Streams mithilfe der Funktion [**editstreamsetname**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetnamea) ändern. Diese Funktion aktualisiert den **szName** -Member der **AVISTREAMINFO** -Struktur, die dem bearbeitbaren Stream zugeordnet ist.

Die Bearbeitungsfunktionen funktionieren in Datenströmen. Sie müssen jeden Stream einzeln Ausschneiden und einfügen und dann die [**avimakefilefromstreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) -Funktion verwenden, um einen neuen Dateizeiger zu erstellen.

> [!Note]  
> Die Bearbeitungs Tabellen in einem bearbeitbaren Stream behalten alle Änderungen für einen Datenstrom bei. Der Quellstream wird nie geändert.

 

 

 




