---
description: TAPI 3 unterstützt die Integration von Dienstanbieter spezifischen Schnittstellen in die Standardobjekte, sodass Anwendungen die anbieterspezifische Funktionalität nutzen können.
ms.assetid: 8077c9a7-3235-41a7-97dc-ca5f3c291ee6
title: Provider-Specific Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f95499f005c8c3b3e854f33835b9c9b183416d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050308"
---
# <a name="provider-specific-interfaces"></a>Provider-Specific Schnittstellen

TAPI 3 unterstützt die Integration von Dienstanbieter spezifischen Schnittstellen in die Standardobjekte, sodass Anwendungen die anbieterspezifische Funktionalität nutzen können. Darüber hinaus ermöglicht TAPI 3 Dienstanbietern, anbieterspezifische Ereignisse als COM-Objekte über die gleiche Schnittstelle zu liefern, auf der die Anwendung Standard Ereignisse empfängt.

TAPI erreicht diese Integration, indem anbieterspezifische Objekte mit den Standardobjekten – TAPI, Address, Terminal, Aufruf und callhub – aggiert werden und unbekannte Methoden an diese anbieterspezifischen Objekte weitergeleitet oder delegiert werden.

Beispielsweise kann ein Dienstanbieter zulassen, dass Anwendungen Informationen über einen Aufruf abrufen, der über die Schnittstelle der [**itcallinfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) -Schnittstelle hinausgeht. Der Anbieter muss eine Schnittstelle definieren, die es Anwendungen ermöglicht, diese zusätzlichen Abfragen vorzunehmen und diese Schnittstelle für ein Objekt zu implementieren. Dieses Objekt implementiert auch eine Schnittstelle für die Informationsabfrage des Anbieters, sodass eine Anwendung ermitteln kann, welche Arten von anbieterspezifischen Funktionen verfügbar sein könnten.

Wenn die Anwendung einen Verweis auf ein calltobjekt erhält, kann die Anwendung die neue anbieterspezifische Schnittstelle und ihre Methoden verwenden, als wären Sie durch das-Objekt selbst implementiert worden.

Eine Liste aller standardmäßigen MSP-Schnittstellen finden Sie unter [Referenz zur Media Service Provider Interface (MSPi)](media-service-provider-interface-mspi-reference.md) .

Unter [ipconf MSP Interfaces](ipconf-msp-interfaces.md) finden Sie eine Liste aller Schnittstellen, die für ipconf MSP spezifisch sind.

 

 



