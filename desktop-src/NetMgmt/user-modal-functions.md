---
title: Modale Benutzer Funktionen
description: Die modalen Funktionen der Netzwerk Verwaltungs Benutzer erhalten und legen systemweite Parameter fest, die sich auf das Verhalten des Sicherheitssystems beziehen.
ms.assetid: e655b9f6-2808-4bd4-998c-c8a2e980920b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c65595f78a412196b9fd54030ec1ac1f1fb8ae59
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949048"
---
# <a name="user-modal-functions"></a><span data-ttu-id="01b87-103">Modale Benutzer Funktionen</span><span class="sxs-lookup"><span data-stu-id="01b87-103">User Modal Functions</span></span>

<span data-ttu-id="01b87-104">Die modalen Funktionen der Netzwerk Verwaltungs Benutzer erhalten und legen systemweite Parameter fest, die sich auf das Verhalten des Sicherheitssystems beziehen.</span><span class="sxs-lookup"><span data-stu-id="01b87-104">The network management user modal functions get and set system-wide parameters related to security system behavior.</span></span>

<span data-ttu-id="01b87-105">Die modalen Benutzer Funktionen sind nachfolgend aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="01b87-105">The user modal functions are listed following.</span></span>



| <span data-ttu-id="01b87-106">Funktion</span><span class="sxs-lookup"><span data-stu-id="01b87-106">Function</span></span>                                     | <span data-ttu-id="01b87-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="01b87-107">Description</span></span>                                                                                                                                                                                             |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01b87-108">**"Nettusermodalsget"**</span><span class="sxs-lookup"><span data-stu-id="01b87-108">**NetUserModalsGet**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget) | <span data-ttu-id="01b87-109">Gibt globale Informationen für alle Benutzer und globalen Gruppen in der Sicherheitsdatenbank zurück, bei der es sich um die SAM-Datenbank (Security Accounts Manager) handelt, oder, im Fall von Domänen Controllern, die Active Directory.</span><span class="sxs-lookup"><span data-stu-id="01b87-109">Returns global information for all users and global groups in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.</span></span> |
| [<span data-ttu-id="01b87-110">**"Nettusermodalsset"**</span><span class="sxs-lookup"><span data-stu-id="01b87-110">**NetUserModalsSet**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) | <span data-ttu-id="01b87-111">Legt globale Informationen für alle Benutzer und globalen Gruppen in der Sicherheitsdatenbank fest.</span><span class="sxs-lookup"><span data-stu-id="01b87-111">Sets global information for all users and global groups in the security database.</span></span>                                                                                                                       |



 

