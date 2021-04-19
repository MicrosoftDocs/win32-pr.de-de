---
description: Wenn ein Treuhänder-Domänen Objekt erstellt wird, wird ihm ein Standardschutz zugewiesen.
ms.assetid: cc554630-7be7-4657-90f2-ce5fa81731b2
title: Schutz von treuhänddomain-Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd27a01c1bcfde12fd062f2e8ae7c92a979991a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353038"
---
# <a name="trusteddomain-object-protection"></a><span data-ttu-id="89f7d-103">Schutz von treuhänddomain-Objekten</span><span class="sxs-lookup"><span data-stu-id="89f7d-103">TrustedDomain Object Protection</span></span>

<span data-ttu-id="89f7d-104">Wenn ein " [**Treuhänder**](trusteddomain-object.md) "-Objekt erstellt wird, wird ihm ein Standardschutz wie folgt zugewiesen:</span><span class="sxs-lookup"><span data-stu-id="89f7d-104">When a [**TrustedDomain**](trusteddomain-object.md) object is created, it is assigned a standard protection as follows:</span></span>

-   <span data-ttu-id="89f7d-105">Der lokalen Gruppe "World" wird generischer \_ Ausführungs Zugriff gewährt.</span><span class="sxs-lookup"><span data-stu-id="89f7d-105">The WORLD local group is granted GENERIC\_EXECUTE access.</span></span>
-   <span data-ttu-id="89f7d-106">Der lokalen \_ Gruppe "Administratoren" werden löschen, generischer \_ Lesezugriff, generischer \_ Schreibzugriff und generischer \_ Ausführungs Zugriff gewährt.</span><span class="sxs-lookup"><span data-stu-id="89f7d-106">The LOCAL\_ADMIN local group is granted DELETE, GENERIC\_READ, GENERIC\_WRITE, and GENERIC\_EXECUTE access.</span></span>
-   <span data-ttu-id="89f7d-107">Die lokale \_ Gruppe "Administratoren" wird als Besitzer und primäre Gruppe des Objekts zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="89f7d-107">The LOCAL\_ADMIN local group is assigned as owner and primary group of the object.</span></span>

 

 



