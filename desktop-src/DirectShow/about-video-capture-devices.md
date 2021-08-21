---
description: Informationen zu Videoaufnahmegeräten
ms.assetid: 1bf6e64f-c3cf-45a4-9f87-1b8cf503d98b
title: Informationen zu Videoaufnahmegeräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff3fff9f3d009006e300afdbe9986bfdc8d0a32ea618fdd2748efe0bd650b5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118160183"
---
# <a name="about-video-capture-devices"></a>Informationen zu Videoaufnahmegeräten

Die meisten neuen Videoaufzeichnungsgeräte verwenden Windows Treibermodelltreiber (WDM). In der WDM-Architektur stellt Microsoft eine Reihe hardwareunabhängiger Treiber bereit, die als Klassentreiber bezeichnet werden, und der Hardwarehersteller stellt hardwarespezifische Minitreiber bereit. Ein Minitreiber implementiert alle Funktionen, die für das Gerät spezifisch sind. Für die meisten Funktionen ruft der Minitreiber den Microsoft-Klassentreiber auf.

In einem DirectShow-Filterdiagramm wird jedes WDM-Erfassungsgerät als [WDM-Videoerfassungsfilter](wdm-video-capture-filter.md) angezeigt. Der WDM Video Capture-Filter konfiguriert sich selbst basierend auf den Merkmalen des Treibers. Er wird unter einem namen angezeigt, der vom Treiber bereitgestellt wird. Ein Filter namens "WDM Video Capture Filter" wird an keiner Stelle im Diagramm angezeigt.

Einige ältere Erfassungsgeräte verwenden Video weiterhin für VFW-Treiber (Windows). Obwohl diese Treiber jetzt veraltet sind, werden sie in DirectShow über den [VFW Capture-Filter](vfw-capture-filter.md) unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Videoerfassung in DirectShow](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



