---
description: Neues in nativem WiFi
ms.assetid: 76d60b95-a34a-4747-b0fa-9230aa60bd63
title: Neues in nativem WiFi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2126627f4cf6431fbac2bf4d1f6ec58561bfd8bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347293"
---
# <a name="whats-new-in-native-wifi"></a><span data-ttu-id="f4797-103">Neues in nativem WiFi</span><span class="sxs-lookup"><span data-stu-id="f4797-103">What's New in Native Wifi</span></span>

## <a name="windows-10-version-2004"></a><span data-ttu-id="f4797-104">Windows 10, Version 2004</span><span class="sxs-lookup"><span data-stu-id="f4797-104">Windows 10, version 2004</span></span>

<span data-ttu-id="f4797-105">Weitere Informationen finden Sie unter [Bereitstellen eines Wi-Fi Profils über eine Website](prov-wifi-profile-via-website.md).</span><span class="sxs-lookup"><span data-stu-id="f4797-105">See [Provision a Wi-Fi profile via a website](prov-wifi-profile-via-website.md).</span></span>

## <a name="windows-10"></a><span data-ttu-id="f4797-106">Windows 10</span><span class="sxs-lookup"><span data-stu-id="f4797-106">Windows 10</span></span>

<span data-ttu-id="f4797-107">Die Unterstützung für Hotspot 2,0 wurde dem [WLAN- \_ Profil Schema](wlan-profileschema-schema.md)hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f4797-107">Support for Hotspot 2.0 has been added to the [WLAN\_profile schema](wlan-profileschema-schema.md).</span></span> <span data-ttu-id="f4797-108">Hotspot 2,0 ermöglicht die automatische Verbindung mit öffentlichen Wi-Fi Diensten unter Verwendung vorhandener Anmelde Informationen und der Mitgliedschaft in Dienstanbieter Netzwerken.</span><span class="sxs-lookup"><span data-stu-id="f4797-108">Hotspot 2.0 enables automatic connection to public Wi-Fi services using existing credentials and membership in service provider networks.</span></span> <span data-ttu-id="f4797-109">Dienstanbieter geben an, wie Verbindungen mithilfe der neuen Schema Elemente hergestellt werden, um zu beschreiben, welche Netzwerke verwendet werden sollen und wie Sie sich bei Ihnen authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="f4797-109">Service providers specify how connections are made using the new schema elements to describe which networks to use, and how to authenticate to them.</span></span> <span data-ttu-id="f4797-110">Weitere Informationen finden Sie in der Dokumentation zum [**Hotspot2**](wlan-profileschema-hotspot2-element.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="f4797-110">See the [**Hotspot2**](wlan-profileschema-hotspot2-element.md) element documentation for details.</span></span>

## <a name="windows-8-and-windows-server-2012"></a><span data-ttu-id="f4797-111">Windows 8 und Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f4797-111">Windows 8 and Windows Server 2012</span></span>

<span data-ttu-id="f4797-112">Die folgenden Features wurden den nativen WiFi-APIs unter Windows 8 und Windows Server 2012 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f4797-112">The following features have been added to the Native Wifi APIs on Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="f4797-113">Eine Wi-Fi Direct-Funktion, die auf der Entwicklung der Wi-Fi Peer-to-Peer Technical Specification v 1.1 von der Wi-Fi Alliance basiert (siehe [veröffentlichte Wi-Fi Alliance-Spezifikationen](https://www.wi-fi.org/)).</span><span class="sxs-lookup"><span data-stu-id="f4797-113">A Wi-Fi Direct feature based on the development of the Wi-Fi Peer-to-Peer Technical Specification v1.1 by the Wi-Fi Alliance (see [Wi-Fi Alliance Published Specifications](https://www.wi-fi.org/)).</span></span> <span data-ttu-id="f4797-114">Das Ziel der Wi-Fi Peer-to-Peer-technischen Spezifikation besteht darin, eine Lösung für die Wi-Fi Geräte-zu-Gerät-Konnektivität bereitzustellen, ohne dass entweder ein drahtloser Zugriffspunkt (drahtlos Zugriffspunkt) zum Einrichten der Verbindung oder die Verwendung des vorhandenen Wi-Fi Ad-hoc-Mechanismus (IBSS) erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="f4797-114">The goal of the Wi-Fi Peer-to-Peer Technical Specification is to provide a solution for Wi-Fi device-to-device connectivity without the need for either a Wireless Access Point (wireless AP) to setup the connection or the use of the existing Wi-Fi adhoc (IBSS) mechanism.</span></span>

<span data-ttu-id="f4797-115">Die folgenden Funktionen unterstützen die Wi-Fi Direct-Funktion.</span><span class="sxs-lookup"><span data-stu-id="f4797-115">The following functions support the Wi-Fi Direct feature.</span></span>

