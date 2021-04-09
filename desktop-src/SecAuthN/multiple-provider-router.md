---
description: Der multianbieterrouter (MPR) übernimmt die Kommunikation zwischen dem Windows-Betriebssystem und den installierten Netzwerkanbietern. Dadurch kann Windows dem Benutzer ein integriertes Netzwerk vorstellen.
ms.assetid: 3f473273-f696-45f7-afbf-fd55f974ba48
title: Mehrere Anbieter Router
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfa7c4e76901c31e3b5dc7f329a23838aba4f7be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867247"
---
# <a name="multiple-provider-router"></a><span data-ttu-id="2d1b8-104">Mehrere Anbieter Router</span><span class="sxs-lookup"><span data-stu-id="2d1b8-104">Multiple Provider Router</span></span>

<span data-ttu-id="2d1b8-105">Der [*multianbieterrouter*](../secgloss/m-gly.md) (MPR) übernimmt die Kommunikation zwischen dem Windows-Betriebssystem und den installierten Netzwerkanbietern.</span><span class="sxs-lookup"><span data-stu-id="2d1b8-105">The [*Multiple Provider Router*](../secgloss/m-gly.md) (MPR) handles communication between the Windows operating system and the installed network providers.</span></span> <span data-ttu-id="2d1b8-106">Dadurch kann Windows dem Benutzer ein integriertes Netzwerk vorstellen.</span><span class="sxs-lookup"><span data-stu-id="2d1b8-106">It enables Windows to present an integrated network to the user.</span></span>

<span data-ttu-id="2d1b8-107">Beim Start der MPR wird die Registrierung überprüft, um zu bestimmen, welche Netzwerkanbieter auf dem System installiert sind und in welcher Reihenfolge Sie durchlaufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2d1b8-107">When the MPR starts, it checks the registry to determine which network providers are installed on the system and the order they should be cycled through.</span></span> <span data-ttu-id="2d1b8-108">Alle registrierten Netzwerkanbieter-DLLs werden geladen und verwendet, um nachfolgende WNET-Aufrufe von der Benutzeroberfläche oder anderen Anwendungen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="2d1b8-108">It loads all registered network provider DLLs and uses them to process subsequent WNet calls made by the user interface or other applications.</span></span>

<span data-ttu-id="2d1b8-109">Weitere Informationen zu WNET-Funktionen finden Sie unter [Windows-Netzwerke](../wnet/windows-networking-wnet-.md).</span><span class="sxs-lookup"><span data-stu-id="2d1b8-109">For more information about WNet functions, see [Windows Networking](../wnet/windows-networking-wnet-.md).</span></span>

 

 
