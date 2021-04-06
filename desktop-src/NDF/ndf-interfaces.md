---
title: NDF-Schnittstellen
description: Die folgenden Schnittstellen können verwendet werden, um die Funktionalität von Microsoft-Hilfsklassen zu erweitern, die als erweiterbar identifiziert werden.
ms.assetid: 55e58eb8-d04e-4398-a892-8c343a88adc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fac7b53329f8d157382f1c68df34d1b0e663327
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036235"
---
# <a name="ndf-interfaces"></a>NDF-Schnittstellen

Die folgenden Schnittstellen können verwendet werden, um die Funktionalität von Microsoft-Hilfsklassen zu erweitern, die als erweiterbar identifiziert werden. Obwohl diese Funktionalität für die meisten Anwendungen nicht erforderlich ist, kann Sie in einigen Fällen spezifischere Diagnosen und Auflösungen bereitstellen.

> [!Note]  
> Diese Schnittstellen und die zugehörigen Methoden sind für Entwickler konzipiert, die ihre eigenen Hilfsklassen von Drittanbietern implementieren, die die NDF-Funktionalität erweitern.

 



| Schnittstellenname                                                 | BESCHREIBUNG                                                                                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**Inetdiaghelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper)                       | Wird von der NDF für die meisten Aktivitäten aufgerufen, die während einer Diagnose auftreten.                                                     |
| [**Inetdiaghelperex**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperex)                   | Wird von der NDF aufgerufen, um Informationen zu Diagnosen und zur Behebung von netzwerkbezogenen Problemen zu erfassen und bereitzustellen. |
| [**Inetdiaghelperinfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo)               | Wird von der NDF aufgerufen, um zu überprüfen, ob Sie über erforderliche Informationen verfügt                                                           |
| [**Inetdiaghelperutilfactory**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperutilfactory) | Ist für das System reserviert.                                                                                                 |



 

 

 




