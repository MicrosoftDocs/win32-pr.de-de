---
description: Die native WiFi-API enthält eine Reihe von Funktionen, die die Verwendung von Wi-Fi Direct für Desktop-Apps unterstützen.
ms.assetid: A649EBBA-1076-4426-9C4D-85AB8C415C66
title: Informationen über die Wi-Fi Direct-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e503cb2bf86f81904b1c85c2bdf96b66c0762e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351544"
---
# <a name="about-the-wi-fi-direct-feature"></a><span data-ttu-id="e8620-103">Informationen über die Wi-Fi Direct-Funktion</span><span class="sxs-lookup"><span data-stu-id="e8620-103">About the Wi-Fi Direct feature</span></span>

<span data-ttu-id="e8620-104">Die native WiFi-API enthält eine Reihe von Funktionen, die die Verwendung von Wi-Fi Direct für Desktop-Apps unterstützen.</span><span class="sxs-lookup"><span data-stu-id="e8620-104">The Native Wifi API contains a set of functions that support the use of Wi-Fi Direct for desktop apps.</span></span> <span data-ttu-id="e8620-105">Ab Windows 8 und Windows Server 2012 wurden der systemeigenen WiFi-API Wi-Fi Direct-Funktionen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e8620-105">Starting on Windows 8 and Windows Server 2012, Wi-Fi Direct functions were added to the Native Wifi API.</span></span>

