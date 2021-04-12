---
title: Drawdib-Vorgänge
description: Drawdib-Vorgänge
ms.assetid: 785ad42e-0c77-44a4-b4ef-be2a0ee2b563
keywords:
- Drawdib, Info
- Drawdib, zugreifen auf
- Drawdib, öffnen
- Drawdib, Vorgänge
- Drawdib, Gerätekontext (DC)
- DC (Gerätekontext)
- Drawdibopen-Funktion
- Drawdibclose-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc366287cdf481d70ef03aa82df5ea248673280b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471749"
---
# <a name="drawdib-operations"></a><span data-ttu-id="d776b-111">Drawdib-Vorgänge</span><span class="sxs-lookup"><span data-stu-id="d776b-111">DrawDib Operations</span></span>

<span data-ttu-id="d776b-112">Mithilfe der [**drawdibopen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) -Funktion können Sie auf die gesamte Gruppe von drawdib-Funktionen zugreifen.</span><span class="sxs-lookup"><span data-stu-id="d776b-112">You can access the entire group of DrawDib functions by using the [**DrawDibOpen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) function.</span></span> <span data-ttu-id="d776b-113">Diese Funktion lädt die dll (Dynamic-Link Library), ordnet Speicherressourcen zu, erstellt einen drawdib-Gerätekontext (DC) und verwaltet einen Verweis Zähler für die Anzahl der DCS, die initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="d776b-113">This function loads the dynamic-link library (DLL), allocates memory resources, creates a DrawDib device context (DC), and maintains a reference count of the number of DCs that are initialized.</span></span> <span data-ttu-id="d776b-114">**Drawdibopen** gibt auch ein Handle des neuen DC zurück, den Sie mit den anderen drawdib-Funktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="d776b-114">**DrawDibOpen** also returns a handle of the new DC that you use with the other DrawDib functions.</span></span>

<span data-ttu-id="d776b-115">Sie können einen drawdib-DC freigeben, wenn Sie die Verwendung mithilfe der [**drawdibclose**](/windows/desktop/api/Vfw/nf-vfw-drawdibclose) -Funktion abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="d776b-115">You can release a DrawDib DC when you finish using it by using the [**DrawDibClose**](/windows/desktop/api/Vfw/nf-vfw-drawdibclose) function.</span></span> <span data-ttu-id="d776b-116">**Drawdibclose** Dekremente auch den Verweis Zähler der Anwendungen, die auf die dll zugreifen.</span><span class="sxs-lookup"><span data-stu-id="d776b-116">**DrawDibClose** also decrements the reference count of the applications accessing the DLL.</span></span> <span data-ttu-id="d776b-117">Der **aufzurufende drawdibclose** -Befehl sollte die letzte drawdib-Funktion in der Anwendung sein.</span><span class="sxs-lookup"><span data-stu-id="d776b-117">The call to **DrawDibClose** should be the last DrawDib function in your application.</span></span>

<span data-ttu-id="d776b-118">Beliebig viele drawdib-DCS können erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d776b-118">You can create as many DrawDib DCs as you want.</span></span> <span data-ttu-id="d776b-119">Sie können mehrere drawdib DCS verwenden, um mehrere Bitmaps gleichzeitig zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="d776b-119">You can use multiple DrawDib DCs to draw several bitmaps simultaneously.</span></span> <span data-ttu-id="d776b-120">Sie können auch mehrere drawdib DCS mit eindeutigen Merkmalen erstellen, sodass Ihre Anwendung den DC mit den geeignetsten Einstellungen auswählen und dann verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="d776b-120">You can also create multiple DrawDib DCs, each with unique characteristics, so your application can choose and then use the DC with the most appropriate settings.</span></span> <span data-ttu-id="d776b-121">Beispielsweise können Sie zwei drawdib-DCS in einer Anwendung erstellen: eine, die ein Bild bei der normalen Auflösung anzeigt, und die andere, die einen vergrößerten Teil des Bilds anzeigt.</span><span class="sxs-lookup"><span data-stu-id="d776b-121">For example, you can create two DrawDib DCs in an application: one that displays an image at its normal resolution, and the other that displays an enlarged portion of the image.</span></span>

<span data-ttu-id="d776b-122">Um effizient auszuführen, benötigen drawdib-Funktionen Informationen zum Anzeige Adapter und dessen Treiber.</span><span class="sxs-lookup"><span data-stu-id="d776b-122">To run efficiently, DrawDib functions require information about the display adapter and its driver.</span></span> <span data-ttu-id="d776b-123">Das Anzeige Profil wird durch Ausführen einer Reihe von Tests auf dem Anzeige Adapter abgerufen, wenn der Zugriff auf die dll, die die drawdib-Funktionen enthält, erstmalig erfolgt.</span><span class="sxs-lookup"><span data-stu-id="d776b-123">The display profile is obtained by running a series of tests on the display adapter the first time the DLL containing the DrawDib functions is accessed.</span></span> <span data-ttu-id="d776b-124">Die drawdib-Funktionen verwenden diese Informationen für alle Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="d776b-124">The DrawDib functions use this information for all applications.</span></span> <span data-ttu-id="d776b-125">Sie können diese Tests bei Bedarf mit der [**drawdibprofiledisplay**](/windows/desktop/api/Vfw/nf-vfw-drawdibprofiledisplay) -Funktion wiederholen.</span><span class="sxs-lookup"><span data-stu-id="d776b-125">You can repeat these tests when necessary by using the [**DrawDibProfileDisplay**](/windows/desktop/api/Vfw/nf-vfw-drawdibprofiledisplay) function.</span></span>

> [!Note]  
> <span data-ttu-id="d776b-126">Das Abrufen und Speichern des Anzeige Profils ist in der Regel ein einmalige vorkommen.</span><span class="sxs-lookup"><span data-stu-id="d776b-126">Retrieving and storing the display profile is typically a one-time occurrence.</span></span> <span data-ttu-id="d776b-127">Wenn die Profilinformationen jedoch gelöscht werden oder ein anderer Anzeigetreiber im System installiert ist, führt drawdib die Tests erneut aus.</span><span class="sxs-lookup"><span data-stu-id="d776b-127">If, however, the profile information is deleted or another display driver is installed in the system, DrawDib reruns the tests.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d776b-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d776b-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d776b-129">Informationen über die drawdib-Funktionen</span><span class="sxs-lookup"><span data-stu-id="d776b-129">About the DrawDib Functions</span></span>](about-the-drawdib-functions.md)
</dt> </dl>

 

 




