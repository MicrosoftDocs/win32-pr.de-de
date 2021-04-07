---
title: System Einträge für Kompressoren, Debug-und Renderer
description: System Einträge für Kompressoren, Debug-und Renderer
ms.assetid: b27bbd5b-a218-49bb-b179-b24ce39869a1
keywords:
- Video für Windows (Vfw), Systemeinträge für den Kompressor
- VFW (Video für Windows), Systemeinträge für den Kompressor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b46d9c6fd8974511698bcb687c580e68be3757ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713301"
---
# <a name="system-entries-for-compressors-decompressors-and-renderers"></a><span data-ttu-id="b5a07-105">System Einträge für Kompressoren, Debug-und Renderer</span><span class="sxs-lookup"><span data-stu-id="b5a07-105">System Entries for Compressors, Decompressors, and Renderers</span></span>

<span data-ttu-id="b5a07-106">Das System verwendet Einträge in der Registrierung, um VCM-Treiber zu suchen.</span><span class="sxs-lookup"><span data-stu-id="b5a07-106">The system uses entries in the registry to find VCM drivers.</span></span> <span data-ttu-id="b5a07-107">Diese Einträge sind in Form von 2 4-Zeichen Codes, die durch einen Zeitraum voneinander getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="b5a07-107">These entries are in the form of two four-character codes separated by a period.</span></span> <span data-ttu-id="b5a07-108">Der erste Code, der aus vier Zeichen besteht, wird vom System definiert und kann eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="b5a07-108">The first four-character code is defined by the system and can be one of the following:</span></span>



| <span data-ttu-id="b5a07-109">Code mit vier Zeichen</span><span class="sxs-lookup"><span data-stu-id="b5a07-109">Four-character code</span></span> | <span data-ttu-id="b5a07-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b5a07-110">Description</span></span>                               |
|---------------------|-------------------------------------------|
| <span data-ttu-id="b5a07-111">VIDC</span><span class="sxs-lookup"><span data-stu-id="b5a07-111">"VIDC"</span></span>              | <span data-ttu-id="b5a07-112">Identifiziert die-Kompressoren und-Debug-Geräte.</span><span class="sxs-lookup"><span data-stu-id="b5a07-112">Identifies compressors and decompressors.</span></span> |
| <span data-ttu-id="b5a07-113">"Vids"</span><span class="sxs-lookup"><span data-stu-id="b5a07-113">"VIDS"</span></span>              | <span data-ttu-id="b5a07-114">Identifiziert videostreamrenderer.</span><span class="sxs-lookup"><span data-stu-id="b5a07-114">Identifies video-stream renderers.</span></span>        |
| <span data-ttu-id="b5a07-115">"Txts"</span><span class="sxs-lookup"><span data-stu-id="b5a07-115">"TXTS"</span></span>              | <span data-ttu-id="b5a07-116">Identifiziert textstreamrenderer.</span><span class="sxs-lookup"><span data-stu-id="b5a07-116">Identifies text-stream renderers.</span></span>         |
| <span data-ttu-id="b5a07-117">Au</span><span class="sxs-lookup"><span data-stu-id="b5a07-117">"AUDS"</span></span>              | <span data-ttu-id="b5a07-118">Identifiziert audiostreamhandler.</span><span class="sxs-lookup"><span data-stu-id="b5a07-118">Identifies audio-stream handlers.</span></span>         |



 

<span data-ttu-id="b5a07-119">Benutzerdefinierte Renderer können Ihre eigenen vier Zeichen Codes definieren.</span><span class="sxs-lookup"><span data-stu-id="b5a07-119">Custom renderers can define their own four-character codes.</span></span>

<span data-ttu-id="b5a07-120">Der zweite Code mit vier Zeichen wird vom Treiber definiert.</span><span class="sxs-lookup"><span data-stu-id="b5a07-120">The second four-character code is defined by the driver.</span></span> <span data-ttu-id="b5a07-121">In der Regel entspricht der zweite aus vier Zeichen bestehende Code dem Datentyp, der vom Treiber verarbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b5a07-121">Typically, the second four-character code corresponds to the type of data the driver can handle.</span></span>

<span data-ttu-id="b5a07-122">Beim Öffnen eines VCM-Treibers gibt eine Anwendung den Typ des Treibers und den Typ des benötigten Daten Handlers an.</span><span class="sxs-lookup"><span data-stu-id="b5a07-122">When opening a VCM driver, an application specifies the type of driver and the type of data handler it needs.</span></span> <span data-ttu-id="b5a07-123">Diese Informationen stammen in der Regel aus dem Datenstrom Header.</span><span class="sxs-lookup"><span data-stu-id="b5a07-123">Typically, this information comes from the stream header.</span></span> <span data-ttu-id="b5a07-124">Das System versucht, den angegebenen Daten Handler zu öffnen. wenn er jedoch fehlschlägt, durchsucht das System die Registrierung nach einem Treiber, der über den erforderlichen Handler verfügt.</span><span class="sxs-lookup"><span data-stu-id="b5a07-124">The system tries to open the specified data handler, but if it fails, the system searches the registry for a driver that has the required handler.</span></span>

<span data-ttu-id="b5a07-125">Bei der Suche nach dem Treiber versucht das System, die vier Zeichen Codes, die für den Treibertyp und den Daten Handler angegeben sind, mit den im Treiber Eintrag angegebenen Zeichen zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="b5a07-125">When searching for the driver, the system tries to match the four-character codes specified for the driver type and data handler with those specified in the driver entry.</span></span> <span data-ttu-id="b5a07-126">Wenn eine Anwendung z. b. den mssq-Kompressor angibt, durchsucht das System die Registrierung nach dem Treiber Eintrag "VIDC. mssq".</span><span class="sxs-lookup"><span data-stu-id="b5a07-126">For example, if an application specifies the compressor MSSQ, the system searches the registry for the driver entry VIDC.MSSQ.</span></span> <span data-ttu-id="b5a07-127">Wenn eine Übereinstimmung nicht gefunden werden kann, öffnet Sie jeden Treiber, der dem Treibertyp entspricht, und sucht einen, der den Typ der von der Anwendung festgelegten Daten verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="b5a07-127">If it cannot find a match, it opens each driver corresponding to the driver type and locates one that can handle the type of data your application specifies.</span></span> <span data-ttu-id="b5a07-128">Wenn das System z. b. "VIDC. mssq" nicht finden konnte, werden alle Treiber mit dem vierstelligen Code "VIDC" geöffnet, und Sie finden einen, der die Daten verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="b5a07-128">In the previous example, if the system could not find VIDC.MSSQ, it would open all drivers with the "VIDC" four-character code and locate one that can handle the data.</span></span>

 

 




