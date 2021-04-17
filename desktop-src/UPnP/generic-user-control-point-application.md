---
title: Generische Benutzer Steuerungspunkt-Anwendung
description: Mit der generischen benutzersteuerungs Punkt-Anwendung (UCP) können Sie Geräte ermitteln, diese ermittelten Geräte steuern und die zugehörigen Informationen über eine grafische Benutzeroberfläche anzeigen.
ms.assetid: 18ac23df-9d69-4a28-91e5-991eb4f3e6ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee56710cc1fafcc8551b34cb53df531f1f8cb601
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104566997"
---
# <a name="generic-user-control-point-application"></a><span data-ttu-id="7c285-103">Generische Benutzer Steuerungspunkt-Anwendung</span><span class="sxs-lookup"><span data-stu-id="7c285-103">Generic User Control Point Application</span></span>

<span data-ttu-id="7c285-104">Mit der generischen benutzersteuerungs Punkt-Anwendung (UCP) können Sie Geräte ermitteln, diese ermittelten Geräte steuern und die zugehörigen Informationen über eine grafische Benutzeroberfläche anzeigen.</span><span class="sxs-lookup"><span data-stu-id="7c285-104">The generic user control point (UCP) application allows you to discover devices, control those discovered devices, and view the related eventing information, all using a graphical interface.</span></span>

<span data-ttu-id="7c285-105">**So starten Sie die generische UCP-Anwendung**</span><span class="sxs-lookup"><span data-stu-id="7c285-105">**To start the generic UCP application**</span></span>

1.  <span data-ttu-id="7c285-106">Erstellen und konfigurieren Sie die Beispiele \\ netds \\ UPnP \\ genericucp \\ cpp \\devtype.txt Datei (oder die \\devtype.txt Datei VisualBasic \\ ) mit Geräteinformationen.</span><span class="sxs-lookup"><span data-stu-id="7c285-106">Create and configure the samples\\netds\\upnp\\GenericUCP\\CPP\\devtype.txt file (or the \\VisualBasic\\devtype.txt file) with device information.</span></span> <span data-ttu-id="7c285-107">Mit dieser Datei können Sie den generischen UCP für die Suchvorgänge "Suchen nach Typ" und "Async Find" konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="7c285-107">This file allows you to configure the generic UCP for the "find by type" and "async find" searches.</span></span> <span data-ttu-id="7c285-108">Jede Zeile der Datei muss einen Gerätetyp und die zugehörige Beschreibung enthalten.</span><span class="sxs-lookup"><span data-stu-id="7c285-108">Each line of the file must contain a device type and the related description.</span></span> <span data-ttu-id="7c285-109">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="7c285-109">For example:</span></span>

    ``` syntax
    upnp:rootdevice All Root Devices
    urn:schemas-upnp-org:device:mediaplayer:1    Media Player
    ```

    <span data-ttu-id="7c285-110">Dieses Beispiel gilt für ein fiktives Media Player-Gerät.</span><span class="sxs-lookup"><span data-stu-id="7c285-110">This example is for a fictitious media player device.</span></span> <span data-ttu-id="7c285-111">Das "Media Player" am Ende der zweiten Zeile ist nicht Teil des Gerätetyps, sondern dient zu Informationszwecken in der generischen UCP-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="7c285-111">The "Media Player" at the end of the second line is not a part of the device type, it is for informational purposes in the Generic UCP application.</span></span> <span data-ttu-id="7c285-112">Das gleiche gilt für "alle Stamm Geräte" in der ersten Zeile.</span><span class="sxs-lookup"><span data-stu-id="7c285-112">The same applies to "All Root Devices" in the first line.</span></span>

    <span data-ttu-id="7c285-113">Fügen Sie eine Zeile hinzu, die den jeweiligen Gerätetyp und die Beschreibung für jedes Gerät enthält.</span><span class="sxs-lookup"><span data-stu-id="7c285-113">Add a line that contains your specific device type and description for each device.</span></span>

2.  <span data-ttu-id="7c285-114">Erstellen und konfigurieren Sie die Beispiele \\ netds \\ UPnP \\ genericucp \\ cpp \\udn.txt Datei (oder die \\udn.txt Datei VisualBasic \\ ) mit udn-Informationen für Ihre Geräte.</span><span class="sxs-lookup"><span data-stu-id="7c285-114">Create and configure the samples\\netds\\upnp\\GenericUCP\\CPP\\udn.txt file (or the \\VisualBasic\\udn.txt file) with UDN information for your devices.</span></span> <span data-ttu-id="7c285-115">Mit dieser Datei können Sie den generischen UCP für die Suche nach udn suchen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="7c285-115">This file allows you to configure the generic UCP for the "find by UDN" search.</span></span> <span data-ttu-id="7c285-116">Jede Zeile verwendet die folgende Form:</span><span class="sxs-lookup"><span data-stu-id="7c285-116">Each line uses the following form:</span></span>

    ``` syntax
    uuid:{7d50b574-4213-4b88-84d9-e5c9241fcb3a}
    ```

    <span data-ttu-id="7c285-117">Fügen Sie eine Zeile hinzu, die ihren spezifischen udn für jedes Gerät enthält.</span><span class="sxs-lookup"><span data-stu-id="7c285-117">Add a line that contains your specific UDN for each device.</span></span>

3.  <span data-ttu-id="7c285-118">Führen Sie GenericUCP.exe aus.</span><span class="sxs-lookup"><span data-stu-id="7c285-118">Run GenericUCP.exe.</span></span> <span data-ttu-id="7c285-119">Das Fenster **generisches UCP** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7c285-119">The **Generic UCP** window appears.</span></span>

    ![Generisches UCP-Fenster](images/generic-ucp.png)

> [!Note]  
> <span data-ttu-id="7c285-121">Die **Ansichts Darstellung** und der **Ansichts Dienst DESC.** -Funktionalität ist nicht im C++-Beispielcode implementiert.</span><span class="sxs-lookup"><span data-stu-id="7c285-121">The **View Presentation** and **View Service Desc.** functionality is not implemented in the C++ sample code.</span></span>

 

 

 




