---
title: Übersicht über Direct2D-Debugebenen
description: Übersicht über Direct2D-Debugebenen
ms.assetid: 7c28e00b-ebb9-4b79-939c-64eade1351ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ad960c50cd125ec8c335d836949457bb05ef65aba4b2edaff1dfbbd3a9cf6d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087770"
---
# <a name="direct2d-debug-layer-overview"></a>Übersicht über Direct2D-Debugebenen

Die Direct2D-Debugebene stellt Debugmeldungen zur Entwurfszeit bereit, mit deren Hilfe Sie Laufzeitanwendungsfehler minimieren können. In dieser Übersicht werden die Grundlagen der Direct2D-Debugebene beschrieben. Es wird davon ausgegangen, dass Sie mit der Erstellung grundlegender Direct2D-Anwendungen vertraut sind.

Diese Übersicht enthält die folgenden Abschnitte.

-   [Was ist die Direct2D-Debugebene?](#what-is-the-direct2d-debug-layer)
-   [Installieren der Direct2D-Debugebene](#installing-the-direct2d-debug-layer)
-   [Aktivieren der Debugebene](#enabling-the-debug-layer)
-   [Debugebenen](#debug-levels)
-   [Zugehörige Themen](#related-topics)

## <a name="what-is-the-direct2d-debug-layer"></a>Was ist die Direct2D-Debugebene?

Die Direct2D-Debugebene, die separat von Direct2D in einer eigenen DLL namens d2d1debug.dll implementiert wird, stellt Debugmeldungen bereit, damit Sie Direct2D-Funktionen genau verwenden können. Die Debugmeldungen resultieren häufig aus API-Vertragsverletzungen wie ungültigen Parametern (kann direct3D-bezogen sein), ungültigen Ressourcen, Threadingverletzungen und Leistungsproblemen wie der Verwendung einer Ebene, wenn ein Clip ausreichen würde. Um anzugeben, wie viele Informationen von der Debugebene nachverfolgt werden, können Sie eine der drei Debugebenen angeben: Information, Warnung und Fehler. und eine Meldung des Ebenenfehlers löst den Haltepunkt aus, um Sie beim Debuggen zu unterstützen.

## <a name="installing-the-direct2d-debug-layer"></a>Installieren der Direct2D-Debugebene

Anweisungen zum Installieren der Debugebene finden Sie unter [Installieren der Direct2D-Debugebene.](installing-the-direct2d-debug-layer.md)

## <a name="enabling-the-debug-layer"></a>Aktivieren der Debugebene

Um die Debugebene in Ihrer Anwendung zu aktivieren, geben Sie einen anderen [**D2D1 \_ DEBUG \_ LEVEL-Wert**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) als **D2D1 \_ DEBUG LEVEL \_ \_ NONE** an, wenn Sie eine Factory mit der [**D2D1CreateFactory-Funktion**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) erstellen.

> [!Note]  
> Wenn die Direct2D-Debugebene aktiviert ist, kann der Direct2D-Farbverwaltungseffekt (CLSID \_ D2D1ColorManagement) beim Festlegen eines Farbkontexts eine Zugriffsverletzung verursachen. Die Problemumgehung besteht darin, die Debugebene bei Verwendung des Farbverwaltungseffekts zu deaktivieren.

 

Das Aktivieren der Debugebene für eine Factory ermöglicht auch das Debuggen von Informationen für jedes objekt, das von dieser Factory erstellt wird.

Im folgenden Beispiel wird die Debugebene für eine Factory aktiviert, wenn die Anwendung für die DEBUG-Buildkonfiguration kompiliert wird.


```C++
        // If you set the options.debugLevel to D2D1_DEBUG_LEVEL_NONE,
        // the debug layer is not enabled.
#if defined(DEBUG) || defined(_DEBUG)
        D2D1_FACTORY_OPTIONS options;
        options.debugLevel = D2D1_DEBUG_LEVEL_INFORMATION;

        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            options,
            &m_pD2DFactory
            );
#else
        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            &m_pD2DFactory
            );
#endif
```



> [!Note]  
> Wenn keine Factoryoptionen angegeben oder die Debugebene "none" angegeben ist, wird die Debugebene nicht aufgerufen. Die Debugebene sollte in der Releaseversion einer Anwendung nie aktiv sein.

 

Im nächsten Abschnitt werden die verschiedenen Debugebenen beschrieben, die durch die [**D2D1 \_ DEBUG \_ LEVEL-Enumeration**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) definiert werden.

## <a name="debug-levels"></a>Debugebenen

Die [**D2D1 \_ DEBUG \_ LEVEL-Enumeration**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) gibt drei Debugebenen an: D2D1 \_ DEBUG LEVEL ERROR \_ \_ (Fehler), D2D1 \_ DEBUG LEVEL WARNING \_ \_ (Warnung) und D2D1 \_ DEBUG LEVEL INFORMATION \_ \_ (Information). Diese Ebenen werden wie folgt interpretiert:

-   **Fehler:** Direct2D sendet schwerwiegende Fehlermeldungen an die Debugebene. Wenn Sie z. B. eine Threadingeinschränkung aufbrechen, wird ein schwerwiegender Fehler generiert.

-   **Warnung:** Direct2D sendet Fehlermeldungen und Warnungen an die Debugebene, damit Sie diese Meldungen beheben können.

-   **Informationen:** Direct2D sendet Fehlermeldungen, Warnungen und zusätzliche Diagnoseinformationen an die Debugebene. Beispielsweise werden Meldungen zur Leistungsverbesserung auf dieser Debugebene gesendet.

Der Wert D2D1 \_ DEBUG \_ LEVEL NONE \_ (none) gibt an, dass Direct2D keine Debugausgabe bereitstellt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Debugmeldungen](direct2ddebuglayer-debugmessages.md)
</dt> </dl>

 

 




