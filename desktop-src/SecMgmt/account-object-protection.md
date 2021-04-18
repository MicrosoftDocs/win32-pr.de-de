---
description: Erläutert, wie Konto Objekte geschützt werden.
ms.assetid: a07ef46e-f4b6-4e21-bdd7-72d03e1c88b3
title: Konto Objektschutz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f495a3dc943ef73eef5074e0edc73247ceb02d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347511"
---
# <a name="account-object-protection"></a><span data-ttu-id="4fc1d-103">Konto Objektschutz</span><span class="sxs-lookup"><span data-stu-id="4fc1d-103">Account Object Protection</span></span>

<span data-ttu-id="4fc1d-104">[**Konto**](account-object.md) Objekte werden wie folgt geschützt:</span><span class="sxs-lookup"><span data-stu-id="4fc1d-104">[**Account**](account-object.md) objects are protected in the following fashion:</span></span>

-   <span data-ttu-id="4fc1d-105">Die Gruppe " **World** " hat eine generische \_ Ausführung.</span><span class="sxs-lookup"><span data-stu-id="4fc1d-105">The group **WORLD** has GENERIC\_EXECUTE.</span></span>
-   <span data-ttu-id="4fc1d-106">Der **lokale \_ Administrator** der Gruppe verfügt über DELETE \_ -, Generic Read-, generic \_ Write-, generic \_ Execute-und Write- \_ DACL-Zugriff.</span><span class="sxs-lookup"><span data-stu-id="4fc1d-106">The group **LOCAL\_ADMIN** has DELETE, GENERIC\_READ, GENERIC\_WRITE, GENERIC\_EXECUTE, and WRITE\_DACL access.</span></span>
-   <span data-ttu-id="4fc1d-107">Der **lokale \_ Administrator** der Gruppe wird als Besitzer und primäre Gruppe von Konto Objekten zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="4fc1d-107">The group **LOCAL\_ADMIN** is assigned as owner and primary group of Account objects.</span></span>

 

 



