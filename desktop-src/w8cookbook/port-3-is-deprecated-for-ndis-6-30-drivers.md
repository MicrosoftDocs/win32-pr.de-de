---
title: Port 3 ist für NDIS 6,30-Treiber veraltet
description: Port 3 ist für NDIS 6,30-Treiber veraltet
ms.assetid: 900BD08D-3EAF-43F3-A74A-359815474FAD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df0b4c7f6a33b179a14d3d7f8151d3850e16dd44
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "104474493"
---
# <a name="port-3-is-deprecated-for-ndis-630-drivers"></a><span data-ttu-id="21878-103">Port 3 ist für NDIS 6,30-Treiber veraltet</span><span class="sxs-lookup"><span data-stu-id="21878-103">Port 3 is deprecated for NDIS 6.30 drivers</span></span>

## <a name="platforms"></a><span data-ttu-id="21878-104">Plattformen</span><span class="sxs-lookup"><span data-stu-id="21878-104">Platforms</span></span>

<span data-ttu-id="21878-105">**Clients** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="21878-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="21878-106">**Server** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="21878-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="21878-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="21878-107">Description</span></span>

<span data-ttu-id="21878-108">Windows 8 entfernt die Platt Form Unterstützung für NDIS Mini Port-WLAN-Treiber, um den IHV-Erweiterbarkeits Port (auch als Dritter Port bezeichnet) zu erstellen oder zu starten.</span><span class="sxs-lookup"><span data-stu-id="21878-108">Windows 8 removes platform support for NDIS miniport WLAN drivers to create or start up the IHV extensibility port (also known as 3rd port).</span></span> <span data-ttu-id="21878-109">Diese Funktion wurde in Windows 7 als provisorische-Measure eingeführt, während die Wi-Fi Alliance (WFA) die Wi-Fi Direct-Spezifikation entwickelte.</span><span class="sxs-lookup"><span data-stu-id="21878-109">This feature was introduced in Windows 7 as a stopgap measure while the Wi-Fi Alliance (WFA) developed the Wi-Fi Direct specification.</span></span> <span data-ttu-id="21878-110">Die Spezifikation ist nun abgeschlossen, Produkte, die Wi-Fi Direct verwenden, werden zertifiziert, und Windows 8 führt einen systemeigenen Wi-Fi direkten Stapel ein.</span><span class="sxs-lookup"><span data-stu-id="21878-110">The specification is now finished, products using Wi-Fi Direct are being certified, and Windows 8 introduces a native Wi-Fi Direct stack.</span></span>

## <a name="manifestation"></a><span data-ttu-id="21878-111">Ausstrahlung</span><span class="sxs-lookup"><span data-stu-id="21878-111">Manifestation</span></span>

<span data-ttu-id="21878-112">Nichts, da der dritte Port eine Platt Form Funktion ist, die WLAN-Mini Port-Treiber startet, wenn Sie diese Funktionalität benötigen.</span><span class="sxs-lookup"><span data-stu-id="21878-112">Nothing, as third port is a platform capability that WLAN miniport drivers start up if they need this functionality.</span></span>

## <a name="solution"></a><span data-ttu-id="21878-113">Lösung</span><span class="sxs-lookup"><span data-stu-id="21878-113">Solution</span></span>

<span data-ttu-id="21878-114">Die Funktion Erweiterbarkeits Port ist für vorhandene Treiber, die NDIS 6,30 nicht melden, verfügbar, um die Gerätekompatibilität zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="21878-114">We are keeping the extensibility port feature available for existing drivers that do not report NDIS 6.30 to maintain device compatibility.</span></span> <span data-ttu-id="21878-115">Neue WLAN-Treiber, die NDIS 6,30 melden, sind jedoch nicht in der Lage, diesen Port zu starten. Stattdessen sollten Entwickler dieser Treiber Wi-Fi Direct verwenden.</span><span class="sxs-lookup"><span data-stu-id="21878-115">However, new WLAN drivers that report NDIS 6.30 will not be able to start this port; instead, developers of these drivers should use Wi-Fi Direct.</span></span>

 

 




