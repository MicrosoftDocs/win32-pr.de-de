---
title: RAS-Server-Sicherheits Authentifizierung
description: Wenn ein Windows NT/Windows 2000-RAS-Server einen Aufruf empfängt, ruft er die Funktion "rassecuritydialogbegin" der registrierten RAS-Sicherheits-DLL auf, sofern vorhanden.
ms.assetid: dd9469ec-9bb1-4444-af5b-72e3ba8b4cb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27184388b418e0fec2a1988fd9e693e942c08e03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036870"
---
# <a name="ras-server-security-authentication"></a><span data-ttu-id="5ed72-103">RAS-Server-Sicherheits Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="5ed72-103">RAS Server Security Authentication</span></span>

<span data-ttu-id="5ed72-104">Wenn ein Windows NT/Windows 2000-RAS-Server einen Aufruf empfängt, ruft er die Funktion " [**rassecuritydialogbegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) " der registrierten RAS-Sicherheits-DLL auf, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5ed72-104">When a Windows NT/Windows 2000 RAS server receives a call, it invokes the [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) function of the registered RAS security DLL, if there is one.</span></span> <span data-ttu-id="5ed72-105">Mit diesem Befehl wird die Sicherheits-DLL benachrichtigt, damit die Authentifizierung des Remote Benutzers gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="5ed72-105">This call notifies the security DLL to begin its authentication of the remote user.</span></span> <span data-ttu-id="5ed72-106">Der RAS-Server ruft vor seiner PPP-oder RAS-Authentifizierung " **rassecuritydialogbegin** " auf.</span><span class="sxs-lookup"><span data-stu-id="5ed72-106">The RAS server calls **RasSecurityDialogBegin** before performing its PPP or RAS authentication.</span></span>

<span data-ttu-id="5ed72-107">Der Befehl " [**rassecuritydialogbegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) " übergibt die folgenden Informationen an die Sicherheits-DLL:</span><span class="sxs-lookup"><span data-stu-id="5ed72-107">The [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) call passes the following information to the security DLL:</span></span>

-   <span data-ttu-id="5ed72-108">Ein Port handle, mit dem die Verbindung identifiziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5ed72-108">A port handle to identify the connection.</span></span>
-   <span data-ttu-id="5ed72-109">Zeiger auf Puffer, die bei der Kommunikation mit dem Remote Benutzer verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5ed72-109">Pointers to buffers to use when communicating with the remote user.</span></span>
-   <span data-ttu-id="5ed72-110">Ein Zeiger auf eine " [**rassecuritydialogcomplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) "-Funktion, die aufgerufen wird, wenn die Authentifizierung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="5ed72-110">A pointer to a [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) function to call when the authentication has been completed.</span></span>

<span data-ttu-id="5ed72-111">Das Port Handle und die Puffer Zeiger sind gültig, bis die Sicherheits-dll " [**rassecuritydialogcomplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) " aufruft, um die Authentifizierungs Transaktion zu beenden.</span><span class="sxs-lookup"><span data-stu-id="5ed72-111">The port handle and buffer pointers are valid until the security DLL calls [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) to terminate the authentication transaction.</span></span>

<span data-ttu-id="5ed72-112">Mit der Datei " [**rassecuritydialogcomplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) " wird der RAS-Server über die Ergebnisse der Authentifizierung der Sicherheits-DLL des Remote Benutzers benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="5ed72-112">The [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) notifies the RAS server of the results of the security DLL's authentication of the remote user.</span></span> <span data-ttu-id="5ed72-113">Wenn die Sicherheits-DLL einen Erfolg meldet, fährt der RAS-Server mit der PPP-und RAS-Authentifizierung des Remote Benutzers fort.</span><span class="sxs-lookup"><span data-stu-id="5ed72-113">If the security DLL reports success, the RAS server proceeds with its PPP and RAS authentication of the remote user.</span></span> <span data-ttu-id="5ed72-114">Wenn die Sicherheits-DLL meldet, dass der Remote Benutzer die Authentifizierung nicht bestanden hat, oder wenn ein Fehler aufgetreten ist, wird der RAS-Server beendet und protokolliert den Fehler oder die Authentifizierung im Ereignisprotokoll.</span><span class="sxs-lookup"><span data-stu-id="5ed72-114">If the security DLL reports that the remote user failed the authentication, or that an error occurred, the RAS server hangs up and logs the error or failed authentication in the event log.</span></span>

 

 




