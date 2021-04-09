---
description: Das Microsoft Windows-Betriebssystem bietet Unterstützung für eine Vielzahl von Hardware Geräten und Netzwerk Zeit Protokollen mithilfe der Zeit Anbieter Architektur.
ms.assetid: a7575373-eeda-4f2a-85e5-d1b50994e7ae
title: Zeit Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c844e2c4d0d49e87e978a47621338b167c4f5a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867380"
---
# <a name="time-provider"></a><span data-ttu-id="c9315-103">Zeit Anbieter</span><span class="sxs-lookup"><span data-stu-id="c9315-103">Time Provider</span></span>

<span data-ttu-id="c9315-104">Das Microsoft Windows-Betriebssystem bietet Unterstützung für eine Vielzahl von Hardware Geräten und Netzwerk Zeit Protokollen mithilfe der *Zeit Anbieter* Architektur.</span><span class="sxs-lookup"><span data-stu-id="c9315-104">The Microsoft Windows operating system provides support for a variety of hardware devices and network time protocols using the *time provider* architecture.</span></span> <span data-ttu-id="c9315-105">Eingabe Zeit Anbieter rufen genaue Zeitstempel von der Hardware oder dem Netzwerk ab, und Ausgabezeit Anbieter stellen Zeitstempel für andere Clients im Netzwerk bereit.</span><span class="sxs-lookup"><span data-stu-id="c9315-105">Input time providers retrieve accurate time stamps from hardware or the network, and output time providers provide time stamps to other clients on the network.</span></span>

<span data-ttu-id="c9315-106">Zeit Anbieter werden vom *Zeit Anbieter-Manager* verwaltet.</span><span class="sxs-lookup"><span data-stu-id="c9315-106">Time providers are managed by the *time provider manager*.</span></span> <span data-ttu-id="c9315-107">Er ist verantwortlich für das Laden, starten und Beenden von Zeit Anbietern, die vom Dienststeuerungs-Manager gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="c9315-107">It is responsible for loading, starting, and stopping time providers as directed by the service control manager.</span></span> <span data-ttu-id="c9315-108">Diese Schnittstelle vereinfacht das Schreiben eines Zeit Anbieters, als ein vollständiger Dienst zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="c9315-108">This interface makes writing a time provider easier than writing a full service.</span></span>

-   [<span data-ttu-id="c9315-109">Erstellen eines Zeit Anbieters</span><span class="sxs-lookup"><span data-stu-id="c9315-109">Creating a Time Provider</span></span>](creating-a-time-provider.md)
-   [<span data-ttu-id="c9315-110">Registrieren eines Zeit Anbieters</span><span class="sxs-lookup"><span data-stu-id="c9315-110">Registering a Time Provider</span></span>](registering-a-time-provider.md)
-   [<span data-ttu-id="c9315-111">Beispiel Zeit Anbieter</span><span class="sxs-lookup"><span data-stu-id="c9315-111">Sample Time Provider</span></span>](sample-time-provider.md)

## <a name="related-topics"></a><span data-ttu-id="c9315-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c9315-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9315-113">Windows-Zeitdienst</span><span class="sxs-lookup"><span data-stu-id="c9315-113">Windows Time Service</span></span>](https://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/security/ws03mngd/26_s3wts.mspx)
</dt> </dl>

 

 



