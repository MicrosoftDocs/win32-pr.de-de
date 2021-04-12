---
description: Die native WiFi-API enthält Funktionen, Strukturen und Enumerationen, die Drahtlos Netzwerk Konnektivität und drahtlose Profilverwaltung unterstützen.
ms.assetid: 686f9ccf-5040-44c5-8633-83f12dc46586
title: Informationen zur nativen WiFi-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280d4f656145430e34d79e05b88bc2bdeb54fe5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218198"
---
# <a name="about-the-native-wifi-api"></a><span data-ttu-id="20768-103">Informationen zur nativen WiFi-API</span><span class="sxs-lookup"><span data-stu-id="20768-103">About the Native Wifi API</span></span>

<span data-ttu-id="20768-104">Die native WiFi-API enthält Funktionen, Strukturen und Enumerationen, die Drahtlos Netzwerk Konnektivität und drahtlose Profilverwaltung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="20768-104">The Native Wifi API contains functions, structures, and enumerations that support wireless network connectivity and wireless profile management.</span></span> <span data-ttu-id="20768-105">Die API kann sowohl für Infrastruktur-als auch für Ad-hoc-Netzwerke verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="20768-105">The API can be used for both infrastructure and ad hoc networks.</span></span> <span data-ttu-id="20768-106">Die drahtlose Ad-hoc-API ist eine vereinfachte objektorientierte Schnittstelle zum Erstellen, verwalten und Verwenden von Ad-hoc-Netzwerken.</span><span class="sxs-lookup"><span data-stu-id="20768-106">The Wireless Ad Hoc API is a simplified object-oriented interface for creating, managing, and using ad hoc networks.</span></span>

> [!Note]  
> <span data-ttu-id="20768-107">Der Ad-hoc-Modus ist möglicherweise in zukünftigen Versionen von Windows nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="20768-107">Ad hoc mode might not be available in future versions of Windows.</span></span> <span data-ttu-id="20768-108">Beginnen Sie mit Windows 8.1 und Windows Server 2012 R2, und verwenden Sie stattdessen [Wi-Fi Direct](about-the-wi-fi-direct-api.md) .</span><span class="sxs-lookup"><span data-stu-id="20768-108">Starting with Windows 8.1 and Windows Server 2012 R2, use [Wi-Fi Direct](about-the-wi-fi-direct-api.md) instead.</span></span>

 

<span data-ttu-id="20768-109">Bei der Implementierung der Ad-hoc-API wird die native WiFi-API verwendet.</span><span class="sxs-lookup"><span data-stu-id="20768-109">The implementation of the Ad Hoc API uses the Native Wifi API.</span></span> <span data-ttu-id="20768-110">Dies bedeutet, dass Ad-hoc-API-Aufrufe Native WiFi-Benachrichtigungen und umgekehrt aufrufen können.</span><span class="sxs-lookup"><span data-stu-id="20768-110">This means that Ad Hoc API calls can trigger Native Wifi notifications, and vice versa.</span></span>

<span data-ttu-id="20768-111">Es wird nicht empfohlen, Native WiFi-API-Aufrufe und drahtlose Ad-hoc-API-Aufrufe zu mischen</span><span class="sxs-lookup"><span data-stu-id="20768-111">Mixing Native Wifi API calls and Wireless Ad Hoc API calls is not recommended.</span></span> <span data-ttu-id="20768-112">Entwickler sollten einen Programmier Ansatz auswählen, bevor Sie eine Anwendung entwerfen.</span><span class="sxs-lookup"><span data-stu-id="20768-112">Developers should choose a programming approach before designing an application.</span></span> <span data-ttu-id="20768-113">Wenn Ihre Anwendung Infrastruktur Netzwerke verwendet oder verwaltet, sollten Sie die native WiFi-API verwenden.</span><span class="sxs-lookup"><span data-stu-id="20768-113">If your application uses or manages infrastructure networks, you should use the Native Wifi API.</span></span> <span data-ttu-id="20768-114">Wenn für Ihre Anwendung Profil Verwaltungsfunktionen erforderlich sind, sollten Sie die native WiFi-API verwenden.</span><span class="sxs-lookup"><span data-stu-id="20768-114">If your application requires profile management functionality, you should use the Native Wifi API.</span></span> <span data-ttu-id="20768-115">Andernfalls sollten Sie die drahtlose Ad-hoc-API verwenden.</span><span class="sxs-lookup"><span data-stu-id="20768-115">Otherwise, you should use the Wireless Ad Hoc API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="20768-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="20768-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20768-117">Informationen zu nativem WiFi</span><span class="sxs-lookup"><span data-stu-id="20768-117">About Native Wifi</span></span>](about-native-wifi.md)
</dt> <dt>

[<span data-ttu-id="20768-118">Native WiFi-API-Unterstützung unter Windows XP</span><span class="sxs-lookup"><span data-stu-id="20768-118">Native Wifi API Support on Windows XP</span></span>](about-wireless-lan-api-for-windows-xp-service-pack-2.md)
</dt> <dt>

[<span data-ttu-id="20768-119">Native WiFi-API-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="20768-119">Native Wifi API Permissions</span></span>](native-wifi-api-permissions.md)
</dt> <dt>

[<span data-ttu-id="20768-120">Informationen zur drahtlosen Ad-hoc-API</span><span class="sxs-lookup"><span data-stu-id="20768-120">About the Wireless Ad Hoc API</span></span>](about-the-wireless-ad-hoc-api.md)
</dt> <dt>

[<span data-ttu-id="20768-121">Herunterladen des Windows Vista SDK</span><span class="sxs-lookup"><span data-stu-id="20768-121">Download the Windows Vista SDK</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf)
</dt> </dl>

 

 



