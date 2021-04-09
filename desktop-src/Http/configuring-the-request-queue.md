---
title: Konfigurieren der Anforderungs Warteschlange
description: Konfigurieren der Anforderungs Warteschlange
ms.assetid: ab03089c-2ef1-457d-a5f5-a4d400f3a7f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42ed397ffbcb42d887d519bc4492bd167dd98c57
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856128"
---
# <a name="configuring-the-request-queue"></a>Konfigurieren der Anforderungs Warteschlange

Wenn die Anforderungs Warteschlange geöffnet oder erstellt wird, empfängt die aufrufende Anwendung ein Handle, das zum Senden von Anforderungen oder Konfigurieren der Anforderungs Warteschlange verwendet werden kann. Wenn Sie [**httpseturlgroupproperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) mit **httpserverbindingproperty** aufrufen und das Anforderungs Warteschlangen Handle in der [**http- \_ Bindungs \_**](/windows/desktop/api/Http/ns-http-http_binding_info) Informationsstruktur bereitstellen, die im *ppropertyinformation* -Parameter angegeben ist, ordnet die URL-Gruppe der Anforderungs Warteschlange zu. Eigenschaften der Anforderungs Warteschlange werden nur von der Anwendung festgelegt, die die Anforderungs Warteschlange erstellt. Wenn Sie z. b. die Eigenschaft Server-Warteschlangen Länge festlegen möchten, ruft die Ersteller-Anwendung [**httpsetrequestqueueproperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) auf, wobei **httpserverqueuelengthproperty** im *Property* -Parameter angegeben wird.

 

 




