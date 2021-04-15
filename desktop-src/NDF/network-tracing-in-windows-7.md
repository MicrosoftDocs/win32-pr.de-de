---
title: Netzwerk Ablauf Verfolgung in Windows 7
description: Windows 7 baut auf dem Netzwerk Diagnose Framework (ndf) auf, um eine schnelle Methode zur Behebung von Problemen mit der Netzwerk Konnektivität bereitzustellen, indem die Erfassung aller benötigten Informationen in einem Schritt und die Verwendung der Ereignis Ablauf Verfolgung für Windows (ETW) zum Protokollieren von Netzwerk Ereignis Paketen in einer einzelnen Datei genutzt wird.
ms.assetid: 7d331362-ff26-4ca0-aa45-07cc97304c7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e3abb4283262703123f8e7060a09af0b810477b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390985"
---
# <a name="network-tracing-in-windows-7"></a><span data-ttu-id="e2e42-103">Netzwerk Ablauf Verfolgung in Windows 7</span><span class="sxs-lookup"><span data-stu-id="e2e42-103">Network Tracing in Windows 7</span></span>

<span data-ttu-id="e2e42-104">Wenn die Komplexität des Netzwerk Stapels zunimmt, ist es oft schwierig, Probleme im Stapel schnell zu verfolgen und zu diagnostizieren.</span><span class="sxs-lookup"><span data-stu-id="e2e42-104">As the complexity of the networking stack increases, it is often difficult to quickly trace and diagnose issues within the stack.</span></span> <span data-ttu-id="e2e42-105">Windows 7 baut auf dem Netzwerk Diagnose Framework (ndf) auf, um eine schnelle Methode zur Behebung von Problemen mit der Netzwerk Konnektivität bereitzustellen, indem die Erfassung aller benötigten Informationen in einem Schritt und die Verwendung der [Ereignis Ablauf Verfolgung für Windows (ETW)](../etw/event-tracing-portal.md) zum Protokollieren von Netzwerk Ereignissen & Paketen in einer einzigen Datei genutzt wird.</span><span class="sxs-lookup"><span data-stu-id="e2e42-105">Windows 7 expands on the Network Diagnostic Framework (NDF) to provide a quick method for troubleshooting network connectivity issues by enabling collection of all the needed information in one step, and by leveraging [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) to log network events & packets in a single file.</span></span>

<span data-ttu-id="e2e42-106">Verwandte Ereignisse und Pakete werden für eine bestimmte Aktivität, z. b. das Durchsuchen einer Website, in den verschiedenen Komponenten im Netzwerk Stapel gruppiert.</span><span class="sxs-lookup"><span data-stu-id="e2e42-106">Related events and packets are grouped together for a given activity, such as browsing a website, across the various components in the networking stack.</span></span> <span data-ttu-id="e2e42-107">Die Ausgabe dieses Prozesses ist eine ETL-Datei (Event Trace Log, Ereignis Ablauf Verfolgungs Protokoll).</span><span class="sxs-lookup"><span data-stu-id="e2e42-107">The output of this process is an Event Trace Log (ETL) file.</span></span> <span data-ttu-id="e2e42-108">Durch das zulassen, dass alle Ereignisse im Zusammenhang mit einer bestimmten Aktivität gleichzeitig in dieser Datei angezeigt werden, kann die Zeit, die zum isolieren und Diagnostizieren von Netzwerkproblemen erforderlich ist, erheblich reduziert werden.</span><span class="sxs-lookup"><span data-stu-id="e2e42-108">By allowing all of the events related to a specific activity to be viewed at once in this file, the time required to isolate and diagnose network issues can be greatly reduced.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e2e42-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="e2e42-109">In This Section</span></span>



| <span data-ttu-id="e2e42-110">Thema</span><span class="sxs-lookup"><span data-stu-id="e2e42-110">Topic</span></span>                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2e42-111">Netzwerk Ablauf Verfolgung in Windows 7: Architektur</span><span class="sxs-lookup"><span data-stu-id="e2e42-111">Network Tracing in Windows 7: Architecture</span></span>](network-tracing-in-windows-7-architecture.md)                                |
| [<span data-ttu-id="e2e42-112">Tools zur Problembehandlung mithilfe der Netzwerk Ablauf Verfolgung in Windows 7</span><span class="sxs-lookup"><span data-stu-id="e2e42-112">Tools for Troubleshooting using Network Tracing in Windows 7</span></span>](tools-for-troubleshooting-network-tracing-in-windows-7.md) |
| [<span data-ttu-id="e2e42-113">Netzwerk Ablauf Verfolgung in Windows 7: Szenarios</span><span class="sxs-lookup"><span data-stu-id="e2e42-113">Network Tracing in Windows 7: Scenarios</span></span>](network-tracing-in-windows-7-scenarios.md)                                      |



 

 

 