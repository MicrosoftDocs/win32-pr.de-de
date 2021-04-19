---
description: Zeigt, wie Wi-Fi Direct-Funktionen in Desktop-Apps verwendet werden.
ms.assetid: 50B95B7D-B860-44DF-8E78-1E7D2DC5A9B6
title: Verwenden der Wi-Fi Direct-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8850f5b278a158e32f78118cf5d0d408c123192e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358430"
---
# <a name="using-the-wi-fi-direct-functions"></a><span data-ttu-id="7bc05-103">Verwenden der Wi-Fi Direct-Funktionen</span><span class="sxs-lookup"><span data-stu-id="7bc05-103">Using the Wi-Fi Direct functions</span></span>

<span data-ttu-id="7bc05-104">In diesem Thema wird gezeigt, wie Sie Wi-Fi Direct-Funktionen in Desktop-Apps verwenden.</span><span class="sxs-lookup"><span data-stu-id="7bc05-104">This topics shows how to use Wi-Fi Direct functions in desktop apps.</span></span> <span data-ttu-id="7bc05-105">Ab Windows 8 und Windows Server 2012 wurden der systemeigenen WiFi-API Wi-Fi Direct-Funktionen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7bc05-105">Starting on Windows 8 and Windows Server 2012, Wi-Fi Direct functions were added to the Native Wifi API.</span></span>

