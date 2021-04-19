---
description: Windows 10 unterstützt Ihre Anwendung bei der Optimierung des Stromverbrauchs bei der Ausführung auf einem mobilen Gerät.
ms.assetid: a956b88c-8a75-4c1c-af27-53c69feb1596
title: Neuerungen bei der Energie Verwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e6c8394c2e5e6750b5d01fd997d374a9f87e10d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362464"
---
# <a name="whats-new-in-power-management"></a><span data-ttu-id="28945-103">Neues bei der Energieverwaltung</span><span class="sxs-lookup"><span data-stu-id="28945-103">What's New in Power Management</span></span>

<span data-ttu-id="28945-104">Windows 10 unterstützt Ihre Anwendung bei der Optimierung des Stromverbrauchs, wenn diese auf einem mobilen Gerät ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="28945-104">Windows 10 helps your application optimize power consumption when it's running on a mobile device.</span></span>

## <a name="battery-saver"></a><span data-ttu-id="28945-105">Stromsparmodus</span><span class="sxs-lookup"><span data-stu-id="28945-105">Battery saver</span></span>

<span data-ttu-id="28945-106">In dieser Version kann die Anwendung benachrichtigt werden, wenn Akku Schoner aktiviert oder ausgeschaltet wird.</span><span class="sxs-lookup"><span data-stu-id="28945-106">In this release, your application can be notified when battery saver is turned on or off.</span></span> <span data-ttu-id="28945-107">Durch die Reaktion auf veränderliche Energiebedingungen kann die Anwendung zusammen mit Akku Schoner zusammenarbeiten, um Energie zu sparen und die Akku Lebensdauer zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="28945-107">By responding to changing power conditions, your application can work in concert with battery saver to save energy and help extend battery life.</span></span> <span data-ttu-id="28945-108">Allgemeine Informationen zum Akku Schoner finden Sie unter [Batterie Schoner (in den Richtlinien für die Hardwarekomponente)](/windows-hardware/design/component-guidelines/battery-saver).</span><span class="sxs-lookup"><span data-stu-id="28945-108">For general information about battery saver, see [battery saver (in the hardware component guidelines)](/windows-hardware/design/component-guidelines/battery-saver).</span></span>

-   <span data-ttu-id="28945-109">[**GUID \_ Energie \_ Spar \_ Status**](power-setting-guids.md) : Verwenden Sie diese neue GUID mit der Funktion " [**powersettingregisternotification**](/windows/desktop/api/Powersetting/nf-powersetting-powersettingregisternotification) ", um benachrichtigt zu werden, wenn Akku Schoner aktiviert oder ausgeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="28945-109">[**GUID\_POWER\_SAVING\_STATUS**](power-setting-guids.md) : Use this new GUID with the [**PowerSettingRegisterNotification**](/windows/desktop/api/Powersetting/nf-powersetting-powersettingregisternotification) function to be notified when battery saver is turned on or off.</span></span>

-   <span data-ttu-id="28945-110">[**System \_ Energie \_ Status**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) : Diese Struktur wurde aktualisiert, um den Akku Schoner zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="28945-110">[**SYSTEM\_POWER\_STATUS**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) : This structure has been updated to support battery saver.</span></span> <span data-ttu-id="28945-111">Der vierte Member, **systemstatusflag** (früher **"reserved1"**), gibt nun an, ob der Akku Schoner eingeschaltet ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="28945-111">The fourth member, **SystemStatusFlag** (previously named **Reserved1**), now indicates if battery saver is engaged or not.</span></span> <span data-ttu-id="28945-112">Verwenden Sie die [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) -Funktion, um einen Zeiger auf diese-Struktur abzurufen.</span><span class="sxs-lookup"><span data-stu-id="28945-112">Use the [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) function to retrieve a pointer to this structure.</span></span>

 

 
