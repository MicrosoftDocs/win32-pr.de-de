---
description: Ein Microsoft DirectX-Effekt ermöglicht die Integration von Vertex-und Pixel-Shadern in den Pipeline Zustand zum Rendern von Objekten. Effekte sind der nächste logische Schritt bei der Kombination von Shadern, um eindeutige renderbedingungen zu erzeugen.
ms.assetid: vs|directx_sdk|~\effects.htm
title: Effekte (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d48d2ff5548dff29ede4b360bd2c319f85fafa3e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345592"
---
# <a name="effects-direct3d-9"></a>Effekte (Direct3D 9)

Ein Microsoft DirectX-Effekt ermöglicht die Integration von Vertex-und Pixel-Shadern in den Pipeline Zustand zum Rendern von Objekten. Effekte sind der nächste logische Schritt bei der Kombination von Shadern, um eindeutige renderbedingungen zu erzeugen.

Effekte bieten außerdem eine bequeme Möglichkeit, Shader für verschiedene Hardware Versionen zu schreiben. Da verschiedene Grafikkarten verschiedene Funktionen unterstützen, kann eine Anwendung mehrere Techniken schreiben, die auf einer Vielzahl von Geräten ausgeführt werden. Auf diese Weise kann die Anwendung, wenn die Anwendung auf der neuesten und größten Hardware ausgeführt wird, die ausgereifteste Effekt Methode ausführen. Auf der anderen Seite können weniger ausgereifte Effekt Techniken automatisch für eine kostengünstigere oder weniger leistungsfähige Hardware ausgewählt werden.

Ein Effekt kann die Vertexverarbeitung und einen Teil der Pixel Verarbeitung ersetzen, die von der Grafik Pipeline ausgeführt wird. Ein Beispiel eines Effekts, der einen Vertex-Shader und einen PixelShader verwendet, ist das basichlsl-Beispiel. Dieses Beispiel finden Sie im DirectX SDK. Weitere Informationen zum DirectX SDK finden Sie unter [wo ist das DirectX SDK?](../directx-sdk--august-2009-.md).

Weitere Informationen zu den Auswirkungen finden Sie in den folgenden Themen:

-   [Schreiben eines Effekts](writing-an-effect.md)
-   [Verwenden eines Effekts](using-an-effect.md)

## <a name="effects-and-the-3d-pipeline"></a>Effekte und 3D-Pipeline

Das folgende Diagramm zeigt die Pipeline.

![Diagramm der 3D--Pipeline](images/effects-block-diagram.png)

Die Pipeline transformiert Eingabedaten in Ausgabe Pixel, die den Frame Puffer ausfüllen. Die Eingabedaten stammen aus Objekten, die aus Scheitel Punkten im Objektbereich bestehen, oder aus höherwertigen Oberflächen, die aus N-Patches, Rechteck Patches und Dreiecks Patches erstellt werden. Nachdem die Eingabedaten im Mosaik Prozess verarbeitet wurden, führt die Pipeline die Vertexverarbeitung, die primitive Verarbeitung und die Pixel Verarbeitung aus, bevor die letzten Pixel Farben erzeugt werden.

Die Vertex-und Pixel Verarbeitung kann von der Fixed-Funktions Pipeline ausgeführt werden oder kann mit programmierbaren Shadern implementiert werden. Die Eingabedaten, die primitive Verarbeitung und die Daten Ausgaben werden über den Pipeline Status gesteuert. All dies kann in einen Effekt integriert werden. Mit einem Effekt wird der Zustand festgelegt, der steuert, wie die Pipeline funktioniert. Effekte Verwaltung programmierbarer Shader und fester Funktionsstatus.

Die Auswirkungen können den Status speichern und wiederherstellen, sodass das Gerät im selben Zustand wie vor dem Ausführen der Auswirkung bleibt. Zu den Zustandstypen, die ein Effekt verwalten kann, zählen:

-   Shader-Zustand. Dies umfasst das Erstellen und Löschen von Shadern, das Festlegen von shaderkonstanten, das Festlegen des Shader-Zustands und das Rendering mit Shadern.
-   Textur-und samplerzustand. Dies umfasst das Angeben von Textur Dateien, das Initialisieren von Textur Stufen, das Erstellen von samplingobjekten und das Festlegen des Sampl
-   Anderer Pipeline Status. Dies schließt Zustände für das Festlegen von Transformationen, Beleuchtung, Materialien und Renderingoptionen ein. Hierbei kann es sich um globale oder lokale Variablen handeln. Die Variablen können entweder durch den Effekt selbst oder durch die Anwendung festgelegt werden.

Effekte enthalten mehrere Renderingoptionen namens Techniken. Jede Technik kapselt globale Variablen, den Pipeline Status, den Textur-und samplerzustand und den Shader-Zustand. Ein einzelner Stil wird in einem Renderingdurchlauf implementiert. Mindestens ein Durchlauf kann in einer Technik gekapselt werden. Alle Durchgänge und Techniken können überprüft werden, um festzustellen, ob der Effekt Code auf dem Hardware Gerät ausgeführt wird.

## <a name="effects-save-and-restore-state"></a>Effekte speichern und Wiederherstellen des Zustands

Auswirkungen der Zustands Verwaltung. Der Word-Status wird hier sehr weitgehend verwendet, da darin alle Arten von Informationen enthalten sind, die die Pipeline zum Angeben der Rendering-Bedingungen benötigt. Dies umfasst fast alle funktionalen Bereiche der Pipeline.

Renderingoptionen werden durch Techniken und Durchgänge gesteuert. Eine Anwendung rendert einen Effekt durch Festlegen einer aktiven Technik und Rendern von einem oder mehreren Durchläufen. Alle Renderingvorgänge werden in einem passenden Paar von [**Begin**](id3dxeffect--begin.md) -und [**End**](id3dxeffect--end.md) -aufrufen durchgeführt. Wenn **Begin** aufgerufen wird, wird ein stateblock erstellt und der Gerätezustand gespeichert (sofern nicht anders angegeben). Nachdem eine Technik die durch die Anwendung festgelegten Übergänge gerendert hat, wird **End** aufgerufen, um die aktive Technik zu beenden. Das Effektsystem antwortet, indem der Pipeline Status, der im Zustands Block aufgezeichnet wurde, automatisch wieder hergestellt wird (es sei denn, Sie deaktivieren diese Speicher-und Wiederherstellungs Funktionalität).

Beim Programmieren mehrerer renderingsequenzen, von denen jeder eine eigene Zustands Einrichtung erfordert, können Effekte die für das Nachverfolgen von Zustandsänderungen erforderliche Verwaltung reduzieren. Weitere Informationen zu den Zuständen, die durch Effekte gespeichert und wieder hergestellt werden können, finden Sie unter [Effect States (Direct3D 9)](effect-states.md).

## <a name="effects-can-share-parameters"></a>Effekte können Parameter freigeben

Effektparameter sind alle nicht statischen Variablen, die in einem Effekt deklariert werden. Dies kann globale Variablen und Anmerkungen enthalten. Effektparameter können von verschiedenen Effekten gemeinsam genutzt werden, indem Parameter mit dem Schlüsselwort "Shared" deklariert und dann der Effekt mit einem Effekt Pool erstellt wird.

Geklonte Effekte verwenden denselben Effekt Pool wie der Effekt, von dem Sie geklont werden. Das Klonen eines Effekts führt zu einer exakten Kopie eines Effekts, einschließlich globaler Variablen, Techniken, Durchläufen und Anmerkungen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmier Handbuch für Direct3D 9](dx9-graphics-programming-guide.md)
</dt> </dl>

 

 
