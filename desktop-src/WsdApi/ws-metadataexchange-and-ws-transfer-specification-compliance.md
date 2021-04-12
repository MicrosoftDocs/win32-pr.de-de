---
description: Vor August 2006 haben WS-MetadataExchange eine eigene Get Metadata Exchange-Methode definiert, die von Geräte Profilen für Webdienste (DPWS) verwendet wurde.
ms.assetid: 2441beac-ee40-405a-8e98-8b8d65477911
title: Konformität von WS-MetadataExchange und WS-Transfer Spezifikation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e6ecad5224256f35b2157088ce091e8bd5751c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130956"
---
# <a name="ws-metadataexchange-and-ws-transfer-specification-compliance"></a><span data-ttu-id="efe2e-103">Konformität von WS-MetadataExchange und WS-Transfer Spezifikation</span><span class="sxs-lookup"><span data-stu-id="efe2e-103">WS-MetadataExchange and WS-Transfer Specification Compliance</span></span>

<span data-ttu-id="efe2e-104">Vor August 2006 hat [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/) seine eigene [Get](get--metadata-exchange--http-request-and-message.md) Metadata Exchange-Methode definiert, die von [Geräte Profilen für Webdienste](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="efe2e-104">Before August 2006, [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/) defined its own [Get](get--metadata-exchange--http-request-and-message.md) metadata exchange method, which was used by [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span></span> <span data-ttu-id="efe2e-105">Die WS-MetadataExchange Specification Version 1,1 hat diese Methode durch die in der WS-Transfer Spezifikation definierte Get-Methode ersetzt.</span><span class="sxs-lookup"><span data-stu-id="efe2e-105">The WS-MetadataExchange specification version 1.1 replaced this method with the Get method defined in the WS-Transfer specification.</span></span>

<span data-ttu-id="efe2e-106">Im aktuellen Modell stellt WS-Transfer die [Get](get--metadata-exchange--http-request-and-message.md) -Methode bereit und macht keinen Verweis auf den Typ des Texts.</span><span class="sxs-lookup"><span data-stu-id="efe2e-106">In the current model, WS-Transfer provides the [Get](get--metadata-exchange--http-request-and-message.md) method and makes no reference to the type of the body.</span></span> <span data-ttu-id="efe2e-107">In WS-MetadataExchange wird das Format des Texts und ein Mechanismus zum Verpacken mehrerer Metadatenelemente in einer einzelnen Antwort beschrieben. Außerdem werden in DPWS bestimmte Metadatenelemente beschrieben, die ein Dienst in eine metadatenantwort einschließen sollte.</span><span class="sxs-lookup"><span data-stu-id="efe2e-107">WS-MetadataExchange describes the format of the body and a mechanism for packaging multiple pieces of metadata in a single response, and DPWS describes specific pieces of metadata that a service should include in a metadata response.</span></span>

<span data-ttu-id="efe2e-108">WSDAPI unterstützt die WS-Transfer Spezifikation nicht vollständig.</span><span class="sxs-lookup"><span data-stu-id="efe2e-108">WSDAPI does not fully support the WS-Transfer specification.</span></span> <span data-ttu-id="efe2e-109">Da nur die [Get](get--metadata-exchange--http-request-and-message.md) -Methode für Geräte erforderlich ist, sind keine anderen Teile der WS-Transfer implementiert.</span><span class="sxs-lookup"><span data-stu-id="efe2e-109">Because only the [Get](get--metadata-exchange--http-request-and-message.md) method is required for devices, no other portions of WS-Transfer have been implemented.</span></span> <span data-ttu-id="efe2e-110">Außerdem implementiert WSDAPI nicht die optionale GetMetadata-Methode, die in WS-MetadataExchange beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="efe2e-110">Also, WSDAPI does not implement the optional GetMetadata method described in WS-MetadataExchange.</span></span>

 

 



