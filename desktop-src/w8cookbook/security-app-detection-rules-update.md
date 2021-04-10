---
title: Aktualisieren von Erkennungsregeln für Sicherheitsanwendungen
description: Aktualisieren von Erkennungsregeln für Sicherheitsanwendungen
ms.assetid: A272C09B-A777-4119-BAB9-F91ABC03717A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242c6f9da8d474c16fab7573e216d3157f93b014
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "104039739"
---
# <a name="security-app-detection-rules-update"></a><span data-ttu-id="10919-103">Aktualisieren von Erkennungsregeln für Sicherheitsanwendungen</span><span class="sxs-lookup"><span data-stu-id="10919-103">Security app detection rules update</span></span>

## <a name="platforms"></a><span data-ttu-id="10919-104">Plattformen</span><span class="sxs-lookup"><span data-stu-id="10919-104">Platforms</span></span>

<span data-ttu-id="10919-105">**Clients** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="10919-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="10919-106">**Server** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="10919-106">**Servers** – Windows Server 2012</span></span>  


### <a name="description"></a><span data-ttu-id="10919-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10919-107">Description</span></span>

<span data-ttu-id="10919-108">Die Windows Store-Apps, die in Windows 8 hinzugefügt werden, werden alle unter "Programme" (% Program Files%) an einem gemeinsamen Speicherort installiert. wird als \\ Programmdateien \\ Windowsapps bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="10919-108">The Windows Store apps being added in Windows 8 are all being installed to a common location under “Program Files” (%programfiles%) called \\program files\\WindowsApps.</span></span>

### <a name="manifestation"></a><span data-ttu-id="10919-109">Ausstrahlung</span><span class="sxs-lookup"><span data-stu-id="10919-109">Manifestation</span></span>

<span data-ttu-id="10919-110">Dies kann zu Konflikten mit vorhandenen Konfigurationen führen, und einige Virenschutz-und antischadsoftwareerkennungen sehen diesen Standort als potenziellen Speicherort an, der eine Ursache für die Sorge ist.</span><span class="sxs-lookup"><span data-stu-id="10919-110">This can cause collisions with existing configurations, and some antivirus/anti-malware detectors see this location as a potential location that is a cause for concern.</span></span>

### <a name="mitigation"></a><span data-ttu-id="10919-111">Minderung</span><span class="sxs-lookup"><span data-stu-id="10919-111">Mitigation</span></span>

<span data-ttu-id="10919-112">Die aktuellen Empfehlungen lauten:</span><span class="sxs-lookup"><span data-stu-id="10919-112">The current recommendations are:</span></span>

-   <span data-ttu-id="10919-113">Wechseln von den \\ Programmdateien \\ Windowsapps zum Speichern beliebiger benutzerdefinierter apps</span><span class="sxs-lookup"><span data-stu-id="10919-113">Move away from \\program files\\WindowsApps for storing any custom apps</span></span>
-   <span data-ttu-id="10919-114">Antiviren-/antischadsoftwarehersteller sollten ihre Heuristik aktualisieren, damit Sie diesen Standort nicht als Malware Speicherort identifizieren können.</span><span class="sxs-lookup"><span data-stu-id="10919-114">Antivirus/antimalware vendors should update their heuristics so they do not identify that location as a malware location</span></span>

 

 




