---
title: Warum werden Kachel Ressourcen benötigt?
description: Gekachelte Ressourcen werden benötigt, sodass weniger GPU-Speicher (Graphics Processing Unit) verschwendet wird, um Bereiche von Oberflächen zu speichern, auf die die Anwendung keinen Zugriff hat, und die Hardware weiß, wie Sie über angrenzende Kacheln filtern kann.
ms.assetid: E2179D65-56D3-481F-A5F3-B9C45A11A179
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d42ccccf66a73d224d8bab9a9d10c87cc330be43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976656"
---
# <a name="why-are-tiled-resources-needed"></a>Warum werden Kachel Ressourcen benötigt?

Gekachelte Ressourcen werden benötigt, sodass weniger GPU-Speicher (Graphics Processing Unit) verschwendet wird, um Bereiche von Oberflächen zu speichern, auf die die Anwendung keinen Zugriff hat, und die Hardware weiß, wie Sie über angrenzende Kacheln filtern kann.

In einem Grafiksystem (d. h. Betriebssystem, Anzeigetreiber und Grafikhardware) ohne Unterstützung für gekachelte Ressourcen verwaltet das Grafiksystem alle Direct3D-Speicher Belegungen in der untergeordneten Quell Granularität. Bei einem [Puffer](overviews-direct3d-11-resources-buffers.md)ist der gesamte Puffer die untergeordnete Quelle. Für eine [Textur](overviews-direct3d-11-resources-textures.md) (z. b. [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d)) ist jede MIP-Ebene eine untergeordnete Quelle. bei einem Textur Array (z. b. [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray)) ist jede MIP-Ebene in einem angegebenen Array Slice eine untergeordnete Quelle. Das Grafiksystem macht nur die Möglichkeit zur Verwaltung der Zuordnung von Zuordnungen in dieser unter Quell Granularität verfügbar. Im Zusammenhang mit den gekachelten Ressourcen bezieht sich "Mapping" darauf, dass Daten für die GPU sichtbar sind.

Angenommen, eine Anwendung weiß, dass ein bestimmter Renderingvorgang nur auf einen kleinen Teil der MipMap-Kette des Bilds zugreifen muss (möglicherweise nicht auf den vollständigen Bereich einer bestimmten MipMap). Im Idealfall könnte die APP das Grafiksystem über diesen Bedarf informieren. Das Grafiksystem würde dann nur dann sicherstellen, dass der benötigte Arbeitsspeicher auf der GPU ohne Paging in zu viel Arbeitsspeicher zugeordnet wird. In der Realität kann das Grafiksystem nur über den Arbeitsspeicher informiert werden, der auf der GPU bei der unter Ressourcen-Granularität zugeordnet werden muss (z. b. ein Bereich von vollständigen MipMap-Ebenen, auf die zugegriffen werden kann). Es gibt auch keinen Anforderungs Fehler im Grafiksystem. Daher muss möglicherweise viel überschüssiger GPU-Speicher verwendet werden, um vollständige unter Ressourcen vor einem Rendering-Befehl, der auf einen beliebigen Teil des Arbeitsspeichers verweist, zugeordnet zu werden. Dies ist nur ein Problem, das die Verwendung großer Speicher Belegungen in Direct3D ohne Unterstützung von unterstützten Ressourcen erschwert.

Direct3D 11 unterstützt [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) -Oberflächen mit bis zu 16384 Pixeln auf einer angegebenen Seite. Ein Bild, das 16384 breit und 4 Bytes pro Pixel ist, würde 1 GB Videospeicher beanspruchen (und das Hinzufügen 16384 von Mipmaps würde diesen Betrag verdoppeln). In der Praxis müssen in einem einzelnen Renderingvorgang nur selten auf alle 1 GB verwiesen werden.

Einige Spielentwickler modellieren die Gelände Flächen so groß wie 128 KB und 128 KB. Die Vorgehensweise zum Arbeiten mit vorhandenen GPUs besteht darin, die Oberfläche in Kacheln zu unterbrechen, die klein genug für die Verarbeitung sind. Die Anwendung muss herausfinden, welche Kacheln benötigt werden, und Sie in einen Zwischenspeicher zwischen den Texturen auf der GPU laden, einem Software-Paging-System. Ein wesentlicher Nachteil dieses Ansatzes ist, dass die Hardware nicht weiß, was das Paging betrifft: Wenn ein Teil eines Abbilds auf dem Bildschirm angezeigt werden muss, der Kacheln durchläuft, weiß die Hardware nicht, wie eine fixierte Funktion (d. h. effizient) gefiltert werden kann. Dies bedeutet, dass die Anwendung, die ihre eigene Software-tiult verwaltet, auf die manuelle Textur Filterung im Shader-Code (der sehr teuer wird, wenn ein guter qualitätsfilterter Filter erwünscht ist) und/oder das vergeuden von Speicher Erstellungs vorspielen bei Kacheln, die Daten aus benachbarten Kacheln enthalten, eine gewisse Unterstützung bieten kann.

