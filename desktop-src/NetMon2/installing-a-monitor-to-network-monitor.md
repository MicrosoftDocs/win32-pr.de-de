---
description: Das Installieren einer Monitor-dll ist ein einfacher Prozess.
ms.assetid: f2c18faa-0010-4d26-b7e9-e8a7b5d11981
title: Installieren eines Monitors zum Netzwerkmonitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7fb6847d1ea93895b190ce2377247c586c06f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218844"
---
# <a name="installing-a-monitor-to-network-monitor"></a><span data-ttu-id="0ce82-103">Installieren eines Monitors zum Netzwerkmonitor</span><span class="sxs-lookup"><span data-stu-id="0ce82-103">Installing a Monitor to Network Monitor</span></span>

<span data-ttu-id="0ce82-104">Das Installieren einer Monitor-dll ist ein einfacher Prozess.</span><span class="sxs-lookup"><span data-stu-id="0ce82-104">Installing a monitor DLL is a simple process.</span></span> <span data-ttu-id="0ce82-105">Kopieren Sie zunächst die dll und das zugehörige HTML-Konfigurations Formular in das Unterverzeichnis Ihrer NPP-Monitore (z \\ . b. C: Windows \\ system32 \\ NPP- \\ Monitore).</span><span class="sxs-lookup"><span data-stu-id="0ce82-105">First, copy the DLL and the associated HTML configuration form to your NPP Monitors subdirectory (for example, C:\\Windows\\System32\\Npp\\Monitors).</span></span> <span data-ttu-id="0ce82-106">Beim Kopieren in das Verzeichnis wird der Monitor erkannt und ist verfügbar, wenn das Überwachungs Steuerungs Tool oder der Überwachungs Steuerungs Dienst (Monitor Control Service, mcsvc) das nächste Mal aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="0ce82-106">When copied to the directory, the monitor will be recognized and available the next time the Monitor Control Tool or Monitor Control Service (MCSVC) is activated.</span></span>

<span data-ttu-id="0ce82-107">Wenn die Umgebungsvariable "% SystemRoot%" beispielsweise "c: \\ Windows" ist, ist das Monitor-Unterverzeichnis "c: \\ Windows \\ system32 \\ NPP \\ Monitors".</span><span class="sxs-lookup"><span data-stu-id="0ce82-107">For example, if the environment variable, %SystemRoot% is C:\\Windows, then the monitor subdirectory is C:\\Windows\\System32\\Npp\\Monitors.</span></span>

 

 



