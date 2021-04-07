---
title: Veröffentlichen mit dem RPC-Namensdienst
description: RPC-Dienste können Ihre Bezeichner in einem Namespace mithilfe der RPC-Namen Dienst-APIs (RpcNs) veröffentlichen.
ms.assetid: 0c8e1207-daeb-4dc8-b83a-a54cd59a46a7
ms.tgt_platform: multiple
keywords:
- Veröffentlichen mit dem RPC-Namensdienst AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b672eec6308d709fe2f4cbc64ad22ecf0d6edd
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038742"
---
# <a name="publishing-with-the-rpc-name-service"></a><span data-ttu-id="c974e-104">Veröffentlichen mit dem RPC-Namensdienst</span><span class="sxs-lookup"><span data-stu-id="c974e-104">Publishing with the RPC Name Service</span></span>

<span data-ttu-id="c974e-105">RPC-Dienste können Ihre Bezeichner in einem Namespace mithilfe der RPC-Namen Dienst-APIs (RpcNs) veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="c974e-105">RPC services can publish their identifiers in a namespace using the RPC name service (RpcNs) APIs.</span></span> <span data-ttu-id="c974e-106">Die RpcNs-APIs in Windows 2000 veröffentlichen die RPC-Einträge in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="c974e-106">The RpcNs APIs in Windows 2000 publish the RPC entries in Active Directory Domain Services.</span></span> <span data-ttu-id="c974e-107">-Dienste erstellen RPC-Bindungen und veröffentlichen Sie im-Namespace als RPC-Server Einträge mit Attributen, einschließlich der eindeutigen Schnittstellen-ID, einer GUID, die von Clients erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="c974e-107">Services create RPC bindings and publish them in the namespace as named RPC Server entries with attributes including the unique interface ID, a GUID that is recognized by clients.</span></span> <span data-ttu-id="c974e-108">Ein Client kann dann nach RPC-Servern suchen, die die gewünschte Schnittstelle anbieten, die Bindung importieren und eine Verbindung mit dem Server herstellen.</span><span class="sxs-lookup"><span data-stu-id="c974e-108">A client can then search for RPC Servers offering the desired interface, import the binding, and connect to the server.</span></span>

<span data-ttu-id="c974e-109">Weitere Informationen zum Veröffentlichen eines RPC-Dienstanbieter finden Sie unter [Server seitige Bindung](/windows/desktop/Rpc/server-side-binding).</span><span class="sxs-lookup"><span data-stu-id="c974e-109">For more information about publishing an RPC service, see [Server-side Binding](/windows/desktop/Rpc/server-side-binding).</span></span>

 

 