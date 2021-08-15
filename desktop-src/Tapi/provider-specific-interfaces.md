---
description: TAPI 3 unterstützt die Integration von dienstanbieterspezifischen Schnittstellen in die Standardobjekte, sodass Anwendungen anbieterspezifische Funktionen nutzen können.
ms.assetid: 8077c9a7-3235-41a7-97dc-ca5f3c291ee6
title: Provider-Specific Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09290bf6d2ade55a9e9d2b0f51315acfc5488805b6c19b23679e00708ddaed45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060568"
---
# <a name="provider-specific-interfaces"></a>Provider-Specific Schnittstellen

TAPI 3 unterstützt die Integration von dienstanbieterspezifischen Schnittstellen in die Standardobjekte, sodass Anwendungen anbieterspezifische Funktionen nutzen können. Darüber hinaus ermöglicht TAPI 3 Dienstanbietern, anbieterspezifische Ereignisse an Anwendungen als COM-Objekte über die gleiche Schnittstelle zu übermitteln, über die die Anwendung Standardereignisse empfängt.

TAPI erreicht diese Integration, indem anbieterspezifische Objekte mit den Standardobjekten TAPI, Address, Terminal, Call und CallHub aggregiert und unbekannte Methoden an diese anbieterspezifischen Objekte verteilt oder delegiert werden.

Beispielsweise kann ein Dienstanbieter Es Anwendungen ermöglichen, Informationen zu einem Aufruf abzurufen, die über das hinausgehen, was von der [**ITCallInfo-Schnittstelle**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) verfügbar gemacht wird. Der Anbieter muss eine Schnittstelle definieren, mit der Anwendungen diese zusätzlichen Abfragen durchführen und diese Schnittstelle für ein Objekt implementieren können. Dieses Objekt implementiert auch eine Anbieterschnittstelle für Informationsabfragen, sodass eine Anwendung ermitteln kann, welche Arten von anbieterspezifischen Funktionen verfügbar sein könnten.

Wenn die Anwendung einen Verweis auf ein Aufrufobjekt abruft, kann die Anwendung die neue anbieterspezifische Schnittstelle und ihre Methoden so verwenden, als ob sie vom Aufrufobjekt selbst implementiert würden.

Eine Liste aller MSP-Standardschnittstellen finden Sie in der [MSPI-Referenz (Media Service Provider Interface).](media-service-provider-interface-mspi-reference.md)

Eine Liste aller Schnittstellen, die für den [IPConf-MSP](ipconf-msp-interfaces.md) spezifisch sind, finden Sie unter IPConf-MSP-Schnittstellen.

 

 



