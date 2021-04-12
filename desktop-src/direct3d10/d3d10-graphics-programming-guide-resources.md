---
description: Eine Ressource ist ein Bereich im Speicher, auf den von der Direct3D-Pipeline zugegriffen werden kann.
ms.assetid: 24859fbc-b5e1-4963-baf8-4f083f41f39a
title: Ressourcen (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e8bb064bc771e36335527d68891bc76a1ce4df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483590"
---
# <a name="resources-direct3d-10"></a>Ressourcen (Direct3D 10)

Eine Ressource ist ein Bereich im Speicher, auf den von der Direct3D-Pipeline zugegriffen werden kann. Damit die Pipeline effizient auf den Arbeitsspeicher zugreifen kann, müssen Daten, die für die Pipeline bereitgestellt werden (z. b. Eingabe Geometrie, Shader-Ressourcen, Texturen usw.), in einer Ressource gespeichert werden. Es gibt zwei Arten von Ressourcen, aus denen alle Direct3D-Ressourcen abgeleitet sind: Puffer und Textur. Für jede Pipelinephase können bis zu 128 Ressourcen aktiv sein.

Jede Anwendung erstellt in der Regel viele Ressourcen. Beispiele für Ressourcen sind: Vertex-Puffer, Index Puffer, konstanter Puffer, Texturen und Shader-Ressourcen. Es gibt mehrere Optionen, die bestimmen, wie Ressourcen verwendet werden können. Sie können Ressourcen erstellen, die stark typisiert sind, oder weniger eingeben. Sie können steuern, ob Ressourcen sowohl Lese-als auch Schreibzugriff haben. Sie können Ressourcen nur für die CPU, die GPU oder beides verfügbar machen. Natürlich gibt es eine Geschwindigkeit im Vergleich zu den Funktionen, die für eine Ressource zu erwarten sind, und desto geringer ist die Leistung, die Sie erwarten sollten.

Da eine Anwendung häufig viele Texturen verwendet, führt Direct3D auch das Konzept eines Textur Arrays ein, um die Textur Verwaltung zu vereinfachen. Ein Textur Array enthält eine oder mehrere Texturen (alle Typen und Dimensionen), die in einer Anwendung oder von Shadern indiziert werden können. Textur Arrays ermöglichen es Ihnen, eine einzelne Schnittstelle mit mehreren Indizes zu verwenden, um auf viele Texturen zuzugreifen. Sie können so viele Textur Arrays erstellen, um unterschiedliche Textur Typen zu verwalten, wie Sie benötigen.

Nachdem Sie die Ressourcen erstellt haben, die von Ihrer Anwendung verwendet werden, verbinden oder binden Sie jede Ressource an die Pipeline Stufen, von denen Sie verwendet werden. Dies wird erreicht, indem eine Bindungs-API aufgerufen wird, die einen Zeiger auf die Ressource annimmt. Da mehr als eine Pipeline Phase möglicherweise Zugriff auf dieselbe Ressource benötigt, führt Direct3D 10 das Konzept einer Ressourcen Ansicht ein. Eine Sicht identifiziert den Teil einer Ressource, auf die zugegriffen werden kann. Sie können m-Sichten oder eine Ressource erstellen und diese an n Pipeline Stufen binden. dabei wird davon ausgegangen, dass Sie die Bindungs Regeln für eine freigegebene Ressource befolgen (die Laufzeit generiert ggf. Fehler zur Kompilierzeit).

Eine Ressourcen Ansicht bietet ein allgemeines Modell für den Zugriff auf eine Ressource (Texturen, Puffer usw.). Da Sie eine Ansicht verwenden können, um der Laufzeit mitzuteilen, auf welche Daten zugegriffen werden soll und wie darauf zugegriffen werden kann, können Sie mit Ressourcen Sichten Typen mit weniger Ressourcen erstellen. Das heißt, Sie können zur Kompilierzeit Ressourcen für eine bestimmte Größe erstellen und dann den Datentyp innerhalb der Ressource deklarieren, wenn die Ressource an die Pipeline gebunden wird. Sichten stellen zahlreiche neue Funktionen für die Verwendung von Ressourcen zur Verfügung, z. b. die Möglichkeit, Tiefe-/Schablone-Oberflächen im Shader zu lesen, dynamische Cubemaps in einem einzigen Durchlauf zu erzeugen und gleichzeitig auf mehrere Slices eines Volumes zu rendern.

Weitere Informationen zu den grundlegenden Ressourcentypen, Textur Arrays und zum Erstellen und Verwenden von Ressourcen finden Sie in den folgenden Themen:

-   [Ressourcentypen](d3d10-graphics-programming-guide-resources-types.md)
-   [Auswählen einer Ressource](d3d10-graphics-programming-guide-resources-choosing-basic.md)
-   [Erstellen von Puffer Ressourcen](d3d10-graphics-programming-guide-resources-creating.md)
-   [Erstellen von Textur Ressourcen](d3d10-graphics-programming-guide-resources-creating-textures.md)
-   [Kopieren und Zugreifen auf Ressourcen Daten](d3d10-graphics-programming-guide-resources-mapping.md)
-   [Arbeitsspeicher Struktur und-Sichten](d3d10-graphics-programming-guide-resources-access-views.md)
-   [Block Komprimierung](d3d10-graphics-programming-guide-resources-block-compression.md)
-   [Tabelle mit Ressourcen Limits](d3d10-graphics-programming-guide-resources-limits.md)
-   [Koordinatensysteme](d3d10-graphics-programming-guide-resources-coordinates.md)
-   [Gleit Komma Regeln](d3d10-graphics-programming-guide-resources-float-rules.md)
-   [Datentyp-Konvertierungsregeln](d3d10-graphics-programming-guide-resources-data-conversion.md)
-   [Mapping von Legacy Formaten](d3d10-graphics-programming-guide-resources-legacy-formats.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmier Handbuch für Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 