-   [<span data-ttu-id="f4797-116">**Rückruf für das Beenden der WFD- \_ \_ Sitzung \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f4797-116">**WFD\_OPEN\_SESSION\_COMPLETE\_CALLBACK**</span></span>](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
-   [<span data-ttu-id="f4797-117">**WF-cancelopensession**</span><span class="sxs-lookup"><span data-stu-id="f4797-117">**WFDCancelOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
-   [<span data-ttu-id="f4797-118">**WF-CloseHandle**</span><span class="sxs-lookup"><span data-stu-id="f4797-118">**WFDCloseHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
-   [<span data-ttu-id="f4797-119">**WF-CloseSession**</span><span class="sxs-lookup"><span data-stu-id="f4797-119">**WFDCloseSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
-   [<span data-ttu-id="f4797-120">**WF-openhandle**</span><span class="sxs-lookup"><span data-stu-id="f4797-120">**WFDOpenHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
-   [<span data-ttu-id="f4797-121">**WF-openlegacysession**</span><span class="sxs-lookup"><span data-stu-id="f4797-121">**WFDOpenLegacySession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
-   [<span data-ttu-id="f4797-122">**WF-startopensession**</span><span class="sxs-lookup"><span data-stu-id="f4797-122">**WFDStartOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
-   [<span data-ttu-id="f4797-123">**WF dupdatedevicevisibility**</span><span class="sxs-lookup"><span data-stu-id="f4797-123">**WFDUpdateDeviceVisibility**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)

## <a name="windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="f4797-124">Windows 7 und Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f4797-124">Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="f4797-125">Die folgenden Features wurden den nativen WiFi-APIs unter Windows 7 und Windows Server 2008 R2 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f4797-125">The following features have been added to the Native Wifi APIs on Windows 7 and Windows Server 2008 R2.</span></span>

<span data-ttu-id="f4797-126">Das drahtlos gehostete Netzwerk ermöglicht einem einzelnen physischen drahtlosen Adapter das Herstellen einer Verbindung als Client mit einem Hardware Zugriffspunkt (AP), während gleichzeitig ein Software-AP-Gerät fungiert, das anderen drahtlos fähigen Geräten das Herstellen einer Verbindung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="f4797-126">The wireless Hosted Network allows a single physical wireless adapter to connect as a client to a hardware access point (AP), while at the same time acting as a software AP allowing other wireless-capable devices to connect to it.</span></span>

<span data-ttu-id="f4797-127">Die folgenden Funktionen unterstützen das Feature für drahtlos gehostete Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="f4797-127">The following functions support the wireless Hosted Network feature.</span></span>

-   [<span data-ttu-id="f4797-128">**Wlanhustednetworkforcestart**</span><span class="sxs-lookup"><span data-stu-id="f4797-128">**WlanHostedNetworkForceStart**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)
-   [<span data-ttu-id="f4797-129">**Wlanhustednetworkforcestop**</span><span class="sxs-lookup"><span data-stu-id="f4797-129">**WlanHostedNetworkForceStop**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop)
-   [<span data-ttu-id="f4797-130">**Wlanhustednetworkinitsettings**</span><span class="sxs-lookup"><span data-stu-id="f4797-130">**WlanHostedNetworkInitSettings**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)
-   [<span data-ttu-id="f4797-131">**Wlanhustednetworkqueryproperty**</span><span class="sxs-lookup"><span data-stu-id="f4797-131">**WlanHostedNetworkQueryProperty**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)
-   [<span data-ttu-id="f4797-132">**Wlanhustednetworkquerysecondarykey**</span><span class="sxs-lookup"><span data-stu-id="f4797-132">**WlanHostedNetworkQuerySecondaryKey**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey)
-   [<span data-ttu-id="f4797-133">**Wlanhustednetworkquerystatus**</span><span class="sxs-lookup"><span data-stu-id="f4797-133">**WlanHostedNetworkQueryStatus**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus)
-   [<span data-ttu-id="f4797-134">**Wlanhustednetworkrefreshsecuritysettings**</span><span class="sxs-lookup"><span data-stu-id="f4797-134">**WlanHostedNetworkRefreshSecuritySettings**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)
-   [<span data-ttu-id="f4797-135">**Wlanhustednetworksetproperty**</span><span class="sxs-lookup"><span data-stu-id="f4797-135">**WlanHostedNetworkSetProperty**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetproperty)
-   [<span data-ttu-id="f4797-136">**Wlanhustednetworksetsecondarykey**</span><span class="sxs-lookup"><span data-stu-id="f4797-136">**WlanHostedNetworkSetSecondaryKey**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey)
-   [<span data-ttu-id="f4797-137">**Wlanhustednetworkstartusing**</span><span class="sxs-lookup"><span data-stu-id="f4797-137">**WlanHostedNetworkStartUsing**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)
-   [<span data-ttu-id="f4797-138">**Wlanhustednetworkstopusing**</span><span class="sxs-lookup"><span data-stu-id="f4797-138">**WlanHostedNetworkStopUsing**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)
-   [<span data-ttu-id="f4797-139">**Wlanregistervirtualstationnotification**</span><span class="sxs-lookup"><span data-stu-id="f4797-139">**WlanRegisterVirtualStationNotification**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanregistervirtualstationnotification)

<span data-ttu-id="f4797-140">Die folgenden neuen Strukturen, die mit einem drahtlos gehosteten Netzwerk funktionieren.</span><span class="sxs-lookup"><span data-stu-id="f4797-140">The following new structures that work with wireless Hosted Network.</span></span>

-   [<span data-ttu-id="f4797-141">**WLAN- \_ gehostete \_ Netzwerk \_ Verbindungs \_ Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="f4797-141">**WLAN\_HOSTED\_NETWORK\_CONNECTION\_SETTINGS**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_connection_settings)
-   [<span data-ttu-id="f4797-142">**vom WLAN \_ gehosteter \_ Netzwerk \_ \_ datenpeer- \_ Status \_ Änderung**</span><span class="sxs-lookup"><span data-stu-id="f4797-142">**WLAN\_HOSTED\_NETWORK\_DATA\_PEER\_STATE\_CHANGE**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_data_peer_state_change)
-   [<span data-ttu-id="f4797-143">**Status des WLAN- \_ gehosteten \_ Netzwerks \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f4797-143">**WLAN\_HOSTED\_NETWORK\_PEER\_STATE**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_peer_state)
-   [<span data-ttu-id="f4797-144">**Funk Status des WLAN- \_ gehosteten \_ Netzwerks \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f4797-144">**WLAN\_HOSTED\_NETWORK\_RADIO\_STATE**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_radio_state)
-   [<span data-ttu-id="f4797-145">**vom WLAN \_ gehostete \_ Netzwerk \_ Sicherheits \_ Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="f4797-145">**WLAN\_HOSTED\_NETWORK\_SECURITY\_SETTINGS**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_security_settings)
-   [<span data-ttu-id="f4797-146">**vom WLAN \_ gehostete \_ Netzwerk \_ Status \_ Änderungen**</span><span class="sxs-lookup"><span data-stu-id="f4797-146">**WLAN\_HOSTED\_NETWORK\_STATE\_CHANGE**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_state_change)
-   [<span data-ttu-id="f4797-147">**Status des WLAN- \_ gehosteten \_ Netzwerks \_**</span><span class="sxs-lookup"><span data-stu-id="f4797-147">**WLAN\_HOSTED\_NETWORK\_STATUS**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_status)

<span data-ttu-id="f4797-148">Die folgenden neuen Enumerationen, die mit einem drahtlos gehosteten Netzwerk funktionieren.</span><span class="sxs-lookup"><span data-stu-id="f4797-148">The following new enumerations that work with wireless Hosted Network.</span></span>

-   [<span data-ttu-id="f4797-149">**über WLAN \_ gehosteter \_ Netzwerk \_ Benachrichtigungs \_ Code**</span><span class="sxs-lookup"><span data-stu-id="f4797-149">**WLAN\_HOSTED\_NETWORK\_NOTIFICATION\_CODE**</span></span>](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_notification_code)
-   [<span data-ttu-id="f4797-150">**WLAN- \_ gehosteter \_ Netzwerk- \_ Opcode**</span><span class="sxs-lookup"><span data-stu-id="f4797-150">**WLAN\_HOSTED\_NETWORK\_OPCODE**</span></span>](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_opcode)
-   [<span data-ttu-id="f4797-151">**\_vom WLAN gehosteter \_ netzwerkpeer-Authentifizierungs \_ \_ \_ Status**</span><span class="sxs-lookup"><span data-stu-id="f4797-151">**WLAN\_HOSTED\_NETWORK\_PEER\_AUTH\_STATE**</span></span>](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_peer_auth_state)
-   [<span data-ttu-id="f4797-152">**Grund für WLAN- \_ gehostete \_ Netzwerke \_**</span><span class="sxs-lookup"><span data-stu-id="f4797-152">**WLAN\_HOSTED\_NETWORK\_REASON**</span></span>](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_reason)
-   [<span data-ttu-id="f4797-153">**WLAN- \_ gehosteter \_ Netzwerk \_ Status**</span><span class="sxs-lookup"><span data-stu-id="f4797-153">**WLAN\_HOSTED\_NETWORK\_STATE**</span></span>](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_state)

## <a name="related-topics"></a><span data-ttu-id="f4797-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f4797-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4797-155">Informationen zum drahtlos gehosteten Netzwerk</span><span class="sxs-lookup"><span data-stu-id="f4797-155">About the Wireless Hosted Network</span></span>](about-the-wireless-hosted-network.md)
</dt> <dt>

[<span data-ttu-id="f4797-156">Verwenden von drahtlos gehosteter Netzwerk-und Internet Verbindungs Freigabe</span><span class="sxs-lookup"><span data-stu-id="f4797-156">Using Wireless Hosted Network and Internet Connection Sharing</span></span>](using-hosted-network-and-internet-connection-sharing.md)
</dt> </dl>

 

 



