---
description: Administrator Überschreibungen
ms.assetid: 25b6ce86-52c8-4f7f-97af-86b2eaf3e9af
title: Administrator Überschreibungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c43e16c9aa3eb3ab9fd5ee7c8d17b9bb4536315
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106363468"
---
# <a name="administrator-overrides"></a><span data-ttu-id="975c4-103">Administrator Überschreibungen</span><span class="sxs-lookup"><span data-stu-id="975c4-103">Administrator Overrides</span></span>

<span data-ttu-id="975c4-104">Windows verfügt über eine einzige Standard-Zugriffs Steuerungs Liste (ACL) für alle Energierichtlinien Objekte.</span><span class="sxs-lookup"><span data-stu-id="975c4-104">Windows has a single default access control list (ACL) on all power policy objects.</span></span> <span data-ttu-id="975c4-105">Die ACL gewährt Mitgliedern der Gruppe "authentifizierte Benutzer" Lese-, Schreib-und Änderungs Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="975c4-105">The ACL grants read, write, and change permissions to members of the Authenticated Users group.</span></span> <span data-ttu-id="975c4-106">Allen anderen Benutzern wird die Berechtigung schreibgeschützt erteilt.</span><span class="sxs-lookup"><span data-stu-id="975c4-106">All other users are granted read-only permission.</span></span> <span data-ttu-id="975c4-107">Anwendungen, die Energierichtlinien Funktionen aufzurufen, können bestimmen, ob ein Benutzer über Berechtigungen für eine angegebene Energie Einstellung verfügt, indem er die Funktion " [**powersettingaccesscheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) " verwendet.</span><span class="sxs-lookup"><span data-stu-id="975c4-107">Applications that call power policy functions can determine whether a user has permissions for a specified power setting by using the [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) function.</span></span>

<span data-ttu-id="975c4-108">Energie Einstellungen können über Gruppenrichtlinie überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="975c4-108">Power settings may be overridden via Group Policy.</span></span> <span data-ttu-id="975c4-109">Außer Kraft setzungen können über eine Domänen Gruppenrichtlinie oder eine lokale Gruppenrichtlinie festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="975c4-109">Overrides can be set through domain group policy or local group policy.</span></span> <span data-ttu-id="975c4-110">[**Powersettingaccesscheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) meldet, ob eine angegebene Energie Einstellung eine Gruppenrichtlinien-außer Kraft Setzung aufweist.</span><span class="sxs-lookup"><span data-stu-id="975c4-110">[**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) will report if a specified power setting has a group policy override.</span></span>

<span data-ttu-id="975c4-111">Das Befehlszeilen Tool **PowerCfg.exe** zeigt eine Fehlermeldung an, wenn ein Befehl nicht abgeschlossen werden kann, da der Benutzer nicht über Berechtigungen zum Ändern der Energie Einstellung verfügt oder weil die Energie Einstellung eine Gruppenrichtlinien-außer Kraft Setzung aufweist.</span><span class="sxs-lookup"><span data-stu-id="975c4-111">The command line tool **PowerCfg.exe** displays an error message when a command cannot be completed either because the user did not have permissions to change the power setting or because the power setting has a group policy override.</span></span>

<span data-ttu-id="975c4-112">Die Anwendung Energieoptionen in der Systemsteuerung bietet keine Unterstützung für das Konfigurieren von Berechtigungen für den Energierichtlinien Zugriff.</span><span class="sxs-lookup"><span data-stu-id="975c4-112">The Power Options application in Control Panel does not provide support for configuring power policy access permissions.</span></span> <span data-ttu-id="975c4-113">Das Ändern von Berechtigungen muss über **PowerCfg.exe** erfolgen.</span><span class="sxs-lookup"><span data-stu-id="975c4-113">Changing permissions must be done via **PowerCfg.exe**.</span></span>

 

 



