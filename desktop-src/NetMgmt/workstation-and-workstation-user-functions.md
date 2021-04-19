---
title: Benutzer Funktionen für Arbeitsstationen und Arbeitsstationen
description: Die Arbeitsstationen der Netzwerk Verwaltungs Arbeitsstation führen administrative Aufgaben auf einer lokalen oder Remote Arbeitsstation aus.
ms.assetid: cc400f43-297b-4ff4-8353-b268839c48b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd445746bca51abaa0cd72877bdf03dd4d00d338
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339509"
---
# <a name="workstation-and-workstation-user-functions"></a><span data-ttu-id="4cf36-103">Benutzer Funktionen für Arbeitsstationen und Arbeitsstationen</span><span class="sxs-lookup"><span data-stu-id="4cf36-103">Workstation and Workstation User Functions</span></span>

<span data-ttu-id="4cf36-104">Die Arbeitsstationen der Netzwerk Verwaltungs Arbeitsstation führen administrative Aufgaben auf einer lokalen oder Remote Arbeitsstation aus.</span><span class="sxs-lookup"><span data-stu-id="4cf36-104">The network management workstation functions perform administrative tasks on a local or remote workstation.</span></span> <span data-ttu-id="4cf36-105">Nur ein Benutzer oder eine Anwendung mit Administrator Gruppenmitgliedschaft auf einem lokalen Server oder einem Remote Server kann administrative Aufgaben auf einer Arbeitsstation ausführen, um den Betrieb, den Benutzer Zugriff und die Ressourcen Freigabe zu steuern.</span><span class="sxs-lookup"><span data-stu-id="4cf36-105">Only a user or application with admin group membership, on a local or remote server, can perform administrative tasks on a workstation to control its operation, user access, and resource sharing.</span></span> <span data-ttu-id="4cf36-106">Weitere Informationen zum Aufrufen von Funktionen, für die Administratorrechte erforderlich sind, finden Sie unter [Ausführen mit speziellen Berechtigungen](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="4cf36-106">For more information about calling functions that require administrator privileges, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

<span data-ttu-id="4cf36-107">Die Arbeitsstations Funktionen sind nachfolgend aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="4cf36-107">The workstation functions are listed following.</span></span>



| <span data-ttu-id="4cf36-108">Funktion</span><span class="sxs-lookup"><span data-stu-id="4cf36-108">Function</span></span>                                   | <span data-ttu-id="4cf36-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4cf36-109">Description</span></span>                                                             |
|--------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="4cf36-110">**Netwkstagetinfo**</span><span class="sxs-lookup"><span data-stu-id="4cf36-110">**NetWkstaGetInfo**</span></span>](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo) | <span data-ttu-id="4cf36-111">Gibt Informationen zu den Konfigurationselementen für eine Arbeitsstation zurück.</span><span class="sxs-lookup"><span data-stu-id="4cf36-111">Returns information about the configuration elements for a workstation.</span></span> |
| [<span data-ttu-id="4cf36-112">**Netwkstasetinfo**</span><span class="sxs-lookup"><span data-stu-id="4cf36-112">**NetWkstaSetInfo**</span></span>](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstasetinfo) | <span data-ttu-id="4cf36-113">Konfiguriert eine Arbeitsstation.</span><span class="sxs-lookup"><span data-stu-id="4cf36-113">Configures a workstation.</span></span>                                               |



 

<span data-ttu-id="4cf36-114">Die Arbeitsstations Funktionen ermöglichen den Zugriff auf zwei diskrete Typen von Arbeitsstations Informationen:</span><span class="sxs-lookup"><span data-stu-id="4cf36-114">The workstation functions allow access to two discrete types of workstation information:</span></span>

-   <span data-ttu-id="4cf36-115">Systeminformationen</span><span class="sxs-lookup"><span data-stu-id="4cf36-115">System information</span></span>
-   <span data-ttu-id="4cf36-116">Plattformspezifische Informationen</span><span class="sxs-lookup"><span data-stu-id="4cf36-116">Platform-specific information</span></span>

<span data-ttu-id="4cf36-117">Innerhalb jedes Typs werden die Daten nach Sicherheits Zugriff kategorisiert.</span><span class="sxs-lookup"><span data-stu-id="4cf36-117">Within each type the data is categorized by security access.</span></span> <span data-ttu-id="4cf36-118">Daten, auf die der Gast Zugriff hat, sind eine Teilmenge der Daten, auf die der Benutzer zugreifen kann, was wiederum eine Teilmenge der Daten ist, auf die vom Administrator zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="4cf36-118">Data that is guest-accessible is a subset of the data that is user-accessible, which is in turn a subset of the admin-accessible data.</span></span>

