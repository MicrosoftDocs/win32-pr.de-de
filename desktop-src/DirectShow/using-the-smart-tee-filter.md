---
description: Verwenden des Smart Tee-Filters
ms.assetid: d2828269-6841-41a8-8d45-f864c7e85857
title: Verwenden des Smart Tee-Filters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8897a93e8be7582a4acce1a2822160c58cfe1df79eb2093bd5d96bad9629b64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650775"
---
# <a name="using-the-smart-tee-filter"></a>Verwenden des Smart Tee-Filters

Wenn ein Erfassungsfilter über separate Erfassungs- und Vorschaupins verfügt, können Sie von einem erfassen, während Sie eine Vorschau anzeigen. Wenn der Filter jedoch über keine Vorschaupins verfügt, können Sie dasselbe tun, indem Sie den [Smart Tee-Filter](smart-tee-filter.md) in das Diagramm eingeben. Dieser Filter teilt Daten aus dem Erfassungspin in zwei identische Datenströme auf: einen für die Erfassung und einen für die Vorschau. Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.

![Erfassungsdiagramm mit intelligentem Teefilter](images/vidcap05.png)

Die [**ICaptureGraphBuilder2::RenderStream-Methode**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) fügt bei Bedarf automatisch den Smart Tee-Filter ein. Wenn Sie jedoch **IGraphBuilder-Methoden** zum Erstellen Ihres Graphen und nicht **RenderStream** verwenden, müssen Sie möglicherweise den Smart Tee-Filter einfügen.

Überprüfen Sie vor dem Rendern von Stecknadeln auf dem Erfassungsfilter, ob der Filter über einen Vorschaupin oder einen Videoportanschluss verfügt. Wenn dies nicht der Benutzer ist und Sie eine Vorschau anzeigen möchten, fügen Sie dem Diagramm den Smart Tee-Filter hinzu, und verbinden Sie ihn mit dem Aufnahmepin des Erfassungsfilters.

> [!Note]  
> Sie können einen Videoportpin (VP) als eine Art Vorschaupin behandeln, sodass ein Filter mit einem VP-Pin keinen Smart Tee-Filter benötigt. VP-Pins haben jedoch einige andere besondere Anforderungen. Weitere Informationen finden Sie unter [Video Port Pins](video-port-pins.md).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweiterte Erfassungsthemen](advanced-capture-topics.md)
</dt> <dt>

[Kombinieren von Videoaufnahme und Vorschau](combining-video-capture-and-preview.md)
</dt> <dt>

[Arbeiten mit Pinkategorien](working-with-pin-categories.md)
</dt> </dl>

 

 



