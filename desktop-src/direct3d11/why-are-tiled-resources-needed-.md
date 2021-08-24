---
title: Warum werden gekachelte Ressourcen benötigt?
description: Gekachelte Ressourcen werden benötigt, sodass weniger GPU-Arbeitsspeicher (Graphics Processing Unit) verschwendet wird, um Bereiche von Oberflächen zu speichern, von denen die Anwendung weiß, dass nicht darauf zugegriffen wird, und die Hardware kann verstehen, wie über angrenzende Kacheln hinweg gefiltert wird.
ms.assetid: E2179D65-56D3-481F-A5F3-B9C45A11A179
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 502c2da8602cb0b2026ea8360c88388c18d37598d5672f547659cc6ea93e78e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631940"
---
# <a name="why-are-tiled-resources-needed"></a>Warum werden gekachelte Ressourcen benötigt?

Gekachelte Ressourcen werden benötigt, sodass weniger GPU-Arbeitsspeicher (Graphics Processing Unit) verschwendet wird, um Bereiche von Oberflächen zu speichern, von denen die Anwendung weiß, dass nicht darauf zugegriffen wird, und die Hardware kann verstehen, wie über angrenzende Kacheln hinweg gefiltert wird.

In einem Grafiksystem (d. h. Betriebssystem, Anzeigetreiber und Grafikhardware) ohne Unterstützung von gekachelten Ressourcen verwaltet das Grafiksystem alle Direct3D-Speicherbelegungen mit Unterressourcengranularität. Für einen [Puffer](overviews-direct3d-11-resources-buffers.md)ist der gesamte Puffer die Unterressource. Bei einer [Textur](overviews-direct3d-11-resources-textures.md) (z. B. [**Texture2D)**](/windows/desktop/direct3dhlsl/sm5-object-texture2d)ist jede Mip-Ebene eine Unterressource; für ein Texturarray (z. B. [**Texture2DArray)**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray)ist jede MIP-Ebene in einem angegebenen Arrayslice eine Unterressource. Das Grafiksystem macht nur die Möglichkeit verfügbar, die Zuordnung von Zuordnungen mit dieser Unterressourcengranularität zu verwalten. Im Kontext von gekachelten Ressourcen bezieht sich "Zuordnung" darauf, Daten für die GPU sichtbar zu machen.

Angenommen, eine Anwendung weiß, dass ein bestimmter Renderingvorgang nur auf einen kleinen Teil einer Mipmapkette des Bilds zugreifen muss (vielleicht nicht einmal auf den gesamten Bereich einer bestimmten Mipmap). Im Idealfall könnte die App das Grafiksystem über diese Notwendigkeit informieren. Das Grafiksystem würde dann nur sicherstellen, dass der benötigte Arbeitsspeicher auf der GPU zugeordnet ist, ohne zu viel Arbeitsspeicher zu pagingen. In Wirklichkeit kann das Grafiksystem ohne Unterstützung von gekachelten Ressourcen nur über den Arbeitsspeicher informiert werden, der auf der GPU mit Unterressourcengranularität zugeordnet werden muss (z. B. eine Reihe vollständiger Mipmapebenen, auf die zugegriffen werden kann). Im Grafiksystem ist auch kein Fehler erforderlich. Daher muss potenziell viel zusätzlicher GPU-Arbeitsspeicher verwendet werden, um vollständige Unterressourcen zugeordnet zu machen, bevor ein Renderingbefehl ausgeführt wird, der auf einen Teil des Arbeitsspeichers verweist. Dies ist nur ein Problem, das die Verwendung großer Speicherzuweisungen in Direct3D ohne Unterstützung von gekachelten Ressourcen erschwert.

Direct3D 11 unterstützt [**Texture2D-Oberflächen**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) mit bis zu 16384 Pixeln auf einer bestimmten Seite. Ein Bild mit einer Breite von 16384 durch eine Höhe von 16384 und 4 Bytes pro Pixel würde 1 GB Videospeicher verbrauchen (und das Hinzufügen von Mipmaps würde diese Menge verdoppelt). In der Praxis müsste nur selten auf alle 1 GB in einem einzigen Renderingvorgang verwiesen werden.

Einige Spieleentwickler modellieren Geländeoberflächen mit einer Fläche von bis zu 128.000 by 128.000. Sie können dies auf vorhandenen GPUs verwenden, um die Oberfläche in Kacheln zu unterbrechen, die klein genug für die Hardware sind. Die Anwendung muss herausfinden, welche Kacheln benötigt werden, und sie in einen Cache von Texturen auf der GPU laden – ein Software paging-System. Ein wesentlicher Nachteil dieses Ansatzes ist, dass die Hardware nichts über das Paging weiß, das vor sich geht: Wenn ein Teil eines Bilds auf dem Bildschirm angezeigt werden muss, der Kacheln umrandet, weiß die Hardware nicht, wie eine feste Funktion (d. h. effiziente) Filterung über Kacheln hinweg durchzuführen ist. Dies bedeutet, dass die Anwendung, die ihre eigenen Softwarekacheln verwalten, auf die manuelle Texturfilterung in Shadercode (die sehr aufwendig wird, wenn ein anisotroper Filter von guter Qualität gewünscht wird) und/oder Speicher für die Erstellung von Bundstechen um Kacheln verschwenden muss, die Daten von benachbarten Kacheln enthalten, damit die feste Funktionshardwarefilterung weiterhin Unterstützung bieten kann.

