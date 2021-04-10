---
title: Informationen zu Windows Connect Now
description: Windows Connect Now (WCN) bietet einen einfachen und sicheren Mechanismus zum Verbinden und Austauschen von Einstellungen für Netzwerk Zugriffspunkte und Geräte (z. b. Drucker, Kameras und PCs).
ms.assetid: 5c654800-e58b-4a94-b7a6-9a603f540603
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0118c6a053c480a36138f8dae850ee0862501944
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102186"
---
# <a name="about-windows-connect-now"></a><span data-ttu-id="0b13b-103">Informationen zu Windows Connect Now</span><span class="sxs-lookup"><span data-stu-id="0b13b-103">About Windows Connect Now</span></span>

<span data-ttu-id="0b13b-104">Windows Connect Now (WCN) bietet einen einfachen und sicheren Mechanismus zum Verbinden und Austauschen von Einstellungen für Netzwerk Zugriffspunkte und Geräte (z. b. Drucker, Kameras und PCs).</span><span class="sxs-lookup"><span data-stu-id="0b13b-104">Windows Connect Now (WCN) provides a simple and secure mechanism for network access points and devices (like printers, camera, and PCs) to connect and exchange settings.</span></span> <span data-ttu-id="0b13b-105">Diese API ist die Microsoft-Implementierung des WPS-Protokolls (Wi-Fi Protected Setup), das von der Wi-Fi Alliance als Lösung für Heimnetzwerke und kleine Unternehmen erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="0b13b-105">This API is the Microsoft implementation of the Wi-Fi Protected Setup (WPS)/Wi-Fi Simple Configuration (WSC) protocol, which was created by the Wi-Fi Alliance as a solution for home networking and small businesses.</span></span> <span data-ttu-id="0b13b-106">Diese Technologie ist nicht für Unternehmens Szenarios vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="0b13b-106">This technology is not intended for enterprise scenarios.</span></span>

> [!Note]  
> <span data-ttu-id="0b13b-107">Der Spezifikations Name wurde zwischen Version 1.0 h und Version 2 geändert.</span><span class="sxs-lookup"><span data-stu-id="0b13b-107">The specification name changed between version 1.0h and version 2.</span></span> <span data-ttu-id="0b13b-108">Die Spezifikation der Version 1.0 wurde Wi-Fi geschütztes Setup (WPS) benannt.</span><span class="sxs-lookup"><span data-stu-id="0b13b-108">The version 1.0h specification was named Wi-Fi Protected Setup (WPS).</span></span> <span data-ttu-id="0b13b-109">Ab Version 2 wird die Spezifikation Wi-Fi Simple Configuration (WSC) benannt.</span><span class="sxs-lookup"><span data-stu-id="0b13b-109">Starting with version 2 specification, the specification is named Wi-Fi Simple Configuration (WSC).</span></span> <span data-ttu-id="0b13b-110">In unserer Dokumentation werden die Begriffe "WPS" und "WSC" austauschbar verwendet, sofern nichts anderes angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0b13b-110">In our documentation, the terms WPS and WSC are used interchangeably unless noted.</span></span>

 

<span data-ttu-id="0b13b-111">Mit Windows Connect können Anwendungen nun mithilfe der [funktionermittlungs-API](/previous-versions/windows/desktop/fundisc/fd-portal)nach WCN-fähigen Geräten suchen.</span><span class="sxs-lookup"><span data-stu-id="0b13b-111">Windows Connect Now enables applications to search for WCN-capable devices using the [Function Discovery API](/previous-versions/windows/desktop/fundisc/fd-portal).</span></span> <span data-ttu-id="0b13b-112">Der Bereich einer Suche kann zu einer bestimmten SSID, einem Status, einer Kategorie oder sogar erweitert werden, um alle WCN-fähigen Geräte einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="0b13b-112">The scope of a search can be narrowed down to a specific SSID, state, category, or even broadened to include all WCN-capable devices.</span></span> <span data-ttu-id="0b13b-113">Nachdem die Geräte gefunden wurden, ermöglicht die WCN-API die Kommunikation mit dem WCN-fähigen Gerät, um die Konfiguration oder Konnektivität zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="0b13b-113">Once devices are located, the WCN API allows communication with the WCN-capable device in order to facilitate configuration or connectivity.</span></span>

 

 