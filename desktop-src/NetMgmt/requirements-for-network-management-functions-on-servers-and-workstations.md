---
title: Anforderungen an Netzwerk Verwaltungsfunktionen auf Servern und Arbeitsstationen
description: Wenn Sie eine der in diesem Thema aufgeführten Netzwerk Verwaltungsfunktionen auf einem Server oder einer Arbeitsstation aufrufen, gelten für Informations Abfragen und Informations Aktualisierungen andere Zugriffs Anforderungen.
ms.assetid: 05ff1771-8058-4c86-8f45-735bf41dc128
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b06e516aa06465c67966cc076a0ca524d4ae4003
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858428"
---
# <a name="requirements-for-network-management-functions-on-servers-and-workstations"></a><span data-ttu-id="01961-103">Anforderungen an Netzwerk Verwaltungsfunktionen auf Servern und Arbeitsstationen</span><span class="sxs-lookup"><span data-stu-id="01961-103">Requirements for Network Management Functions on Servers and Workstations</span></span>

<span data-ttu-id="01961-104">Wenn Sie eine der in diesem Thema aufgeführten Netzwerk Verwaltungsfunktionen auf einem Server oder einer Arbeitsstation aufrufen, gelten für Informations Abfragen und Informations Aktualisierungen andere Zugriffs Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="01961-104">If you call one of the network management functions listed in this topic on a server or workstation, different access requirements apply to information queries and information updates.</span></span>

## <a name="queries"></a><span data-ttu-id="01961-105">Abfragen</span><span class="sxs-lookup"><span data-stu-id="01961-105">Queries</span></span>

<span data-ttu-id="01961-106">Wenn Sie eine der folgenden Funktionen zum Ausführen einer Abfrage auf einem Server oder einer Arbeitsstation aufzurufen, können alle authentifizierten Benutzer standardmäßig die Informationen lesen und auflisten.</span><span class="sxs-lookup"><span data-stu-id="01961-106">If you call one of the following functions to perform a query on a server or workstation, by default, all authenticated users can read and enumerate the information.</span></span>

-   <span data-ttu-id="01961-107">[**Netgroupum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum), [**netgroupgetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo), [**netgroupgetusers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers)</span><span class="sxs-lookup"><span data-stu-id="01961-107">[**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum), [**NetGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo), [**NetGroupGetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers)</span></span>
-   <span data-ttu-id="01961-108">[**Netlocalgroupum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum), [**netlocalgroupgetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo), [**netlocalgroupgetmembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers)</span><span class="sxs-lookup"><span data-stu-id="01961-108">[**NetLocalGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum), [**NetLocalGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo), [**NetLocalGroupGetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers)</span></span>
-   [<span data-ttu-id="01961-109">**NetQueryDisplayInformation**</span><span class="sxs-lookup"><span data-stu-id="01961-109">**NetQueryDisplayInformation**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)
-   <span data-ttu-id="01961-110">" [**Nettessiongetinfo**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) " (nur Stufen 1 und 2)</span><span class="sxs-lookup"><span data-stu-id="01961-110">[**NetSessionGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) (levels 1 and 2 only)</span></span>
-   <span data-ttu-id="01961-111">[**Netshareaufumum**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum) (nur Ebenen 2 und 502)</span><span class="sxs-lookup"><span data-stu-id="01961-111">[**NetShareEnum**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum) (levels 2 and 502 only)</span></span>
-   <span data-ttu-id="01961-112">" [**Nettuserenum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum)", " [**nettusergetgroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups)", " [**nettusergetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo)", " [**nettusergetlocalgroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups)", " [**nettusermodalsget**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget) "</span><span class="sxs-lookup"><span data-stu-id="01961-112">[**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum), [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups), [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo), [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups), [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget)</span></span>
-   <span data-ttu-id="01961-113">[**Netwkstagetinfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo), [ **netwkstausererium**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)</span><span class="sxs-lookup"><span data-stu-id="01961-113">[**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo), [**NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)</span></span>

