---
description: Ein Microsoft DirectX-Effekt ermöglicht die Integration von Vertex- und Pixel-Shadern in den Pipelinezustand zum Rendern von Objekten. Effekte sind der nächste logische Schritt beim Kombinieren von Shadern, um eindeutige Renderbedingungen zu erzeugen.
ms.assetid: vs|directx_sdk|~\effects.htm
title: Effekte (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59ed52a3a75f4b0682be4447f02ed305cf026af6aa30a59e921f4fa23f0e2211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985985"
---
# <a name="effects-direct3d-9"></a>Effekte (Direct3D 9)

Ein Microsoft DirectX-Effekt ermöglicht die Integration von Vertex- und Pixel-Shadern in den Pipelinezustand zum Rendern von Objekten. Effekte sind der nächste logische Schritt beim Kombinieren von Shadern, um eindeutige Renderbedingungen zu erzeugen.

Effekte bieten auch eine bequeme Möglichkeit, Shader für verschiedene Hardwareversionen zu schreiben. Da verschiedene Grafikkarten unterschiedliche Funktionen unterstützen, kann eine Anwendung mehrere Techniken schreiben, die auf einer Vielzahl von Geräten ausgeführt werden. Auf diese Weise kann die Anwendung die ausgereifteste Effekttechnik ausführen, wenn die Anwendung auf der neuesten und besten Hardware ausgeführt wird. Andererseits können weniger ausgereifte Effekttechniken automatisch ausgewählt werden, um auf kostengünstigerer oder weniger leistungsfähiger Hardware ausgeführt zu werden.

Ein Effekt kann die Scheitelpunktverarbeitung und einen Teil der Pixelverarbeitung ersetzen, die von der Grafikpipeline ausgeführt wird. Ein Beispiel für einen Effekt, der einen Scheitelpunkt-Shader und einen Pixel-Shader verwendet, ist im BasicHLSL-Beispiel. Sie erhalten dieses Beispiel und erfahren mehr über das DirectX SDK. Informationen zum DirectX SDK finden Sie unter [Wo befindet sich das DirectX SDK?](../directx-sdk--august-2009-.md).

Weitere Informationen zu Effekten finden Sie in den folgenden Themen:

-   [Schreiben eines Effekts](writing-an-effect.md)
-   [Verwenden eines Effekts](using-an-effect.md)

## <a name="effects-and-the-3d-pipeline"></a>Effekte und die 3D-Pipeline

Das folgende Diagramm zeigt die Pipeline.

![Diagramm der 3D-Pipeline](images/effects-block-diagram.png)

Die Pipeline transformiert Eingabedaten in Ausgabepixel, die den Rahmenpuffer füllen. Die Eingabedaten stammen von Objekten, die aus Scheitelpunkten im Objektbereich oder Oberflächen höherer Ordnung bestehen, die aus N-Patches, Rechteckpatches und Dreieckspatches erstellt wurden. Sobald die Eingabedaten mosaikiert wurden, führt die Pipeline die Scheitelpunktverarbeitung, primitive Verarbeitung und Pixelverarbeitung durch, bevor die endgültigen Pixelfarben generiert werden.

Die Vertex- und Pixelverarbeitung kann von der festen Funktionspipeline ausgeführt oder mit programmierbaren Shadern implementiert werden. Das Mosaik der Eingabedaten, die primitive Verarbeitung und die Datenausgaben werden durch den Pipelinezustand gesteuert. All dies kann in einen Effekt integriert werden. Ein Effekt legt den Zustand fest, der steuert, wie die Pipeline funktioniert. Wirkt sich auf verwaltbare programmierbare Shader sowie auf einen festen Funktionszustand aus.

Effekte können den Zustand speichern und wiederherstellen, sodass sich das Gerät im selben Zustand befindet wie vor der Ausführung des Effekts. Zu den Zustandstypen, die ein Effekt verwalten kann, gehören:

-   Shaderstatus. Dazu gehören das Erstellen und Löschen von Shadern, das Festlegen von Shaderkonstanten, das Festlegen des Shaderzustands und das Rendern mit Shadern.
-   Textur- und Samplerzustand. Dazu gehören das Angeben von Texturdateien, das Initialisieren von Texturstufen, das Erstellen von Samplerobjekten und das Festlegen des Samplerzustands.
-   Anderer Pipelinestatus. Dies schließt Zustände zum Festlegen von Transformationen, Beleuchtung, Materialien und Renderingoptionen ein. Dabei kann es sich um globale oder lokale Variablen handeln. Die Variablen können entweder durch den Effekt selbst oder durch die Anwendung festgelegt werden.

Effekte enthalten mehrere Renderingoptionen, die als Techniken bezeichnet werden. Jedes Verfahren kapselt globale Variablen, den Pipelinezustand, den Textur- und Samplerzustand sowie den Shaderzustand. Ein einzelner Stil wird in einem Renderingdurchlauf implementiert. Ein oder mehrere Durchläufe können in einer Technik gekapselt werden. Alle Durchläufe und Techniken können überprüft werden, um festzustellen, ob der Effektcode auf dem Hardwaregerät ausgeführt wird.

## <a name="effects-save-and-restore-state"></a>Auswirkungen: Speichern und Wiederherstellen des Zustands

Effekte verwalten den Zustand. Der Wortzustand wird hier sehr allgemein verwendet, da er alle Arten von Informationen enthält, die die Pipeline zum Angeben der Renderbedingungen benötigt. Dies schließt fast alle Funktionsbereiche der Pipeline ein.

Renderingoptionen werden durch Techniken und Durchläufe gesteuert. Eine Anwendung rendert einen Effekt, indem sie eine aktive Technik festlegt und einen oder mehrere Durchläufe rendert. Das gesamte Rendering in einem Effekt erfolgt innerhalb eines übereinstimmenden Paars von [**Begin-**](id3dxeffect--begin.md) und [**End-Aufrufen.**](id3dxeffect--end.md) Wenn **Begin** aufgerufen wird, wird ein Zustandsblock erstellt und der Gerätezustand gespeichert (sofern nicht anders angegeben). Nachdem eine Technik die Durchläufe gerendert hat, die die Anwendung zum Rendern angibt, wird **End** aufgerufen, um die aktive Technik zu beenden. Das Effektsystem reagiert durch automatisches Wiederherstellen des Pipelinezustands, der im Zustandsblock erfasst wurde (es sei denn, Sie deaktivieren diese Speicher- und Wiederherstellungsfunktion).

Beim Programmieren von Renderingsequenzen mit mehreren Durchläufen, von denen jede eine eigene Zustandseinrichtung erfordert, können Effekte die für die Nachverfolgung von Zustandsänderungen erforderliche Haltung reduzieren. Weitere Informationen zu den Zuständen, die durch Effekte gespeichert und wiederhergestellt werden können, finden Sie unter [Effektzustände (Direct3D 9).](effect-states.md)

## <a name="effects-can-share-parameters"></a>Effekte können Parameter freigeben

Effektparameter sind alle nicht statischen Variablen, die in einem Effekt deklariert werden. Dies kann globale Variablen und Anmerkungen enthalten. Effektparameter können von verschiedenen Effekten gemeinsam genutzt werden, indem Parameter mit dem shared-Schlüsselwort deklariert und dann der Effekt mit einem Effektpool erstellt wird.

Geklonte Effekte verwenden denselben Effektpool wie der Effekt, aus dem sie geklont werden. Beim Klonen eines Effekts wird eine genaue Kopie eines Effekts erstellt, einschließlich globaler Variablen, Techniken, Durchläufe und Anmerkungen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierhandbuch für Direct3D 9](dx9-graphics-programming-guide.md)
</dt> </dl>

 

 
