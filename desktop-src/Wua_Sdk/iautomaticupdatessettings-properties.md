---
description: Die iautomaticupdatessettings-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: 663aaf7d-c701-4da8-ba92-7e0a6d0f35ba
title: Iautomaticupdatessettings-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2463fdc69fc93960ee45c0003a65894eaaf7399
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958992"
---
# <a name="iautomaticupdatessettings-properties"></a><span data-ttu-id="c1556-103">Iautomaticupdatessettings-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c1556-103">IAutomaticUpdatesSettings Properties</span></span>

<span data-ttu-id="c1556-104">Die [**iautomaticupdatessettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) -Schnittstelle definiert die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c1556-104">The [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) interface defines the following properties.</span></span>



| <span data-ttu-id="c1556-105">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c1556-105">Property</span></span>                                                                                 | <span data-ttu-id="c1556-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c1556-106">Description</span></span>                                                                                      |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1556-107">**NotificationLevel**</span><span class="sxs-lookup"><span data-stu-id="c1556-107">**NotificationLevel**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel)                 | <span data-ttu-id="c1556-108">Ruft ab und legt fest, wie Benutzer über automatische Aktualisierungs Ereignisse benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="c1556-108">Gets and sets how users are notified about Automatic Update events.</span></span>                              |
| [<span data-ttu-id="c1556-109">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="c1556-109">**ReadOnly**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_readonly)                                   | <span data-ttu-id="c1556-110">Ruft einen booleschen Wert ab, der angibt, ob die Einstellungen für automatisches Update schreibgeschützt sind.</span><span class="sxs-lookup"><span data-stu-id="c1556-110">Gets a Boolean value that indicates whether the Automatic Update settings are read-only.</span></span>         |
| [<span data-ttu-id="c1556-111">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="c1556-111">**Required**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_required)                                   | <span data-ttu-id="c1556-112">Ruft einen booleschen Wert ab, der angibt, ob für Gruppenrichtlinie der automatische Updates-Dienst erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c1556-112">Gets a Boolean value that indicates whether Group Policy requires the Automatic Updates service.</span></span> |
| [<span data-ttu-id="c1556-113">**Scheduledinstallationday**</span><span class="sxs-lookup"><span data-stu-id="c1556-113">**ScheduledInstallationDay**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday)   | <span data-ttu-id="c1556-114">Ruft die Wochentage ab, an denen automatische Updates Updates installiert oder deinstalliert, oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="c1556-114">Gets and sets the days of the week on which Automatic Updates installs or uninstalls updates.</span></span>    |
| [<span data-ttu-id="c1556-115">**Scheduledinstallationtime**</span><span class="sxs-lookup"><span data-stu-id="c1556-115">**ScheduledInstallationTime**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime) | <span data-ttu-id="c1556-116">Ruft den Zeitpunkt ab, zu dem automatische Updates Updates installiert oder deinstalliert, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="c1556-116">Gets and sets the time at which Automatic Updates installs or uninstalls updates.</span></span>                |



 

> [!Note]  
> <span data-ttu-id="c1556-117">Windows 8, Windows 8.1, Windows Server 2012 und Windows Server 2012 R2 bieten nur eingeschränkte Unterstützung für [**scheduledinstallationday**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday) und [**scheduledinstallationtime**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime).</span><span class="sxs-lookup"><span data-stu-id="c1556-117">Windows 8, Windows 8.1, Windows Server 2012, and Windows Server 2012 R2 provide only limited support for [**ScheduledInstallationDay**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday) and [**ScheduledInstallationTime**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime).</span></span> <span data-ttu-id="c1556-118">Wenn der Computer über Gruppenrichtlinie konfiguriert wurde, um einen Tag und eine Uhrzeit für die geplante Installation zu verwenden, geben die Eigenschaften **scheduledinstallationday** und **scheduledinstallationtime** diesen geplanten Tag und diese Uhrzeit zurück.</span><span class="sxs-lookup"><span data-stu-id="c1556-118">If the computer has been configured through Group Policy to use a scheduled installation day and time, the **ScheduledInstallationDay** and **ScheduledInstallationTime** properties return this scheduled day and time.</span></span> <span data-ttu-id="c1556-119">Wenn der Computer auf diese Weise nicht über Gruppenrichtlinie konfiguriert wurde, geben die Eigenschaften **scheduledinstallationday** und **scheduledinstallationtime** standardmäßige und unzuverlässige Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="c1556-119">If the computer hasn't been configured through Group Policy in this way, the **ScheduledInstallationDay** and **ScheduledInstallationTime** properties return default and unreliable values.</span></span> <span data-ttu-id="c1556-120">Wenn Sie versuchen, den Tag und die Uhrzeit für die geplante Installation unter diesen Betriebssystemen zu ändern, sind **scheduledinstallationday** und **scheduledinstallationtime** anscheinend erfolgreich, haben jedoch keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="c1556-120">If you try to modify the scheduled installation day and time on these operating systems, **ScheduledInstallationDay** and **ScheduledInstallationTime** appear to succeed but have no effect.</span></span>

 

 

 



