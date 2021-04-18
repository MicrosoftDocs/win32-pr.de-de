---
description: Der Dienststeuerungs-Manager (SCM) wird beim Systemstart gestartet. Dabei handelt es sich um einen RPC-Server (Remote Procedure Aufruf), sodass Dienst Konfiguration und Dienst Steuerungsprogramme Dienste auf Remote Computern bearbeiten können.
ms.assetid: 56ad011d-17c4-4410-b598-6ef47fb3638f
title: Dienststeuerungs-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a8a35fd34bd2714d22d40ccf618c89a8b66a6c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343277"
---
# <a name="service-control-manager"></a><span data-ttu-id="82b6f-104">Dienststeuerungs-Manager</span><span class="sxs-lookup"><span data-stu-id="82b6f-104">Service Control Manager</span></span>

<span data-ttu-id="82b6f-105">Der Dienststeuerungs-Manager (SCM) wird beim Systemstart gestartet.</span><span class="sxs-lookup"><span data-stu-id="82b6f-105">The service control manager (SCM) is started at system boot.</span></span> <span data-ttu-id="82b6f-106">Dabei handelt es sich um einen RPC-Server (Remote Procedure Aufruf), sodass Dienst Konfiguration und Dienst Steuerungsprogramme Dienste auf Remote Computern bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="82b6f-106">It is a remote procedure call (RPC) server, so that service configuration and service control programs can manipulate services on remote machines.</span></span>

<span data-ttu-id="82b6f-107">Die Dienstfunktionen stellen eine Schnittstelle für die folgenden vom SCM ausgeführten Aufgaben bereit:</span><span class="sxs-lookup"><span data-stu-id="82b6f-107">The service functions provide an interface for the following tasks performed by the SCM:</span></span>

-   <span data-ttu-id="82b6f-108">Die Datenbank der installierten Dienste wird beibehalten.</span><span class="sxs-lookup"><span data-stu-id="82b6f-108">Maintaining the database of installed services.</span></span>
-   <span data-ttu-id="82b6f-109">Starten von Diensten und Treiber Diensten entweder beim Systemstart oder nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="82b6f-109">Starting services and driver services either upon system startup or upon demand.</span></span>
-   <span data-ttu-id="82b6f-110">Die installierten Dienste und Treiber Dienste werden aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="82b6f-110">Enumerating installed services and driver services.</span></span>
-   <span data-ttu-id="82b6f-111">Verwalten von Statusinformationen für die Ausführung von Diensten und Treiber Diensten</span><span class="sxs-lookup"><span data-stu-id="82b6f-111">Maintaining status information for running services and driver services.</span></span>
-   <span data-ttu-id="82b6f-112">Übertragen von Steuerungsanforderungen an die laufenden Dienste</span><span class="sxs-lookup"><span data-stu-id="82b6f-112">Transmitting control requests to running services.</span></span>
-   <span data-ttu-id="82b6f-113">Sperren und Entsperren der Dienst Datenbank.</span><span class="sxs-lookup"><span data-stu-id="82b6f-113">Locking and unlocking the service database.</span></span>

<span data-ttu-id="82b6f-114">In den folgenden Abschnitten wird der SCM ausführlicher beschrieben:</span><span class="sxs-lookup"><span data-stu-id="82b6f-114">The following sections describe the SCM in more detail:</span></span>

-   [<span data-ttu-id="82b6f-115">Datenbank der installierten Dienste</span><span class="sxs-lookup"><span data-stu-id="82b6f-115">Database of Installed Services</span></span>](database-of-installed-services.md)
-   [<span data-ttu-id="82b6f-116">Dienste werden automatisch gestartet</span><span class="sxs-lookup"><span data-stu-id="82b6f-116">Automatically Starting Services</span></span>](automatically-starting-services.md)
-   [<span data-ttu-id="82b6f-117">Starten von Diensten bei Bedarf</span><span class="sxs-lookup"><span data-stu-id="82b6f-117">Starting Services on Demand</span></span>](starting-services-on-demand.md)
-   [<span data-ttu-id="82b6f-118">Dienst Daten Satz Liste</span><span class="sxs-lookup"><span data-stu-id="82b6f-118">Service Record List</span></span>](service-record-list.md)
-   [<span data-ttu-id="82b6f-119">SCM-Handles</span><span class="sxs-lookup"><span data-stu-id="82b6f-119">SCM Handles</span></span>](scm-handles.md)

 

 



