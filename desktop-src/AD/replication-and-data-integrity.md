---
title: Replikation und Datenintegrität
description: Active Directory Domain Services eine Multimasteraktualisierung bereitstellen.
ms.assetid: 99d35e16-9d1e-40d9-b1b0-600966165e45
ms.tgt_platform: multiple
keywords:
- Active Directory, Verwendung, Replikation und Datenintegrität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499f7e2c3193a280d009f53521e7a94fa3b89c5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341419"
---
# <a name="replication-and-data-integrity"></a>Replikation und Datenintegrität

Active Directory Domain Services eine *Multimasteraktualisierung* bereitstellen. Das Multi-Master-Update bedeutet, dass alle vollständigen Replikate einer bestimmten Partition beschreibbar sind (die partiellen Replikate auf globalen Katalog Servern sind nicht beschreibbar). Das Multi-Master-Update bedeutet, dass Updates nicht blockiert werden, auch wenn einige Replikate nicht funktionsfähig sind. Der Active Directory Server überträgt die Änderungen vom aktualisierten Replikat an alle anderen Replikate. Die Replikation erfolgt automatisch und transparent.

Weitere Informationen finden Sie in den nachfolgenden Themen.

-   [Das Replikations Modell in Active Directory Domain Services](replication-model-in-active-directory-domain-services.md)
-   [Replikations Verhalten in Active Directory Domain Services](replication-behavior-in-active-directory-domain-services.md)
-   [Erkennen und vermeiden von Replikations Latenz](detecting-and-avoiding-replication-latency.md)

 

 




