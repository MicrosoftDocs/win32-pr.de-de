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
# <a name="provider-specific-interfaces"></a><span data-ttu-id="e3cd0-103">Provider-Specific Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="e3cd0-103">Provider-Specific Interfaces</span></span>

<span data-ttu-id="e3cd0-104">TAPI 3 unterstützt die Integration von Dienstanbieter spezifischen Schnittstellen in die Standardobjekte, sodass Anwendungen die anbieterspezifische Funktionalität nutzen können.</span><span class="sxs-lookup"><span data-stu-id="e3cd0-104">TAPI 3 supports integration of service provider-specific interfaces into the standard objects, allowing applications to take advantage of provider-specific functionality.</span></span> <span data-ttu-id="e3cd0-105">Darüber hinaus ermöglicht TAPI 3 Dienstanbietern, anbieterspezifische Ereignisse als COM-Objekte über die gleiche Schnittstelle zu liefern, auf der die Anwendung Standard Ereignisse empfängt.</span><span class="sxs-lookup"><span data-stu-id="e3cd0-105">Additionally, TAPI 3 allows service providers to deliver vendor-specific events to applications as COM objects over the same interface on which the application receives standard events.</span></span>

<span data-ttu-id="e3cd0-106">TAPI erreicht diese Integration, indem anbieterspezifische Objekte mit den Standardobjekten – TAPI, Address, Terminal, Aufruf und callhub – aggiert werden und unbekannte Methoden an diese anbieterspezifischen Objekte weitergeleitet oder delegiert werden.</span><span class="sxs-lookup"><span data-stu-id="e3cd0-106">TAPI achieves this integration by aggregating provider-specific objects with the standard objects – TAPI, Address, Terminal, Call, and CallHub – and dispatching or delegating unknown methods to these provider-specific objects.</span></span>

<span data-ttu-id="e3cd0-107">Beispielsweise kann ein Dienstanbieter zulassen, dass Anwendungen Informationen über einen Aufruf abrufen, der über die Schnittstelle der [**itcallinfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) -Schnittstelle hinausgeht.</span><span class="sxs-lookup"><span data-stu-id="e3cd0-107">For example, a service provider may allow applications to obtain information about a call beyond what is exposed by the [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) interface.</span></span> <span data-ttu-id="e3cd0-108">Der Anbieter muss eine Schnittstelle definieren, die es Anwendungen ermöglicht, diese zusätzlichen Abfragen vorzunehmen und diese Schnittstelle für ein Objekt zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="e3cd0-108">The vendor must define an interface that allows applications to make these extra queries and implement that interface on an object.</span></span> <span data-ttu-id="e3cd0-109">Dieses Objekt implementiert auch eine Schnittstelle für die Informationsabfrage des Anbieters, sodass eine Anwendung ermitteln kann, welche Arten von anbieterspezifischen Funktionen verfügbar sein könnten.</span><span class="sxs-lookup"><span data-stu-id="e3cd0-109">This object also implements a vendor information-querying interface so that an application can discover what sorts of provider-specific functions might be available.</span></span>

<span data-ttu-id="e3cd0-110">Wenn die Anwendung einen Verweis auf ein calltobjekt erhält, kann die Anwendung die neue anbieterspezifische Schnittstelle und ihre Methoden verwenden, als wären Sie durch das-Objekt selbst implementiert worden.</span><span class="sxs-lookup"><span data-stu-id="e3cd0-110">When the application obtains a reference to a call object, the application can use the new provider-specific interface and its methods as if they were implemented by the call object itself.</span></span>

<span data-ttu-id="e3cd0-111">Eine Liste aller standardmäßigen MSP-Schnittstellen finden Sie unter [Referenz zur Media Service Provider Interface (MSPi)](media-service-provider-interface-mspi-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="e3cd0-111">See [Media Service Provider Interface (MSPI) Reference](media-service-provider-interface-mspi-reference.md) for a list of all standard MSP interfaces.</span></span>

<span data-ttu-id="e3cd0-112">Unter [ipconf MSP Interfaces](ipconf-msp-interfaces.md) finden Sie eine Liste aller Schnittstellen, die für ipconf MSP spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="e3cd0-112">See [IPConf MSP Interfaces](ipconf-msp-interfaces.md) for a list of all interfaces specific to the IPConf MSP.</span></span>

 

 



