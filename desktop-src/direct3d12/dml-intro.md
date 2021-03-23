---
title: Introduction to DirectML (Einführung in DirectML)
description: Direct Machine Learning (directml) ist eine API auf niedriger Ebene für Machine Learning (ml).
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: 2dd37bc4c27364e26e4bbd4ae2cf5d43031c3314
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103979"
---
# <a name="introduction-to-directml"></a>Introduction to DirectML (Einführung in DirectML)

## <a name="summary"></a>Zusammenfassung

Direct Machine Learning (directml) ist eine API auf niedriger Ebene für Machine Learning (ml). Hardware beschleunigter Machine Learning-primitiv (als Operatoren bezeichnet) sind die Bausteine der directml. Von diesen Bausteinen aus können Sie solche Machine Learning-Techniken wie das hochskalieren, das Antialiasing und die Übertragung von Schriftformen entwickeln, um den Namen zu benennen. Durch die Kennzeichnung und die superauflösung können Sie beispielsweise beeindruckende Raytracing-Effekte mit weniger Strahlen pro Pixel erzielen.

Sie können Machine Learning-Rückschlussworkloads in Ihr Spiel, Ihre Engine, Ihre Middleware, Ihr Back-End oder in eine andere Anwendung integrieren. Directml verfügt über eine vertraute (native C++, Nano-com) DirectX 12-Programmierschnittstelle und einen Workflow und wird von allen mit DirectX 12 kompatiblen Hardware unterstützt. Directml-Beispielanwendungen, einschließlich eines Beispiels einer minimalen directml-Anwendung, finden Sie unter [directml-Beispielanwendungen](dml-min-app.md).

Directml wird in Windows 10, Version 1903, und in der entsprechenden Version des Windows SDK eingeführt.

## <a name="is-directml-appropriate-for-my-project"></a>Ist die directml für mein Projekt geeignet?

Directml ist eine Komponente unter der [Windows Machine Learning](/windows/ai) -Ober Schirm. Die winml-API auf höherer Ebene ist hauptsächlich Modell orientiert, mit dem Workflow für die Last Bindung und-Auswertung. Domänen, wie Spiele und Engines, benötigen jedoch in der Regel eine niedrigere Abstraktions Ebene und ein höheres Maß an Entwickler Kontrolle, um das gesamte Silicon zu nutzen. Wenn Sie Millisekunden zählen und Frame Zeiten drücken, erfüllt directml ihre Machine Learning-Anforderungen.

Verwenden Sie die directml (anstelle von winml), um zuverlässige Echt Zeit-, Hochleistungs-und/oder Ressourcen eingeschränkte Szenarien zu verwenden. Sie können directml direkt in Ihre vorhandene Engine oder Renderingpipeline integrieren. Oder auf einer höheren Ebene für benutzerdefinierte Machine Learning-Frameworks und Middleware kann directml ein leistungsfähiges Back-End unter Windows bereitstellen.

Winml wird selbst mithilfe von directml als eine seiner Back-Ends implementiert.

## <a name="what-work-does-directml-do-and-what-work-must-i-do-as-the-developer"></a>Funktionsweise von directml und welche Arbeit muss *ich* als Entwickler tun?

