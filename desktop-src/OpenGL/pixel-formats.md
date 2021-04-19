---
title: Pixel Formate
description: Pixel Formate
ms.assetid: 2e179340-c487-4b72-a22e-078b800af11d
keywords:
- OpenGL unter Windows, Pixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d16f9f78edc0cf935fb602de8d88792091588ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342087"
---
# <a name="pixel-formats"></a>Pixel Formate

Ein *Pixel Format* gibt mehrere Eigenschaften einer OpenGL-Zeichen Oberfläche an. Einige der Eigenschaften, die durch ein Pixel Format angegeben werden, sind:

-   Gibt an, ob der Pixel Puffer einzeln oder doppelt gepuffert ist.
-   Gibt an, ob sich die Pixeldaten im RGBA-oder Farb Index Formular befinden.
-   Die Anzahl der Bits, die zum Speichern von Farbdaten verwendet werden.
-   Die Anzahl der Bits, die für den tiefen Puffer (z-Achse) verwendet werden.
-   Die Anzahl der Bits, die für den Schablonen Puffer verwendet werden.
-   Die Anzahl der Ebenen für Überlagerung und Unterebene.
-   Verschiedene Sichtbarkeits Masken.

Die Microsoft-Implementierung von OpenGL für Windows verwendet die Pixel [**formatdescriptor**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) -Datenstruktur, um Pixel Formatierungsdaten zu vermitteln. Die Member der Struktur geben die vorangehenden Eigenschaften und mehrere andere an.

Ein bestimmter Gerätekontext kann mehrere Pixel Formate unterstützen. Windows identifiziert die Pixel Formate, die ein Gerätekontext mit aufeinander folgenden einbasierten Indexwerten unterstützt (1, 2, 3, 4 usw.). Ein Gerätekontext kann nur ein Aktuelles Pixel Format aufweisen, das aus den von ihm unterstützten Pixel Formaten ausgewählt wird.

Jedes Fenster verfügt über ein eigenes Aktuelles Pixel Format in OpenGL in Windows. Dies bedeutet beispielsweise, dass eine Anwendung RGBA-und Color-Index OpenGL-Fenster gleichzeitig anzeigen kann, oder ein Single-und Double-Buffered OpenGL-Fenster. Diese Funktion für die Pixel Formate pro Fenster ist auf OpenGL-Fenster beschränkt.

Normalerweise erhalten Sie einen Gerätekontext, legen das Pixel Format des Geräte Kontexts fest und erstellen dann einen OpenGL-renderingkontext, der für dieses Gerät geeignet ist.

> [!Note]  
> Sie legen das Pixel Format vor dem Erstellen eines renderingkontexts fest, da der renderingkontext das Pixel Format des Geräte Kontexts erbt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixel Format Funktionen](pixel-format-functions.md)
</dt> </dl>

 

 




