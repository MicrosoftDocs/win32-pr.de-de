---
title: Erstellen und Binden an eine Anforderungswarteschlange
description: Eine Anforderungswarteschlange ist eine Dienstwarteschlange, die ausstehende Anforderungen für eine bestimmte Anwendung enthält.
ms.assetid: 93f8b230-af0a-4582-b35b-d65f6841e525
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24c3a36fbbb9a8bcaa1c4e708240e99c276b09448ca56615df7da3d2cdf26836
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914280"
---
# <a name="creating-and-binding-to-a-request-queue"></a>Erstellen und Binden an eine Anforderungswarteschlange

Eine Anforderungswarteschlange ist eine Dienstwarteschlange, die ausstehende Anforderungen für eine bestimmte Anwendung enthält. Eine Anwendung erstellt die Anforderungswarteschlange unabhängig von der URL-Gruppe oder Serversitzung, indem sie die [**HttpCreateRequestQueue-Funktion**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) aufruft, und legt die Eigenschaften der Anforderungswarteschlange fest, indem sie die [**HttpSetRequestQueueProperty-Funktion**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) aufruft. Diese Eigenschaften sind die Ausführlichkeit von 503 Antworten, die maximale Länge der Warteschlange und der Aktivitätsstatus.

Damit Anforderungen an die Anforderungswarteschlange geroutet werden, bindet die Anwendung die URL-Gruppe, die sie im Rahmen der Laufzeitkonfiguration erstellt hat, an die Warteschlange, indem sie [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) mit **httpServerBindingProperty** aufruft, die im [Property-Parameter](run-time-configuration.md) angegeben ist.  Eingehende Anforderungen von den URLs in der Gruppe werden dann an die angegebene Anforderungswarteschlange geroutet.

 

 




