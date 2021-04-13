---
title: Dynamische Authentifizierungs Konfiguration
description: Anwendungen können Authentifizierungs Konfigurationen für eine URL-Gruppe oder Server Sitzung jederzeit ändern.
ms.assetid: 8a5cc119-0427-487d-a155-74c14e2104d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84c68daf04d870d4aa50596397f4f021ac1729af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309488"
---
# <a name="dynamic-authentication-configuration"></a><span data-ttu-id="27878-103">Dynamische Authentifizierungs Konfiguration</span><span class="sxs-lookup"><span data-stu-id="27878-103">Dynamic Authentication Configuration</span></span>

<span data-ttu-id="27878-104">Standardmäßig führt die HTTP-Server-API keine Authentifizierung aus, es sei denn, Sie wird von der Anwendung ausdrücklich aktiviert.</span><span class="sxs-lookup"><span data-stu-id="27878-104">By default, the HTTP Server API does not perform authentication unless the application specifically enables it.</span></span> <span data-ttu-id="27878-105">Anwendungen können Authentifizierungs Konfigurationen für eine URL-Gruppe oder Server Sitzung jederzeit ändern.</span><span class="sxs-lookup"><span data-stu-id="27878-105">Applications can change authentication configurations on a URL Group or server session at any time.</span></span> <span data-ttu-id="27878-106">Änderungen an der Authentifizierungs Konfiguration wirken sich nicht auf Anforderungen aus, die bereits authentifiziert sind oder an die Anwendung gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="27878-106">Changes to the authentication configuration do not affect requests that are already authenticated or being dispatched to the application</span></span>

<span data-ttu-id="27878-107">Für Authentifizierungs Schemas, in denen mehrere Schlag runden erforderlich sind, löscht die HTTP-Server-API den Authentifizierungs Hand Shake, wenn das aktuelle Schema aufgrund von Konfigurationsänderungen von der Anwendung nicht mehr unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="27878-107">For authentication schemes where multiple rounds of handshake are required, the HTTP Server API drops the authentication handshake if the current scheme is no longer supported due to configuration changes from the application.</span></span> <span data-ttu-id="27878-108">Wenn die Anwendung z. b. das Aushandeln und Deaktivieren von NTLM ermöglicht und die HTTP-Server-API den zwischengeschalteten Authentifizierungs Handshake für NTLM hat, wird der Handshake für NTLM verworfen, und die Anforderung wird an die Anwendung übermittelt.</span><span class="sxs-lookup"><span data-stu-id="27878-108">For example, if the application enables Negotiate and disables NTLM, and the HTTP Server API is in the intermediate authentication handshake for NTLM, the handshake for NTLM is discarded and the request is passed to the application.</span></span> <span data-ttu-id="27878-109">Die Anwendung sendet eine 401-Authentifizierungs Aufforderung mit den neuen Authentifizierungs Typen, die im WWW-Authenticate-Header angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="27878-109">The application sends a 401 authentication challenge with the new authentication types specified in the WWW-Authenticate header.</span></span>

 

 




