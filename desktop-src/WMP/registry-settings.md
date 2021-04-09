---
title: Registrierungseinstellungen
description: Registrierungseinstellungen
ms.assetid: aeb1f731-9d1f-4962-9101-fadf2dd23b4b
keywords:
- Windows Media Player, Registrierung
- Registrierung, Einstellungen für Windows-Media Player
- SDK (Software Development Kit), Registrierung
- Software Development Kit (SDK), Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1a57d792d252a5b50c57726be8e82aa1d4dd682
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856063"
---
# <a name="registry-settings"></a><span data-ttu-id="120f7-107">Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="120f7-107">Registry Settings</span></span>

<span data-ttu-id="120f7-108">Windows Media Player 9 oder höher verwendet die Registrierung, um bestimmte Einstellungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="120f7-108">Windows Media Player 9 Series or later uses the registry to store certain settings.</span></span> <span data-ttu-id="120f7-109">Sie können Änderungen an diesen Einstellungen vornehmen, um das Verhalten von Windows Media Player und dem Windows Media Player-Steuerelement zu ändern.</span><span class="sxs-lookup"><span data-stu-id="120f7-109">You can make changes to these settings to change the behavior of Windows Media Player and the Windows Media Player control.</span></span>

<span data-ttu-id="120f7-110">In den folgenden Abschnitten werden die unterstützten Registrierungs Einstellungen ausführlich erläutert.</span><span class="sxs-lookup"><span data-stu-id="120f7-110">The following sections detail the supported registry settings.</span></span>



| <span data-ttu-id="120f7-111">`Section`</span><span class="sxs-lookup"><span data-stu-id="120f7-111">Section</span></span>                                                                                                        | <span data-ttu-id="120f7-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="120f7-112">Description</span></span>                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="120f7-113">Registrierungs Einstellungen für die Dateinamenerweiterung</span><span class="sxs-lookup"><span data-stu-id="120f7-113">File Name Extension Registry Settings</span></span>](file-name-extension-registry-settings.md)                             | <span data-ttu-id="120f7-114">Beschreibt, wie eine benutzerdefinierte Dateinamenerweiterung registriert wird.</span><span class="sxs-lookup"><span data-stu-id="120f7-114">Describes how to register a custom file name extension.</span></span>                                                                                                               |
| [<span data-ttu-id="120f7-115">Registrierungs Einstellungen für benutzerdefinierte Schemas</span><span class="sxs-lookup"><span data-stu-id="120f7-115">Custom Scheme Registry Settings</span></span>](custom-scheme-registry-settings.md)                                         | <span data-ttu-id="120f7-116">Beschreibt, wie ein benutzerdefiniertes Schema registriert wird.</span><span class="sxs-lookup"><span data-stu-id="120f7-116">Describes how to register a custom scheme.</span></span>                                                                                                                            |
| [<span data-ttu-id="120f7-117">Registrierungs Einstellungen für die Ordner Überwachung</span><span class="sxs-lookup"><span data-stu-id="120f7-117">Folder Monitoring Registry Settings</span></span>](folder-monitoring-registry-settings.md)                                 | <span data-ttu-id="120f7-118">Hier wird beschrieben, wie Sie Datei Ordner registrieren, die von Windows Media Player überwacht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="120f7-118">Describes how to register file folders to be monitored by Windows Media Player.</span></span>                                                                                       |
| [<span data-ttu-id="120f7-119">Registrierungs Einstellungen für den Firewallport</span><span class="sxs-lookup"><span data-stu-id="120f7-119">Firewall Port Registry Settings</span></span>](firewall-port-registry-settings.md)                                         | <span data-ttu-id="120f7-120">Beschreibt einen Registrierungs Eintrag, der von Windows Media Player festgelegt wird, um anzugeben, ob Firewalls Ports für die Bibliotheks Freigabe geöffnet lassen sollen.</span><span class="sxs-lookup"><span data-stu-id="120f7-120">Describes a registry entry that Windows Media Player sets to specify whether firewalls should leave ports open for library sharing.</span></span>                                   |
| [<span data-ttu-id="120f7-121">Registrierungs Einstellung für automatische Übernahme</span><span class="sxs-lookup"><span data-stu-id="120f7-121">Silent Acquisition Registry Setting</span></span>](silent-acquisition-registry-setting.md)                                 | <span data-ttu-id="120f7-122">Beschreibt einen Registrierungs Eintrag, den Windows Media Player verwendet, um zu bestimmen, ob die Nutzungsrechte automatisch heruntergeladen werden sollen, wenn der Benutzer geschützte Inhalte wieder gibt oder synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="120f7-122">Describes a registry entry that Windows Media Player uses to determine whether to download usage rights automatically when the user plays or syncs protected content.</span></span> |
| [<span data-ttu-id="120f7-123">Anwendungs Abhängigkeit wird registriert</span><span class="sxs-lookup"><span data-stu-id="120f7-123">Registering Application Dependency</span></span>](registering-application-dependency.md)                                   | <span data-ttu-id="120f7-124">Enthält Informationen zum Registrieren Ihrer Anwendung, um sicherzustellen, dass auf dem Computer des Benutzers korrekte Laufzeitdateien vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="120f7-124">Provides information about how to register your application to ensure the correct runtime files exist on the user's computer.</span></span>                                         |
| [<span data-ttu-id="120f7-125">Registrierungseinträge zum Nachverfolgen des Installations Fortschritts</span><span class="sxs-lookup"><span data-stu-id="120f7-125">Registry Entries for Tracking Installation Progress</span></span>](registry-entries-for-tracking-installation-progress.md) | <span data-ttu-id="120f7-126">Beschreibt Registrierungseinträge, die von Installationsprogrammen verwendet werden können, um den Fortschritt von Windows Media Player-Setup zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="120f7-126">Describes registry entries that installation programs can use to track the progress of Windows Media Player setup.</span></span>                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="120f7-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="120f7-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="120f7-128">**Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="120f7-128">**Windows Media Player**</span></span>](windows-media-player.md)
</dt> </dl>

 

 




