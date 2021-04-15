---
title: Binden an den Such Start Punkt
description: Der Startpunkt für eine Suche ist ein Container, der direkt oder indirekt die gesuchten Objekte enthält.
ms.assetid: f93c1310-7c8b-4d28-bd4d-6fab969d3353
ms.tgt_platform: multiple
keywords:
- Active Directory Beispiele Active Directory, binden an einen Such Startpunkt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 741986e651848c1d2a88ab016b63365db91b26b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470765"
---
# <a name="binding-to-the-search-start-point"></a>Binden an den Such Start Punkt

Der Startpunkt für eine Suche ist ein Container, der direkt oder indirekt die gesuchten Objekte enthält. Die Suche wird in Containern über dem Such Startpunkt nicht durchgeführt. Nehmen Sie z. b. die folgende hypothetische Verzeichnisstruktur:

``` syntax
Domain A
    Container 1
        Object 1
        Object 2
    Container 2
        Object 3
        Object 4
```

Wenn für alle Objekte eine Suche durchgeführt wird und der Such Startpunkt "Container 2" ist, werden nur "Object 3" und "Object 4" abgerufen. Wenn dieselbe Suche mit dem Such Startpunkt bei "Container 1" durchgeführt wurde, werden "Objekt 1" und "Objekt 2" abgerufen.

Binden Sie zum Binden an den Such Startpunkt an den ADsPath des Containers, der als Such Startpunkt verwendet werden soll.

 

 




