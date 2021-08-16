---
description: Sie können einer XAPO Laufzeitparameterunterstützung hinzufügen, indem Sie die IXAPOParameters-Schnittstelle implementieren. Die Unterstützung von Laufzeitparametern ermöglicht es einem XAPO, sein Verhalten basierend auf den Parametern zu ändern, die zur Laufzeit an ihn übergeben werden.
ms.assetid: 13f974ec-fcf5-1749-e69d-88de79b7d82b
title: "So wird's gemacht: Hinzufügen der Laufzeitparameterunterstützung zu einem XAPO"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbf69fcc2570e26f188766a7f908a76d0dfcf3ec190d9fd0d7a1c434b242fdf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805540"
---
# <a name="how-to-add-run-time-parameter-support-to-an-xapo"></a>So wird's gemacht: Hinzufügen der Laufzeitparameterunterstützung zu einem XAPO

Sie können einer XAPO Laufzeitparameterunterstützung hinzufügen, indem Sie die [**IXAPOParameters-Schnittstelle**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) implementieren. Die Unterstützung von Laufzeitparametern ermöglicht es einem XAPO, sein Verhalten basierend auf den Parametern zu ändern, die zur Laufzeit an ihn übergeben werden.

1.  Führen Sie die Schritte unter [Vorgehensweise: Erstellen einer XAPO](how-to--create-an-xapo.md)aus.
2.  Ändern Sie die XAPO so, dass sie von [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) und [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase)abgeleitet wird.
3.  Fügen Sie der Implementierung von [**IXAPO::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process)Aufrufe der Methoden [**CXAPOParametersBase::BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) und [**CXAPOParametersBase::EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) hinzu.

    > [!Note]  
    > Durch Das Hinzufügen dieser Methoden zu [IXAPO::P rocess](how-to--build-a-basic-audio-processing-graph.md) kann [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) die Kopien der Effektparameter in einem threadsicheren Zustand speichern. Rufen Sie [**CXAPOParametersBase::BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) am Anfang von [**IXAPO::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process)und [**CXAPOParametersBase::EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) am Ende von **IXAPO::P rocess** auf.

     

4.  Fügen Sie der [**IXAPO::P rocess-Implementierung**](/windows/win32/api/xapo/nf-xapo-ixapo-process) weiteren Code hinzu, um das Verhalten entsprechend den von der [**SetParameters-Methode gespeicherten**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) Werten zu ändern.

    > [!Note]  
    > Das Hinzufügen von Code zur [**IXAPO::P rocess-Methode**](/windows/win32/api/xapo/nf-xapo-ixapo-process) zur Verwendung der von [**SetParameters angegebenen**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) Parameter ermöglicht es, das Verhalten des XAPO während seiner gesamten Lebensdauer zu ändern.

     

5.  Wenn Sie eine Instanz des Effekts erstellen, ordnen Sie einen Puffer von drei der Strukturen zu, die die Parameter des Effekts darstellen, und übergeben Sie ihn an den [**CXAPOParametersBase-Konstruktor.**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase)

    > [!Note]  
    > Die [**CXAPOParametersBase-Instanz**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) verwendet diesen Puffer intern zum Verwalten von Effektparametern, die beim Aufrufen von [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters)übergeben werden. Sie müssen alle Prozessparameterblöcke in *pParameterBlocks* mit demselben Standardwert initialisieren, bevor Sie eine der [**Methoden IXAPO::P rocess,**](/windows/win32/api/xapo/nf-xapo-ixapo-process) [**IXAPOParameters::GetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-getparameters)und **IXAPOParameters::SetParameters** aufrufen. Normalerweise wird diese Initialisierung in [**IXAPO::Initialize**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) oder in [**IXAPO::LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess)verarbeitet.

     

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audioeffekte](audio-effects.md)
</dt> <dt>

[Übersicht über XAPO](xapo-overview.md)
</dt> </dl>

 

 
