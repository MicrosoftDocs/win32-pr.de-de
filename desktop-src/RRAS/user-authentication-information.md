---
title: Informationen zur Benutzerauthentifizierung
description: Der RAS-Verbindungs-Manager-Dienst auf dem Client Computer sendet einen Benutzernamen und ein Kennwort an den RAS-Server auf dem Remote Computer.
ms.assetid: b27bf520-d871-4314-8ed9-3a6a9583ab52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0cb95d0e941c47deb398c03277013e0e0a35f9d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858291"
---
# <a name="user-authentication-information"></a><span data-ttu-id="4ad9f-103">Informationen zur Benutzerauthentifizierung</span><span class="sxs-lookup"><span data-stu-id="4ad9f-103">User Authentication Information</span></span>

<span data-ttu-id="4ad9f-104">Der RAS-Verbindungs-Manager-Dienst auf dem Client Computer sendet einen Benutzernamen und ein Kennwort an den RAS-Server auf dem Remote Computer.</span><span class="sxs-lookup"><span data-stu-id="4ad9f-104">The Remote Access Connection Manager service on the client computer sends a user name and password to the RAS server on the remote computer.</span></span> <span data-ttu-id="4ad9f-105">Bevor eine Verbindung hergestellt wird, werden diese Informationen vom Remote Server zum Authentifizieren des Benutzers verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ad9f-105">Before it establishes a connection, the remote server uses this information to authenticate the user.</span></span> <span data-ttu-id="4ad9f-106">Standardmäßig sendet der RAS-Verbindungs-Manager den Benutzernamen und das Kennwort des aktuell angemeldeten Benutzers.</span><span class="sxs-lookup"><span data-stu-id="4ad9f-106">By default, the Remote Access Connection Manager sends the user name and password of the currently logged-on user.</span></span> <span data-ttu-id="4ad9f-107">Der RAS-Client kann die im Befehl " [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) " angegebene Struktur " [**rasdialparameams**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) " verwenden, um einen anderen Benutzernamen und ein anderes Kennwort anzugeben.</span><span class="sxs-lookup"><span data-stu-id="4ad9f-107">The RAS client can use the [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) structure specified in the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) call to specify a different user name and password.</span></span>

<span data-ttu-id="4ad9f-108">Wenn der Remote Server den Benutzer nicht mit den angegebenen Informationen authentifizieren kann, kann der Verbindungsvorgang in einen [angehaltenen Zustand](paused-states.md) versetzt werden, damit der RAS-Client verschiedene Authentifizierungsdaten des Benutzers erfassen kann.</span><span class="sxs-lookup"><span data-stu-id="4ad9f-108">If the remote server cannot authenticate the user with the specified information, it can allow the connection operation to enter a [paused state](paused-states.md) to enable the RAS client to collect different authentication data from the user.</span></span>

 

 