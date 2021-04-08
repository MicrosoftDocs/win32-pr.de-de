---
description: Das callhub-Objekt stellt eine Drittanbieter Ansicht eines mehr Parteien Aufrufes dar.
ms.assetid: ea23ae25-2fbb-4060-8273-cd7921d49e52
title: Callhub-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d43594db13c9175490b4cbb0941d1fb4e45b2ced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960106"
---
# <a name="callhub-object"></a><span data-ttu-id="2f3a2-103">Callhub-Objekt</span><span class="sxs-lookup"><span data-stu-id="2f3a2-103">CallHub Object</span></span>

<span data-ttu-id="2f3a2-104">Das callhub-Objekt stellt eine Drittanbieter Ansicht eines mehr Parteien Aufrufes dar.</span><span class="sxs-lookup"><span data-stu-id="2f3a2-104">The CallHub object represents a third-party view of a multiparty call.</span></span> <span data-ttu-id="2f3a2-105">Die zugeordneten Schnittstellen und Methoden erhalten und legen Informationen über den Hub fest, z. b. ob er aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="2f3a2-105">The associated interfaces and methods get and set information concerning the hub, such as whether it is active.</span></span> <span data-ttu-id="2f3a2-106">Mithilfe des callhub-Objekts kann ein Benutzer mit der erforderlichen Sicherheit andere Teilnehmer in einem Aufruf erkennen und möglicherweise steuern.</span><span class="sxs-lookup"><span data-stu-id="2f3a2-106">Using the CallHub object, a user with the required security can discover and potentially control other participants in a call.</span></span>

<span data-ttu-id="2f3a2-107">Ein callhub-Objekt kann nicht direkt von einer Anwendung erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2f3a2-107">A CallHub object cannot be created directly by an application.</span></span> <span data-ttu-id="2f3a2-108">Ein callhub-Objekt wird indirekt erstellt, wenn ein eingehender Aufruf über TAPI 3 empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="2f3a2-108">A CallHub object is created indirectly when an incoming call is received through TAPI 3.</span></span>

<span data-ttu-id="2f3a2-109">TAPI 3 nutzt TAPI-Dienstanbieter, um die erforderlichen Informationen über Aufrufe zur Implementierung mit dem callhub-Objekt bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="2f3a2-109">TAPI 3 relies on TAPI service providers to provide the necessary information about calls to implement using the CallHub object.</span></span> <span data-ttu-id="2f3a2-110">Da nicht alle Dienstanbieter diese Informationen bereitstellen und nicht alle Hardware die callhub-Nachverfolgung unterstützen, sind die Informationen zu den anderen Benutzern in der Verbindung möglicherweise nur eingeschränkt oder nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="2f3a2-110">Because not all service providers provide this information, and not all hardware supports call hub tracking, the information available about the other users in the connection may be limited or nonexistent.</span></span>

<span data-ttu-id="2f3a2-111">Das Beispiel [Erstellen eines einfachen Konferenz](create-a-simple-conference.md) Codes veranschaulicht die Verwendung eines callhub-Objekts.</span><span class="sxs-lookup"><span data-stu-id="2f3a2-111">The [Create a Simple Conference](create-a-simple-conference.md) code example illustrates use of a CallHub object.</span></span>

<span data-ttu-id="2f3a2-112">Unter [callhub-Objekt Schnittstellen](callhub-object-interfaces.md) finden Sie eine Liste aller Schnittstellen, die dem callhub-Objekt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="2f3a2-112">See [CallHub Object Interfaces](callhub-object-interfaces.md) for a list of all interfaces associated with the CallHub object.</span></span>

 

 



