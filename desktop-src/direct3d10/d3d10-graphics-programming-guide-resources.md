---
description: Eine Ressource ist ein Bereich im Speicher, auf den von der Direct3D-Pipeline zugegriffen werden kann.
ms.assetid: 24859fbc-b5e1-4963-baf8-4f083f41f39a
title: Ressourcen (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93448fadd14d1a0849c9b730d34030b70d42a8cbc0926743e7059e222a6ea9c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567050"
---
# <a name="resources-direct3d-10"></a>Ressourcen (Direct3D 10)

Eine Ressource ist ein Bereich im Speicher, auf den von der Direct3D-Pipeline zugegriffen werden kann. Damit die Pipeline effizient auf den Arbeitsspeicher zugreifen kann, müssen daten, die für die Pipeline bereitgestellt werden (z. B. Eingabegeometrie, Shaderressourcen, Texturen usw.), in einer Ressource gespeichert werden. Es gibt zwei Arten von Ressourcen, aus denen alle Direct3D-Ressourcen abgeleitet sind: Puffer und Textur. Für jede Pipelinephase können bis zu 128 Ressourcen aktiv sein.

Jede Anwendung erstellt in der Regel viele Ressourcen. Beispiele für Ressourcen sind: Scheitelpunktpuffer, Indexpuffer, Konstantenpuffer, Texturen und Shaderressourcen. Es gibt mehrere Optionen, die bestimmen, wie Ressourcen verwendet werden können. Sie können Ressourcen erstellen, die stark typisiert oder weniger typisiert sind. Sie können steuern, ob Ressourcen sowohl Lese- als auch Schreibzugriff haben. Sie können Ressourcen nur für die CPU, GPU oder beides zugänglich machen. Natürlich kommt es zu einem Kompromiss zwischen Geschwindigkeit und Funktionalität. Je mehr Funktionalität Sie einer Ressource gestatten, desto weniger Leistung sollten Sie erwarten.

Da eine Anwendung häufig viele Texturen verwendet, führt Direct3D auch das Konzept eines Texturarrays ein, um die Texturverwaltung zu vereinfachen. Ein Texturarray enthält eine oder mehrere Texturen (alle gleichen Typen und Dimensionen), die innerhalb einer Anwendung oder von Shadern indiziert werden können. Texturarrays ermöglichen es Ihnen, eine einzelne Schnittstelle mit mehreren Indizes zu verwenden, um auf viele Texturen zuzugreifen. Sie können beliebig viele Texturarrays erstellen, um verschiedene Texturtypen zu verwalten.

Nachdem Sie die Ressourcen erstellt haben, die von Ihrer Anwendung verwendet werden, stellen Sie eine Verbindung mit den Pipelinephasen her, die sie verwenden, oder binden sie an diese. Dies wird erreicht, indem eine Bindungs-API aufgerufen wird, die einen Zeiger auf die Ressource annimmt. Da möglicherweise mehr als eine Pipelinephase Zugriff auf dieselbe Ressource benötigt, führt Direct3D 10 das Konzept einer Ressourcenansicht ein. Eine Ansicht identifiziert den Teil einer Ressource, auf den zugegriffen werden kann. Sie können m-Ansichten oder eine Ressource erstellen und sie an n Pipelinestufen binden, vorausgesetzt, Sie befolgen Bindungsregeln für freigegebene Ressourcen (andernfalls generiert die Runtime Fehler zur Kompilierzeit).

Eine Ressourcenansicht bietet ein allgemeines Modell für den Zugriff auf eine Ressource (Texturen, Puffer usw.). Da Sie eine Ansicht verwenden können, um der Laufzeit mitzuteilen, auf welche Daten zugegriffen werden soll und wie darauf zugegriffen werden soll, können Sie mithilfe von Ressourcenansichten weniger Ressourcen erstellen. Das heißt, Sie können zur Kompilierzeit Ressourcen für eine bestimmte Größe erstellen und dann den Datentyp innerhalb der Ressource deklarieren, wenn die Ressource an die Pipeline gebunden wird. Ansichten machen viele neue Funktionen für die Verwendung von Ressourcen verfügbar, z. B. die Möglichkeit, Tiefen-/Schablonenoberflächen im Shader zurückzulesen, dynamische Cubemaps in einem einzelnen Durchlauf zu generieren und gleichzeitig in mehrere Slices eines Volumes zu rendern.

Weitere Informationen zu den grundlegenden Ressourcentypen, Texturarrays und zum Erstellen und Verwenden von Ressourcen finden Sie in den folgenden anderen Themen:

-   [Ressourcentypen](d3d10-graphics-programming-guide-resources-types.md)
-   [Auswählen einer Ressource](d3d10-graphics-programming-guide-resources-choosing-basic.md)
-   [Erstellen von Pufferressourcen](d3d10-graphics-programming-guide-resources-creating.md)
-   [Erstellen von Texturressourcen](d3d10-graphics-programming-guide-resources-creating-textures.md)
-   [Kopieren und Zugreifen auf Ressourcendaten](d3d10-graphics-programming-guide-resources-mapping.md)
-   [Speicherstruktur und Ansichten](d3d10-graphics-programming-guide-resources-access-views.md)
-   [Blockkomprimierung](d3d10-graphics-programming-guide-resources-block-compression.md)
-   [Tabelle der Ressourcenlimits](d3d10-graphics-programming-guide-resources-limits.md)
-   [Koordinatensysteme](d3d10-graphics-programming-guide-resources-coordinates.md)
-   [Gleitkommaregeln](d3d10-graphics-programming-guide-resources-float-rules.md)
-   [Datentypkonvertierungsregeln](d3d10-graphics-programming-guide-resources-data-conversion.md)
-   [Zuordnen von Legacyformaten](d3d10-graphics-programming-guide-resources-legacy-formats.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierhandbuch für Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 



