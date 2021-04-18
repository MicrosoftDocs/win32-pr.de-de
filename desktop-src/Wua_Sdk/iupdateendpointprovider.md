---
description: Enthält die Methode, mit der ein Endpunkt zum Herstellen einer Verbindung mit einem Dienst verwendet wird.
ms.assetid: 4380776A-3B89-444B-B1E9-DCF640D0AEB4
title: Iupdateendpointprovider-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointProvider
api_type:
- COM
ms.openlocfilehash: 81e9481f5233fac05e7fa7bdf3afa53c4c55513a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345748"
---
# <a name="iupdateendpointprovider-interface"></a><span data-ttu-id="59b5a-103">Iupdateendpointprovider-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="59b5a-103">IUpdateEndpointProvider interface</span></span>

<span data-ttu-id="59b5a-104">Enthält die Methode, mit der ein Endpunkt zum Herstellen einer Verbindung mit einem Dienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="59b5a-104">Contains the method used to get an endpoint that is used to connect to a service.</span></span> <span data-ttu-id="59b5a-105">Diese Schnittstelle wird beim Schreiben eines Endpunkt Anbieters implementiert.</span><span class="sxs-lookup"><span data-stu-id="59b5a-105">This interface is implemented when writing an endpoint provider.</span></span>

## <a name="members"></a><span data-ttu-id="59b5a-106">Member</span><span class="sxs-lookup"><span data-stu-id="59b5a-106">Members</span></span>

<span data-ttu-id="59b5a-107">Die **iupdateendpointprovider** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="59b5a-107">The **IUpdateEndpointProvider** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="59b5a-108">**Iupdateendpointprovider** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="59b5a-108">**IUpdateEndpointProvider** also has these types of members:</span></span>

-   [<span data-ttu-id="59b5a-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="59b5a-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="59b5a-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="59b5a-110">Methods</span></span>

<span data-ttu-id="59b5a-111">Die **iupdateendpointprovider** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="59b5a-111">The **IUpdateEndpointProvider** interface has these methods.</span></span>



| <span data-ttu-id="59b5a-112">Methode</span><span class="sxs-lookup"><span data-stu-id="59b5a-112">Method</span></span>                                                                       | <span data-ttu-id="59b5a-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="59b5a-113">Description</span></span>                                                           |
|:-----------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="59b5a-114">**Getserviceendpoint**</span><span class="sxs-lookup"><span data-stu-id="59b5a-114">**GetServiceEndpoint**</span></span>](iupdateendpointauthprovider-getserviceendpoint.md) | <span data-ttu-id="59b5a-115">Fordert einen Endpunkt an, der zum Herstellen einer Verbindung mit einem Dienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="59b5a-115">Requests an endpoint that is used to connect to a service.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="59b5a-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="59b5a-116">Remarks</span></span>

<span data-ttu-id="59b5a-117">WUA Ruft die [**getserviceendpoint**](iupdateendpointauthprovider-getserviceendpoint.md) -Methode auf, um den Aushandlungs Prozess zu starten.</span><span class="sxs-lookup"><span data-stu-id="59b5a-117">WUA calls the [**GetServiceEndpoint**](iupdateendpointauthprovider-getserviceendpoint.md) method to start the negotiation process.</span></span> <span data-ttu-id="59b5a-118">Wenn der-Befehl durchgeführt wird, übergibt WUA die registrierten Tokentypen, und die Implementierung dieser Schnittstelle gibt die Tokentypen zurück, die verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="59b5a-118">When the call is made, WUA passes in the registered token types, and the implementation of this interface returns the token types that it prefers to use.</span></span>

 

 
