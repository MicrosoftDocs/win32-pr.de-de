---
description: Mit der Device Power API können Sie leicht feststellen, welche Geräte das System aus dem Ruhezustand reaktivieren können und in welchen Ruhe Zuständen diese Geräte das Erwachen unterstützen. Weitere Informationen zu Ruhe Zuständen finden Sie unter System Energiezustände.
ms.assetid: aaa776e5-3fc2-41bd-a805-6c09ef73807b
title: Geräte Energie Verwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0982b7de23f7b7d8cf39686c854d64f284d1ce2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959746"
---
# <a name="device-power-management"></a><span data-ttu-id="a63a7-104">Geräte Energie Verwaltung</span><span class="sxs-lookup"><span data-stu-id="a63a7-104">Device Power Management</span></span>

<span data-ttu-id="a63a7-105">Mit der Device Power API können Sie leicht feststellen, welche Geräte das System aus dem Ruhezustand reaktivieren können und in welchen Ruhe Zuständen diese Geräte das Erwachen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a63a7-105">The Device Power API makes it easy to determine which devices are able to wake the system from a sleep state, and which sleep states those devices support waking from.</span></span> <span data-ttu-id="a63a7-106">Weitere Informationen zu Ruhe Zuständen finden Sie unter [System Energiezustände](system-power-states.md).</span><span class="sxs-lookup"><span data-stu-id="a63a7-106">For more information about sleep states, see [System Power States](system-power-states.md).</span></span>

<span data-ttu-id="a63a7-107">Die [**devicepowerenumdevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) -Funktion kann verwendet werden, um die Geräteliste nach Geräten zu durchsuchen, die mit den angegebenen Kriterien übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a63a7-107">The [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) function can be used to search the device list for devices that match specified criteria.</span></span> <span data-ttu-id="a63a7-108">Die Kriterien können die Fähigkeit des Geräts enthalten, einen Systemstatus zu unterstützen oder diesen Zustand zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a63a7-108">The criteria may include the device's ability to support a system state, or wake from that state.</span></span> <span data-ttu-id="a63a7-109">Zurzeit werden unterstützte Flags in "Winnt. h" und "devpower. h" gefunden.</span><span class="sxs-lookup"><span data-stu-id="a63a7-109">Currently supported flags can be found in WinNT.h and DevPower.h.</span></span>

<span data-ttu-id="a63a7-110">Die [**devicepowersetdevicestate**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) -Funktion aktiviert oder deaktiviert, dass ein angegebenes Gerät das System aus dem Ruhezustand reaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a63a7-110">The [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) function enables or disables a specified device from waking the system from a sleep state.</span></span>

<span data-ttu-id="a63a7-111">Mit der Device Power API können Entwickler eine bessere Benutzer Leistung erzielen, indem Sie dem Benutzer mehr Informationen über das, was das System leistet, und mehr Kontrolle über die Geräte im System geben.</span><span class="sxs-lookup"><span data-stu-id="a63a7-111">The Device Power API allows developers to create a better user experience by giving the user more information about what the system is doing, and more control over the devices in the system.</span></span> <span data-ttu-id="a63a7-112">Die Geräteleistung ist in Situationen nützlich, in denen der Energieverbrauch wichtig ist, z. b. auf tragbaren Geräten, die unter Batterien ausgeführt werden</span><span class="sxs-lookup"><span data-stu-id="a63a7-112">Device Power is useful in situations where power consumption is critical, such as in portable devices running on batteries.</span></span> <span data-ttu-id="a63a7-113">Beispielsweise ist das Energie Verwaltungs Schema, das auf einem Desktop Computer verwendet wird, möglicherweise nicht das optimale Schema für einen Laptop Computer, sodass der Benutzer bestimmte Geräte vor dem Reaktivieren des Systems deaktivieren möchte.</span><span class="sxs-lookup"><span data-stu-id="a63a7-113">For example, the power management scheme used in a desktop computer may not be the optimal scheme for a laptop computer, so the user may want to disable certain devices from waking the system.</span></span> <span data-ttu-id="a63a7-114">Dadurch können Energie gespart werden, da die deaktivierten Geräte keine Stromversorgung zeichnen, während sich das System im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="a63a7-114">This can conserve energy because the disabled devices will not draw power while the system is in sleep mode.</span></span>

<span data-ttu-id="a63a7-115">Ein Beispiel finden Sie unter [Verwenden der Device Power API](using-the-device-power-api.md).</span><span class="sxs-lookup"><span data-stu-id="a63a7-115">For an example, see [Using the Device Power API](using-the-device-power-api.md).</span></span>

 

 



