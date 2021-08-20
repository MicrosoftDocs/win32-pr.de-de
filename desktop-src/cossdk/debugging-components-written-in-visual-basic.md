---
description: Debuggen von in Visual Basic geschriebenen Komponenten
ms.assetid: 2b00ed29-8b48-4a54-83e8-d5e69e5f883e
title: Debuggen von in Visual Basic geschriebenen Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff0dc8e4d98a41f0059de8e3eb44deeb9dcd8e4fbfdc6dba0510bd227a189c40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991180"
---
# <a name="debugging-components-written-in-visual-basic"></a>Debuggen von in Visual Basic geschriebenen Komponenten

Sie können die Microsoft Visual Basic 6.0-Entwicklungsumgebung für das Debuggen in bestimmten Szenarien verwenden. Die Verwendung von Visual Basic zum Debuggen ermöglicht den Zugriff auf Tools, die Visual Basic Programmierern vertraut sind. Andererseits kann es erforderlich sein, während des Debuggens Visual Basic Komponenten innerhalb des Prozesses der Visual Basic Umgebung ausgeführt werden, die Komponente zu debuggen, nachdem sie mithilfe der Microsoft Visual C++ Entwicklungsumgebung kompiliert wurde.

Weitere Informationen zum Debuggen innerhalb der Visual Basic integrierten Entwicklungsumgebung (Integrated Development Environment, IDE) finden Sie unter [Debuggen in der Visual Basic IDE.](debugging-in-the-visual-basic-ide.md) Weitere Informationen zum Debuggen Visual Basic Komponenten nach der Kompilierung mithilfe der Visual C++ Entwicklungsumgebung finden Sie unter [Debuggen kompilierter Visual Basic Komponenten.](debugging-compiled-visual-basic-components.md)

Darüber hinaus wurden mehrere Einschränkungen im Zusammenhang mit der Verwendung der Visual Basic-Umgebung zum Debuggen von Komponenten mit MTS für COM+ behoben. Weitere Informationen finden Sie unter [COM+ Visual Basic Debugunterstützung im Vergleich zu MTS.](com--visual-basic-debugging-support-contrasted-with-mts.md)

> [!Note]  
> Wenn Sie bereits Visual Basic auf demselben Computer wie COM+ verwendet haben, haben Sie möglicherweise bemerkt, dass das Komponentendienste-Add-In in der Visual Basic-Umgebung verfügbar ist. Ursprünglich in MTS wurde dieses Feature entwickelt, um die Registrierung jedes Mal zu aktualisieren, wenn Sie eine Komponente in einer COM+-Anwendung neu kompiliert haben. Angesichts der Art der Interaktion von Microsoft Windows Registry und der COM+-Registrierungsdatenbank werden einige Einstellungen möglicherweise nicht vollständig aktualisiert. Anstatt die mit diesem Add-In verfügbaren Befehle zu verwenden, sollten Sie daher die Komponenten entfernen und neu installieren, um die Einstellungen nach der Neukompilierung zu aktualisieren.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Debuggen von in Visual C++ geschriebenen Komponenten](debugging-components-written-in-visual-c--.md)
</dt> </dl>

 

 