<span data-ttu-id="01b87-112">Die Funktionen " **nettusermodalsget** " und " **nettusermodalsset** " überprüfen und ändern die modalen Einstellungen, bei denen es sich um globale Parameter handelt, die sich auf jedes Konto in der Sicherheitsdatenbank auswirken (z. b. die minimal zulässige Kenn Wort Länge</span><span class="sxs-lookup"><span data-stu-id="01b87-112">The **NetUserModalsGet** and **NetUserModalsSet** functions examine and modify the modal settings, which are global parameters that affect every account in the security database (for example, the minimum allowable password length).</span></span> <span data-ttu-id="01b87-113">Alle modalen Einstellungen können durch Aufrufen von " **nettusermodalsset**" geändert werden.</span><span class="sxs-lookup"><span data-stu-id="01b87-113">All modal settings can be altered by calling **NetUserModalsSet**.</span></span> <span data-ttu-id="01b87-114">Die meisten modale können auch mit dem Befehl **net Accounts** geändert werden.</span><span class="sxs-lookup"><span data-stu-id="01b87-114">Most of the modals can also be altered by using the **net accounts** command.</span></span> <span data-ttu-id="01b87-115">Die modalen Funktionen der Netzwerk Verwaltungs Benutzer erfordern nicht, dass der Server über Sicherheit auf Benutzerebene verfügt.</span><span class="sxs-lookup"><span data-stu-id="01b87-115">The network management user modal functions do not require the server to have user-level security.</span></span>

<span data-ttu-id="01b87-116">Benutzer modale Informationen sind auf folgenden Ebenen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="01b87-116">User modal information is available at the following levels:</span></span>

-   [<span data-ttu-id="01b87-117">**Benutzer \_ modals \_ Info \_ 0**</span><span class="sxs-lookup"><span data-stu-id="01b87-117">**USER\_MODALS\_INFO\_0**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_0)
-   [<span data-ttu-id="01b87-118">**Benutzer \_ modals \_ Info \_ 1**</span><span class="sxs-lookup"><span data-stu-id="01b87-118">**USER\_MODALS\_INFO\_1**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1)
-   [<span data-ttu-id="01b87-119">**Benutzer- \_ modals \_ Info \_ 2**</span><span class="sxs-lookup"><span data-stu-id="01b87-119">**USER\_MODALS\_INFO\_2**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_2)
-   [<span data-ttu-id="01b87-120">**Benutzer \_ modals \_ Info \_ 3**</span><span class="sxs-lookup"><span data-stu-id="01b87-120">**USER\_MODALS\_INFO\_3**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_3)

<span data-ttu-id="01b87-121">Die folgenden Informationsebenen sind nur für ' [**nettusermodalsset**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) ' gültig und ersetzen die ältere Methode zum Übergeben eines *Parametern* zum Festlegen eines bestimmten Felds:</span><span class="sxs-lookup"><span data-stu-id="01b87-121">The following information levels are valid only for [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) and replace the older way of passing in a *Parmnum* to set a specific field:</span></span>

-   [<span data-ttu-id="01b87-122">**Benutzer- \_ modals- \_ Informationen \_ 1001**</span><span class="sxs-lookup"><span data-stu-id="01b87-122">**USER\_MODALS\_INFO\_1001**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1001)
-   [<span data-ttu-id="01b87-123">**Benutzer- \_ modals- \_ Informationen \_ 1002**</span><span class="sxs-lookup"><span data-stu-id="01b87-123">**USER\_MODALS\_INFO\_1002**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1002)
-   [<span data-ttu-id="01b87-124">**Benutzer- \_ modals- \_ Informationen \_ 1003**</span><span class="sxs-lookup"><span data-stu-id="01b87-124">**USER\_MODALS\_INFO\_1003**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1003)
-   [<span data-ttu-id="01b87-125">**Benutzer- \_ modals- \_ Informationen \_ 1004**</span><span class="sxs-lookup"><span data-stu-id="01b87-125">**USER\_MODALS\_INFO\_1004**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1004)
-   [<span data-ttu-id="01b87-126">**Benutzer- \_ modals- \_ Informationen \_ 1005**</span><span class="sxs-lookup"><span data-stu-id="01b87-126">**USER\_MODALS\_INFO\_1005**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1005)
-   [<span data-ttu-id="01b87-127">**Benutzer- \_ modals- \_ Informationen \_ 1006**</span><span class="sxs-lookup"><span data-stu-id="01b87-127">**USER\_MODALS\_INFO\_1006**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1006)
-   [<span data-ttu-id="01b87-128">**Benutzer- \_ modals- \_ Informationen \_ 1007**</span><span class="sxs-lookup"><span data-stu-id="01b87-128">**USER\_MODALS\_INFO\_1007**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1007)

<span data-ttu-id="01b87-129">Wenn Sie für Active Directory programmieren, können Sie möglicherweise bestimmte Active Directory Service Interface (ADSI)-Methoden aufrufen, um dieselbe Funktionalität zu erreichen, die Sie erreichen können, indem Sie die modalen Funktionen der Netzwerk Verwaltungs Benutzer aufrufen.</span><span class="sxs-lookup"><span data-stu-id="01b87-129">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management user modal functions.</span></span> <span data-ttu-id="01b87-130">Weitere Informationen finden Sie unter [**iadsdomain**](/windows/desktop/api/iads/nn-iads-iadsdomain).</span><span class="sxs-lookup"><span data-stu-id="01b87-130">For more information, see [**IADsDomain**](/windows/desktop/api/iads/nn-iads-iadsdomain).</span></span>

 

 