Die directml führt effizient die einzelnen Ebenen Ihres Rückschluss Modells auf der GPU (oder auf Ki-Beschleunigung-Kernen, falls vorhanden) aus. Jede Ebene ist ein Operator, und directml stellt eine Bibliothek mit Hardware beschleunigten Machine Learning-Operatoren auf niedriger Ebene bereit. Diese Operatoren verfügen über Hardware spezifische und architekturspezifische Optimierungen, die für Sie entwickelt wurden (Weitere Informationen dazu finden Sie im Abschnitt [Warum ist directml so gut?](#why-does-directml-perform-so-well)). Gleichzeitig sehen Sie als Entwickler eine einzelne, herstellerunabhängige Schnittstelle zum Ausführen dieser Operatoren.

Die Bibliothek der Operatoren in directml stellt alle üblichen Vorgänge bereit, die Sie in einer Machine Learning-Arbeitsauslastung verwenden können.

- Aktivierungs Operatoren, wie z. b. **linear**, **relu**, **sigmuid**, **tanh** und mehr.
- Element Weise Operatoren, wie z. b. **Add**, **Exp**, **Log**, **Max**, **Min**, **Sub** und viele mehr.
- Operatoren für die Zusammenstellung, z. b. 2D und **3D-** Zusammenstellung, usw.
- Reduzierungs Operatoren, z. b. **argmin**, **Average**, **L2**, **Sum** usw.
- Pooling-Operatoren wie " **Average**", " **LP**" und " **Max**".
- NN-Operatoren (neuronale Netzwerk), wie z. b. **GEMM**, **GRU**, **LSTM** und **RNN**.
- Und vieles mehr.

Um die maximale Leistung zu erzielen, und Sie nicht für das bezahlen, was Sie nicht verwenden, stellt directml das Steuerelement als Entwickler vor, wie Ihre Machine Learning-Arbeitsauslastung auf der Hardware ausgeführt wird. Herauszufinden, welche Operatoren ausgeführt werden müssen, und wann ist die Verantwortung für den Entwickler. Zu den Aufgaben, die zu ihrer Diskretion gehören, gehören: Umschreiben des Modells; vereinfachen und Optimieren von Ebenen Gewichtungen werden geladen. Ressourcen Zuordnung, Bindung, Speicherverwaltung (genau wie bei Direct3D 12); und die Ausführung des Diagramms.

Sie behalten allgemeine Kenntnisse der Diagramme (Sie können Ihr Modell direkt codieren, oder Sie können Ihr eigenes Modell Lader schreiben). Sie können z. b. ein upskalierungsmodell entwerfen, indem Sie mehrere Ebenen für die **Upsample** **-,** **zunormalisierungs-, normalisierungs**-und **Aktivierungs** Operatoren verwenden. Mit dieser Vertrautheit, sorgfältigen Planung und Barriere-Verwaltung können Sie die meisten Parallelität und Leistung von der Hardware extrahieren. Wenn Sie ein Spiel entwickeln, können Sie mit der sorgfältigen Ressourcenverwaltung und der Steuerung der Zeitplanung die Machine Learning-Workloads und die herkömmliche renderingarbeit überspringen, um die GPU zu entladen.

## <a name="whats-the-high-level-directml-workflow"></a>Was ist der allgemeine directml-Workflow?

Hier ist das allgemeine Rezept für die Verwendung von directml. Innerhalb der beiden Hauptphasen der Initialisierung und Ausführung zeichnen Sie die Arbeit in Befehlslisten auf und führen Sie dann in einer Warteschlange aus.

### <a name="initialization"></a>Initialisierung

1. Erstellen Sie Ihre Direct3D 12-Ressourcen mit &mdash; dem Direct3D 12-Gerät, der Befehls Warteschlange, der Befehlsliste und Ressourcen wie deskriptorheaps.
2. Da Sie Machine Learning-Rückschlüsse und ihre renderingworkloads durchführen, erstellen Sie directml-Ressourcen mit &mdash; dem directml-Gerät und Operator Instanzen. Wenn Sie über ein Machine Learning-Modell verfügen, in dem Sie einen bestimmten Kontotyp mit einer bestimmten Größe von Filter tensorflow mit einem bestimmten Datentyp ausführen müssen, sind dies alle Parameter für den **Konvolution** -Operator von directml.
3. Directml-Datensätze funktionieren in Direct3D 12-Befehlslisten. Sobald die Initialisierung abgeschlossen ist, notieren Sie die Bindung und Initialisierung von (z. b.) ihren Operator "Operator" in der Befehlsliste. Schließen Sie anschließend die Befehlsliste in Ihrer Warteschlange, und führen Sie Sie wie gewohnt aus.

### <a name="execution"></a>Ausführung

1. Laden Sie Ihre Gewichtungs-Tensoren in Ressourcen hoch. Ein tensorflow in directml wird mithilfe einer regulären Direct3D 12-Ressource dargestellt. Wenn Sie z. b. Ihre Gewichtungsdaten auf die GPU hochladen möchten, führen Sie dies genauso wie bei jeder anderen Direct3D 12-Ressource aus (verwenden Sie einen uploadheap oder die Kopier Warteschlange).
2. Als nächstes müssen Sie diese Direct3D 12-Ressourcen als Eingabe-und Ausgabe Tensoren binden. Notieren Sie die Bindung und die Ausführung der Operatoren in der Befehlsliste.
3. Schließen Sie die Befehlsliste, und führen Sie Sie aus.

Ebenso wie bei Direct3D 12 liegen die Ressourcen Lebensdauer und die Synchronisierung in ihrer Verantwortung. Geben Sie Ihre directml-Objekte z. b. nicht mindestens so lange frei, bis die Ausführung auf der GPU abgeschlossen ist.

## <a name="why-does-directml-perform-so-well"></a>Warum funktioniert directml auch?

Es gibt einen guten Grund, warum Sie nicht einfach Ihren eigenen Konvolution-Operator (z. b.) als HLSL in einem [Compute-Shader](/windows/desktop/direct3d12/pipelines-and-shaders-with-directx-12#direct3d-12-compute-pipeline)schreiben sollten. Der Vorteil der Verwendung von directml besteht darin, dass Sie &mdash; nicht nur den Aufwand für das Heim Betrieb Ihrer eigenen Lösung, &mdash; sondern auch eine viel bessere Leistung bieten, als Sie mit einem handgeschriebenen, allgemeinen Compute-Shader für etwas wie " **Konvolution**" oder " **LSTM**" erreichen können.

Directml erreicht dies teilweise aufgrund der Funktion Direct3D 12 Metacommands. Metacommands machen eine Blackbox-Funktionalität bis zur directml verfügbar, die es Hardwareanbietern ermöglicht, directml-Zugriff auf Hardware spezifische und architekturspezifische Optimierungen des Herstellers bereitzustellen. Beispielsweise können mehrere Operatoren &mdash; , gefolgt von der Aktivierung, &mdash; zu einem einzigen Metacommand *verschmolzen* werden. Aufgrund dieser Faktoren bietet directml die Möglichkeit, die Leistung von sogar einem sehr gut geschriebenen, Hand optimierten Compute-Shader zu überschreiten, der für die Ausführung auf einer Vielzahl von Hardware geschrieben wurde.

Metacommands sind Teil der Direct3D 12-API, auch wenn Sie lose verknüpft sind. Ein Metacommand wird durch eine feste [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid)gekennzeichnet, während fast alle anderen Informationen (von seinem Verhalten und der Semantik bis zur Signatur und dem Namen) nicht unbedingt Teil der Direct3D 12-API sind. Stattdessen wird ein Metacommand zwischen seinem Autor und dem Treiber angegeben, der ihn implementiert. In diesem Fall ist der Autor directml. Metacommands sind Direct3D 12 primitive (wie z. b. Ziehungen und Verteiler), sodass Sie in einer Befehlsliste aufgezeichnet werden können und für die Ausführung geplant werden.

Directml beschleunigt Ihre Machine Learning-Workloads mit einer gesamten Suite von Machine Learning-Metacommands. Folglich müssen Sie keine herstellerspezifischen Codepfade schreiben, um eine Hardwarebeschleunigung für Ihre Rückschlüsse zu erzielen. Wenn Sie die Ausführung auf einem AI-beschleunigten Chip ausführen, wird diese Hardware von directml verwendet, um Vorgänge wie z. b. die Zusammenführung erheblich zu beschleunigen. Sie können denselben Code verwenden, den Sie geschrieben haben, ohne ihn zu ändern, indem Sie ihn auf einem Chip ausführen, der nicht Ki-beschleunigt ist (vielleicht die integrierte GPU in Ihrem Laptop), und dennoch eine gute GPU-Hardwarebeschleunigung erzielen. Wenn keine GPU verfügbar ist, greift directml auf die CPU zurück.
