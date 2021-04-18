---
title: Direct2D Übersicht über die Debug-Ebene
description: .
ms.assetid: 7c28e00b-ebb9-4b79-939c-64eade1351ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df560595ea0ae6c7a56c3fa568f2f94ae56652ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338372"
---
# <a name="direct2d-debug-layer-overview"></a>Direct2D Übersicht über die Debug-Ebene

Die Direct2D Debug-Schicht stellt Entwurfszeit-Debugmeldungen bereit, mit denen Sie den Lauf Zeit Anwendungs Ausfall minimieren können In dieser Übersicht werden die Grundlagen der Direct2D Debug-Ebene beschrieben. Es wird vorausgesetzt, dass Sie mit dem Erstellen von Direct2D-Basisanwendungen vertraut sind.

Diese Übersicht enthält die folgenden Abschnitte.

-   [Was ist die Direct2D-Debug-Ebene?](#what-is-the-direct2d-debug-layer)
-   [Installieren der Direct2D Debug-Ebene](#installing-the-direct2d-debug-layer)
-   [Aktivieren der Debug-Ebene](#enabling-the-debug-layer)
-   [Debugstufen](#debug-levels)
-   [Zugehörige Themen](#related-topics)

## <a name="what-is-the-direct2d-debug-layer"></a>Was ist die Direct2D-Debug-Ebene?

Die Direct2D-debugschicht, die separat von Direct2D in der eigenen dll mit dem Namen d2d1debug.dll implementiert wurde, stellt Debugmeldungen bereit, damit Sie Direct2D-Funktionen genau verwenden können. Die Debugmeldungen resultieren häufig aus API-Vertragsverstößen, wie z. b. ungültigen Parametern (Direct3D-bezogen), ungültigen Ressourcen, Threading Verstößen und Leistungsproblemen wie der Verwendung einer Ebene, wenn ein Clip ausreichen würde. Um anzugeben, wie viele Informationen von der debugschicht verfolgt werden, können Sie eine der drei debugebenen angeben: Information, Warnung und Fehler. und eine Fehlermeldungs Ebene löst den Haltepunkt aus, um Sie beim Debuggen zu unterstützen.

## <a name="installing-the-direct2d-debug-layer"></a>Installieren der Direct2D Debug-Ebene

Anweisungen zum Installieren der debugschicht finden Sie unter [Installieren der Direct2D-debugschicht](installing-the-direct2d-debug-layer.md).

## <a name="enabling-the-debug-layer"></a>Aktivieren der Debug-Ebene

Um die Debugebene in der Anwendung zu aktivieren, geben Sie den Wert [**D2D1 \_ Debug \_ Level**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) than **D2D1 \_ Debug \_ Level \_ None** an, wenn Sie eine Factory mit der [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) -Funktion erstellen.

> [!Note]  
> Wenn die Direct2D Debug-Ebene aktiviert ist, kann der Direct2D Color Management Effect (CLSID \_ D2D1ColorManagement) beim Festlegen eines Farb Kontexts eine Zugriffsverletzung verursachen. Die Problem Umgehung besteht darin, die debugschicht bei Verwendung des Farb Verwaltungs Effekts zu deaktivieren.

 

Wenn Sie die debugschicht für eine Factory aktivieren, werden auch Debuginformationen für jedes von dieser Factory erstellte Objekt aktiviert.

Im folgenden Beispiel wird die debugschicht für eine Factory aktiviert, wenn die Anwendung für die Debug-Buildkonfiguration kompiliert wird.


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
> Wenn keine Factory-Optionen angegeben werden oder die Debugebene "None" angegeben ist, wird die debugschicht nicht aufgerufen. Die debugschicht sollte in der Releaseversion einer Anwendung nie aktiv sein.

 

Im nächsten Abschnitt werden die verschiedenen debugebenen beschrieben, die von der [**D2D1 \_ Debug \_ Level**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) -Enumeration definiert werden.

## <a name="debug-levels"></a>Debugstufen

Die [**D2D1 \_ Debug \_ Level**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) -Enumeration gibt drei debugebenen an: D2D1 \_ Debug \_ Level \_ Error (Error), D2D1 \_ Debug \_ Level \_ Warning (Warning) und D2D1 \_ Debug \_ Level \_ Information (Informationen). Diese Ebenen werden wie folgt interpretiert:

-   **Fehler:** Direct2D sendet schwerwiegende Fehlermeldungen an die debugschicht. Beispielsweise wird durch das Unterbrechen einer Threading Einschränkung ein schwerwiegender Fehler generiert.

-   **Warnung:** Direct2D sendet Fehlermeldungen und Warnungen an die debugschicht, damit Sie diese Nachrichten adressieren können.

-   **Informationen:** Direct2D sendet Fehlermeldungen, Warnungen und zusätzliche Diagnoseinformationen an die debugschicht. Beispielsweise werden Meldungen zur Leistungsverbesserung auf dieser Debugebene gesendet.

Der Wert D2D1 \_ Debug \_ Level \_ None (None) gibt an, dass Direct2D keine Debugausgabe bereitstellt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Debugmeldungen](direct2ddebuglayer-debugmessages.md)
</dt> </dl>

 

 




