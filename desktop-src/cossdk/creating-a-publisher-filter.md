---
description: Erstellen eines Herausgeber Filters
ms.assetid: d91efecc-f02a-41c6-acf7-37b74723e7e8
title: Erstellen eines Herausgeber Filters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 997fe37cf0021bcb2aa153c2dc4b73597e0c43cc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127556"
---
# <a name="creating-a-publisher-filter"></a>Erstellen eines Herausgeber Filters

Es gibt zwei Methoden zum Einrichten des Herausgeber Filters: mithilfe der multipublisherfilterclsid-Eigenschaft der Ereignisklasse oder mit [**IEventControl:: setpublisherfilter**](/windows/desktop/api/Eventsys/nf-eventsys-ieventcontrol-setpublisherfilter).

-   Da es Ihnen ermöglicht, das Ereignis Objekt mit dem com+-Dienst in der [Warteschlange für die Warteschlange](com--queued-components.md) zu verfassen, ist die bevorzugte Methode die Verwendung der multipublisherfilterclsid-Eigenschaft in der Ereignisklasse, um den Herausgeber Filter festzulegen. Dadurch wird ein Filter Objekt für alle Methoden der Ereignis Schnittstellen für ein Ereignis Objekt festgelegt. Das Ereignis Objekt aktiviert den Herausgeber Filter, wenn das Ereignis Klassenobjekt mithilfe von [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)instanziiert wird.
-   Sie können auch [**setpublisherfilter**](/windows/desktop/api/Eventsys/nf-eventsys-ieventcontrol-setpublisherfilter)verwenden. Wenn Sie diese Methode auswählen, kann die Schnittstelle jedoch nicht in die Warteschlange eingereiht werden und kann daher nicht das Ereignis Objekt mit dem com+-Dienst in der Warteschlange für die Warteschlange zwischen dem Verleger und dem Ereignis Klassenobjekt verwenden. Weitere Informationen zur Verwendung des Dienstanbieter für die Warteschlange mit com+-Ereignissen finden Sie unter [Verwenden von COM+-Ereignissen mit COM+-Komponenten in der Warteschlange](using-com--events-with-com--queued-components.md).

Ein Ereignis kann über ein oder mehrere Filter Objekte oder gar keine verfügen. Die Verleger Filter Objekte müssen entweder [**ipublisherfilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) oder [**imultiinterfacepublisherfilter**](/windows/desktop/api/EventSys/nn-eventsys-imultiinterfacepublisherfilter)unterstützen, je nachdem, ob Sie über eine einzelne auslöserschnittstelle oder mehrere auslösenden Schnittstellen für das Ereignis Klassenobjekt verfügen. Die **ipublisherfilter** -Schnittstelle und die **imultiinterfacepublisherfilter** -Schnittstelle geben beide eine **Initialize** -Methode an. Die **Initialize** -Methode wird direkt nach dem Erstellen des Filter Objekts vom Ereignis Klassenobjekt aufgerufen.

Com+-Ereignisse versuchen, zwei Methoden für den Filter aufzurufen. Zuerst wird [**ipublisherfilter::P**](/windows/desktop/api/EventSys/nf-eventsys-ipublisherfilter-preparetofire) Analyse Trigger aufgerufen und ein [**ifiringcontrol**](/windows/desktop/api/EventSys/nn-eventsys-ifiringcontrol) -Schnittstellen Zeiger an den Filter übergibt. Anschließend wird das Filter Objekt für die Ereignis Schnittstelle abgefragt. Wenn der Filter die Ereignis Schnittstelle unterstützt, ruft er eine Methode dafür auf. Dies ermöglicht den Zugriff auf die Verleger Parameter für ein Ereignis. Der Filter kann diese Parameter verwenden, um zu bestimmen, welche Abonnements ausgelöst werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Filtern von Ereignissen in com+](filtering-events-in-com-.md)
</dt> </dl>

 

 
