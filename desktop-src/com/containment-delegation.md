---
title: Einschluss/Delegierung
description: Der häufigste Mechanismus für die Wiederverwendung von Objekten in com ist die Kapselung/Delegierung.
ms.assetid: 56396c11-889a-4f28-8fa7-9e48c805c501
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d26e0c1d1e48596cb9acef740405c797f6f0f46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311297"
---
# <a name="containmentdelegation"></a>Einschluss/Delegierung

Der häufigste Mechanismus für die Wiederverwendung von Objekten in com ist die Kapselung */Delegierung*. Diese Art der Wiederverwendung ist ein bekanntes Konzept, das in den meisten objektorientierten Sprachen und Systemen enthalten ist. Das äußere Objekt, das das innere Objekt verwenden muss, fungiert als Objekt Client für das innere Objekt. Das äußere Objekt "enthält" das innere Objekt, und wenn das äußere Objekt die Dienste des inneren Objekts erfordert, delegiert das äußere Objekt die Implementierung explizit an die Methoden des inneren Objekts. Das heißt, das äußere Objekt verwendet die Dienste des inneren Objekts, um sich selbst zu implementieren.

Es ist nicht erforderlich, dass die äußeren und inneren Objekte die gleichen Schnittstellen unterstützen, obwohl es sicherlich sinnvoll ist, ein Objekt zu enthalten, das eine Schnittstelle implementiert, die das äußere Objekt nicht implementiert, und die Methoden des äußeren Objekts einfach als Aufrufe der entsprechenden Methoden im inneren Objekt implementiert. Wenn die Komplexität der äußeren und inneren Objekte stark abweicht, kann das äußere Objekt jedoch einige der Methoden der Schnittstellen implementieren, indem Aufrufe an Schnittstellen Methoden delegiert werden, die im inneren Objekt implementiert werden.

Es ist einfach, die Kapselung für ein äußeres Objekt zu implementieren. Das äußere Objekt erstellt die inneren Objekte, die es für jeden anderen Client verwenden muss. Das ist nichts neues – der Prozess ähnelt einem C++-Objekt, das ein C++-Zeichen folgen Objekt enthält, das für die Ausführung bestimmter Zeichen folgen Funktionen verwendet wird. Dies gilt auch, wenn das äußere Objekt nicht als eigenes Zeichen folgen Objekt betrachtet wird. Wenn Sie dann den Zeiger auf das innere Objekt verwenden, generiert ein aufrufungs Methode im äußeren Objekt einen aufzurufenden inneren Objektmethode.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aggregation](aggregation.md)
</dt> </dl>

 

 




