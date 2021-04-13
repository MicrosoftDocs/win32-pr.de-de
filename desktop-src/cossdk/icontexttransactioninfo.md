---
description: Bietet Zugriff auf Kontext Objekteigenschaften, die sich auf Transaktionen beziehen.
ms.assetid: 3b309153-be7d-444e-be23-777887f1ee95
title: Icontexttransaktioninfo-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: 499ab2371eda6dda6512b5fddb097d3adc2a6f05
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483438"
---
# <a name="icontexttransactioninfo-interface"></a><span data-ttu-id="91a45-103">Icontexttransaktioninfo-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="91a45-103">IContextTransactionInfo interface</span></span>

<span data-ttu-id="91a45-104">Bietet Zugriff auf Kontext Objekteigenschaften, die sich auf Transaktionen beziehen.</span><span class="sxs-lookup"><span data-stu-id="91a45-104">Provides access to context object properties that relate to transactions.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="91a45-105">Gründe für die Implementierung</span><span class="sxs-lookup"><span data-stu-id="91a45-105">When to implement</span></span>

<span data-ttu-id="91a45-106">Sie sollten diese Schnittstelle nicht implementieren.</span><span class="sxs-lookup"><span data-stu-id="91a45-106">You should not implement this interface.</span></span> <span data-ttu-id="91a45-107">Die Standard Implementierung bietet umfassende Funktionen.</span><span class="sxs-lookup"><span data-stu-id="91a45-107">The standard implementation provides complete functionality.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="91a45-108">Verwendung</span><span class="sxs-lookup"><span data-stu-id="91a45-108">When to use</span></span>

<span data-ttu-id="91a45-109">Verwenden Sie diese Schnittstelle für den Zugriff auf Kontext Objekteigenschaften, die sich auf Transaktionen beziehen.</span><span class="sxs-lookup"><span data-stu-id="91a45-109">Use this interface to access context object properties that relate to transactions.</span></span>

## <a name="members"></a><span data-ttu-id="91a45-110">Member</span><span class="sxs-lookup"><span data-stu-id="91a45-110">Members</span></span>

<span data-ttu-id="91a45-111">Die **icontexttransaktioninfo** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="91a45-111">The **IContextTransactionInfo** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="91a45-112">**Icontexttransaktioninfo** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="91a45-112">**IContextTransactionInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="91a45-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="91a45-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="91a45-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="91a45-114">Methods</span></span>

<span data-ttu-id="91a45-115">Die **icontexttransaktioninfo** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="91a45-115">The **IContextTransactionInfo** interface has these methods.</span></span>



| <span data-ttu-id="91a45-116">Methode</span><span class="sxs-lookup"><span data-stu-id="91a45-116">Method</span></span>                                                                                         | <span data-ttu-id="91a45-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="91a45-117">Description</span></span>                                                                                                                 |
|:-----------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="91a45-118">**Fetchtransaction**</span><span class="sxs-lookup"><span data-stu-id="91a45-118">**FetchTransaction**</span></span>](icontexttransactioninfo-registertransactionproxy.md)                   | <span data-ttu-id="91a45-119">Ruft ggf. den Transaktions-oder Transaktions Proxy ab, der dem aktuellen Kontext zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="91a45-119">Retrieves the transaction or transaction proxy that is associated with the current context, if any.</span></span><br/>              |
| [<span data-ttu-id="91a45-120">**Gettxisolationlevelandtimeout**</span><span class="sxs-lookup"><span data-stu-id="91a45-120">**GetTxIsolationLevelAndTimeout**</span></span>](icontexttransactioninfo-gettxisolationlevelandtimeout.md) | <span data-ttu-id="91a45-121">Ruft die Isolationsstufe und den Timeout Wert einer Transaktion ab, die im Stamm Transaktionskontext gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="91a45-121">Retrieves the isolation level and timeout value of a transaction that is hosted in the root transaction context.</span></span><br/> |
| [<span data-ttu-id="91a45-122">**Registertransaktionproxy**</span><span class="sxs-lookup"><span data-stu-id="91a45-122">**RegisterTransactionProxy**</span></span>](icontexttransactioninfo-fetchtransaction.md)                   | <span data-ttu-id="91a45-123">Ordnet eine [**itransaktionproxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) -Implementierung dem aktuellen Kontext zu.</span><span class="sxs-lookup"><span data-stu-id="91a45-123">Associates an [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) implementation with the current context.</span></span><br/>            |



 

## <a name="requirements"></a><span data-ttu-id="91a45-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91a45-124">Requirements</span></span>



| <span data-ttu-id="91a45-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="91a45-125">Requirement</span></span> | <span data-ttu-id="91a45-126">Wert</span><span class="sxs-lookup"><span data-stu-id="91a45-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="91a45-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="91a45-127">Minimum supported client</span></span><br/> | <span data-ttu-id="91a45-128">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91a45-128">Windows XP with SP2 \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="91a45-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="91a45-129">Minimum supported server</span></span><br/> | <span data-ttu-id="91a45-130">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91a45-130">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/> |



 

