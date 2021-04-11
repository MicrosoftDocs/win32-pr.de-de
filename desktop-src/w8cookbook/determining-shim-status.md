---
title: Bestimmen des Shim-Status
description: Bestimmen des Shim-Status
ms.assetid: 8D0B633F-9117-4F90-BF8C-AC5F57FCD30B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b830cbb4579aa2e523dfe2ec1129ed9cd10f37
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310904"
---
# <a name="determining-shim-status"></a><span data-ttu-id="8ddd0-103">Bestimmen des Shim-Status</span><span class="sxs-lookup"><span data-stu-id="8ddd0-103">Determining shim status</span></span>

## <a name="platforms"></a><span data-ttu-id="8ddd0-104">Plattformen</span><span class="sxs-lookup"><span data-stu-id="8ddd0-104">Platforms</span></span>

<dl> <span data-ttu-id="8ddd0-105">Clients-Windows 8</span><span class="sxs-lookup"><span data-stu-id="8ddd0-105">Clients - Windows 8</span></span>  
<span data-ttu-id="8ddd0-106">Server-Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8ddd0-106">Servers - Windows Server 2012</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="8ddd0-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8ddd0-107">Description</span></span>

<span data-ttu-id="8ddd0-108">Windows 8 protokolliert Ereignisse, wenn für Apps aus verschiedenen Gründen ein Shim durchlaufen wird.</span><span class="sxs-lookup"><span data-stu-id="8ddd0-108">Windows 8 logs events when apps are being shimmed for various reasons.</span></span> <span data-ttu-id="8ddd0-109">Die einfachste Möglichkeit, um zu ermitteln, ob Ihre APP Shim ist, besteht darin, die Ereignisanzeige zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="8ddd0-109">The easiest way to determine if your app is being shimmed is to check the event viewer.</span></span> <span data-ttu-id="8ddd0-110">Wechseln Sie zu Anwendungs-und Dienst Protokolle \\ Microsoft Windows Application-Experience-Programm \\ Telemetrie.</span><span class="sxs-lookup"><span data-stu-id="8ddd0-110">Go to Applications and Services Logs\\Microsoft Windows Application-Experience Program\\Telemetry.</span></span>

## <a name="mitigation"></a><span data-ttu-id="8ddd0-111">Minderung</span><span class="sxs-lookup"><span data-stu-id="8ddd0-111">Mitigation</span></span>

<span data-ttu-id="8ddd0-112">Die beste Möglichkeit, das Shimmen zu erreichen, besteht darin, die ausführbare Datei umzubenennen oder die Hauptversion um 1 zu erhöhen (die ausführbare Datei neu zu kompilieren).</span><span class="sxs-lookup"><span data-stu-id="8ddd0-112">The best way to get yourself out of shimming is to rename the executable or to increase the major version by 1 (recompile the executable).</span></span>

 

 




