---
description: Veröffentlichen eines Ereignisses
ms.assetid: b40d10aa-43bc-4c53-9e89-94c585d34238
title: Veröffentlichen eines Ereignisses
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c060d8bf67e12fc7429b2afc768794468a1c49ad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344212"
---
# <a name="publishing-an-event"></a>Veröffentlichen eines Ereignisses

Zum Veröffentlichen eines Ereignisses instanziieren Sie einfach ein Ereignis Objekt, indem Sie [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) oder die Microsoft Visual Basic **CreateObject** -Methode mithilfe von eventclassid oder EventClassName als Argument aufrufen. Der Verleger ruft [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für das Ereignis Objekt auf, um die vom Ereignis Klassenobjekt unterstützten Schnittstellen zu erhalten, und ruft eine Methode für das Ereignis Objekt über die-Schnittstelle auf, um das Ereignis zu veröffentlichen. Das Ereignis System veröffentlicht dann Ereignisse in der Ereignisklasse CLSID \_ eventobjectchange mit der Schnittstellen-ID IID \_ ieventobjectchange.

Um die Übermittlung von Ereignissen an mehrere Abonnenten zu unterstützen, sollten Ereignis Klassen Methoden nur in-Parametern enthalten.

Mithilfe der Eigenschaft "freinparallel" des Objekts " [Event Class](the-com--event-class-object.md) " können Verleger anfordern, dass das Ereignis System mehrere Threads verwendet, um ein Ereignis an mehr als einen Abonnenten zu übermitteln. Die Auswahl eines parallelen Übermittlungs Mechanismus garantiert nicht die gleichzeitige Übermittlung des Ereignisses an mehrere Abonnenten, sondern weist den com+-Ereignis Dienst an, dies zuzulassen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Veröffentlichen und Bereitstellung von Ereignissen in com+](publishing-and-delivering-events-in-com-.md)
</dt> </dl>

 

 
