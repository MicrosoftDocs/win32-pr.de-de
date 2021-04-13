---
title: DRM-Netzwerk Vorgänge
description: DRM-Netzwerk Vorgänge
ms.assetid: 4a10c811-2aa1-4b97-8a72-61e8b04075a8
keywords:
- Windows Media-Format-SDK, DRM-Netzwerk Vorgänge
- Advanced Systems Format (ASF), DRM-Netzwerk Vorgänge
- ASF (Advanced Systems Format), DRM-Netzwerk Vorgänge
- Digital Rights Management (DRM), Netzwerk Vorgänge
- DRM (Digital Rights Management), Netzwerk Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 875186e43e066d71847da014468e9b1764b60cf2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309387"
---
# <a name="drm-network-operations"></a><span data-ttu-id="61f5f-108">DRM-Netzwerk Vorgänge</span><span class="sxs-lookup"><span data-stu-id="61f5f-108">DRM Network Operations</span></span>

<span data-ttu-id="61f5f-109">Mehrere DRM-bezogene Vorgänge erfordern, dass Ihre Anwendung eine Verbindung mit einem Dienst herstellt, der in einem Netzwerk ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="61f5f-109">Several DRM-related operations require your application to connect to a service running on a network.</span></span> <span data-ttu-id="61f5f-110">Zu diesen Vorgängen gehören die Personalisierung, der Lizenzerwerb, die Lizenz Sperrung und die Lizenz Sicherung und-Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="61f5f-110">These operations include individualization, license acquisition, license revocation, and license backup and restoration.</span></span>

<span data-ttu-id="61f5f-111">Wie bei jeder Netzwerk Transaktion sollte Ihre Anwendung eine Vielzahl von Schwierigkeiten berücksichtigen, wenn Sie Features einschließen, für die Netzwerk Vorgänge erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="61f5f-111">As with any network transaction, your application should account for a variety of difficulties when including features that require network operations.</span></span> <span data-ttu-id="61f5f-112">Die Anwendung sollte den Status des Vorgangs bis zu dem für das jeweilige Feature möglichen Umfang nachverfolgen, normalerweise durch die Verarbeitung von Statusmeldungen.</span><span class="sxs-lookup"><span data-stu-id="61f5f-112">Your application should track the status of the operation to whatever extent is possible for the specific feature, usually by handling status messages.</span></span> <span data-ttu-id="61f5f-113">Sie sollten dem Benutzer Feedback zum Status geben.</span><span class="sxs-lookup"><span data-stu-id="61f5f-113">You should provide feedback to the user about status.</span></span> <span data-ttu-id="61f5f-114">Wenn beim ersten Versuch ein Vorgang fehlschlägt, sollten Sie dem Benutzer die Möglichkeit geben, den Vorgang zu wiederholen.</span><span class="sxs-lookup"><span data-stu-id="61f5f-114">If an operation fails on the first try, you should give the user the opportunity to retry.</span></span> <span data-ttu-id="61f5f-115">In vielen Fällen tritt beim ersten Versuch eine Schwierigkeit auf, ein nachfolgende Versuch wird jedoch ohne Fehler abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="61f5f-115">In many cases, the first attempt encounters difficulty, but a subsequent try completes without error.</span></span>

> [!Note]  
> <span data-ttu-id="61f5f-116">DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="61f5f-116">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="61f5f-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="61f5f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61f5f-118">**Aktivieren DRM-Unterstützung**</span><span class="sxs-lookup"><span data-stu-id="61f5f-118">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