<span data-ttu-id="7bc05-106">Die Wi-Fi Direct-Funktion basiert auf der Entwicklung der Wi-Fi Peer-to-Peer Technical Specification v 1.1 von der Wi-Fi Alliance (siehe [veröffentlichte Wi-Fi Alliance-Spezifikationen](https://www.wi-fi.org/)).</span><span class="sxs-lookup"><span data-stu-id="7bc05-106">The Wi-Fi Direct feature is based on the development of the Wi-Fi Peer-to-Peer Technical Specification v1.1 by the Wi-Fi Alliance (see [Wi-Fi Alliance Published Specifications](https://www.wi-fi.org/)).</span></span> <span data-ttu-id="7bc05-107">Das Ziel der Wi-Fi Peer-to-Peer-technischen Spezifikation besteht darin, eine Lösung für die Wi-Fi Geräte-zu-Gerät-Konnektivität bereitzustellen, ohne dass ein drahtloser Zugriffspunkt (Wireless AP) zum Einrichten der Verbindung oder die Verwendung des vorhandenen Wi-Fi Ad-hoc-Mechanismus (IBSS) erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7bc05-107">The goal of the Wi-Fi Peer-to-Peer Technical Specification is to provide a solution for Wi-Fi device-to-device connectivity without the need for either a Wireless Access Point (wireless AP) to setup the connection or the use of the existing Wi-Fi ad hoc (IBSS) mechanism.</span></span>

> [!Note]  
> <span data-ttu-id="7bc05-108">Der Ad-hoc-Modus ist möglicherweise in zukünftigen Versionen von Windows nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7bc05-108">Ad hoc mode might not be available in future versions of Windows.</span></span> <span data-ttu-id="7bc05-109">Beginnen Sie mit Windows 8.1 und Windows Server 2012 R2, und verwenden Sie stattdessen Wi-Fi Direct.</span><span class="sxs-lookup"><span data-stu-id="7bc05-109">Starting with Windows 8.1 and Windows Server 2012 R2, use Wi-Fi Direct instead.</span></span>

 

<span data-ttu-id="7bc05-110">Die folgenden Funktionen unterstützen die Wi-Fi Direct-Funktion.</span><span class="sxs-lookup"><span data-stu-id="7bc05-110">The following functions support the Wi-Fi Direct feature.</span></span>

-   <span data-ttu-id="7bc05-111">[**Wfdcancelopensession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) : gibt an, dass die APP eine ausstehende [**wfdstartopensession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) -Funktion abbrechen möchte, die noch nicht abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="7bc05-111">[**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) - Indicates that the app wants to cancel a pending [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function that has not completed.</span></span>
-   <span data-ttu-id="7bc05-112">[**Wfdclosehandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) : schließt ein Handle für den Wi-Fi Direct-Dienst.</span><span class="sxs-lookup"><span data-stu-id="7bc05-112">[**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) - Closes a handle to the Wi-Fi Direct service.</span></span>
-   <span data-ttu-id="7bc05-113">[**Wfdclosesession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) : schließt eine Sitzung nach einem zuvor erfolgreichen Rückruf der [**wfdstartopensession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="7bc05-113">[**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) - Closes a session after a previously successful call to the [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function.</span></span>
-   <span data-ttu-id="7bc05-114">[**Wfdopenhandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) : öffnet ein Handle für den Wi-Fi Direct-Dienst und aushandiert eine Version der direkten Wi-Fi-API für die Verwendung von.</span><span class="sxs-lookup"><span data-stu-id="7bc05-114">[**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) - Opens a handle to the Wi-Fi Direct service and negotiates a version of the Wi-FI Direct API to use.</span></span>
-   <span data-ttu-id="7bc05-115">[**WF dopenlegacysession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) : Ruft ein gespeichertes Profil für ein Wi-Fi direktes Legacy Gerät ab und wendet es an.</span><span class="sxs-lookup"><span data-stu-id="7bc05-115">[**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) - Retrieves and applies a stored profile for a Wi-Fi Direct legacy device.</span></span>
-   <span data-ttu-id="7bc05-116">[**Wfdstartopensession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) : startet eine Bedarfs gesteuerte Verbindung mit einem bestimmten Wi-Fi Direct-Gerät, das zuvor durch die Windows-Kopplung kombiniert wurde.</span><span class="sxs-lookup"><span data-stu-id="7bc05-116">[**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) - Starts an on-demand connection to a specific Wi-Fi Direct device, which has been previously paired through the Windows Pairing experience.</span></span>
-   <span data-ttu-id="7bc05-117">[**WF dupdatedevicevisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) : aktualisiert die Geräte Sichtbarkeit für die Wi-Fi direkte Geräteadresse für einen bestimmten installierten Wi-Fi direkt Geräteknoten.</span><span class="sxs-lookup"><span data-stu-id="7bc05-117">[**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) - Updates device visibility for the Wi-Fi Direct device address for a given installed Wi-Fi Direct device node.</span></span>
-   <span data-ttu-id="7bc05-118">[**WFD \_ \_Sitzung zum \_ abschließen \_ der Sitzung öffnen**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) : definiert die Rückruffunktion, die von der [**wfdstartopensession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) -Funktion aufgerufen wird, wenn der **wfdstartopensession** -Vorgang abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="7bc05-118">[**WFD\_OPEN\_SESSION\_COMPLETE\_CALLBACK**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) - Defines the callback function that is called by the [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function when the **WFDStartOpenSession** operation completes</span></span>

<span data-ttu-id="7bc05-119">Für eine Desktop-App erfordert die Wi-Fi Direct-Funktion, dass WLAN-Geräte zuvor vom Benutzer mit der Benutzeroberfläche der Windows-paarweise gekoppelt werden.</span><span class="sxs-lookup"><span data-stu-id="7bc05-119">For a desktop app, the Wi-Fi Direct feature requires that Wi-FI Direct devices be previously paired by the user with the Windows Pairing experience user interface.</span></span> <span data-ttu-id="7bc05-120">Nachdem diese Kopplung abgeschlossen ist, wird ein Profil gespeichert, mit dem die Wi-Fi Direct-Funktionen zum Starten einer Wi-Fi direkten Sitzung verwendet werden können, um eine Verbindung zwischen den Wi-Fi direkt Geräten herzustellen.</span><span class="sxs-lookup"><span data-stu-id="7bc05-120">Once this pairing is completed, a profile is stored that allows the Wi-Fi Direct functions to be used to start a Wi-Fi Direct session to establish a connection between the Wi-Fi Direct devices.</span></span>

<span data-ttu-id="7bc05-121">Um Wi-Fi Direct verwenden zu können, muss eine App zunächst ein Handle für den Wi-Fi Direct-Dienst abrufen, indem Sie die [**wfdopenhandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7bc05-121">In order to use Wi-Fi Direct, an app must first obtain a handle to the Wi-Fi Direct service by calling the [**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) function.</span></span> <span data-ttu-id="7bc05-122">Das von der **wfdopenhandle** -Funktion zurückgegebene Wi-Fi Direct-handle (WFD) wird für nachfolgende Wi-Fi direkte Funktionsaufrufe verwendet, die an den Wi-Fi Direct-Dienst gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="7bc05-122">The Wi-Fi Direct (WFD) handle returned by the **WFDOpenHandle** function is used for subsequent Wi-Fi Direct function calls made to the Wi-Fi Direct service.</span></span>

<span data-ttu-id="7bc05-123">Die [**wfdstartopensession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) -Funktion startet einen asynchronen Vorgang, um eine Bedarfs gesteuerte Verbindung mit einem bestimmten Wi-Fi Direct-Gerät zu starten.</span><span class="sxs-lookup"><span data-stu-id="7bc05-123">The [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function starts an asynchronous operation to start an on-demand connection to a specific Wi-Fi Direct device.</span></span> <span data-ttu-id="7bc05-124">Das Ziel Wi-Fi Gerät muss zuvor mit der Windows-Kopplung gekoppelt sein.</span><span class="sxs-lookup"><span data-stu-id="7bc05-124">The target Wi-Fi device must previously have been paired through the Windows Pairing experience.</span></span> <span data-ttu-id="7bc05-125">Wenn der asynchrone Vorgang abgeschlossen ist, wird die im *pfncallback* -Parameter angegebene Rückruffunktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="7bc05-125">When the asynchronous operation completes, the callback function specified in the *pfnCallback* parameter is called.</span></span>

<span data-ttu-id="7bc05-126">Sobald eine Anwendung mit dem Wi-Fi Direct-Dienst ausgeführt wird, sollte die Anwendung die [**wfdclosehandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) -Funktion so anrufen, dass Sie an den Wi-Fi Direct-Dienst signalisiert, dass die Anwendung mit dem Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7bc05-126">Once an application is done using the Wi-Fi Direct service, the application should call the [**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) function to signal to the Wi-Fi Direct service that the application is done using the service.</span></span> <span data-ttu-id="7bc05-127">Dies ermöglicht es dem Wi-Fi Direct-Dienst, von der Anwendung verwendete Ressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="7bc05-127">This allows the Wi-Fi Direct service to release resources used by the application.</span></span>

<span data-ttu-id="7bc05-128">Weitere Informationen zu Wi-Fi Direct für die Verwendung in Windows Store-Apps finden Sie unter " [**Peer Erfinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) " und verwandte Klassen im [**Windows. Networking. near**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041) -Namespace.</span><span class="sxs-lookup"><span data-stu-id="7bc05-128">For more information on Wi-Fi Direct for use in Windows Store apps, see [**PeerFinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) and related classes in the [**Windows.Networking.Proximity**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041) namespace.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7bc05-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7bc05-129">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="7bc05-130">**Weitere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="7bc05-130">**Other resources**</span></span>
</dt> <dt>

[<span data-ttu-id="7bc05-131">Informationen zu nativem WiFi</span><span class="sxs-lookup"><span data-stu-id="7bc05-131">About Native Wifi</span></span>](about-native-wifi.md)
</dt> <dt>

[<span data-ttu-id="7bc05-132">Informationen zur nativen WiFi-API</span><span class="sxs-lookup"><span data-stu-id="7bc05-132">About the Native Wifi API</span></span>](about-the-native-wifi-api.md)
</dt> <dt>

[<span data-ttu-id="7bc05-133">Informationen über die Wi-Fi Direct-Funktion</span><span class="sxs-lookup"><span data-stu-id="7bc05-133">About the Wi-Fi Direct feature</span></span>](about-the-wi-fi-direct-api.md)
</dt> <dt>

<span data-ttu-id="7bc05-134">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="7bc05-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7bc05-135">**Peer Erfinder**</span><span class="sxs-lookup"><span data-stu-id="7bc05-135">**PeerFinder**</span></span>](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041)
</dt> <dt>

[<span data-ttu-id="7bc05-136">**Rückruf für das Beenden der WFD- \_ \_ Sitzung \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7bc05-136">**WFD\_OPEN\_SESSION\_COMPLETE\_CALLBACK**</span></span>](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
</dt> <dt>

[<span data-ttu-id="7bc05-137">**WF-cancelopensession**</span><span class="sxs-lookup"><span data-stu-id="7bc05-137">**WFDCancelOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
</dt> <dt>

[<span data-ttu-id="7bc05-138">**WF-CloseHandle**</span><span class="sxs-lookup"><span data-stu-id="7bc05-138">**WFDCloseHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
</dt> <dt>

[<span data-ttu-id="7bc05-139">**WF-CloseSession**</span><span class="sxs-lookup"><span data-stu-id="7bc05-139">**WFDCloseSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
</dt> <dt>

[<span data-ttu-id="7bc05-140">**WF-openhandle**</span><span class="sxs-lookup"><span data-stu-id="7bc05-140">**WFDOpenHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
</dt> <dt>

[<span data-ttu-id="7bc05-141">**WF-openlegacysession**</span><span class="sxs-lookup"><span data-stu-id="7bc05-141">**WFDOpenLegacySession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
</dt> <dt>

[<span data-ttu-id="7bc05-142">**WF-startopensession**</span><span class="sxs-lookup"><span data-stu-id="7bc05-142">**WFDStartOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
</dt> <dt>

[<span data-ttu-id="7bc05-143">**WF dupdatedevicevisibility**</span><span class="sxs-lookup"><span data-stu-id="7bc05-143">**WFDUpdateDeviceVisibility**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)
</dt> <dt>

[<span data-ttu-id="7bc05-144">**Windows.Networking.Proximity**</span><span class="sxs-lookup"><span data-stu-id="7bc05-144">**Windows.Networking.Proximity**</span></span>](/uwp/api/Windows.Networking.Proximity?view=winrt-19041)
</dt> </dl>

 

 
