---
title: Details zur EAP-Implementierung
description: Zugriffspunkte (APS), z. b. RAS (RAS), interagieren mit EAP-Implementierungen durch die Verwendung von Funktionsaufrufen, die von der EAP-dll von Drittanbietern exportiert werden müssen.
ms.assetid: 85775c03-7538-41a1-9f83-42e71025a79c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41115b16d843b0c1b087eac1c348a0491df1173a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314883"
---
# <a name="eap-implementation-details"></a><span data-ttu-id="eaddf-103">Details zur EAP-Implementierung</span><span class="sxs-lookup"><span data-stu-id="eaddf-103">EAP Implementation Details</span></span>

<span data-ttu-id="eaddf-104">Zugriffspunkte (APS), z. b. RAS (RAS), interagieren mit EAP-Implementierungen durch die Verwendung von Funktionsaufrufen, die von der EAP-dll von Drittanbietern exportiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="eaddf-104">Access Points (APs), such as Remote Access Service (RAS), interact with EAP implementations through the use of function calls that must be exported by the third-party EAP DLL.</span></span> <span data-ttu-id="eaddf-105">Das heißt, dass EAP eine Anbieter-API ist, was bedeutet, dass Plug-ins oder DLLs Code implementieren, um einen EAP-Anbieter zu werden, aber nicht die EAP-APIs selbst aufrufen dürfen.</span><span class="sxs-lookup"><span data-stu-id="eaddf-105">In other words, EAP is a provider API, meaning that plug-ins or DLLs implement code to become an EAP provider, but must not call the EAP APIs themselves.</span></span> <span data-ttu-id="eaddf-106">Beispielsweise erstellt ein Programmierer einer EAP-DLL Code für eine EAP-Initialisierungs Routine und platziert diesen Code in der vordefinierten EAP-Funktion [**raseapinitialize**](/previous-versions/windows/desktop/legacy/aa363527(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="eaddf-106">For example, a programmer of an EAP DLL creates code for an EAP initialization routine and places this code in the EAP predefined function [**RasEapInitialize**](/previous-versions/windows/desktop/legacy/aa363527(v=vs.85)).</span></span> <span data-ttu-id="eaddf-107">Dann ruft der AP-Verbindungs-Manager zur Laufzeit die **raseapinitialize** -Funktion auf, die den Code enthält, um die EAP-Implementierung zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="eaddf-107">Then at run-time, the AP connection manager calls the **RasEapInitialize** function, which contains the code, to initialize the EAP implementation.</span></span>

<span data-ttu-id="eaddf-108">In den folgenden Themen wird diese Interaktion ausführlich erläutert:</span><span class="sxs-lookup"><span data-stu-id="eaddf-108">The following topics detail this interaction:</span></span>

-   [<span data-ttu-id="eaddf-109">Zugriffspunkt Initialisierung von EAP</span><span class="sxs-lookup"><span data-stu-id="eaddf-109">Access Point Initialization of EAP</span></span>](ras-initialization-of-eap.md)
-   [<span data-ttu-id="eaddf-110">Initialisierung des Authentifizierungs Protokolls</span><span class="sxs-lookup"><span data-stu-id="eaddf-110">Authentication Protocol Initialization</span></span>](authentication-protocol-initialization.md)
-   [<span data-ttu-id="eaddf-111">Interaktion zwischen Zugriffspunkt und Authentifizierungsprotokoll</span><span class="sxs-lookup"><span data-stu-id="eaddf-111">Access Point and Authentication Protocol Interaction</span></span>](ras-and-authentication-protocol-interaction-during-authentication.md)
-   [<span data-ttu-id="eaddf-112">Abschluss der Authentifizierungs Sitzung</span><span class="sxs-lookup"><span data-stu-id="eaddf-112">Completion of the Authentication Session</span></span>](completion-of-the-authentication-session.md)

 

 