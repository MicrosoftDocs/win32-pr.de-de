---
description: Verwenden der mehrsprachigen Benutzeroberfläche
ms.assetid: caf167ad-f9a8-4093-9581-57bc507d1f6a
title: Verwenden der mehrsprachigen Benutzeroberfläche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 287acc88d144c7775d2125cbb4a055784370d87f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218688"
---
# <a name="using-multilingual-user-interface"></a><span data-ttu-id="d2524-103">Verwenden der mehrsprachigen Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="d2524-103">Using Multilingual User Interface</span></span>

<span data-ttu-id="d2524-104">In diesem Abschnitt wird beschrieben, wie Sie Ihre Anwendungen mit der mehrsprachigen Benutzeroberfläche (MUI) entwerfen und implementieren.</span><span class="sxs-lookup"><span data-stu-id="d2524-104">This section describes how to use Multilingual User Interface (MUI) functionality to design and implement your applications.</span></span> <span data-ttu-id="d2524-105">Im folgenden werden die Aspekte der MUI-Technologie erläutert, die in den meisten Phasen des Anwendungslebenszyklus berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="d2524-105">The following are aspects of MUI technology that will come into play at most stages of the application lifecycle.</span></span>

-   <span data-ttu-id="d2524-106">Anwendungsentwicklung, einschließlich Ressourcen Vorbereitung, Festlegen von Einstellungen für die Anwendungs Sprache, Auffinden und Laden von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d2524-106">Application development, including resource preparation, setting of application language preferences, finding and loading of resources</span></span>
-   <span data-ttu-id="d2524-107">Entwickeln und lokalisieren der Anwendung</span><span class="sxs-lookup"><span data-stu-id="d2524-107">Building and localizing the application</span></span>
-   <span data-ttu-id="d2524-108">Bereitstellen der Anwendung</span><span class="sxs-lookup"><span data-stu-id="d2524-108">Deploying the application</span></span>

<span data-ttu-id="d2524-109">Im folgenden finden Sie einige Fragen, die beim Entwerfen und Implementieren einer MUI-Anwendung zu berücksichtigen sind.</span><span class="sxs-lookup"><span data-stu-id="d2524-109">Here are some questions to consider when designing and implementing a MUI application.</span></span>

-   <span data-ttu-id="d2524-110">Welche Versionen von Windows werden von der Anwendung unterstützt?</span><span class="sxs-lookup"><span data-stu-id="d2524-110">What are the versions of Windows that the application will support?</span></span>
-   <span data-ttu-id="d2524-111">In welchen Sprachen wird die Anwendung lokalisiert?</span><span class="sxs-lookup"><span data-stu-id="d2524-111">In what languages will the application be localized?</span></span>
-   <span data-ttu-id="d2524-112">Sollten die Anwendungs Spracheinstellungen immer den Spracheinstellungen für das Betriebssystem entsprechen oder sollte der Anwendungs Benutzer in der Lage sein, bestimmte Sprachen festzulegen?</span><span class="sxs-lookup"><span data-stu-id="d2524-112">Should the application language settings always follow language settings for the operating system, or should the application user be able to set specific languages?</span></span>
-   <span data-ttu-id="d2524-113">Welche Art von Benutzeroberflächen Ressourcen werden von der Anwendung verwendet, und wo werden Sie gespeichert?</span><span class="sxs-lookup"><span data-stu-id="d2524-113">What type of user interface resources does the application use and where are they stored?</span></span>

<span data-ttu-id="d2524-114">In diesem Abschnitt werden folgende Themen behandelt.</span><span class="sxs-lookup"><span data-stu-id="d2524-114">This section includes the following topics.</span></span> <span data-ttu-id="d2524-115">Die Beschreibungen nehmen eine MUI-Anwendung an, die auf Windows Vista und höher ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="d2524-115">The descriptions assume a MUI application targeted at Windows Vista and later.</span></span> <span data-ttu-id="d2524-116">Die Ressourcen für diese Anwendung sind Win32-Ressourcen mit sprachspezifischen Ressourcen und ausführbarem Code, der in separaten Win32 PE-Dateien gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="d2524-116">The resources for this application are Win32 resources, with language-specific resources and executable code residing in separate Win32 PE files.</span></span> <span data-ttu-id="d2524-117">Besondere Überlegungen zur Unterstützung von Betriebssystemen vor Windows Vista oder für verschiedene Arten von Ressourcen werden nach Bedarf hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d2524-117">Special considerations for support of pre-Windows Vista operating systems or for different types of resources are added as appropriate.</span></span>

-   [<span data-ttu-id="d2524-118">Vorbereiten von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d2524-118">Preparing Resources</span></span>](preparing-resources.md)
-   [<span data-ttu-id="d2524-119">Festlegen der Einstellungen für die Anwendungs Sprache</span><span class="sxs-lookup"><span data-stu-id="d2524-119">Setting Application Language Preferences</span></span>](setting-application-language-preferences.md)
-   [<span data-ttu-id="d2524-120">Suchen von Win32 PE-Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d2524-120">Locating Win32 PE Resources</span></span>](locating-win32-pe-resources.md)
-   [<span data-ttu-id="d2524-121">Suchen von nicht-Win32 PE-Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d2524-121">Locating Non-Win32 PE Resources</span></span>](locating-non-win32-pe-resources.md)
-   [<span data-ttu-id="d2524-122">Lokalisieren von Ressourcen und entwickeln der Anwendung</span><span class="sxs-lookup"><span data-stu-id="d2524-122">Localizing Resources and Building the Application</span></span>](localizing-resources-and-building-the-application.md)
-   [<span data-ttu-id="d2524-123">MUI: System Settings-Anwendungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="d2524-123">MUI: System Settings Application Sample</span></span>](mui-system-settings-application-sample.md)
-   [<span data-ttu-id="d2524-124">Beispiel für MUI: Application-Specific Einstellungen (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="d2524-124">MUI: Application-Specific Settings Sample (Windows Vista)</span></span>](mui-application-specific-settings-sample-vista.md)
-   [<span data-ttu-id="d2524-125">Beispiel für MUI: Application-Specific Einstellungen (Pre-Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="d2524-125">MUI: Application-Specific Settings Sample (Pre-Windows Vista)</span></span>](mui-application-specific-settings-sample-pre-vista.md)

 

 



