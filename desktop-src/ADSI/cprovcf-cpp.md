---
title: CPROVCF. Cpp
description: In der Beispielanbieterkomponente befindet sich ein Codebeispiel für den Factorycode der ADs-Anbieterobjektklasse in cprovcf.cpp.
ms.assetid: 53a4da74-3f36-4e6d-ae93-8d595680bcf3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea3b77ea7fe1b1d6fe946b9a8b509be33c11f2a075ee658ee305f0f7ba2d2c6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023668"
---
# <a name="cprovcfcpp"></a>CPROVCF. Cpp

In der Beispielanbieterkomponente befindet sich ein Codebeispiel für den Factorycode der ADs-Anbieterobjektklasse in cprovcf.cpp. Die Anbieterkomponente erstellt nie direkt eine Instanz dieses Objekts, es sei denn, das Objekt wird automatisch während der Bindungsvorgänge in [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) oder der internen Funktion in der Visual Basic-Methode **GetObject erstellt.** Die unterstützte Methode ist in der folgenden Tabelle aufgeführt.



| Methode                                  | Beschreibung                                                           |
|-----------------------------------------|-----------------------------------------------------------------------|
| **CSampleDSProviderCF::CreateInstance** | Erstellt eine Instanz der Klassen factory für das ADS-Anbieterobjekt. |



 

 

 




