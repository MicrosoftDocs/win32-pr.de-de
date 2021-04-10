---
description: Net.exe können zum Abbrechen und Starten des IPv6-Protokolls verwendet werden.
ms.assetid: faa555d9-eb20-4b7a-94eb-b67a48ee630e
title: Net.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5074696b71ce000ef330f2c88fceef0f60b0222e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862552"
---
# <a name="netexe"></a><span data-ttu-id="647d2-103">Net.exe</span><span class="sxs-lookup"><span data-stu-id="647d2-103">Net.exe</span></span>

<span data-ttu-id="647d2-104">Net.exe können zum Abbrechen und Starten des IPv6-Protokolls verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="647d2-104">Net.exe can be used to stop and start the IPv6 protocol.</span></span> <span data-ttu-id="647d2-105">Durch einen Neustart von IPv6 wird das Protokoll neu initialisiert, als wenn der Computer neu gestartet wird, wodurch die Schnittstellen Nummern geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="647d2-105">Restarting IPv6 reinitializes the protocol as if the computer were restarting, which may change interface numbers.</span></span> <span data-ttu-id="647d2-106">Net.exe weist viele Unterbefehle auf.</span><span class="sxs-lookup"><span data-stu-id="647d2-106">Net.exe has many subcommands.</span></span> <span data-ttu-id="647d2-107">Die folgenden Befehle sind für IPv6 relevant:</span><span class="sxs-lookup"><span data-stu-id="647d2-107">The following commands are relevant to IPv6:</span></span>

<dl> <dt>

<span data-ttu-id="647d2-108"><span id="net_stop_tcpip6"></span><span id="NET_STOP_TCPIP6"></span>**NET-tcpip6**</span><span class="sxs-lookup"><span data-stu-id="647d2-108"><span id="net_stop_tcpip6"></span><span id="NET_STOP_TCPIP6"></span>**net stop tcpip6**</span></span>
</dt> <dd>

<span data-ttu-id="647d2-109">Beendet das IPv6-Protokoll und entlädt es aus dem Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="647d2-109">Stops the IPv6 protocol and unloads it from memory.</span></span> <span data-ttu-id="647d2-110">Dieser Befehl schlägt fehl, wenn IPv6-Sockets geöffnet sind.</span><span class="sxs-lookup"><span data-stu-id="647d2-110">This command fails if any IPv6 sockets are open.</span></span>

</dd> <dt>

<span data-ttu-id="647d2-111"><span id="net_start_tcpip6"></span><span id="NET_START_TCPIP6"></span>**NET Start tcpip6**</span><span class="sxs-lookup"><span data-stu-id="647d2-111"><span id="net_start_tcpip6"></span><span id="NET_START_TCPIP6"></span>**net start tcpip6**</span></span>
</dt> <dd>

<span data-ttu-id="647d2-112">Startet das IPv6-Protokoll, wenn es beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="647d2-112">Starts the IPv6 protocol if it was stopped.</span></span> <span data-ttu-id="647d2-113">Wenn eine neue Tcpip6.sys Treiberdatei im Verzeichnis "% SystemRoot% System32 Drivers" vorhanden ist \\ \\ , wird diese Treiberdatei geladen.</span><span class="sxs-lookup"><span data-stu-id="647d2-113">If a new Tcpip6.sys driver file is present in the %systemroot%\\System32\\Drivers directory, that driver file is loaded.</span></span>

</dd> </dl>

 

 



