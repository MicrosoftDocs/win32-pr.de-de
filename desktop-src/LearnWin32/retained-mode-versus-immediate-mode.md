---
title: Modus für beibehaltene Modus und unmittelbarer
description: Grafik-APIs können in beibehaltene Modus-APIs und APIs für den unmittelbaren Modus aufgeteilt werden.
ms.assetid: 0a98e8ee-4bc1-490c-867e-42bceae8a1f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec3b89cd300f957211a9d4990c35ccbb70fa2b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104559486"
---
# <a name="retained-mode-versus-immediate-mode"></a>Modus für beibehaltene Modus und unmittelbarer

Grafik-APIs können in *beibehaltene Modus-* APIs und APIs für den *unmittelbaren Modus* aufgeteilt werden. Direct2D ist eine API im unmittelbaren Modus. Windows Presentation Foundation (WPF) ist ein Beispiel für eine API im beibehaltenen Modus.

Eine API im beibehaltenen Modus ist deklarativ. Die Anwendung erstellt eine Szene aus Grafik primitiven, z. b. Formen und Linien. In der Grafikbibliothek wird ein Modell der Szene im Arbeitsspeicher gespeichert. Um einen Frame zu zeichnen, transformiert die Grafikbibliothek die Szene in eine Reihe von Zeichnungs Befehlen. Zwischen Frames hält die Grafikbibliothek die Szene im Speicher. Um zu ändern, was gerendert wird, gibt die Anwendung einen Befehl zum Aktualisieren der Szene aus, z. –. um eine Form hinzuzufügen oder zu entfernen. Die Bibliothek ist dann für das Neuzeichnen der Szene verantwortlich.

![ein Diagramm, das Grafik im beibehaltenen Modus anzeigt.](images/graphics06.png)

Eine API im sofortigen Modus ist Verfahrensweise. Jedes Mal, wenn ein neuer Frame gezeichnet wird, gibt die Anwendung die Zeichnungs Befehle direkt aus. Die Grafikbibliothek speichert kein Szenen Modell zwischen Frames. Stattdessen wird die Szene von der Anwendung nachverfolgt.

![ein Diagramm, das Grafik im unmittelbaren Modus anzeigt.](images/graphics07.png)

APIs im beibehaltenen Modus können einfacher zu verwenden sein, da die API mehr Arbeit für Sie erledigt, wie z. b. Initialisierung, Zustands Verwaltung und Bereinigung. Sie sind dagegen oft weniger flexibel, da die API ein eigenes Szenen Modell erzwingt. Außerdem kann eine API im beibehaltenen Modus höhere Speicheranforderungen aufweisen, da Sie ein allgemeines Szenen Modell bereitstellen muss. Mit einer API im unmittelbaren Modus können Sie gezielte Optimierungen implementieren.

## <a name="next"></a>Nächste

[Ihr erstes Direct2D-Programm](your-first-direct2d-program.md)

 

 




