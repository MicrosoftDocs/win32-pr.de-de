---
description: Verwenden des Smart Tee-Filters
ms.assetid: d2828269-6841-41a8-8d45-f864c7e85857
title: Verwenden des Smart Tee-Filters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5260469634c613fe05c25eb9f55e24e108e8c434
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373141"
---
# <a name="using-the-smart-tee-filter"></a>Verwenden des Smart Tee-Filters

Wenn für einen Erfassungs Filter separate Erfassungs-und Vorschau Pins verfügbar sind, können Sie von einem Erfassungs Filter erfassen, während Sie die Vorschau anzeigen. Wenn der Filter jedoch keine Vorschau-Pin hat, können Sie das gleiche tun, indem Sie den [Smart Tee](smart-tee-filter.md) -Filter in das Diagramm einschließen. Dieser Filter teilt die Daten aus dem Erfassungs-PIN in zwei identische Datenströme auf, einen für Capture und einen für die Vorschau. Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.

![Diagramm mit Smart Tee-Filter erfassen](images/vidcap05.png)

Die [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -Methode fügt ggf. automatisch den intelligenten Tee-Filter ein. Wenn Sie jedoch **igraphbuilder** -Methoden verwenden, um das Diagramm zu erstellen, und nicht **RenderStream**, müssen Sie möglicherweise den Smart Tee-Filter einfügen.

Überprüfen Sie vor dem Rendering von Pins im Erfassungs Filter, ob der Filter eine Vorschau-PIN oder eine Videoport-Pin aufweist. Wenn dies nicht der Fall ist und Sie eine Vorschau anzeigen möchten, fügen Sie dem Diagramm den intelligenten Tee-Filter hinzu, und verbinden Sie ihn mit der Erfassungs-PIN im Erfassungs Filter.

> [!Note]  
> Sie können eine textport-PIN (VP) als eine Art von Vorschau-Pin behandeln, sodass ein Filter mit einer VP-Pin keinen intelligenten Tee-Filter benötigt. Allerdings haben VP Pins einige andere besondere Anforderungen. Weitere Informationen finden Sie unter [Video Port Pins](video-port-pins.md).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweiterte Erfassungs Themen](advanced-capture-topics.md)
</dt> <dt>

[Kombinieren von Video Erfassung und Vorschau](combining-video-capture-and-preview.md)
</dt> <dt>

[Arbeiten mit PIN-Kategorien](working-with-pin-categories.md)
</dt> </dl>

 

 