Wenn eine gekachelte Darstellung von Oberflächen Zuordnungen eine erste Klasse im Grafiksystem darstellen könnte, könnte die Anwendung der Hardware mitteilen, welche Kacheln verfügbar gemacht werden sollen. Auf diese Weise verschwendet weniger GPU-Speicher die Speicherung von Oberflächen Bereichen, auf die die Anwendung keinen Zugriff hat, und die Hardware kann verstehen, wie Sie auf angrenzenden Kacheln filtern, um einige der Probleme zu beseitigen, die Entwickler haben, die Software-tichen selbst durchführen.

Um jedoch eine komplette Lösung bereitzustellen, müssen Sie sich mit der Tatsache befassen, dass unabhängig davon, ob die tik innerhalb einer Oberfläche unterstützt wird, die Oberfläche für die Oberfläche derzeit 16384 ist. Es ist ein Ansatz, nur die Hardware zu benötigen, um größere Textur Größen zu unterstützen. es gibt jedoch beträchtliche Kosten und/oder Kompromisse bei dieser Route. Der Textur Filter Pfad von Direct3D 11 und der Renderingpfad sind bereits in Bezug auf die Genauigkeit bei der Unterstützung von 16K-Texturen mit den anderen Anforderungen erschöpft, wie z. b. das unterstützen von Viewport-Blöcken, die während des Renderings von der Oberfläche entfernt werden, oder das Eine Möglichkeit besteht darin, einen Kompromiss so zu definieren, dass die Textur-und Genauigkeits Größe in gewisser Weise erhöht wird, wenn die Textur Größe über 16K steigt. Auch bei dieser Gewährung sind möglicherweise zusätzliche Hardwarekosten in Bezug auf die Adressierungs Fähigkeit im gesamten Hardwaresystem erforderlich, um zu größeren Textur Größen zu wechseln.

Ein Problem, das im Zusammenhang mit Texturen auftritt, liegt darin, dass die Texturkoordinaten mit einer Gleit Komma Zahl mit einfacher Genauigkeit (und die zugehörigen Interpolatoren zur Unterstützung der rasterisierung) nicht mehr präzise sind, um Orte auf der Oberfläche genau anzugeben. Die Textur Filterung von Jittery würde folgen. Eine teure Option wäre die Unterstützung von Interpolatoren mit doppelter Genauigkeit, die jedoch aufgrund einer angemessenen Alternative überschrieben werden könnte.

Ein alternativer Name für Kachel Ressourcen ist "Sparse Texture". "Sparse" vermittelt sowohl die gekachelte Natur der Ressourcen als auch den Hauptgrund dafür, dass Sie nicht alle gleichzeitig zugeordnet werden sollen. Tatsächlich könnte eine Anwendung eine Kachel Ressource erstellen, in der keine Daten für alle Regionen und MIPS der Ressource absichtlich erstellt werden. Der Inhalt selbst könnte geringer sein, und die Zuordnung des Inhalts im GPU-Speicher zu einem bestimmten Zeitpunkt wäre eine Teilmenge dieser (noch stärker geringer).

Ein weiteres Szenario, das von gekachelten Ressourcen bedient werden könnte, besteht darin, dass mehrere Ressourcen mit unterschiedlichen Dimensionen/Formaten denselben Arbeitsspeicher gemeinsam verwenden. Manchmal haben Anwendungen exklusive Ressourcen Sätze, die bekanntermaßen nicht gleichzeitig verwendet werden sollen, oder Ressourcen, die nur für eine sehr kurze Verwendung erstellt und dann zerstört wurden, gefolgt von der Erstellung anderer Ressourcen. Eine Form der Generalität, die von "gekachelten Ressourcen" abweichen kann, besteht darin, dass es möglich ist, dem Benutzer zu ermöglichen, mehrere verschiedene Ressourcen im gleichen (überlappenden) Arbeitsspeicher zu verweisen. Anders ausgedrückt: die Erstellung und Zerstörung von "Resources" (die eine Dimension/ein Format definieren usw.) kann von der Verwaltung des Arbeitsspeichers, der den Ressourcen zugrunde liegt, von der Sicht der Anwendung entkoppelt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Gekachelte Ressourcen](tiled-resources.md)
</dt> </dl>

 

 