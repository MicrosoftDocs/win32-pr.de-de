---
title: Binden an den Suchstartpunkt
description: Der Ausgangspunkt für eine Suche ist ein Container, der direkt oder indirekt die gesuchten Objekte enthält.
ms.assetid: f93c1310-7c8b-4d28-bd4d-6fab969d3353
ms.tgt_platform: multiple
keywords:
- 'Active Directory-Beispiele: Active Directory, Bindung an einen Suchstartpunkt'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 268b6b419c88911aaebf4bf4cae0ed2e2108baffe54a4f019f354b7f0aa3d7ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118023887"
---
# <a name="binding-to-the-search-start-point"></a>Binden an den Suchstartpunkt

Der Ausgangspunkt für eine Suche ist ein Container, der direkt oder indirekt die gesuchten Objekte enthält. Die Suche wird nicht in Containern oberhalb des Suchstartpunkts ausgeführt. Nehmen Sie beispielsweise die folgende hypothetische Verzeichnisstruktur:

``` syntax
Domain A
    Container 1
        Object 1
        Object 2
    Container 2
        Object 3
        Object 4
```

Wenn eine Suche für alle Objekte ausgeführt wird und der Suchstartpunkt "Container 2" lautet, werden nur "Objekt 3" und "Objekt 4" abgerufen. Wenn dieselbe Suche mit dem Suchstartpunkt bei "Container 1" durchgeführt wurde, werden "Objekt 1" und "Objekt 2" abgerufen.

Um eine Bindung an den Suchstartpunkt zu erhalten, binden Sie an den ADsPath des Containers, der der Suchstartpunkt sein wird.

 

 




