---
title: Implementieren von Rendering
description: Implementieren von Rendering
ms.assetid: 9b3a64f6-6803-457c-8e63-e8a799089e18
keywords:
- Visualisierungen, zeitgesteuerte Ereignisse
- benutzerdefinierte Visualisierungen, zeitgesteuerte Ereignisse
- Visualisierungen, Rendering-Funktion
- benutzerdefinierte Visualisierungen, Rendering-Funktion
- Visualisierungen, renderwindow-Funktion
- benutzerdefinierte Visualisierungen, renderwindow-Funktion
- Funktion "Rendering", Parameter
- Renderwindow-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99db0a96a07c361d18de579fb0235befa11838c8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038561"
---
# <a name="implementing-render"></a>Implementieren von Rendering

Die einfachste Möglichkeit, die Visualisierungs Programmierung vorzustellen, besteht darin, dass Sie einen Handler für ein Zeit gesteuerter Ereignis erstellen. In bestimmten Intervallen nimmt Windows Media Player eine Momentaufnahme der Audiodaten, die Sie wiedergeben, und stellt die Moment Aufnahmedaten für die aktuell geladene Visualisierung bereit. Dies ähnelt der ereignisgesteuerten Programmierung und ist Teil des Programmiermodells von Microsoft Windows. Sie schreiben Code und warten darauf, dass er von einem bestimmten Ereignis aufgerufen wird.

Wenn Ihr Code eine Implementierung der [iwmpeffects::](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) Rendering-Funktion für das Rendering im fensterlosen Modus ist, empfängt er die folgenden Parameter:

*Timedlevel*

Dies ist eine Struktur, die die Audiodaten definiert, die vom Code analysiert werden. Die Struktur besteht aus zwei Arrays. Das erste Array basiert auf Häufigkeits Informationen und enthält eine Momentaufnahme des Audiospektrums, das in 1024 Teile aufgeteilt ist. Jede Zelle des Arrays enthält einen Wert zwischen 0 und 255. Die erste Zelle beginnt bei 20 Hz und der letzte bei 22050 Hz. Das Array ist zweidimensional, um Stereo-Audiodaten darzustellen. Das zweite Array basiert auf Wellenform-Informationen und entspricht der Audioleistung. je stärker die Welle ist, desto größer ist der Wert. Das Wellenform-Array ist eine präzise Momentaufnahme der letzten 1024 Slices von audiostromdaten, die in sehr kleinen Zeitintervallen entnommen wurden. Dieses Array ist auch zweidimensional, um Stereo-Audiodaten darzustellen.

*HDC*

Dies ist ein Microsoft Windows-Handle für einen Gerätekontext. Dies bietet eine Möglichkeit, die Zeichen Oberfläche für Windows zu identifizieren. Sie müssen Sie nicht erstellen, sondern nur für bestimmte Zeichnungs Funktionsaufrufe verwenden.

*Rect*

Dies ist ein Microsoft Windows-Rechteck, das die Größe einer Zeichen Oberfläche definiert. Dabei handelt es sich um ein einfaches Rechteck mit vier Eigenschaften: **Links**, **Rechts**, **oben** und **unten**. Die tatsächlichen Werte werden von Windows Media Player bereitgestellt, damit Sie bestimmen können, wie der Benutzer oder der Skin-Entwickler das Fenster, das Sie zeichnen, skaliert hat. Außerdem wird die Position auf dem HDC festgelegt, in der der Effekt dargestellt werden soll.

Wenn Ihr Code eine Implementierung der **IWMPEffects2:: renderwindowed** -Funktion für das Rendering in einem Fenster ist, empfängt er die folgenden Parameter:

*Timedlevel*

Dies sind die gleichen Informationen, die von der Funktion " **Rendering** " empfangen werden.

*frequiredrender*

Der Parameter " *frequiredrender* " informiert Sie darüber, dass sich ihre Visualisierung selbst neu zeichnen muss, z. –. Wenn ein anderes Fenster darauf gezogen wird. Wenn dieser Wert false ist, können Sie den Renderingcode gefahrlos überspringen, wenn das aktuelle Medien Element beendet oder angehalten wurde. So können Sie unnötige CPU-Zyklen vermeiden.

Das Beispiel-Plug-in, das vom Plug-in-Assistenten generiert wurde, stellt keine benutzerdefinierte Implementierung für **renderwindowed** bereit. Stattdessen ruft der Beispiel-Plug-in-Code den Gerätekontext aus dem übergeordneten Fenster ab, das von der Windows-Media Player in [IWMPEffects2:: Create](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-create)bereitgestellt wird. Anschließend wird die Dimension des übergeordneten Fensters als Rect-Struktur abgerufen, und dann wird aufgerufen **, um mithilfe** des Geräte Kontexts, des Rect und des Zeigers auf der Zeitüberschreitung von **renderwindowed** geren

In den folgenden Abschnitten finden Sie weitere Informationen zur Implementierung von " **Rendering**":

-   [Verwenden von zeitgesteuerten Ebenen](using-timed-levels.md)
-   [Verwenden von Geräte Kontexten](using-device-contexts.md)
-   [Verwenden von Rechtecke](using-rectangles.md)
-   [Beispiel-Rendering-Code](sample-render-code.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren des Codes**](implementing-your-code.md)
</dt> </dl>

 

 




