---
description: Verwalten von Video Bearbeitungs Projekten
ms.assetid: f8d74807-562f-429b-93a1-e65d0f15163b
title: Verwalten von Video Bearbeitungs Projekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 491cfcb9a6e94874d2cae43567b61666bbd43cd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344912"
---
# <a name="managing-video-editing-projects"></a>Verwalten von Video Bearbeitungs Projekten

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

Die folgenden Tipps helfen Ihnen beim Verwalten von Projekten in [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md).

Änderungen an der Zeitachse

-   Wenn Sie die Zeitachse nach dem Erstellen des Filter Diagramms ändern, müssen Sie " [**unenderengine:: connectfrontend**](irenderengine-connectfrontend.md) " erneut ausführen, um das Front-End wiederherzustellen. Normalerweise wirkt sich dies nicht auf den Rest des Diagramms aus. Gelegentlich muss die Renderingengine jedoch das gesamte Diagramm löschen, bevor es das Front-End neu erstellt. (Dies ist z. b. der Fall, wenn Sie eine Gruppe hinzufügen oder entfernen.) Die **connectfrontend** -Methode gibt "S \_ Warn \_ outputreset" zurück, um zu signalisieren, dass Sie das Diagramm gelöscht hat. Wenn dies der Fall ist, muss die Anwendung den Renderingabschnitt des Diagramms neu erstellen.
-   Um alle Objekte vollständig aus der Zeitachse zu entfernen, müssen Sie die [**iamtimeline:: clearallgroups**](iamtimeline-clearallgroups.md) -Methode aufrufen.

**Bereinigung**

-   Wenn Sie mit der Verwendung einer Rendering-Engine fertig sind, müssen Sie die Methode " [**irienderengine:: scrapit**](irenderengine-scrapit.md) " aufzurufen. Stellen Sie wie bei jedem COM-Objekt sicher, dass Sie jeden Schnittstellen Zeiger freigeben, wenn Sie ihn nicht mehr verwenden.
-   Die Renderingengine behält keinen Verweis Zähler auf der Zeitachse. Veröffentlichen Sie die Zeitachse nicht, bevor Sie Sie verwenden, und fordern Sie zuerst in der Renderingengine zuerst " **scrapit** " an.
-   Wenn Sie alle Verweise auf eine Zeitachse freigeben, sollten Sie keines der Objekte in dieser Zeitachse verwenden, auch wenn Sie Verweis Zähler für Sie enthalten.

**Mehrere Zeitachsen Instanzen**

-   Verschieben Sie keine Zeitachsen Objekte Zwischenzeit Achsen. Jedes Objekt in einer Zeitachse muss von dieser Zeitachse erstellt werden. Die Zeitachse enthält einen internen Cache mit Informationen zu den Objekten, die Sie erstellt. das Verschieben von Zeitachsen Objekten kann den Cache stören.
-   Verwenden Sie niemals dieselbe Instanz eines rendermoduls mit mehr als einer Zeitachse. Die Renderingengine enthält einen Cache mit Informationen über die Zeitachse. Mehrere Zeitachsen stören den Cache und verursachen unvorhersehbare Ergebnisse. Wenn Sie zwei aktive Zeitachsen benötigen, erstellen Sie separate Instanzen von renderengines für jede Zeitachse.
-   Eine Zeitachse kann mehr als eine Renderingengine verwenden, aber nicht gleichzeitig. Löschen Sie die alte Rendering-Engine, bevor Sie eine andere Renderengine verwenden (Dies würden Sie in der Regel tun, wenn Sie von der Verwendung der grundlegenden Renderingengine für die Vorschauversion zum intelligenten Renderingmodul zum Schreiben von Dateien wechseln

**Persistenz**

-   Das Filter Diagramm ist nicht persistent, wenn Sie das Projekt in einer XML-Datei speichern. Daher verlieren Sie alle Informationen im Zusammenhang mit der intelligenten Neukomprimierung, dem Komprimierungs Format oder den Komprimierungs Parametern. Die Anwendung kann diese Parameter nach dem Laden eines Projekts wiederherstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von DirectShow-Bearbeitungs Diensten](using-directshow-editing-services.md)
</dt> </dl>

 

 



