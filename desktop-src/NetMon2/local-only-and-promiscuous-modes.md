---
description: Monitore können Frames im reinen Modus oder im gemischten-Modus untersuchen.
ms.assetid: 4646f5bb-e3e3-4929-91b7-f68c5b70ccb3
title: Local-Only-und Promiscuous-Modi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd1188760d8de31836de3fbd437854a5df138402
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354512"
---
# <a name="local-only-and-promiscuous-modes"></a><span data-ttu-id="fc676-103">Local-Only-und Promiscuous-Modi</span><span class="sxs-lookup"><span data-stu-id="fc676-103">Local-Only and Promiscuous Modes</span></span>

<span data-ttu-id="fc676-104">Monitore können Frames im reinen Modus oder im gemischten-Modus untersuchen.</span><span class="sxs-lookup"><span data-stu-id="fc676-104">Monitors can examine frames in local-only mode or promiscuous mode.</span></span>

<span data-ttu-id="fc676-105">Im reinen Modus gibt der Netzwerk Paketanbieter (NPP) Frames zurück, die an den bzw. von dem Computer gesendet werden, auf dem der Monitor ausgeführt wird, einschließlich der Übertragungen und mit, die an den lokalen Computer weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="fc676-105">In local-only mode, the network packet provider (NPP) returns frames that are sent to or from the computer on which the monitor is running, including broadcasts and multicasts directed to the local machine.</span></span> <span data-ttu-id="fc676-106">Der lokale Modus ist zwar auf Lokal gesteuerte Frames beschränkt, aber auch der lokale Modus ist weitaus weniger Prozessor intensiv.</span><span class="sxs-lookup"><span data-stu-id="fc676-106">Although limited to locally directed frames, local-mode is also much less processor intensive.</span></span>

<span data-ttu-id="fc676-107">Im gemischten-Modus kann der Monitor auch auf Datenverkehr achten, der nicht an den lokalen Computer weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="fc676-107">In promiscuous mode, the monitor can also watch for traffic that is not directed to or from the local computer.</span></span> <span data-ttu-id="fc676-108">Wenn für den Monitor nicht das Flag, MCS \_ Create \_ pmode \_ , \_ in der [onloadingdll](onloadingdll.md) -Funktion nicht erforderlich angegeben ist, geht der Monitor Steuerungs Dienst (Monitor Control Service, mcsvc) davon aus, dass der Monitor beim Laden der Monitor-DLL den gemischten-Modus erfordert.</span><span class="sxs-lookup"><span data-stu-id="fc676-108">Unless the monitor has specified the flag, MCS\_CREATE\_PMODE\_NOT\_REQUIRED, in the [OnLoadingDLL](onloadingdll.md) function, the Monitor Control Service (MCSVC) assumes that the monitor requires promiscuous mode when it loads the monitor DLL.</span></span>

 

 



