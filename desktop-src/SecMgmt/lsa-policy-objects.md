---
description: Die LSA speichert Informationen zu lokalen Sicherheitsrichtlinien in einem Satz von Objekten. Die Anwendung kann die lokale Sicherheitsrichtlinie Abfragen oder bearbeiten, indem Sie auf diese Objekte zugreift.
ms.assetid: c8ed5cd8-55cf-43e7-92a3-9bd17a1147a9
title: LSA-Richtlinien Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1481b6a6f49e973ecc2a2e1b53830bf22c67a77f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959861"
---
# <a name="lsa-policy-objects"></a><span data-ttu-id="a6dc4-104">LSA-Richtlinien Objekte</span><span class="sxs-lookup"><span data-stu-id="a6dc4-104">LSA Policy Objects</span></span>

<span data-ttu-id="a6dc4-105">Die LSA speichert Informationen zu lokalen Sicherheitsrichtlinien in einem Satz von Objekten.</span><span class="sxs-lookup"><span data-stu-id="a6dc4-105">The LSA stores local security policy information in a set of objects.</span></span> <span data-ttu-id="a6dc4-106">Die Anwendung kann die lokale Sicherheitsrichtlinie Abfragen oder bearbeiten, indem Sie auf diese Objekte zugreift.</span><span class="sxs-lookup"><span data-stu-id="a6dc4-106">Your application can query or edit the local security policy by accessing these objects.</span></span>

<span data-ttu-id="a6dc4-107">Der Satz besteht aus den folgenden vier Objekten:</span><span class="sxs-lookup"><span data-stu-id="a6dc4-107">The set consists of the following four objects:</span></span>

-   <span data-ttu-id="a6dc4-108">Die [Richtlinie](policy-object.md) enthält Informationen zur globalen Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="a6dc4-108">[Policy](policy-object.md) contains global policy information.</span></span>
-   <span data-ttu-id="a6dc4-109">" [Treuhänder Domäne](trusteddomain-object.md) " enthält Informationen zu einer vertrauenswürdigen Domäne.</span><span class="sxs-lookup"><span data-stu-id="a6dc4-109">[TrustedDomain](trusteddomain-object.md) contains information about a trusted domain.</span></span>
-   <span data-ttu-id="a6dc4-110">Das [Konto](account-object.md) enthält Informationen zu einem Benutzer-, Gruppen-oder lokalen Gruppenkonto.</span><span class="sxs-lookup"><span data-stu-id="a6dc4-110">[Account](account-object.md) contains information about a user, group, or local group account.</span></span>
-   <span data-ttu-id="a6dc4-111">[Private Daten](private-data-object.md) enthalten geschützte Informationen, wie z. b. Server Konto Kennwörter.</span><span class="sxs-lookup"><span data-stu-id="a6dc4-111">[Private Data](private-data-object.md) contains protected information, such as server account passwords.</span></span> <span data-ttu-id="a6dc4-112">Diese Informationen werden als verschlüsselte Zeichen folgen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a6dc4-112">This information is stored as encrypted strings.</span></span>

<span data-ttu-id="a6dc4-113">Weitere Informationen zur Verwendung der LSA-Richtlinien Funktionen zum Verwalten der in diesen Objekten gespeicherten Informationen finden [Sie unter Verwenden der LSA-Richtlinie](using-lsa-policy.md).</span><span class="sxs-lookup"><span data-stu-id="a6dc4-113">For more information on how to use the LSA Policy functions to manage the information stored in these objects, see [Using LSA Policy](using-lsa-policy.md).</span></span>

 

 



