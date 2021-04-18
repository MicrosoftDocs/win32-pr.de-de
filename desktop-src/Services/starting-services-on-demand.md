---
description: Der Benutzer kann einen Dienst mit dem Dienststeuerungs-Hilfsprogramm "Dienste" starten. Der Benutzer kann Argumente für den Dienst im Feld Start Parameter angeben. Ein Dienst Steuerungsprogramm kann einen Dienst starten und seine Argumente mit der Start Service-Funktion angeben.
ms.assetid: 72f51b38-d62c-4400-a38d-b9a0e90e9db4
title: Starten von Diensten bei Bedarf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c70be74e6cf54468f244ca798ae7ca48da3512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351513"
---
# <a name="starting-services-on-demand"></a><span data-ttu-id="16788-105">Starten von Diensten bei Bedarf</span><span class="sxs-lookup"><span data-stu-id="16788-105">Starting Services on Demand</span></span>

<span data-ttu-id="16788-106">Der Benutzer kann einen Dienst mit dem Dienststeuerungs-Hilfsprogramm "Dienste" starten.</span><span class="sxs-lookup"><span data-stu-id="16788-106">The user can start a service with the Services control panel utility.</span></span> <span data-ttu-id="16788-107">Der Benutzer kann Argumente für den Dienst im Feld **Start Parameter** angeben.</span><span class="sxs-lookup"><span data-stu-id="16788-107">The user can specify arguments for the service in the **Start parameters** field.</span></span> <span data-ttu-id="16788-108">Ein Dienst Steuerungsprogramm kann einen Dienst starten und seine Argumente mit der [**Start Service**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) -Funktion angeben.</span><span class="sxs-lookup"><span data-stu-id="16788-108">A service control program can start a service and specify its arguments with the [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) function.</span></span>

<span data-ttu-id="16788-109">Wenn der Dienst gestartet wird, führt der SCM die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="16788-109">When the service is started, the SCM performs the following steps:</span></span>

-   <span data-ttu-id="16788-110">Ruft die in der-Datenbank gespeicherten Kontoinformationen ab.</span><span class="sxs-lookup"><span data-stu-id="16788-110">Retrieve the account information stored in the database.</span></span>
-   <span data-ttu-id="16788-111">Melden Sie sich mit dem Dienst Konto an.</span><span class="sxs-lookup"><span data-stu-id="16788-111">Log on the service account.</span></span>
-   <span data-ttu-id="16788-112">Laden Sie das Benutzerprofil.</span><span class="sxs-lookup"><span data-stu-id="16788-112">Load the user profile.</span></span>
-   <span data-ttu-id="16788-113">Erstellen Sie den Dienst im Zustand "angehalten".</span><span class="sxs-lookup"><span data-stu-id="16788-113">Create the service in the suspended state.</span></span>
-   <span data-ttu-id="16788-114">Weisen Sie das Anmelde Token dem Prozess zu.</span><span class="sxs-lookup"><span data-stu-id="16788-114">Assign the logon token to the process.</span></span>
-   <span data-ttu-id="16788-115">Ermöglicht die Ausführung des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="16788-115">Allow the process to execute.</span></span>

 

 



