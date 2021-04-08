---
description: Der Dienststeuerungs-Manager (Service Control Manager, SCM) verwaltet eine Datenbank installierter Dienste und Treiber Dienste und bietet eine einheitliche und sichere Möglichkeit, Sie zu steuern.
ms.assetid: a3af8340-d367-417b-9759-7282edf1d694
title: Informationen zu Diensten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87aeec6dfcdc4e2dc0cc0ab3ef084b7927b2c3bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960117"
---
# <a name="about-services"></a><span data-ttu-id="31742-103">Informationen zu Diensten</span><span class="sxs-lookup"><span data-stu-id="31742-103">About Services</span></span>

<span data-ttu-id="31742-104">Der [Dienststeuerungs-Manager (Service Control Manager](service-control-manager.md) , SCM) verwaltet eine Datenbank installierter Dienste und Treiber Dienste und bietet eine einheitliche und sichere Möglichkeit, Sie zu steuern.</span><span class="sxs-lookup"><span data-stu-id="31742-104">The [service control manager](service-control-manager.md) (SCM) maintains a database of installed services and driver services, and provides a unified and secure means of controlling them.</span></span> <span data-ttu-id="31742-105">Die Datenbank enthält Informationen darüber, wie die einzelnen Dienst-oder Treiber Dienste gestartet werden sollten.</span><span class="sxs-lookup"><span data-stu-id="31742-105">The database includes information on how each service or driver service should be started.</span></span> <span data-ttu-id="31742-106">Außerdem ermöglicht es Systemadministratoren, die Sicherheitsanforderungen für jeden Dienst anzupassen und damit den Zugriff auf den Dienst zu steuern.</span><span class="sxs-lookup"><span data-stu-id="31742-106">It also enables system administrators to customize security requirements for each service and thereby control access to the service.</span></span>

<span data-ttu-id="31742-107">In den folgenden Programmtypen werden die vom SCM bereitgestellten Funktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="31742-107">The following types of programs use the functions provided by the SCM.</span></span>



| <span data-ttu-id="31742-108">type</span><span class="sxs-lookup"><span data-stu-id="31742-108">Type</span></span>                          | <span data-ttu-id="31742-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="31742-109">Description</span></span>                                                                                                                                                                                                                                                                                                                               |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31742-110">Dienstprogramm</span><span class="sxs-lookup"><span data-stu-id="31742-110">Service program</span></span>               | <span data-ttu-id="31742-111">Ein Programm, das ausführbaren Code für einen oder mehrere Dienste bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="31742-111">A program that provides executable code for one or more services.</span></span> <span data-ttu-id="31742-112">Dienstprogramme verwenden Funktionen, die eine Verbindung mit dem SCM herstellen und Statusinformationen an den SCM senden.</span><span class="sxs-lookup"><span data-stu-id="31742-112">Service programs use functions that connect to the SCM and send status information to the SCM.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="31742-113">Dienst Konfigurationsprogramm</span><span class="sxs-lookup"><span data-stu-id="31742-113">Service configuration program</span></span> | <span data-ttu-id="31742-114">Ein Programm, das die Dienst Datenbank abfragt oder ändert.</span><span class="sxs-lookup"><span data-stu-id="31742-114">A program that queries or modifies the services database.</span></span> <span data-ttu-id="31742-115">Dienst Konfigurationsprogramme verwenden Funktionen, die die Datenbank öffnen, Dienste in der Datenbank installieren oder löschen und die Konfigurations-und Sicherheitsparameter für installierte Dienste Abfragen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="31742-115">Service configuration programs use functions that open the database, install or delete services in the database, and query or modify the configuration and security parameters for installed services.</span></span> <span data-ttu-id="31742-116">Dienst Konfigurationsprogramme verwalten sowohl Dienste als auch Treiber Dienste.</span><span class="sxs-lookup"><span data-stu-id="31742-116">Service configuration programs manage both services and driver services.</span></span> |
| <span data-ttu-id="31742-117">Dienst Steuerungsprogramm</span><span class="sxs-lookup"><span data-stu-id="31742-117">Service control program</span></span>       | <span data-ttu-id="31742-118">Ein Programm, das Dienste und Treiber Dienste startet und steuert.</span><span class="sxs-lookup"><span data-stu-id="31742-118">A program that starts and controls services and driver services.</span></span> <span data-ttu-id="31742-119">Dienst Steuerungsprogramme verwenden Funktionen, die Anforderungen an den SCM senden, der die Anforderung ausführt.</span><span class="sxs-lookup"><span data-stu-id="31742-119">Service control programs use functions that send requests to the SCM, which carries out the request.</span></span>                                                                                                                                                                     |



 

<span data-ttu-id="31742-120">In dieser Übersicht werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="31742-120">This overview discusses the following topics:</span></span>

-   [<span data-ttu-id="31742-121">Dienststeuerungs-Manager</span><span class="sxs-lookup"><span data-stu-id="31742-121">Service Control Manager</span></span>](service-control-manager.md)
-   [<span data-ttu-id="31742-122">Dienstprogramme</span><span class="sxs-lookup"><span data-stu-id="31742-122">Service Programs</span></span>](service-programs.md)
-   [<span data-ttu-id="31742-123">Dienst Konfigurationsprogramme</span><span class="sxs-lookup"><span data-stu-id="31742-123">Service Configuration Programs</span></span>](service-configuration-programs.md)
-   [<span data-ttu-id="31742-124">Dienst Steuerungsprogramme</span><span class="sxs-lookup"><span data-stu-id="31742-124">Service Control Programs</span></span>](service-control-programs.md)
-   [<span data-ttu-id="31742-125">Dienst Benutzerkonten</span><span class="sxs-lookup"><span data-stu-id="31742-125">Service User Accounts</span></span>](service-user-accounts.md)
-   [<span data-ttu-id="31742-126">Interaktive Dienste</span><span class="sxs-lookup"><span data-stu-id="31742-126">Interactive Services</span></span>](interactive-services.md)
-   [<span data-ttu-id="31742-127">Dienst Sicherheit und Zugriffsrechte</span><span class="sxs-lookup"><span data-stu-id="31742-127">Service Security and Access Rights</span></span>](service-security-and-access-rights.md)
-   [<span data-ttu-id="31742-128">Debugging a Service (Debuggen eines Diensts)</span><span class="sxs-lookup"><span data-stu-id="31742-128">Debugging a Service</span></span>](debugging-a-service.md)
-   [<span data-ttu-id="31742-129">Dienst Triggerereignisse</span><span class="sxs-lookup"><span data-stu-id="31742-129">Service Trigger Events</span></span>](service-trigger-events.md)

 

 



