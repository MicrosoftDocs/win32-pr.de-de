---
title: Vom Benutzer zugewiesene Beispielunterstützung
description: Vom Benutzer zugewiesene Beispielunterstützung
ms.assetid: c747139e-e157-4ea0-9132-256dc70e2b15
keywords:
- Windows Medienformat-SDK, Vom Benutzer zugewiesene Beispielunterstützung
- Advanced Systems Format (ASF), Vom Benutzer zugewiesene Beispielunterstützung
- ASF (Advanced Systems Format), Vom Benutzer zugewiesene Beispielunterstützung
- Vom Benutzer zugewiesene Beispielunterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b8cba2d20586cc47845d961e5c92a0138a37d5d0db07feb23dbb68dda1b72eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845254"
---
# <a name="user-allocated-sample-support"></a>Vom Benutzer zugewiesene Beispielunterstützung

Unter normalen Umständen erstellen sowohl das Readerobjekt als auch das synchrone Readerobjekt ein neues Pufferobjekt für jedes Beispiel, das an Ihre Anwendung übermittelt wird. Dies liegt daran, dass das Leseobjekt nicht wissen kann, was Ihre Anwendung mit den Beispielen macht, nachdem es sie erhält. Obwohl viele Anwendungen Beispiele nur lesen, um sie sofort zu rendern, müssen einige Anwendungen die Stichproben möglicherweise über einen längeren Zeitraum warten. Das Leseobjekt kann daher keinen der Puffer wiederverwenden, die es zuordnet. sie werden an Ihre Anwendung übermittelt, die dann die Kontrolle über sie hat.

Das Problem bei diesem Ansatz besteht darin, dass eine Datei eine große Anzahl von Stichproben enthalten kann. Wenn für jede dieser Objekte ein neues Pufferobjekt erstellt werden muss, wird viel Prozessorzeit mit der Zuweisung und Freigabe von Arbeitsspeicher verschwendet. In zeitkritischen Anwendungen wie Media Playern kann dieser Mehraufwand die Leistung beeinträchtigen.

Um leistungsbezogene Probleme bei vom Reader zugeordneten Stichproben zu beheben, unterstützen sowohl der Reader als auch der synchrone Reader benutzerseitig zugeordnete Beispiele. Um von Ihrer Anwendung zugeordnete Beispiele zu verwenden, ruft das Leseobjekt eine von Ihnen implementierte Rückrufmethode für die Stichprobenzuordnung auf. Die Logik, die vom Rückruf zum Übermitteln von Puffern an das Leseobjekt verwendet wird, liegt vollständig bei Ihnen. Sie können einen Pool von Puffern für die gesamte Datei oder mehrere Pufferpools verwenden, einen für jede Ausgabe oder jeden Stream oder ein anderes Schema, das für Ihre Anwendung funktioniert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Zuordnen von Puffern zum Lesen von Dateien**](allocating-buffers-for-file-reading.md)
</dt> <dt>

[**Funktionen zum Lesen von Dateien**](file-reading-features.md)
</dt> </dl>

 

 




