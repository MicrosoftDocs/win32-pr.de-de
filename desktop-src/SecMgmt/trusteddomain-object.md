---
description: Das Objekt "trustddomain" speichert Informationen zu einer Vertrauensstellung mit einer Domäne.
ms.assetid: fab69367-2143-49ef-a1b9-9c1d846fd4e1
title: Treuhänder-Domänen Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 837d8a9e56273a87b22b9697ef4e5917d73bcc81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862296"
---
# <a name="trusteddomain-object"></a><span data-ttu-id="c4788-103">Treuhänder-Domänen Objekt</span><span class="sxs-lookup"><span data-stu-id="c4788-103">TrustedDomain Object</span></span>

<span data-ttu-id="c4788-104">Das Objekt " **trustddomain** " speichert Informationen zu einer Vertrauensstellung mit einer Domäne.</span><span class="sxs-lookup"><span data-stu-id="c4788-104">The **TrustedDomain** object stores information about a trust relationship with a domain.</span></span> <span data-ttu-id="c4788-105">Auf dem vertrauenden System wird ein Vertrauensstellungs **Domänen** Objekt erstellt, mit dem ein Konto innerhalb der vertrauenswürdigen Domäne identifiziert wird, das zum Senden von Authentifizierungsanforderungen und zum Ausführen anderer Vorgänge, wie z. b. Name und [*Sicherheits*](/windows/desktop/SecGloss/s-gly) -ID (SID), verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c4788-105">A **TrustedDomain** object is created on the trusting system to identify an account within the trusted domain that can be used to submit authentication requests and to perform other operations, such as name and [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) translations.</span></span>

<span data-ttu-id="c4788-106">Zu den in einem " **Treuhänder Domain** "-Objekt gespeicherten Informationen gehören:</span><span class="sxs-lookup"><span data-stu-id="c4788-106">The information stored in a **TrustedDomain** object includes:</span></span>

-   <span data-ttu-id="c4788-107">Die SID der vertrauenswürdigen Domäne.</span><span class="sxs-lookup"><span data-stu-id="c4788-107">The SID of the trusted domain.</span></span> <span data-ttu-id="c4788-108">Diese Informationen können nicht geändert werden und müssen in allen " **Treuhänder Domain** "-Objekten eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="c4788-108">This information is not modifiable and must be unique among all **TrustedDomain** objects.</span></span>
-   <span data-ttu-id="c4788-109">Der Name der vertrauenswürdigen Domäne.</span><span class="sxs-lookup"><span data-stu-id="c4788-109">The name of the trusted domain.</span></span> <span data-ttu-id="c4788-110">Diese Informationen können nicht geändert werden und müssen in allen " **Treuhänder Domain** "-Objekten eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="c4788-110">This information is not modifiable and must be unique among all **TrustedDomain** objects.</span></span>
-   <span data-ttu-id="c4788-111">Der Name des Kontos in der vertrauenswürdigen Domäne, das zum Senden von Authentifizierungsanforderungen und zum Ausführen von Namen-und sid-Übersetzungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c4788-111">The name of the account in the trusted domain used to submit authentication requests and to perform name and SID translations.</span></span> <span data-ttu-id="c4788-112">Dieser Name kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="c4788-112">This name is not modifiable.</span></span>
-   <span data-ttu-id="c4788-113">Das Kennwort, mit dem Authentifizierungsanforderungen gesendet und Namens-und sid-Übersetzungen durchgeführt werden</span><span class="sxs-lookup"><span data-stu-id="c4788-113">The password used to submit authentication requests and perform name and SID translations.</span></span>

<span data-ttu-id="c4788-114">Weitere Informationen finden Sie [unter dem Objekttyp "Treuhänder Domäne](the-trusteddomain-object-type.md)".</span><span class="sxs-lookup"><span data-stu-id="c4788-114">For more information, see [The TrustedDomain Object Type](the-trusteddomain-object-type.md).</span></span>

 

 
