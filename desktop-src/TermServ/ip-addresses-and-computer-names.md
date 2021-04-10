---
title: IP-Adressen und Computernamen
description: Es darf nicht davon ausgegangen werden, dass der Computername oder die dem Computer zugewiesene IP-Adresse mit einem einzelnen Benutzer zusammenhängen, da mehrere Benutzer gleichzeitig an einem Remote Desktop Session Host-Server (RD Session Host) angemeldet sein können.
ms.assetid: 17cfd14e-1fff-4154-89a6-8dbbf19a6cae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 574ab1ca0ae10996212fc555b22c2c21663c4b1e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316196"
---
# <a name="ip-addresses-and-computer-names"></a><span data-ttu-id="89b21-103">IP-Adressen und Computernamen</span><span class="sxs-lookup"><span data-stu-id="89b21-103">IP addresses and computer names</span></span>

<span data-ttu-id="89b21-104">Mehrere Benutzer können gleichzeitig an einem Remotedesktop-Sitzungshost Server (RD-Sitzungshost) angemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="89b21-104">Multiple users can be logged on simultaneously to a Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="89b21-105">Folglich ist es nicht sicher anzunehmen, dass der Computername oder die IP-Adresse, die dem Computer zugewiesen ist, einem einzelnen Benutzer zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="89b21-105">Consequently, it is not safe to assume that the computer name or the IP address assigned to the computer are associated with a single user.</span></span> <span data-ttu-id="89b21-106">Dies unterscheidet sich von einer Einzelbenutzer-Windows-Umgebung, in der jeweils nur ein Benutzer angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="89b21-106">This differs from a single-user Windows environment, in which only one user is logged on at a time.</span></span>

<span data-ttu-id="89b21-107">Anwendungen, die den Computernamen oder die IP-Adresse für die Lizenzierung oder die Identifizierung einer Iterations Iterations Anwendung im Netzwerk verwenden, funktionieren in einer Remotedesktopdienste Umgebung nicht ordnungsgemäß, da der Computername oder die IP-Adresse des Servers vielen Benutzern zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="89b21-107">Applications that use the computer name or IP address for licensing or as a means of identifying an iteration of the application on the network will not work properly in a Remote Desktop Services environment, because the server's computer name or IP address can be associated with many users.</span></span>

<span data-ttu-id="89b21-108">In einer Remotedesktopdienste Umgebung hat jedes Client Terminal oder jeder Terminal Emulator eine separate IP-Adresse und einen anderen Computernamen.</span><span class="sxs-lookup"><span data-stu-id="89b21-108">In a Remote Desktop Services environment, each client terminal or terminal emulator has a separate IP address and computer name.</span></span> <span data-ttu-id="89b21-109">Rufen Sie zum Abrufen der IP-Adresse und des Computer namens eines Clients die [**wzquerysessioninformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="89b21-109">To retrieve the IP address and computer name of a client, call the [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) function.</span></span> <span data-ttu-id="89b21-110">Andere Funktionen, die diese Netzwerkadressen und Computernamen abrufen, rufen den Namen und die Adresse des RD-Sitzungshost Servers ab.</span><span class="sxs-lookup"><span data-stu-id="89b21-110">Other functions that retrieve these network addresses and computer names retrieve the name and address of the RD Session Host server.</span></span> <span data-ttu-id="89b21-111">Die Funktion [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) gibt z. b. den Computernamen des Servers zurück.</span><span class="sxs-lookup"><span data-stu-id="89b21-111">For example, the [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) function returns the computer name of the server.</span></span>

 

 