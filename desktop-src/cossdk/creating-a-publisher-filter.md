---
description: Erstellen eines Publisher Filters
ms.assetid: d91efecc-f02a-41c6-acf7-37b74723e7e8
title: Erstellen eines Publisher Filters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2cf3391cd331f7d81c3bb7ff467c140a78b0c8e30fb609ea655596dfe745a74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128792"
---
# <a name="creating-a-publisher-filter"></a>Erstellen eines Publisher Filters

Es gibt zwei Methoden zum Einrichten des Herausgeberfilters: die Verwendung der MultiPublisherFilterCLSID-Eigenschaft der Ereignisklasse oder die Verwendung von [**IEventControl::SetPublisherFilter.**](/windows/desktop/api/Eventsys/nf-eventsys-ieventcontrol-setpublisherfilter)

-   Da Sie das Ereignisobjekt mit dem [COM+-Komponentendienst](com--queued-components.md) in der Warteschlange zusammenstellen können, ist die bevorzugte Methode die Verwendung der MultiPublisherFilterCLSID-Eigenschaft in der Ereignisklasse, um den Herausgeberfilter festzulegen. Dadurch wird ein Filterobjekt für alle Methoden der Ereignisschnittstellen für ein Ereignisobjekt eingerichtet. Das Ereignisobjekt aktiviert den Herausgeberfilter, wenn das Ereignisklassenobjekt mit [**coCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)instanziiert wird.
-   Sie können auch [**SetPublisherFilter**](/windows/desktop/api/Eventsys/nf-eventsys-ieventcontrol-setpublisherfilter)verwenden. Wenn Sie diese Methode auswählen, ist die Schnittstelle jedoch nicht warteschlangenfähig und kann daher das Ereignisobjekt nicht mit dem COM+-Komponentendienst in der Warteschlange zwischen dem Verleger und dem Ereignisklassenobjekt verwenden. Weitere Informationen zur Verwendung des Diensts für in der Warteschlange enthaltene Komponenten mit COM+-Ereignissen finden Sie unter [Verwenden von COM+-Ereignissen mit COM+-Komponenten in der Warteschlange.](using-com--events-with-com--queued-components.md)

Ein Ereignis kann über ein oder mehrere Filterobjekte oder gar keins verfügen. Die Herausgeberfilterobjekte müssen entweder [**IPublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) oder [**IMultiInterfacePublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-imultiinterfacepublisherfilter)unterstützen, je nachdem, ob Sie über eine einzelne auslösende Schnittstelle oder mehrere auslösende Schnittstellen für das Ereignisklassenobjekt verfügen. Die Schnittstellen **IPublisherFilter** und **IMultiInterfacePublisherFilter** geben beide eine **Initialize-Methode** an. Die **Initialize-Methode** wird vom Ereignisklassenobjekt unmittelbar nach dem Erstellen des Filterobjekts aufgerufen.

COM+-Ereignisse versucht, zwei Methoden für den Filter aufzurufen. Zuerst ruft sie [**IPublisherFilter::P repareToFire**](/windows/desktop/api/EventSys/nf-eventsys-ipublisherfilter-preparetofire) auf und übergibt einen [**IFiringControl-Schnittstellenzeiger**](/windows/desktop/api/EventSys/nn-eventsys-ifiringcontrol) an den Filter. Anschließend wird das Filterobjekt nach der Ereignisschnittstelle abgefragt. Wenn der Filter die Ereignisschnittstelle unterstützt, ruft er eine -Methode dafür auf. Dies ermöglicht den Zugriff auf die Herausgeberparameter für ein Ereignis. Der Filter kann diese Parameter verwenden, um zu bestimmen, welche Abonnements ausgelöst werden sollen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Filtern von Ereignissen in COM+](filtering-events-in-com-.md)
</dt> </dl>

 

 
