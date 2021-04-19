---
title: Auflösung mehrerer Aggregations Komponenten, die dieselbe Schnittstelle unterstützen
description: Es ist ungewöhnlich, dass zwei Erweiterungen die gleiche Schnittstelle für ADSI verfügbar machen.
ms.assetid: 87cb1a17-04f7-4ad0-989a-a9506dfdca05
ms.tgt_platform: multiple
keywords:
- Auflösung mehrerer Aggregations Komponenten, die dieselbe Schnittstelle ADSI unterstützen
- Auflösung mehrerer Aggregations Komponenten, die dieselbe Schnittstelle ADSI unterstützen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f58b7b606a05543444a172e2f76b436f6048431
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342237"
---
# <a name="resolution-of-multiple-aggregation-components-supporting-the-same-interface"></a>Auflösung mehrerer Aggregations Komponenten, die dieselbe Schnittstelle unterstützen

Es ist ungewöhnlich, dass zwei Erweiterungen die gleiche Schnittstelle für ADSI verfügbar machen. In diesem Fall gelten die folgenden Regeln:

-   Wenn eine Schnittstelle, z. b. **IMyInterface**, sowohl vom Aggregator (ADSI) als auch von Erweiterungs Objekten unterstützt wird, gibt **QueryInterface** immer die **IMyInterface** für ADSI zurück.
-   Wenn eine Schnittstelle, z. b. **IMyInterface**, nicht vom Aggregator (ADSI) unterstützt wird, sondern von mehr als einem Erweiterungs Objekt unterstützt wird, gibt **QueryInterface** die **IMyInterface** des ersten Erweiterungs Objekts zurück, das in der Registrierung aufgeführt ist, die die-Schnittstelle unterstützt.

Beachten Sie, dass die Reihenfolge der Komponenten in der Registrierung auch die Auflösung von Namenskonflikten bei der Automatisierung beeinträchtigt. Weitere Informationen finden Sie unter Auflösen [von Funktions-/Eigenschaftenname-Konflikten in Automation in Extensions](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md).

 

 




