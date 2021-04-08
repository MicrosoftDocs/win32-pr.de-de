---
description: Eine Anwendung, die als Standardbenutzer ausgeführt wird, kommuniziert mithilfe eines Remote Prozedur Aufrufs (RPC) mit einem Dienst, der als System ausgeführt wird.
ms.assetid: c0bcebe3-f7eb-471f-a21d-5840d2e26729
title: Betriebs System-Dienstmodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ce545c60da8e480247c8fc8b02cfc01e4487340
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960139"
---
# <a name="operating-system-service-model"></a><span data-ttu-id="47a79-103">Betriebs System-Dienstmodell</span><span class="sxs-lookup"><span data-stu-id="47a79-103">Operating System Service Model</span></span>

<span data-ttu-id="47a79-104">Im Betriebssystem-Dienstmodell kommuniziert eine Anwendung, die als Standardbenutzer ausgeführt wird, mit einem Dienst, der als **System** ausgeführt wird, mithilfe des [Remote Prozedur Aufrufs](/windows/desktop/Rpc/rpc-start-page) (RPC).</span><span class="sxs-lookup"><span data-stu-id="47a79-104">In the operating system service model, an application running as a standard user communicates with a service running as **SYSTEM** by using [Remote Procedure Call](/windows/desktop/Rpc/rpc-start-page) (RPC).</span></span>

<span data-ttu-id="47a79-105">Die Standardbenutzer Anwendung wird im Anwendungs Manifest mit dem **requestedExecutionLevel-Wert** " **asInvoker**" gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="47a79-105">The standard user application is marked in the application manifest with a **requestedExecutionLevel** of **asInvoker**.</span></span> <span data-ttu-id="47a79-106">Um einen Vorgang auszuführen, für den Administratorrechte erforderlich sind, stellt die Standardbenutzer Anwendung eine Anforderung an den Dienst.</span><span class="sxs-lookup"><span data-stu-id="47a79-106">To perform an operation that requires administrator privilege, the standard user application makes a request to the service.</span></span>

<span data-ttu-id="47a79-107">Eine Verwendung für das Dienstmodell des Betriebssystems besteht darin, Anwendungen zu verwalten, die sich auf das System auswirken können, z. b. Antivirensoftware oder andere unerwünschte Software und Spyware.</span><span class="sxs-lookup"><span data-stu-id="47a79-107">One use for the operating system service model is to manage applications that could impact the system, such as antivirus or other unwanted software and spyware.</span></span> <span data-ttu-id="47a79-108">Mit der Standardbenutzer Anwendung kann der angemeldete Benutzer einige Aspekte des dienstanwendungs-Dienstanbieter steuern.</span><span class="sxs-lookup"><span data-stu-id="47a79-108">The standard user application allows the logged on user to control some aspects of the service.</span></span> <span data-ttu-id="47a79-109">Der Dienst ist verantwortlich für die Bestimmung der Vorgänge, die er für eine Standardbenutzer Anwendung ausführt.</span><span class="sxs-lookup"><span data-stu-id="47a79-109">The service is responsible for determining which operations it performs for a standard user application.</span></span> <span data-ttu-id="47a79-110">Beispielsweise kann ein Antivirendienst einem Standardbenutzer ermöglichen, eine Überprüfung des Systems zu starten, aber es ist nicht möglich, dass ein Standardbenutzer die Echt Zeit Viren Überprüfung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="47a79-110">For example, an antivirus service might allow a standard user to start a scan of the system, but it might not allow a standard user to disable real-time virus checking.</span></span>

<span data-ttu-id="47a79-111">Ein wesentlicher Vorteil der Verwendung des Betriebssystem-Dienst Modells ist, dass keine Eingabeaufforderung zur Rechte Erweiterung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="47a79-111">A major benefit of using the operating system service model is that no elevation prompting is required.</span></span>

<span data-ttu-id="47a79-112">Ein Nachteil bei der Verwendung des Betriebssystem-Dienst Modells besteht darin, dass ein auf dem System ausgeführt Dienst mehr Ressourcen als eine Aufgabe verwendet und ein Dienst nicht von einem Standardbenutzer angehalten werden kann.</span><span class="sxs-lookup"><span data-stu-id="47a79-112">One drawback of using the operating system service model is that a service running on the system uses more resources than a task, and a service cannot be stopped by a standard user.</span></span> <span data-ttu-id="47a79-113">Verwenden Sie ggf. das [Modell mit erhöhten](elevated-task-model.md) rechten.</span><span class="sxs-lookup"><span data-stu-id="47a79-113">Consider using the [Elevated Task Model](elevated-task-model.md) if it suffices.</span></span>

<span data-ttu-id="47a79-114">Um das Betriebssystem-Dienstmodell zu implementieren, erstellen Sie eine Standardbenutzer-Client Anwendung und einen Betriebssystem Dienst.</span><span class="sxs-lookup"><span data-stu-id="47a79-114">To implement the operating system service model, create a standard user client application and an operating system service.</span></span> <span data-ttu-id="47a79-115">Installieren Sie den Dienst während der Installation des Produkts im Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="47a79-115">Install the service in the operating system during product installation time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="47a79-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="47a79-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47a79-117">Entwickeln von Anwendungen, für die Administrator Rechte erforderlich sind</span><span class="sxs-lookup"><span data-stu-id="47a79-117">Developing Applications that Require Administrator Privilege</span></span>](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[<span data-ttu-id="47a79-118">Administrator Broker Modell</span><span class="sxs-lookup"><span data-stu-id="47a79-118">Administrator Broker Model</span></span>](administrator-broker-model.md)
</dt> <dt>

[<span data-ttu-id="47a79-119">COM-Objektmodell für Administratoren</span><span class="sxs-lookup"><span data-stu-id="47a79-119">Administrator COM Object Model</span></span>](administrator-com-object-model.md)
</dt> <dt>

[<span data-ttu-id="47a79-120">Modell mit erhöhten Rechten</span><span class="sxs-lookup"><span data-stu-id="47a79-120">Elevated Task Model</span></span>](elevated-task-model.md)
</dt> </dl>

 

 
