---
title: NDF-Schnittstellen
description: Die folgenden Schnittstellen können verwendet werden, um die Funktionalität von Microsoft-Hilfsklassen zu erweitern, die als erweiterbar identifiziert werden.
ms.assetid: 55e58eb8-d04e-4398-a892-8c343a88adc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b16ff5dde9246798392903f47370e663e26dd6be7f21252f8791bfee267018b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801950"
---
# <a name="ndf-interfaces"></a>NDF-Schnittstellen

Die folgenden Schnittstellen können verwendet werden, um die Funktionalität von Microsoft-Hilfsklassen zu erweitern, die als erweiterbar identifiziert werden. Obwohl diese Funktionalität für die meisten Anwendungen nicht erforderlich ist, kann sie in einigen Fällen spezifischere Diagnosen und Lösungen bereitstellen.

> [!Note]  
> Diese Schnittstellen und die zugehörigen Methoden sind für Entwickler, die ihre eigenen Hilfsklassen von Drittanbietern implementieren, die die NDF-Funktionalität erweitern.

 



| Schnittstellenname                                                 | BESCHREIBUNG                                                                                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper)                       | Wird von der NDF für die meisten Aktivitäten aufgerufen, die während einer Diagnose auftreten.                                                     |
| [**INetDiagHelperEx**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperex)                   | Wird von der NDF aufgerufen, um Informationen im Zusammenhang mit Diagnosen und der Lösung von netzwerkbezogenen Problemen zu erfassen und zur Verfügung zu stellen. |
| [**INetDiagHelperInfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo)               | Wird von der NDF aufgerufen, um zu überprüfen, ob sie über erforderliche Informationen verfügt.                                                           |
| [**INetDiagHelperUtilFactory**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperutilfactory) | Ist für das System reserviert.                                                                                                 |



 

 

 




