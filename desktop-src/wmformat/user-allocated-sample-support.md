---
title: Vom Benutzer zugewiesene Beispiel Unterstützung
description: Vom Benutzer zugewiesene Beispiel Unterstützung
ms.assetid: c747139e-e157-4ea0-9132-256dc70e2b15
keywords:
- Windows Media-Format-SDK, vom Benutzer zugewiesene Beispiel Unterstützung
- Advanced Systems Format (ASF), vom Benutzer zugeordnete Beispiel Unterstützung
- ASF (Advanced Systems Format), vom Benutzer zugeordnete Beispiel Unterstützung
- vom Benutzer zugewiesene Beispiel Unterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80d6a0d9a7e19b46940093fc370bd2c8c70590d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036721"
---
# <a name="user-allocated-sample-support"></a>Vom Benutzer zugewiesene Beispiel Unterstützung

Unter normalen Umständen erstellen sowohl das Reader-Objekt als auch das synchrone Reader-Objekt ein neues Buffer-Objekt für jedes Beispiel, das an die Anwendung übermittelt wird. Dies liegt daran, dass das Lese Objekt nicht weiß, wie Ihre Anwendung die Beispiele durchführt, nachdem Sie sie abgerufen haben. Obwohl viele Anwendungen nur Beispiele lesen, um Sie sofort zu Rendering, müssen einige Anwendungen möglicherweise lange Zeit Beispiele verwalten. Das Lese Objekt kann daher keinen der von ihm zugewiesenen Puffer wieder verwenden. Sie werden an Ihre Anwendung übermittelt, die dann die Kontrolle darüber hat.

Das Problem bei diesem Ansatz besteht darin, dass eine Datei eine immense Anzahl von Stichproben enthalten kann. Wenn für jedes von Ihnen ein neues Puffer Objekt erstellt werden muss, wird die Zuordnung und Freigabe von Arbeitsspeicher viel Prozessorzeit verschwendet. Bei zeitsensiblen Anwendungen, wie z. b. Media Players, kann sich dieser Aufwand stark auf die Leistung auswirken.

Um die Leistungsprobleme der von Lesern zugewiesenen Beispiele zu verringern, unterstützen sowohl der Reader als auch der synchrone Reader vom Benutzer zugeordnete Beispiele. Um die von der Anwendung zugeordneten Beispiele verwenden zu können, führt das Lese Objekt Aufrufe an eine von Ihnen implementierte Beispiel-Zuweisungs Rückruf Methode aus. Die Logik, die vom Rückruf verwendet wird, um Puffer an das Lese Objekt zu übermitteln, ist vollständig. Sie können einen Pufferpool für die gesamte Datei verwenden oder mehrere Pufferpools verwenden, einen für jede Ausgabe oder einen Stream bzw. ein beliebiges anderes Schema, das für Ihre Anwendung geeignet ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Puffer für Datei Lesevorgänge werden zugewiesen.**](allocating-buffers-for-file-reading.md)
</dt> <dt>

[**Funktionen zum Lesen von Dateien**](file-reading-features.md)
</dt> </dl>

 

 




