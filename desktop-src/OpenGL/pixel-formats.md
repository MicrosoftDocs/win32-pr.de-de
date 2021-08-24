---
title: Pixelformate
description: Pixelformate
ms.assetid: 2e179340-c487-4b72-a22e-078b800af11d
keywords:
- OpenGL auf Windows Pixeln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbcd49b17c298d00d0ab41391172c8ae4c3bce8cb295db619d1c9787a2bca36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119486190"
---
# <a name="pixel-formats"></a>Pixelformate

Ein *Pixelformat* gibt mehrere Eigenschaften einer OpenGL-Zeichnungsoberfläche an. Einige der durch ein Pixelformat angegebenen Eigenschaften sind:

-   Gibt an, ob der Pixelpuffer ein- oder doppelt gepuffert ist.
-   Gibt an, ob die Pixeldaten in RGBA- oder Farbindexform vorliegen.
-   Die Anzahl der Bits, die zum Speichern von Farbdaten verwendet werden.
-   Die Anzahl der Bits, die für den Tiefenpuffer (z-Achse) verwendet werden.
-   Die Anzahl von Bits, die für den Schablonenpuffer verwendet werden.
-   Die Anzahl der Überlagerungs- und Unterlageebenen.
-   Verschiedene Sichtbarkeitsmasken.

Die Microsoft-Implementierung von OpenGL für Windows verwendet die [**PIXELFORMATDESCRIPTOR-Datenstruktur,**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) um Pixelformatdaten zu übermitteln. Die Elemente der Struktur geben die vorangehenden Eigenschaften und einige andere an.

Ein angegebener Gerätekontext kann mehrere Pixelformate unterstützen. Windows identifiziert die Pixelformate, die ein Gerätekontext unterstützt, mit aufeinander folgenden einbasierten Indexwerten (1, 2, 3, 4 usw.). Ein Gerätekontext kann nur ein aktuelles Pixelformat aufweisen, das aus den unterstützten Pixelformaten ausgewählt wird.

Jedes Fenster verfügt über ein eigenes aktuelles Pixelformat in OpenGL in Windows. Dies bedeutet beispielsweise, dass eine Anwendung gleichzeitig RGBA- und Farbindex-OpenGL-Fenster oder ein- und doppelt gepufferte OpenGL-Fenster anzeigen kann. Diese Pixelformatfunktion pro Fenster ist auf OpenGL-Fenster beschränkt.

In der Regel erhalten Sie einen Gerätekontext, legen das Pixelformat des Gerätekontexts fest und erstellen dann einen für dieses Gerät geeigneten OpenGL-Renderingkontext.

> [!Note]  
> Sie legen das Pixelformat fest, bevor Sie einen Renderingkontext erstellen, da der Renderingkontext das Pixelformat des Gerätekontexts erbt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelformatfunktionen](pixel-format-functions.md)
</dt> </dl>

 

 




