---
title: Erstellen und Binden an eine Anforderungs Warteschlange
description: Eine Anforderungs Warteschlange ist eine Dienst Warteschlange, die ausstehende Anforderungen für eine bestimmte Anwendung enthält.
ms.assetid: 93f8b230-af0a-4582-b35b-d65f6841e525
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 945b8451f9128357b7da0ddc64600b74deffd0d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388552"
---
# <a name="creating-and-binding-to-a-request-queue"></a>Erstellen und Binden an eine Anforderungs Warteschlange

Eine Anforderungs Warteschlange ist eine Dienst Warteschlange, die ausstehende Anforderungen für eine bestimmte Anwendung enthält. Eine Anwendung erstellt die Anforderungs Warteschlange unabhängig von der URL-Gruppe oder der Server Sitzung durch Aufrufen der Funktion [**httpcreaterequestqueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) und legt die Eigenschaften der Anforderungs Warteschlange durch Aufrufen der Funktion [**httpsetrequestqueueproperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) fest. Bei diesen Eigenschaften handelt es sich um die Ausführlichkeit von 503 Antworten, die maximale Länge der Warteschlange und den Aktivitäts Zustand.

Um zu bewirken, dass Anforderungen an die Anforderungs Warteschlange weitergeleitet werden, bindet die Anwendung die URL-Gruppe, die Sie als Teil der [Laufzeitkonfiguration](run-time-configuration.md) erstellt hat, durch Aufrufen von [**httpseturlgroupproperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) mit **httpserverbindingproperty** in den *Property* -Parameter. Eingehende Anforderungen von den URLs in der Gruppe werden dann an die angegebene Anforderungs Warteschlange weitergeleitet.

 

 