Wenn eine gekachelte Darstellung von Oberflächenzuordnungen ein erstklassiges Feature im Grafiksystem sein könnte, könnte die Anwendung der Hardware mitteilen, welche Kacheln verfügbar sein sollen. Auf diese Weise wird weniger GPU-Arbeitsspeicher verschwendet, um Bereiche von Oberflächen zu speichern, von denen die Anwendung weiß, dass nicht darauf zugegriffen wird, und die Hardware kann verstehen, wie über angrenzende Kacheln hinweg gefiltert werden kann, um einige der Nächsten zu vermeiden, die von Entwicklern, die Softwarekacheln selbst ausführen, auftreten.

Um jedoch eine vollständige Lösung zu bieten, muss etwas getan werden, um damit um zu umgehen, dass die maximale Oberflächendimension derzeit 16384 beträgt– unabhängig davon, ob Kacheln innerhalb einer Oberfläche unterstützt werden – nahezu die 128.000, die Anwendungen bereits wünschen. Es ist nur erforderlich, dass die Hardware größere Texturgrößen unterstützt, es gibt jedoch erhebliche Kosten und/oder Vor- und Abkniffe für diese Route. Der Texturfilterpfad und Renderingpfad von Direct3D 11 sind bereits hinsichtlich der Genauigkeit in Bezug auf die Unterstützung von 16K-Texturen mit den anderen Anforderungen übersättigt, z. B. die Unterstützung von Viewportbereichs, die während des Renderings von der Oberfläche fallen, oder die Unterstützung des Texturumbruchs vom Oberflächenrand während der Filterung. Eine Möglichkeit besteht in der Definition eines Kompromisses, bei dem die Texturgröße auf mehr als 16.000 erhöht wird und Funktionalität/Genauigkeit in irgendeiner Weise nicht mehr zur Verfügung steht. Selbst bei diesem Problem sind jedoch möglicherweise zusätzliche Hardwarekosten in Bezug auf die Adressierungsfunktion im gesamten Hardwaresystem erforderlich, um größere Texturgrößen zu verwenden.

Ein Problem, das ins Spiel kommt, wenn Texturen sehr groß werden, ist, dass Texturkoordinaten mit einzelner Genauigkeit (und die zugehörigen Interpolatoren zur Unterstützung der Rasterung) nicht mehr genau sind, um Positionen auf der Oberfläche genau anzugeben. Jittery texture filtering would be end. Eine teure Option wäre, interpolator-Unterstützung mit doppelter Genauigkeit zu erfordern. Dies könnte jedoch aufgrund einer sinnvollen Alternative zu hoch sein.

Ein alternativer Name für gekachelte Ressourcen ist "Sparsetextur". "Sparse" vermittelt sowohl die gekachelte Natur der Ressourcen als auch vielleicht den Hauptgrund für deren Kacheln– dass nicht alle ressourcen gleichzeitig zugeordnet werden sollen. Tatsächlich könnte eine Anwendung absichtlich eine gekachelte Ressource erstellen, in der keine Daten für alle Regionen und Mips der Ressource erstellen. Der Inhalt selbst könnte also nur eine spärliche Darstellung sein, und die Zuordnung des Inhalts im GPU-Arbeitsspeicher zu einem bestimmten Zeitpunkt wäre eine Teilmenge davon (noch mehr).

Ein weiteres Szenario, das von gekachelten Ressourcen bedient werden kann, ist die Möglichkeit, dass mehrere Ressourcen mit unterschiedlichen Dimensionen/Formaten denselben Arbeitsspeicher gemeinsam nutzen können. Manchmal verfügen Anwendungen über exklusive Ressourcensätze, von denen bekannt ist, dass sie nicht gleichzeitig verwendet werden, oder Ressourcen, die nur für sehr kurze Verwendung erstellt und dann zerstört werden, gefolgt von der Erstellung anderer Ressourcen. Eine Form der Allgemeinheit, die aus "gekachelten Ressourcen" fallen kann, besteht in der Möglichkeit, dem Benutzer zu erlauben, mehrere verschiedene Ressourcen auf denselben (überlappenden) Speicher zu verweisen. Anders ausgedrückt: Die Erstellung und Zerstörung von "Ressourcen" (die eine Dimension/ein Format definieren, und so weiter) kann aus Sicht der Anwendung von der Verwaltung des Speichers entkoppelt werden, der den Ressourcen zugrunde liegt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Gekachelte Ressourcen](tiled-resources.md)
</dt> </dl>

 

 