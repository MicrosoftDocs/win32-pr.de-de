---
description: In Visual Basic geschriebene debuggingkomponenten
ms.assetid: 2b00ed29-8b48-4a54-83e8-d5e69e5f883e
title: In Visual Basic geschriebene debuggingkomponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 085dd1d6f45cc7f6665851b232402ecee01c069f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344626"
---
# <a name="debugging-components-written-in-visual-basic"></a>In Visual Basic geschriebene debuggingkomponenten

In bestimmten Szenarien können Sie die Entwicklungsumgebung von Microsoft Visual Basic 6,0 zum Debuggen verwenden. Die Verwendung von Visual Basic für das Debugging ermöglicht den Zugriff auf Tools, die Visual Basic Programmierern vertraut sind Da hingegen während des Debuggens Visual Basic Komponenten innerhalb des Prozesses der Visual Basic Umgebung ausgeführt werden, kann es erforderlich sein, die Komponente zu debuggen, nachdem Sie mithilfe der Microsoft Visual C++ Entwicklungsumgebung kompiliert wurde.

Weitere Informationen zum Debuggen in der Visual Basic integrierten Entwicklungsumgebung (Integrated Development Environment, IDE) finden Sie unter [Debuggen in der Visual Basic IDE](debugging-in-the-visual-basic-ide.md). Weitere Informationen zum Debuggen Visual Basic Komponenten, nachdem diese mithilfe der Visual C++ Entwicklungsumgebung kompiliert wurden, finden Sie unter [Debuggen von kompilierten Visual Basic Komponenten](debugging-compiled-visual-basic-components.md)

Außerdem wurden verschiedene Einschränkungen im Zusammenhang mit der Verwendung der Visual Basic Umgebung zum Debuggen von Komponenten mit MTS für com+ aufgelöst. Weitere Informationen finden Sie [unter com+-Visual Basic Debuggingunterstützung gegen MTS](com--visual-basic-debugging-support-contrasted-with-mts.md).

> [!Note]  
> Wenn Sie Visual Basic bereits auf demselben Computer wie com+ verwendet haben, haben Sie möglicherweise bemerkt, dass das Add-in für Komponenten Dienste in der Visual Basic-Umgebung verfügbar ist. Diese Funktion wurde ursprünglich in MTS entworfen, um die Registrierung jedes Mal zu aktualisieren, wenn Sie eine Komponente in einer COM+-Anwendung neu kompiliert haben. Aufgrund der Art der Interaktion der Microsoft Windows-Registrierung und der COM+-Registrierungsdatenbank werden einige Einstellungen jedoch möglicherweise nicht vollständig aktualisiert. Anstatt die Befehle zu verwenden, die mit diesem Add-in verfügbar sind, sollten Sie daher die Komponenten entfernen und neu installieren, um die Einstellungen nach der erneuten Kompilierung zu aktualisieren.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[In Visual C++ geschriebene debuggingkomponenten](debugging-components-written-in-visual-c--.md)
</dt> </dl>

 

 