<span data-ttu-id="01961-114">Im folgenden finden Sie weitere Informationen über den anonymen Zugriff beim Lesen und Auflisten von Informationen.</span><span class="sxs-lookup"><span data-stu-id="01961-114">Following is additional information about anonymous access when reading and enumerating information.</span></span>

<span data-ttu-id="01961-115">**Windows Server 2003 und Windows XP:** Anonymer Zugriff auf Informationen ist möglich, wenn die Richtlinien Einstellung "everyoneincludesanall" den anonymen Zugriff zulässt.</span><span class="sxs-lookup"><span data-stu-id="01961-115">**Windows Server 2003 and Windows XP:** Anonymous access to information is possible if the EveryoneIncludesAnonymous policy setting allows anonymous access.</span></span>

<span data-ttu-id="01961-116">**Windows 2000:** Der anonyme Zugriff auf Sicherungs fähige Objekte ist möglich, wenn die einschränier Bare Richtlinien Einstellung anonymen Zugriff zulässt.</span><span class="sxs-lookup"><span data-stu-id="01961-116">**Windows 2000:** Anonymous access to securable objects is possible if the RestrictAnonymous policy setting allows anonymous access.</span></span> <span data-ttu-id="01961-117">Sie können den anonymen Zugriff einschränken, indem Sie den folgenden Schlüssel in der Registrierung auf den Wert 1 festlegen.</span><span class="sxs-lookup"><span data-stu-id="01961-117">You can restrict anonymous access by setting the following key in the registry to the value 1.</span></span>

<span data-ttu-id="01961-118">**HKEY \_ Lokales \_ Computer \\ System \\ CurrentControlSet \\ Control \\ LSA** \\ **restrictanfts=** 1</span><span class="sxs-lookup"><span data-stu-id="01961-118">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\Lsa**\\**RestrictAnonymous** = 1</span></span>

<span data-ttu-id="01961-119">Weitere Informationen finden Sie im folgenden Artikel in der Microsoft Knowledge Base:</span><span class="sxs-lookup"><span data-stu-id="01961-119">For more information, see the following article in the Microsoft Knowledge Base:</span></span>

<span data-ttu-id="01961-120">Artikel-ID: [Q246261](https://support.microsoft.com/kb/246261)</span><span class="sxs-lookup"><span data-stu-id="01961-120">ARTICLE ID: [Q246261](https://support.microsoft.com/kb/246261)</span></span>

<span data-ttu-id="01961-121">Title: Verwenden des einschrändenden Registrierungs Werts.</span><span class="sxs-lookup"><span data-stu-id="01961-121">TITLE: How to use the RestrictAnonymous registry Value.</span></span>

## <a name="updates"></a><span data-ttu-id="01961-122">Aktualisierungen</span><span class="sxs-lookup"><span data-stu-id="01961-122">Updates</span></span>

<span data-ttu-id="01961-123">Standardmäßig können nur Administratoren und Hauptbenutzer Informationen schreiben.</span><span class="sxs-lookup"><span data-stu-id="01961-123">By default, only Administrators and Power Users can write information.</span></span>

<span data-ttu-id="01961-124">Weitere Informationen zum Steuern des Zugriffs auf Sicherungs fähige Objekte finden Sie unter [Access Control](/windows/desktop/SecAuthZ/access-control), [Berechtigungen](/windows/desktop/SecAuthZ/privileges)und Sicherungs [fähige Objekte](/windows/desktop/SecAuthZ/securable-objects).</span><span class="sxs-lookup"><span data-stu-id="01961-124">For more information about controlling access to securable objects, see [Access Control](/windows/desktop/SecAuthZ/access-control), [Privileges](/windows/desktop/SecAuthZ/privileges), and [Securable Objects](/windows/desktop/SecAuthZ/securable-objects).</span></span> <span data-ttu-id="01961-125">Weitere Informationen zum Aufrufen von Funktionen, für die Administratorrechte erforderlich sind, finden Sie unter [Ausführen mit speziellen Berechtigungen](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="01961-125">For more information about calling functions that require administrator privileges, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

 

 