---
title: Implementieren von Rendern
description: Implementieren von Rendern
ms.assetid: 9b3a64f6-6803-457c-8e63-e8a799089e18
keywords:
- Visualisierungen, Zeitereignisse
- Benutzerdefinierte Visualisierungen, Zeitereignisse
- Visualisierungen, Renderfunktion
- Benutzerdefinierte Visualisierungen, Renderfunktion
- Visualisierungen,RenderWindow-Funktion
- Benutzerdefinierte Visualisierungen, RenderWindow-Funktion
- Renderfunktion, Parameter
- RenderWindow-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5af44299c8a8e34c8f63844dc7d2c143f1d85e0b622c50dd246ea12571d94af8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119390690"
---
# <a name="implementing-render"></a>Implementieren von Rendern

Die einfachste Möglichkeit zur Visualisierungsprogrammierung besteht darin, dass Sie einen Handler für ein Zeitereignis erstellen. In bestimmten Intervallen erstellt Windows Media Player eine Momentaufnahme der Audiodaten, die wiedergegeben werden, und stellt die Momentaufnahmedaten für die aktuell geladene Visualisierung bereit. Dies ähnelt der ereignisgesteuerten Programmierung und ist Teil des Programmiermodells von Microsoft Windows. Sie schreiben Code und warten, bis er von einem bestimmten Ereignis aufgerufen wird.

Wenn Ihr Code eine Implementierung der [IWMPEffects::Render-Funktion](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) zum Rendern im fensterlosen Modus ist, erhält er die folgenden Parameter:

*TimedLevel*

Dies ist eine Struktur, die die Audiodaten definiert, die Ihr Code analysiert. Die -Struktur besteht aus zwei Arrays. Das erste Array basiert auf Frequency-Informationen und enthält eine Momentaufnahme des Audiospektrums, unterteilt in 1024 Teile. Jede Zelle des Arrays enthält einen Wert zwischen 0 und 255. Die erste Zelle beginnt bei 20 Hz und die letzte bei 22050 Hz. Das Array ist zweidimensional, um Stereoaudio darzustellen. Das zweite Array basiert auf Wellenforminformationen und entspricht der Audioleistung, wobei je stärker die Welle ist, desto größer der Wert. Das Wellenformarray ist eine präzise Momentaufnahme der letzten 1024 Slices der Audioleistung, die in sehr kleinen Zeitintervallen aufgenommen wurden. Dieses Array ist auch zweidimensional, um Stereoaudio darzustellen.

*Hdc*

Dies ist ein Microsoft Windows Handle für einen Gerätekontext. Dies bietet eine Möglichkeit, die zu Windows Zeichnungsoberfläche zu identifizieren. Sie müssen sie nicht erstellen, sie müssen sie nur für bestimmte Zeichnungsfunktionsaufrufe verwenden.

*Rect*

Dies ist ein Microsoft Windows Rechteck, das die Größe einer Zeichnungsoberfläche definiert. Dies ist ein einfaches Rechteck mit vier Eigenschaften: **links,** **rechts,** **oben** und **unten.** Die tatsächlichen Werte werden von Windows Media Player bereitgestellt, sodass Sie bestimmen können, wie der Benutzer oder Der Skinentwickler die Größe des Fensters festgelegt hat, auf das Sie zeichnen möchten. Außerdem wird die Position auf dem HDC bestimmt, auf der der Effekt gerendert werden soll.

Wenn Ihr Code eine Implementierung der **IWMPEffects2::RenderWindowed-Funktion** zum Rendern in einem Fenster ist, empfängt er die folgenden Parameter:

*TimedLevel*

Dies sind die gleichen Informationen, die die **Render-Funktion** empfängt.

*fRequiredRender*

Der *Parameter fRequiredRender* informiert Sie darüber, dass ihre Visualisierung sich selbst neu malen muss, z. B. wenn ein anderes Fenster darüber gezogen wird. Wenn dieser Wert false ist, können Sie den Renderingcode problemlos überspringen, wenn das aktuelle Medienelement beendet oder angehalten wird. Dadurch können Sie vermeiden, dass CPU-Zyklen unnötig verbraucht werden.

Das vom Plug-In-Assistenten generierte Beispiel-Plug-In stellt keine benutzerdefinierte Implementierung für **RenderWindowed** bereit. Stattdessen ruft der Beispiel-Plug-In-Code den Gerätekontext aus dem übergeordneten Fenster ab, das von Windows Media Player in [IWMPEffects2::Create](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-create)bereitgestellt wird, ruft dann die Dimensionen des übergeordneten Fensters als RECT-Struktur ab und ruft dann mithilfe des Gerätekontexts, des RECT und des Zeigers auf Zeitebene von **RenderWindowed** auf **Rendern** auf.

Die folgenden Abschnitte enthalten weitere Informationen zum Implementieren von **Render:**

-   [Verwenden von zeitierten Ebenen](using-timed-levels.md)
-   [Verwenden von Gerätekontexten](using-device-contexts.md)
-   [Verwenden von Rechtecke](using-rectangles.md)
-   [Beispiel für Rendercode](sample-render-code.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren ihres Codes**](implementing-your-code.md)
</dt> </dl>

 

 




