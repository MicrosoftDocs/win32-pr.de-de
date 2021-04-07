---
description: Die iautomaticupdatessettings-Schnittstelle definiert die folgenden Methoden.
ms.assetid: 2c6df896-bb59-4d77-acde-64e36ecb7d75
title: Iautomaticupdatessettings-Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a9ecfc43539f70b9373a6db298acc6c688e83a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863747"
---
# <a name="iautomaticupdatessettings-methods"></a><span data-ttu-id="b8f40-103">Iautomaticupdatessettings-Methoden</span><span class="sxs-lookup"><span data-stu-id="b8f40-103">IAutomaticUpdatesSettings Methods</span></span>

<span data-ttu-id="b8f40-104">Die [**iautomaticupdatessettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) -Schnittstelle definiert die folgenden Methoden.</span><span class="sxs-lookup"><span data-stu-id="b8f40-104">The [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) interface defines the following methods.</span></span>



| <span data-ttu-id="b8f40-105">Methode</span><span class="sxs-lookup"><span data-stu-id="b8f40-105">Method</span></span>                                               | <span data-ttu-id="b8f40-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b8f40-106">Description</span></span>                                      |
|------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="b8f40-107">**Aktualisieren**</span><span class="sxs-lookup"><span data-stu-id="b8f40-107">**Refresh**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-refresh) | <span data-ttu-id="b8f40-108">Ruft die neuesten automatische Updates Einstellungen ab.</span><span class="sxs-lookup"><span data-stu-id="b8f40-108">Retrieves the latest Automatic Updates settings.</span></span> |
| [<span data-ttu-id="b8f40-109">**Speichern**</span><span class="sxs-lookup"><span data-stu-id="b8f40-109">**Save**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save)       | <span data-ttu-id="b8f40-110">Wendet die aktuellen automatische Updates Einstellungen an.</span><span class="sxs-lookup"><span data-stu-id="b8f40-110">Applies the current Automatic Updates settings.</span></span>  |



 

> [!Note]  
> <span data-ttu-id="b8f40-111">Unter Windows RT können Sie die [**iautomaticupdatessettings:: Save**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save) -Methode nicht mehr verwenden, um Windows Update Einstellungen Programm gesteuert zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="b8f40-111">On Windows RT, you can no longer use the [**IAutomaticUpdatesSettings::Save**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save) method to configure Windows Update settings programmatically.</span></span> <span data-ttu-id="b8f40-112">Der Konfigurations Vorgang schlägt fehl, wenn Sie " **Speichern** " verwenden, um einen anderen Wert als 4 ("[**aunlscheduledinstallations**](/windows/win32/api/wuapi/ne-wuapi-automaticupdatesnotificationlevel)") festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b8f40-112">The configuration operation fails if you use **Save** to set any value other than 4 ([**aunlScheduledInstallation**](/windows/win32/api/wuapi/ne-wuapi-automaticupdatesnotificationlevel)).</span></span>

 

 

 



