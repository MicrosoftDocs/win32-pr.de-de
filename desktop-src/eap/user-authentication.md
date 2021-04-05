---
title: Benutzerauthentifizierung
description: Das Authentifizierungsprotokoll selbst kann den Benutzer über das geschützte EAP (PEAP) authentifizieren.
ms.assetid: 7e0ff5e3-3274-4b52-8c53-101ad01e3034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10de1d08a0daffe7fb415c3eab4ba939afa9387
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "103719571"
---
# <a name="user-authentication"></a><span data-ttu-id="0f05a-103">Benutzerauthentifizierung</span><span class="sxs-lookup"><span data-stu-id="0f05a-103">User Authentication</span></span>

<span data-ttu-id="0f05a-104">Das Authentifizierungsprotokoll selbst kann den Benutzer über das geschützte EAP (PEAP) authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="0f05a-104">The authentication protocol itself can authenticate the user via Protected EAP (PEAP).</span></span> <span data-ttu-id="0f05a-105">Es gibt auch zwei Authentifizierungs Anbieter, die in das Betriebssystem integriert sind: Windows-Domänen Authentifizierung (Zugriff über Verzeichnisdienste) und RAS (Remote Access Dial-in User Service).</span><span class="sxs-lookup"><span data-stu-id="0f05a-105">There are also two authentication providers built into the operating system: Windows domain authentication (accessed via Directory Services) and Remote Access Dial-In User Service (RADIUS).</span></span>

<span data-ttu-id="0f05a-106">Wenn RADIUS der Authentifizierungs Anbieter ist, wird das EAP-Plug-in auf dem RADIUS-Server und nicht auf dem drahtlos Zugriffspunkt-Server (z. b. einem RAS-Server) installiert.</span><span class="sxs-lookup"><span data-stu-id="0f05a-106">In the case where RADIUS is the authentication provider, the EAP Plug-in is installed on the RADIUS server rather than on the wireless Access Point (AP) server, such as a RAS server.</span></span> <span data-ttu-id="0f05a-107">Der AP-Server übergibt EAP-Pakete direkt vom Client an den Authentifizierungsdienst auf dem RADIUS-Server.</span><span class="sxs-lookup"><span data-stu-id="0f05a-107">The AP server passes EAP packets directly from the client to the authentication service on the RADIUS server.</span></span> <span data-ttu-id="0f05a-108">Der AP-Server verarbeitet keine der Informationen in den EAP-Paketen, er muss jedoch die vom serverseitigen, vollständigen PEAP generierten Verschlüsselungsschlüssel (256 Bit) akzeptieren, um die sichere Verbindung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0f05a-108">The AP server does not process any of the information in the EAP packets, but it must accept the server-side, full strength (256 bit) PEAP generated encryption keys in order to create the secure connection.</span></span>

 

 




