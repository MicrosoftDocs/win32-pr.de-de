---
description: Informationen zu Video Erfassungs Geräten
ms.assetid: 1bf6e64f-c3cf-45a4-9f87-1b8cf503d98b
title: Informationen zu Video Erfassungs Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98ab9797c11b5c22f6196a5b4e781e50ce34edec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746376"
---
# <a name="about-video-capture-devices"></a>Informationen zu Video Erfassungs Geräten

Die meisten neuen Video Erfassungsgeräte verwenden Windows-Treibermodell-Treiber (WDM). In der WDM-Architektur stellt Microsoft eine Reihe von hardwareunabhängigen Treibern bereit, die als Klassen Treiber bezeichnet werden, und der Hardwarehersteller stellt Hardware spezifische Mini Treiber bereit. Ein Mini Treiber implementiert alle Funktionen, die für das Gerät spezifisch sind. für die meisten Funktionen ruft der Mini Treiber den Microsoft-Klassen Treiber auf.

In einem DirectShow-Filter Diagramm wird jedes WDM-Erfassungsgerät als [WDM-Video Erfassungs](wdm-video-capture-filter.md) Filter angezeigt. Der WDM-Video Erfassungs Filter konfiguriert sich selbst basierend auf den Merkmalen des Treibers. Sie wird unter einem vom Treiber bereitgestellten Namen angezeigt – Sie sehen keinen Filter mit dem Namen "WDM-Video Erfassungs Filter" an einer beliebigen Stelle im Diagramm.

Einige ältere Erfassungsgeräte verwenden weiterhin Video für Windows-Treiber (Vfw). Obwohl diese Treiber mittlerweile veraltet sind, werden Sie in DirectShow über den [VFW-Erfassungs](vfw-capture-filter.md) Filter unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Video Erfassung in DirectShow](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



