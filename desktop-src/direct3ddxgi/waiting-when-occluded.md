---
description: Apps können auf ein Ereignis warten, wenn das Rendern auf dem Bildschirm unnötig ist (d. h., während Sie ausgeblendet werden).
ms.assetid: B9EC23C9-A311-4BD9-BBE8-908A1334A541
title: Warten auf ein Ereignis, wenn das Rendering unnötig ist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b553ef52e812c5117e5d9669ba13b47b9f4280c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344310"
---
# <a name="waiting-on-an-event-when-rendering-is-unnecessary"></a><span data-ttu-id="ce0a7-103">Warten auf ein Ereignis, wenn das Rendering unnötig ist</span><span class="sxs-lookup"><span data-stu-id="ce0a7-103">Waiting on an event when rendering is unnecessary</span></span>

<span data-ttu-id="ce0a7-104">Apps können auf ein Ereignis warten, wenn das Rendern auf dem Bildschirm unnötig ist (d. h., während Sie ausgeblendet werden).</span><span class="sxs-lookup"><span data-stu-id="ce0a7-104">Apps can wait on an event when rendering to the screen is unnecessary (that is, while they are occluded).</span></span> <span data-ttu-id="ce0a7-105">Wenn die Desktopfenster-Manager (DWM) oder eine APP synchronisiert werden, ist kein Rendering erforderlich, und das Betriebssystem kann für längere Zeit in niedrigeren Energiezuständen bleiben.</span><span class="sxs-lookup"><span data-stu-id="ce0a7-105">When the Desktop Window Manager (DWM) or an app is occluded, no rendering is necessary and the operating system can stay in lower power states for longer periods of time.</span></span> <span data-ttu-id="ce0a7-106">Dies spart Strom und erweitert die Akku Lebensdauer.</span><span class="sxs-lookup"><span data-stu-id="ce0a7-106">This saves power and extends battery life.</span></span>

<span data-ttu-id="ce0a7-107">Eine APP kann auf ein Ereignis warten, wenn Folgendes folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="ce0a7-107">An app can wait on an event when:</span></span>

-   <span data-ttu-id="ce0a7-108">Alle Monitore sind deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="ce0a7-108">All the monitors are off.</span></span>
-   <span data-ttu-id="ce0a7-109">Die Sitzung, in der die app ausgeführt wird, wird getrennt.</span><span class="sxs-lookup"><span data-stu-id="ce0a7-109">The session that the app runs in is disconnected.</span></span>
-   <span data-ttu-id="ce0a7-110">Die APP wird ausschließlich in einer einzigen Monitor Konfiguration im Vollbildmodus ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ce0a7-110">The app runs in full screen exclusively on a single monitor configuration.</span></span>
-   <span data-ttu-id="ce0a7-111">Die APP wird auf einem anderen Desktop als der aktive Desktop ausgeführt und verfügt nicht über die Berechtigung zum renderingzugriff auf dem aktiven Desktop.</span><span class="sxs-lookup"><span data-stu-id="ce0a7-111">The app runs on a different desktop than the active desktop and does not have permission to render on the active desktop.</span></span>

<span data-ttu-id="ce0a7-112">Das Betriebssystem löst das Ereignis aus, wenn die APP wieder gereinigen werden kann.</span><span class="sxs-lookup"><span data-stu-id="ce0a7-112">The operating system triggers the event when the app is able to render again.</span></span> <span data-ttu-id="ce0a7-113">Das Ereignis wird während eines Treiber Upgrades oder einer TDR-Prozession (Timeout Erkennung und Wiederherstellung) nicht gelöscht, es wird jedoch gelöscht, wenn der neue Adapter und die Monitore aktiv werden.</span><span class="sxs-lookup"><span data-stu-id="ce0a7-113">The event is not cleared during a driver upgrade, or timeout detection and recovery (TDR) procession, however it is cleared when the new adapter and monitors become active.</span></span>

<span data-ttu-id="ce0a7-114">Wenn Sie möchten, dass Ihre APP über Änderungen des Status der Okklusion benachrichtigt wird, muss sich die APP für diese Änderungen registrieren.</span><span class="sxs-lookup"><span data-stu-id="ce0a7-114">If you want your app to be notified about changes of occlusion status, the app must register for these changes.</span></span> <span data-ttu-id="ce0a7-115">Eine APP kann sich registrieren, um über Änderungen des Status der Okklusion über eine Nachricht an ein Fenster oder durch Ereignis Signalisierung benachrichtigt zu werden.</span><span class="sxs-lookup"><span data-stu-id="ce0a7-115">An app can register to be notified about changes of occlusion status through a message to a window or through event signaling.</span></span> <span data-ttu-id="ce0a7-116">Um sich zu registrieren, um Benachrichtigungs Statusänderungen an einem Fenster zu empfangen, ruft eine APP die [**IDXGIFactory2:: registeroksionstatuswindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="ce0a7-116">To register to receive notification messages to a window about occlusion status changes, an app calls the [**IDXGIFactory2::RegisterOcclusionStatusWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow) method.</span></span> <span data-ttu-id="ce0a7-117">Um sich zu registrieren, um Benachrichtigungen über die Statusänderungen der Okklusion per Ereignis Signalisierung zu empfangen, ruft eine APP die [**IDXGIFactory2:: registeroksionstatusevent**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="ce0a7-117">To register to receive notification of occlusion status changes via event signaling, an app calls the [**IDXGIFactory2::RegisterOcclusionStatusEvent**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent) method.</span></span> <span data-ttu-id="ce0a7-118">Beide Methoden geben einen Zeiger auf einen Schlüsselwert zurück, der von der APP zum Aufheben der Registrierung der Benachrichtigung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ce0a7-118">Both methods return a pointer to a key value that the app can use to unregister the notification.</span></span> <span data-ttu-id="ce0a7-119">Um die Registrierung der Benachrichtigung aufzuheben, übergibt die APP diesen Schlüsselwert an die [**IDXGIFactory2:: unregisteroksionstatus**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus) -Methode.</span><span class="sxs-lookup"><span data-stu-id="ce0a7-119">To unregister the notification, the app passes this key value to the [**IDXGIFactory2::UnregisterOcclusionStatus**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce0a7-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ce0a7-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce0a7-121">DXGI 1,2-Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="ce0a7-121">DXGI 1.2 Improvements</span></span>](dxgi-1-2-improvements.md)
</dt> </dl>

 

 



