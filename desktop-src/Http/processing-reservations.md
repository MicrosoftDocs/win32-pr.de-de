---
title: Verarbeitungs Reservierungen
description: Reservierungen für Teile des URL-Namespace werden vom Systemadministrator vorgenommen und im permanenten Reservierungs Speicher abgelegt.
ms.assetid: deab6323-d114-463b-a0e7-acd173149b63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a0a78fd6d374ede14e0eba7c1b22ad33ba50648
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104391190"
---
# <a name="processing-reservations"></a><span data-ttu-id="68d63-103">Verarbeitungs Reservierungen</span><span class="sxs-lookup"><span data-stu-id="68d63-103">Processing Reservations</span></span>

<span data-ttu-id="68d63-104">Reservierungen für Teile des URL-Namespace werden vom Systemadministrator vorgenommen und im permanenten Reservierungs Speicher abgelegt.</span><span class="sxs-lookup"><span data-stu-id="68d63-104">Reservations for portions of the URL namespace are made by the system administrator and placed in the persistent reservation store.</span></span> <span data-ttu-id="68d63-105">Der Stamm des URL-Namespace für http ist der Systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="68d63-105">The root of the URL namespace for HTTP is owned by the system administrator.</span></span> <span data-ttu-id="68d63-106">Für alle Host-und Port Werte werden die beiden folgenden Reservierungen immer im Stamm des **relativeUri** -Namespace angenommen.</span><span class="sxs-lookup"><span data-stu-id="68d63-106">For all host and port values, the following two reservations are always assumed at the root of the **relativeUri** namespace.</span></span>



| <span data-ttu-id="68d63-107">Reservierter Namespace</span><span class="sxs-lookup"><span data-stu-id="68d63-107">Namespace reserved</span></span>                 | <span data-ttu-id="68d63-108">Reserviert für</span><span class="sxs-lookup"><span data-stu-id="68d63-108">Reserved for</span></span>              |
|------------------------------------|---------------------------|
| <span data-ttu-id="68d63-109"> https:// <host> :<port>/</span><span class="sxs-lookup"><span data-stu-id="68d63-109">https://<host>:<port>/</span></span>  | <span data-ttu-id="68d63-110">LocalSystem-Administrator</span><span class="sxs-lookup"><span data-stu-id="68d63-110">LocalSystem Administrator</span></span> |
| <span data-ttu-id="68d63-111"> https:// <host> :<port>/</span><span class="sxs-lookup"><span data-stu-id="68d63-111">https://<host>:<port>/</span></span> | <span data-ttu-id="68d63-112">LocalSystem-Administrator</span><span class="sxs-lookup"><span data-stu-id="68d63-112">LocalSystem Administrator</span></span> |



 

<span data-ttu-id="68d63-113">Diese impliziten Reservierungen können nicht entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="68d63-113">These implicit reservations cannot be removed.</span></span> <span data-ttu-id="68d63-114">Es ist jedoch möglich, explizite Stamm Reservierungen an andere Benutzer zu delegieren.</span><span class="sxs-lookup"><span data-stu-id="68d63-114">However, it is possible to delegate explicit root reservations to other users.</span></span> <span data-ttu-id="68d63-115">Durch Reservierungen wie die folgenden werden solche Delegierungen erstellt:</span><span class="sxs-lookup"><span data-stu-id="68d63-115">Reservations such as the following would create such delegations:</span></span>



| <span data-ttu-id="68d63-116">Reservierter Namespace</span><span class="sxs-lookup"><span data-stu-id="68d63-116">Namespace reserved</span></span>        | <span data-ttu-id="68d63-117">Reserviert für</span><span class="sxs-lookup"><span data-stu-id="68d63-117">Reserved for</span></span> |
|---------------------------|--------------|
| `https://+:80/`           | <span data-ttu-id="68d63-118">UserA, userc</span><span class="sxs-lookup"><span data-stu-id="68d63-118">UserA, UserC</span></span> |
| `https://adatum.com:443/` | <span data-ttu-id="68d63-119">UserB</span><span class="sxs-lookup"><span data-stu-id="68d63-119">UserB</span></span>        |



 

<span data-ttu-id="68d63-120">Wenn diese Delegierten Reservierungen vom Systemadministrator entfernt werden, wird der Besitz des-Namespaces auf die implizite Reservierung der entsprechenden Host-und Port Werte zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="68d63-120">If these delegated reservations are removed by the system administrator, ownership of the namespace reverts to the implicit reservation for the corresponding host and port values.</span></span>

 

 




