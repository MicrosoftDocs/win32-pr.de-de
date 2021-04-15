---
title: Cprovcf. CPP
description: In der Beispiel Anbieter Komponente befindet sich in cprovcf. cpp ein Codebeispiel für den Hersteller des ADS-Anbieter Objektklassen-Factory.
ms.assetid: 53a4da74-3f36-4e6d-ae93-8d595680bcf3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d086cd79086f40bab6d898b844ed52fc0161bc7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470813"
---
# <a name="cprovcfcpp"></a>Cprovcf. CPP

In der Beispiel Anbieter Komponente befindet sich in cprovcf. cpp ein Codebeispiel für den Hersteller des ADS-Anbieter Objektklassen-Factory. Die Anbieter Komponente erstellt niemals direkt eine Instanz dieses Objekts, außer wenn das Objekt während der Bindungs Vorgänge in " [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) " oder der internen Funktion in der Visual Basic-Methode " **GetObject**" automatisch erstellt wird. Die unterstützte Methode ist in der folgenden Tabelle aufgeführt.



| Methode                                  | BESCHREIBUNG                                                           |
|-----------------------------------------|-----------------------------------------------------------------------|
| **Csampledsprovidercf:: kreateinstance** | Erstellt eine Instanz der Klassenfactory für das ADS-Anbieter Objekt. |



 

 

 




