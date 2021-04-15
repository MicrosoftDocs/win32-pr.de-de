---
description: Sie können die Unterstützung von Lauf Zeitparametern zu einem xapo hinzufügen, indem Sie die ixapoparameters-Schnittstelle implementieren. Durch die Unterstützung von Lauf Zeitparametern kann ein xapo sein Verhalten basierend auf den Parametern ändern, die ihm zur Laufzeit übergeben werden.
ms.assetid: 13f974ec-fcf5-1749-e69d-88de79b7d82b
title: "So wird's gemacht: Hinzufügen der Laufzeitparameterunterstützung zu einem XAPO"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 582f51b3dfbdc6d31422494906d5f945f77ccb03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485179"
---
# <a name="how-to-add-run-time-parameter-support-to-an-xapo"></a>So wird's gemacht: Hinzufügen der Laufzeitparameterunterstützung zu einem XAPO

Sie können die Unterstützung von Lauf Zeitparametern zu einem xapo hinzufügen, indem Sie die [**ixapoparameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) -Schnittstelle implementieren. Durch die Unterstützung von Lauf Zeitparametern kann ein xapo sein Verhalten basierend auf den Parametern ändern, die ihm zur Laufzeit übergeben werden.

1.  Führen Sie die Schritte unter Gewusst [wie: Erstellen eines xapo](how-to--create-an-xapo.md)aus.
2.  Ändern Sie den xapo-Wert, um von [**cxapoparametersbase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) und [**cxapobase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase)abgeleitet zu werden.
3.  Fügen Sie den-Methoden [**cxapoparametersbase:: beginprocess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) und [**cxapoparametersbase:: endprocess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) Aufrufe der-Implementierung von [**ixapo::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process)hinzu.

    > [!Note]  
    > Das Hinzufügen dieser Methoden zu [ixapo::P rocess](how-to--build-a-basic-audio-processing-graph.md) ermöglicht [**cxapoparametersbase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) , seine Kopien der Effektparameter in einem Thread sicheren Zustand zu belassen. Aufrufen von [**cxapoparametersbase:: beginprocess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) am Anfang von [**ixapo::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process)und [**cxapoparametersbase:: endprocess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) am Ende von **ixapo::P rocess**.

     

4.  Fügen Sie der [**ixapo::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) -Implementierung weiteren Code hinzu, um das Verhalten entsprechend den Werten zu ändern, die von der [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) -Methode gespeichert werden.

    > [!Note]  
    > Wenn Sie der [**ixapo::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) -Methode Code hinzufügen, um die von [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) angegebenen Parameter zu verwenden, kann das xapo-Verhalten während des gesamten Lebenszyklus geändert werden.

     

5.  Wenn Sie eine Instanz des Effekts erstellen, weisen Sie einen Puffer mit drei der Strukturen zu, die die Parameter des Effekts darstellen, und übergeben Sie ihn an den [**cxapoparametersbase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) -Konstruktor.

    > [!Note]  
    > Die [**cxapoparametersbase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) -Instanz verwendet diesen Puffer intern zum Verwalten von Effekt Parametern, die an Sie übergeben werden, wenn [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters)aufgerufen wird. Sie müssen alle Prozessparameter Blöcke in *pparameterblocks* auf denselben Standardwert initialisieren, bevor Sie eine der Methoden [**ixapo::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process), [**ixapoparameters:: GetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-getparameters)und **ixapoparameters:: SetParameters** aufrufen. Normalerweise wird diese Initialisierung in [**ixapo:: Initialize**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) oder [**ixapo:: lockforprocess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess)behandelt.

     

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audioeffekte](audio-effects.md)
</dt> <dt>

[Übersicht über xapo](xapo-overview.md)
</dt> </dl>

 

 