<span data-ttu-id="4cf36-119">Arbeitsstations Informationen sind auf folgenden Ebenen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="4cf36-119">Workstation information is available at the following levels:</span></span>

-   [<span data-ttu-id="4cf36-120">**Wksta- \_ Informationen \_ 100**</span><span class="sxs-lookup"><span data-stu-id="4cf36-120">**WKSTA\_INFO\_100**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_100)
-   [<span data-ttu-id="4cf36-121">**Wksta- \_ Informationen \_ 101**</span><span class="sxs-lookup"><span data-stu-id="4cf36-121">**WKSTA\_INFO\_101**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_101)
-   [<span data-ttu-id="4cf36-122">**Wksta- \_ Informationen \_ 102**</span><span class="sxs-lookup"><span data-stu-id="4cf36-122">**WKSTA\_INFO\_102**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_102)

<span data-ttu-id="4cf36-123">Die Benutzer Funktionen der Netzwerk Verwaltungs Arbeitsstation ermöglichen den Zugriff auf benutzerspezifische Informationen.</span><span class="sxs-lookup"><span data-stu-id="4cf36-123">The network management workstation user functions allow access to user-specific information.</span></span> <span data-ttu-id="4cf36-124">Die benutzerspezifischen Informationen werden von den Arbeitsstations Informationen getrennt, da es mehr als einen Benutzer auf einer Arbeitsstation geben kann.</span><span class="sxs-lookup"><span data-stu-id="4cf36-124">The user-specific information is separated from the workstation information because there can be more than one user on a workstation.</span></span>

<span data-ttu-id="4cf36-125">Die Benutzer Funktionen der Arbeitsstation sind nachfolgend aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="4cf36-125">The workstation user functions are listed following.</span></span>



| <span data-ttu-id="4cf36-126">Funktion</span><span class="sxs-lookup"><span data-stu-id="4cf36-126">Function</span></span>                                           | <span data-ttu-id="4cf36-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4cf36-127">Description</span></span>                                                                         |
|----------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="4cf36-128">**Netwkstauserereration**</span><span class="sxs-lookup"><span data-stu-id="4cf36-128">**NetWkstaUserEnum**</span></span>](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)       | <span data-ttu-id="4cf36-129">Listet Informationen zu allen Benutzern, die zurzeit auf der Arbeitsstation angemeldet sind.</span><span class="sxs-lookup"><span data-stu-id="4cf36-129">Lists information about all users currently logged on to the workstation.</span></span>           |
| [<span data-ttu-id="4cf36-130">**NetWkstaUserGetInfo**</span><span class="sxs-lookup"><span data-stu-id="4cf36-130">**NetWkstaUserGetInfo**</span></span>](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausergetinfo) | <span data-ttu-id="4cf36-131">Gibt Informationen zu einem aktuell angemeldeten Benutzer zurück.</span><span class="sxs-lookup"><span data-stu-id="4cf36-131">Returns information about one currently logged-on user.</span></span>                             |
| [<span data-ttu-id="4cf36-132">**Netwkstauserot**</span><span class="sxs-lookup"><span data-stu-id="4cf36-132">**NetWkstaUserSetInfo**</span></span>](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausersetinfo) | <span data-ttu-id="4cf36-133">Legt die benutzerspezifischen Informationen für die Konfigurationselemente einer Arbeitsstation fest.</span><span class="sxs-lookup"><span data-stu-id="4cf36-133">Sets the user-specific information for the configuration elements of a workstation.</span></span> |



 

<span data-ttu-id="4cf36-134">Die Benutzerinformationen für die Arbeitsstation sind auf folgenden Ebenen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="4cf36-134">Workstation user information is available at the following levels:</span></span>

-   [<span data-ttu-id="4cf36-135">**Wksta- \_ Benutzer \_ Informationen \_ 0**</span><span class="sxs-lookup"><span data-stu-id="4cf36-135">**WKSTA\_USER\_INFO\_0**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_0)
-   [<span data-ttu-id="4cf36-136">**Wksta- \_ Benutzer \_ Informationen \_ 1**</span><span class="sxs-lookup"><span data-stu-id="4cf36-136">**WKSTA\_USER\_INFO\_1**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_1)
-   [<span data-ttu-id="4cf36-137">**Wksta- \_ Benutzer \_ Informationen \_ 1101**</span><span class="sxs-lookup"><span data-stu-id="4cf36-137">**WKSTA\_USER\_INFO\_1101**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_1101)

 

 