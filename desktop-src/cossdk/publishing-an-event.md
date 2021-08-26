---
description: Veröffentlichen eines Ereignisses
ms.assetid: b40d10aa-43bc-4c53-9e89-94c585d34238
title: Veröffentlichen eines Ereignisses
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 724dc94ddf9cc25ec3b11cc31376805241e9d6d67250f8a494f8b417b9d201a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990500"
---
# <a name="publishing-an-event"></a>Veröffentlichen eines Ereignisses

Um ein Ereignis zu veröffentlichen, instanziieren Sie einfach ein Ereignisobjekt, indem Sie [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) oder die Microsoft Visual Basic **CreateObject-Methode** aufrufen, indem Sie EventClassID oder EventClassName als Argument verwenden. Der Herausgeber ruft [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für das Ereignisobjekt auf, um die vom Ereignisklassenobjekt unterstützten Schnittstellen zu erhalten, und ruft eine Methode für das Ereignisobjekt über die Schnittstelle auf, um das Ereignis zu veröffentlichen. Das Ereignissystem veröffentlicht dann Ereignisse in der Ereignisklasse CLSID EventObjectChange mit der \_ Schnittstellen-ID IID \_ IEventObjectChange.

Um die Übermittlung von Ereignissen an mehrere Abonnenten zu unterstützen, sollten Ereignisklassenmethoden nur in Parametern enthalten.

Mithilfe der FireInParallel-Eigenschaft des Ereignisklassenobjekts können Herausgeber anfordern, dass das Ereignissystem mehrere Threads verwendet, um ein Ereignis an mehrere Abonnenten zu senden. [](the-com--event-class-object.md) Die Auswahl eines parallelen Übermittlungsmechanismus garantiert nicht die gleichzeitige Übermittlung des Ereignisses an mehrere Abonnenten, weist jedoch den COM+-Ereignisdienst an, dies zu ermöglichen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Veröffentlichen und Bereitstellen von Ereignissen in COM+](publishing-and-delivering-events-in-com-.md)
</dt> </dl>

 

 
