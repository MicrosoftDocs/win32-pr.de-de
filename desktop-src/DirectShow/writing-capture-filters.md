---
description: Schreiben von Erfassungs Filtern
ms.assetid: 7dfd1009-da09-49dc-a200-3d7a9f1c70c1
title: Schreiben von Erfassungs Filtern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de1a64de2b56dbc0728432307036fc46387f539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350279"
---
# <a name="writing-capture-filters"></a><span data-ttu-id="669ee-103">Schreiben von Erfassungs Filtern</span><span class="sxs-lookup"><span data-stu-id="669ee-103">Writing Capture Filters</span></span>

<span data-ttu-id="669ee-104">Das Schreiben eines Audiofilters oder Video Erfassungs Filters für DirectShow wird nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="669ee-104">Writing an audio or video capture filter for DirectShow is not recommended.</span></span> <span data-ttu-id="669ee-105">Stattdessen bietet DirectShow automatische Unterstützung für Audiogeräte und Video Erfassungsgeräte, mithilfe von Wrapper Filtern und dem [Enumerator des System Geräts](system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="669ee-105">Instead, DirectShow provides automatic support for audio and video capture devices, using wrapper filters and the [System Device Enumerator](system-device-enumerator.md).</span></span> <span data-ttu-id="669ee-106">Weitere Informationen zum Implementieren eines Gerätetreibers finden Sie in der Dokumentation zum Windows-Treiberkit (WDK).</span><span class="sxs-lookup"><span data-stu-id="669ee-106">For more information about implementing a device driver, refer to the Windows Driver Kit (WDK) documentation.</span></span>

<span data-ttu-id="669ee-107">Dieser Abschnitt ist nur für Entwickler gedacht, die benutzerdefinierte Daten von einem ungewöhnlichen Hardware Gerät erfassen müssen.</span><span class="sxs-lookup"><span data-stu-id="669ee-107">This section is intended only for developers who need to capture some kind of custom data from an unusual hardware device.</span></span>

<span data-ttu-id="669ee-108">Dieser Artikel enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="669ee-108">This article contains the following sections:</span></span>

-   [<span data-ttu-id="669ee-109">PIN-Anforderungen für Erfassungs Filter</span><span class="sxs-lookup"><span data-stu-id="669ee-109">Pin Requirements for Capture Filters</span></span>](pin-requirements-for-capture-filters.md)
-   [<span data-ttu-id="669ee-110">Implementieren einer Vorschau-PIN (optional)</span><span class="sxs-lookup"><span data-stu-id="669ee-110">Implementing a Preview Pin (Optional)</span></span>](implementing-a-preview-pin--optional.md)
-   [<span data-ttu-id="669ee-111">Erstellen von Daten in einem Erfassungs Filter</span><span class="sxs-lookup"><span data-stu-id="669ee-111">Producing Data in a Capture Filter</span></span>](producing-data-in-a-capture-filter.md)

## <a name="related-topics"></a><span data-ttu-id="669ee-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="669ee-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="669ee-113">Schreiben von DirectShow-Filtern</span><span class="sxs-lookup"><span data-stu-id="669ee-113">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



