---
title: Konfigurieren der Anforderungswarteschlange
description: Konfigurieren der Anforderungswarteschlange
ms.assetid: ab03089c-2ef1-457d-a5f5-a4d400f3a7f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e08a8f931d8875fda43b485bada93d2bf5291d0d2b90e85c8b31bd631e8c7fbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014928"
---
# <a name="configuring-the-request-queue"></a>Konfigurieren der Anforderungswarteschlange

Wenn die Anforderungswarteschlange geöffnet oder erstellt wird, erhält die aufrufende Anwendung ein Handle für sie, das zum Senden von Anforderungen oder Konfigurieren der Anforderungswarteschlange verwendet werden kann. Das [**Aufrufen von HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) mit **HttpServerBindingProperty** und das Angeben des Anforderungswarteschlangenhandles in der [**HTTP BINDING \_ \_ INFO-Struktur,**](/windows/desktop/api/Http/ns-http-http_binding_info) die im *pPropertyInformation-Parameter* angegeben ist, ordnet die URL-Gruppe der Anforderungswarteschlange zu. Anforderungswarteschlangeneigenschaften werden nur von der Anwendung festgelegt, die die Anforderungswarteschlange erstellt. Beispielsweise ruft die Erstelleranwendung [**httpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) auf und gibt **httpServerQueueLengthProperty** im *Property-Parameter* an, um die Serverwarteschlangenlänge festzulegen.

 

 




