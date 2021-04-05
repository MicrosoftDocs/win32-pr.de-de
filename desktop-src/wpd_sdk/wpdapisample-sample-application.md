---
description: Wpdapisample-Anwendung
ms.assetid: 854a6304-5d62-4f00-9366-8c2244568250
title: Wpdapisample-Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87c384d542c9b93ac733c91ee249938d744e40ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751184"
---
# <a name="wpdapisample-application"></a><span data-ttu-id="1930e-103">Wpdapisample-Anwendung</span><span class="sxs-lookup"><span data-stu-id="1930e-103">WpdApiSample Application</span></span>

<span data-ttu-id="1930e-104">Die Beispielanwendung wpdapisample ist eine Desktop Anwendung für die Befehlszeile, die es Ihnen ermöglicht, verbundene Geräte aufzulisten, Geräte zu durchsuchen, Objekte für Eigenschaften und Attribute abzufragen, Objekte zu senden und abzurufen usw.</span><span class="sxs-lookup"><span data-stu-id="1930e-104">The WpdApiSample sample application is a command-line desktop application that enables you to enumerate connected devices, explore devices, query objects for properties and attributes, send and retrieve objects, and so on.</span></span> <span data-ttu-id="1930e-105">Beim Start öffnet die Anwendung ein Befehlsfenster, in dem die Aufgaben aufgelistet sind, die Sie ausführen können.</span><span class="sxs-lookup"><span data-stu-id="1930e-105">On startup, the application opens a command window that lists the tasks you can perform.</span></span>

<span data-ttu-id="1930e-106">Die Beispielanwendung wpdapisample umfasst die folgenden Dateien:</span><span class="sxs-lookup"><span data-stu-id="1930e-106">The WpdApiSample sample application includes the following files:</span></span>



| <span data-ttu-id="1930e-107">**File**</span><span class="sxs-lookup"><span data-stu-id="1930e-107">**File**</span></span>               | <span data-ttu-id="1930e-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1930e-108">**Description**</span></span>                                                                                                                                                                                           |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1930e-109">"Contentenumeration. cpp"</span><span class="sxs-lookup"><span data-stu-id="1930e-109">ContentEnumeration.cpp</span></span> | <span data-ttu-id="1930e-110">Enthält Funktionen, die alle-Objekte auf einem Gerät auflisten.</span><span class="sxs-lookup"><span data-stu-id="1930e-110">Contains functions that enumerate all the objects on a device.</span></span>                                                                                                                                            |
| <span data-ttu-id="1930e-111">Contentproperties. cpp</span><span class="sxs-lookup"><span data-stu-id="1930e-111">ContentProperties.cpp</span></span>  | <span data-ttu-id="1930e-112">Enthält Funktionen, die Objekteigenschaften lesen und schreiben und Bulk-Eigenschaften festgelegte/Get-Anforderungen machen.</span><span class="sxs-lookup"><span data-stu-id="1930e-112">Contains functions that read and write object properties and make bulk property set/get requests.</span></span>                                                                                                         |
| <span data-ttu-id="1930e-113">Contenttransfer. cpp</span><span class="sxs-lookup"><span data-stu-id="1930e-113">ContentTransfer.cpp</span></span>    | <span data-ttu-id="1930e-114">Enthält Funktionen, die Inhalte auf das oder vom Gerät übertragen, Objekttyp Anforderungen lesen und einen Ordner auf dem Gerät erstellen.</span><span class="sxs-lookup"><span data-stu-id="1930e-114">Contains functions that transfer content to or from the device, read object type requirements, and create a folder on the device.</span></span>                                                                         |
| <span data-ttu-id="1930e-115">Devicecapabili. cpp</span><span class="sxs-lookup"><span data-stu-id="1930e-115">DeviceCapabilities.cpp</span></span> | <span data-ttu-id="1930e-116">Enthält Funktionen zum Auflisten der funktionalen Objekttypen auf dem Gerät, zum Auflisten der von jedem funktionalen Objekttyp unterstützten Inhaltstypen und zum Anzeigen von renderingobjektprofilen.</span><span class="sxs-lookup"><span data-stu-id="1930e-116">Contains functions to list the functional object types on the device, list the content types supported by each functional object type, and display rendering object profiles.</span></span>                             |
| <span data-ttu-id="1930e-117">Deviceenumeration. cpp</span><span class="sxs-lookup"><span data-stu-id="1930e-117">DeviceEnumeration.cpp</span></span>  | <span data-ttu-id="1930e-118">Listet die anzeigen Amen, Hersteller und Beschreibungen aller verbundenen Geräte auf.</span><span class="sxs-lookup"><span data-stu-id="1930e-118">Lists the friendly names, manufacturers, and descriptions of all connected devices.</span></span>                                                                                                                       |
| <span data-ttu-id="1930e-119">Deviceevents. cpp</span><span class="sxs-lookup"><span data-stu-id="1930e-119">DeviceEvents.cpp</span></span>       | <span data-ttu-id="1930e-120">Enthält Funktionen, die Geräte Ereignisse und ihre Parameter protokollieren, wenn Ereignisse ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="1930e-120">Contains functions that log device events and their parameters whenever events are fired.</span></span>                                                                                                                 |
| <span data-ttu-id="1930e-121">stdafx.cpp</span><span class="sxs-lookup"><span data-stu-id="1930e-121">Stdafx.cpp</span></span>             | <span data-ttu-id="1930e-122">Schließt die Standard Dateien ein.</span><span class="sxs-lookup"><span data-stu-id="1930e-122">Includes the standard files.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="1930e-123">Wpdapisample. cpp</span><span class="sxs-lookup"><span data-stu-id="1930e-123">WpdApiSample.cpp</span></span>       | <span data-ttu-id="1930e-124">Hostet die **\_ Tmain** -Start Funktion, die die lokale **domenu** -Funktion aufruft, die eine Liste der verfügbaren Geräte und Tasks anzeigt und die Funktion aufruft, die für die Menü Auswahl des Benutzers geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="1930e-124">Hosts the **\_tmain** startup function, which calls the local **DoMenu** function, which displays a list of available devices and tasks and calls the function appropriate for the user's menu selection.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="1930e-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1930e-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1930e-126">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1930e-126">Sample</span></span>](sample.md)
</dt> </dl>

 

 