<span data-ttu-id="e8620-106">Die Wi-Fi Direct-Funktion basiert auf der Entwicklung der Wi-Fi Peer-to-Peer Technical Specification v 1.1 von der Wi-Fi Alliance (siehe [veröffentlichte Wi-Fi Alliance-Spezifikationen](https://www.wi-fi.org/)).</span><span class="sxs-lookup"><span data-stu-id="e8620-106">The Wi-Fi Direct feature is based on the development of the Wi-Fi Peer-to-Peer Technical Specification v1.1 by the Wi-Fi Alliance (see [Wi-Fi Alliance Published Specifications](https://www.wi-fi.org/)).</span></span> <span data-ttu-id="e8620-107">Das Ziel der Wi-Fi Peer-to-Peer-technischen Spezifikation besteht darin, eine Lösung für die Wi-Fi Geräte-zu-Gerät-Konnektivität bereitzustellen, ohne dass ein drahtloser Zugriffspunkt (Wireless AP) zum Einrichten der Verbindung oder die Verwendung des vorhandenen Wi-Fi Ad-hoc-Mechanismus (IBSS) erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="e8620-107">The goal of the Wi-Fi Peer-to-Peer Technical Specification is to provide a solution for Wi-Fi device-to-device connectivity without the need for either a Wireless Access Point (wireless AP) to setup the connection or the use of the existing Wi-Fi ad hoc (IBSS) mechanism.</span></span>

> [!Note]  
> <span data-ttu-id="e8620-108">Der Ad-hoc-Modus ist möglicherweise in zukünftigen Versionen von Windows nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e8620-108">Ad hoc mode might not be available in future versions of Windows.</span></span> <span data-ttu-id="e8620-109">Beginnen Sie mit Windows 8.1 und Windows Server 2012 R2, und verwenden Sie stattdessen Wi-Fi Direct.</span><span class="sxs-lookup"><span data-stu-id="e8620-109">Starting with Windows 8.1 and Windows Server 2012 R2, use Wi-Fi Direct instead.</span></span>

 

<span data-ttu-id="e8620-110">Für eine Desktop-App erfordert die Wi-Fi Direct-Funktion, dass WLAN-Geräte zuvor vom Benutzer mit der Benutzeroberfläche der Windows-paarweise gekoppelt werden.</span><span class="sxs-lookup"><span data-stu-id="e8620-110">For a desktop app, the Wi-Fi Direct feature requires that Wi-FI Direct devices be previously paired by the user with the Windows Pairing experience user interface.</span></span> <span data-ttu-id="e8620-111">Nachdem diese Kopplung abgeschlossen ist, wird ein Profil gespeichert, mit dem die Wi-Fi Direct-Funktionen zum Starten einer Wi-Fi direkten Sitzung verwendet werden können, um eine Verbindung zwischen den Wi-Fi direkt Geräten herzustellen.</span><span class="sxs-lookup"><span data-stu-id="e8620-111">Once this pairing is completed, a profile is stored that allows the Wi-Fi Direct functions to be used to start a Wi-Fi Direct session to establish a connection between the Wi-Fi Direct devices.</span></span>

<span data-ttu-id="e8620-112">Die folgenden Funktionen unterstützen die Wi-Fi Direct-Funktion.</span><span class="sxs-lookup"><span data-stu-id="e8620-112">The following functions support the Wi-Fi Direct feature.</span></span>

-   <span data-ttu-id="e8620-113">[**Wfdcancelopensession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) : gibt an, dass die APP eine ausstehende [**wfdstartopensession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) -Funktion abbrechen möchte, die noch nicht abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="e8620-113">[**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) - Indicates that the app wants to cancel a pending [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function that has not completed.</span></span>
-   <span data-ttu-id="e8620-114">[**Wfdclosehandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) : schließt ein Handle für den Wi-Fi Direct-Dienst.</span><span class="sxs-lookup"><span data-stu-id="e8620-114">[**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) - Closes a handle to the Wi-Fi Direct service.</span></span>
-   <span data-ttu-id="e8620-115">[**Wfdclosesession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) : schließt eine Sitzung nach einem zuvor erfolgreichen Rückruf der [**wfdstartopensession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="e8620-115">[**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) - Closes a session after a previously successful call to the [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function.</span></span>
-   <span data-ttu-id="e8620-116">[**Wfdopenhandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) : öffnet ein Handle für den Wi-Fi Direct-Dienst und aushandiert eine Version der direkten Wi-Fi-API für die Verwendung von.</span><span class="sxs-lookup"><span data-stu-id="e8620-116">[**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) - Opens a handle to the Wi-Fi Direct service and negotiates a version of the Wi-FI Direct API to use.</span></span>
-   <span data-ttu-id="e8620-117">[**WF dopenlegacysession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) : Ruft ein gespeichertes Profil für ein Wi-Fi direktes Legacy Gerät ab und wendet es an.</span><span class="sxs-lookup"><span data-stu-id="e8620-117">[**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) - Retrieves and applies a stored profile for a Wi-Fi Direct legacy device.</span></span>
-   <span data-ttu-id="e8620-118">[**Wfdstartopensession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) : startet eine Bedarfs gesteuerte Verbindung mit einem bestimmten Wi-Fi Direct-Gerät, das zuvor durch die Windows-Kopplung kombiniert wurde.</span><span class="sxs-lookup"><span data-stu-id="e8620-118">[**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) - Starts an on-demand connection to a specific Wi-Fi Direct device, which has been previously paired through the Windows Pairing experience.</span></span>
-   <span data-ttu-id="e8620-119">[**WF dupdatedevicevisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) : aktualisiert die Geräte Sichtbarkeit für die Wi-Fi direkte Geräteadresse für einen bestimmten installierten Wi-Fi direkt Geräteknoten.</span><span class="sxs-lookup"><span data-stu-id="e8620-119">[**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) - Updates device visibility for the Wi-Fi Direct device address for a given installed Wi-Fi Direct device node.</span></span>
-   <span data-ttu-id="e8620-120">[**WFD \_ \_Sitzung zum \_ abschließen \_ der Sitzung öffnen**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) : definiert die Rückruffunktion, die von der [**wfdstartopensession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) -Funktion aufgerufen wird, wenn der **wfdstartopensession** -Vorgang abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="e8620-120">[**WFD\_OPEN\_SESSION\_COMPLETE\_CALLBACK**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) - Defines the callback function that is called by the [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function when the **WFDStartOpenSession** operation completes</span></span>

<span data-ttu-id="e8620-121">Weitere Informationen zur Verwendung von Wi-Fi Direct in einer Desktop-App finden [Sie unter Verwenden der Wi-Fi Direct-Funktionen](using-the-wi-fi-direct-api.md).</span><span class="sxs-lookup"><span data-stu-id="e8620-121">For more information on using Wi-Fi Direct in a desktop app, see [Using the Wi-Fi Direct functions](using-the-wi-fi-direct-api.md).</span></span>

<span data-ttu-id="e8620-122">Weitere Informationen zu Wi-Fi Direct für die Verwendung in Windows Store-Apps finden Sie unter " [**Peer Erfinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) " und verwandte Klassen im [**Windows. Networking. near**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041) -Namespace.</span><span class="sxs-lookup"><span data-stu-id="e8620-122">For more information on Wi-Fi Direct for use in Windows Store apps, see [**PeerFinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) and related classes in the [**Windows.Networking.Proximity**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041) namespace.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8620-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e8620-123">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e8620-124">**Weitere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="e8620-124">**Other resources**</span></span>
</dt> <dt>

[<span data-ttu-id="e8620-125">Informationen zu nativem WiFi</span><span class="sxs-lookup"><span data-stu-id="e8620-125">About Native Wifi</span></span>](about-native-wifi.md)
</dt> <dt>

[<span data-ttu-id="e8620-126">Informationen zur nativen WiFi-API</span><span class="sxs-lookup"><span data-stu-id="e8620-126">About the Native Wifi API</span></span>](about-the-native-wifi-api.md)
</dt> <dt>

[<span data-ttu-id="e8620-127">Informationen zur drahtlosen Ad-hoc-API</span><span class="sxs-lookup"><span data-stu-id="e8620-127">About the Wireless Ad Hoc API</span></span>](about-the-wireless-ad-hoc-api.md)
</dt> <dt>

[<span data-ttu-id="e8620-128">Verwenden der Wi-Fi Direct-Funktionen</span><span class="sxs-lookup"><span data-stu-id="e8620-128">Using the Wi-Fi Direct functions</span></span>](using-the-wi-fi-direct-api.md)
</dt> <dt>

<span data-ttu-id="e8620-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="e8620-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e8620-130">**Peer Erfinder**</span><span class="sxs-lookup"><span data-stu-id="e8620-130">**PeerFinder**</span></span>](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041)
</dt> <dt>

[<span data-ttu-id="e8620-131">**Rückruf für das Beenden der WFD- \_ \_ Sitzung \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e8620-131">**WFD\_OPEN\_SESSION\_COMPLETE\_CALLBACK**</span></span>](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
</dt> <dt>

[<span data-ttu-id="e8620-132">**WF-cancelopensession**</span><span class="sxs-lookup"><span data-stu-id="e8620-132">**WFDCancelOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
</dt> <dt>

[<span data-ttu-id="e8620-133">**WF-CloseHandle**</span><span class="sxs-lookup"><span data-stu-id="e8620-133">**WFDCloseHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
</dt> <dt>

[<span data-ttu-id="e8620-134">**WF-CloseSession**</span><span class="sxs-lookup"><span data-stu-id="e8620-134">**WFDCloseSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
</dt> <dt>

[<span data-ttu-id="e8620-135">**WF-openhandle**</span><span class="sxs-lookup"><span data-stu-id="e8620-135">**WFDOpenHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
</dt> <dt>

[<span data-ttu-id="e8620-136">**WF-openlegacysession**</span><span class="sxs-lookup"><span data-stu-id="e8620-136">**WFDOpenLegacySession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
</dt> <dt>

[<span data-ttu-id="e8620-137">**WF-startopensession**</span><span class="sxs-lookup"><span data-stu-id="e8620-137">**WFDStartOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
</dt> <dt>

[<span data-ttu-id="e8620-138">**WF dupdatedevicevisibility**</span><span class="sxs-lookup"><span data-stu-id="e8620-138">**WFDUpdateDeviceVisibility**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)
</dt> <dt>

[<span data-ttu-id="e8620-139">**Windows.Networking.Proximity**</span><span class="sxs-lookup"><span data-stu-id="e8620-139">**Windows.Networking.Proximity**</span></span>](/uwp/api/Windows.Networking.Proximity?view=winrt-19041)
</dt> </dl>

 

 
