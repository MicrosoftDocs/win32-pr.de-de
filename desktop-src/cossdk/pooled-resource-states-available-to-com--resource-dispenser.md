---
description: In einem Pool zusammengefasste Ressourcen Zustände für com+-Ressourcen Spender verfügbar
ms.assetid: 5037f11c-d113-49b0-b26f-0e3bc59ae8b3
title: In einem Pool zusammengefasste Ressourcen Zustände für com+-Ressourcen Spender verfügbar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff0bc59dcc2b7e95e060c0d6e96a5880d09d26e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483430"
---
# <a name="pooled-resource-states-available-to-com-resource-dispenser"></a><span data-ttu-id="67522-103">In einem Pool zusammengefasste Ressourcen Zustände für com+-Ressourcen Spender verfügbar</span><span class="sxs-lookup"><span data-stu-id="67522-103">Pooled Resource States Available to COM+ Resource Dispenser</span></span>

<span data-ttu-id="67522-104">Eine Ressource wird zu einem beliebigen Zeitpunkt entweder verwendet oder nicht verwendet und ist entweder eingetragen oder nicht in eine Transaktion eingetragen.</span><span class="sxs-lookup"><span data-stu-id="67522-104">At any one time, a resource is either in use or not in use and is either enlisted or not enlisted in a transaction.</span></span> <span data-ttu-id="67522-105">Dies ergibt vier mögliche Ressourcen Zustände, wie im folgenden dargestellt:</span><span class="sxs-lookup"><span data-stu-id="67522-105">This yields four possible resource states, as follows:</span></span>

-   <span data-ttu-id="67522-106">**Ressourcen in der aufgelistete Inventur.**</span><span class="sxs-lookup"><span data-stu-id="67522-106">**Resources in unenlisted inventory.**</span></span> <span data-ttu-id="67522-107">Eine Ressource, die nicht von einem Objekt verwendet wird und nicht in einer Transaktion eingetragen ist, befindet sich in der aufgelistete Inventur.</span><span class="sxs-lookup"><span data-stu-id="67522-107">A resource that is not in use by an object and not enlisted in a transaction is in unenlisted inventory.</span></span> <span data-ttu-id="67522-108">Eine Ressource im allgemeinen bestand ist für die Zuweisung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="67522-108">A resource in general inventory is available for assignment.</span></span>

-   <span data-ttu-id="67522-109">**Ressourcen in der eingetragenen Inventur.**</span><span class="sxs-lookup"><span data-stu-id="67522-109">**Resources in enlisted inventory.**</span></span> <span data-ttu-id="67522-110">Eine Ressource, die nicht von einem Objekt verwendet wird, sondern in einer Transaktion eingetragen ist, befindet sich in der eingetragenen Inventur.</span><span class="sxs-lookup"><span data-stu-id="67522-110">A resource that is not in use by an object but is enlisted in a transaction is in enlisted inventory.</span></span> <span data-ttu-id="67522-111">Eine solche Ressource steht nur für Objekte zur Verfügung, die in derselben Transaktion ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="67522-111">Such a resource is available for assignment only to objects running in the same transaction.</span></span> <span data-ttu-id="67522-112">Eine Ressource wird von der eingetragenen Inventur in die Registrierung eingetragen, wenn com+ den Dispenser-Manager benachrichtigt, dass die Transaktion abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="67522-112">A resource moves from enlisted inventory to unenlisted inventory when COM+ notifies the dispenser manager that the transaction is complete.</span></span>

-   <span data-ttu-id="67522-113">**Ressourcen in der aufgelistete Verwendung.**</span><span class="sxs-lookup"><span data-stu-id="67522-113">**Resources in unenlisted use.**</span></span> <span data-ttu-id="67522-114">Wenn eine Ressource einem Objekt zugewiesen ist und die Instanz nicht in einer Transaktion ausgeführt wird oder der Ressourcen Verteiler die Ressource als nicht transaktional identifiziert hat, befindet sich diese Ressource in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="67522-114">If a resource is assigned to an object and the instance is not running in a transaction or the resource dispenser has identified the resource as non-transactional, this resource is in unenlisted use.</span></span>

-   <span data-ttu-id="67522-115">**In eingetragene Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="67522-115">**Resources in enlisted use.**</span></span> <span data-ttu-id="67522-116">Wenn eine Ressource einem Objekt zugewiesen ist, wird die Instanz in einer Transaktion ausgeführt, und der Ressourcen Verteiler hat die Ressource erfolgreich in die Transaktion eingetragen. diese Ressource wird in eingetragen verwendet.</span><span class="sxs-lookup"><span data-stu-id="67522-116">If a resource is assigned to an object, the instance is running in a transaction, and the resource dispenser has successfully enlisted the resource in the transaction, this resource is in enlisted use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="67522-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="67522-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67522-118">Konzepte des com+-Ressourcen Verteilers</span><span class="sxs-lookup"><span data-stu-id="67522-118">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> <dt>

[<span data-ttu-id="67522-119">Eintragen einer Ressource in eine Transaktion</span><span class="sxs-lookup"><span data-stu-id="67522-119">Enlisting a Resource in a Transaction</span></span>](enlisting-a-resource-in-a-transaction.md)
</dt> </dl>

 

 



