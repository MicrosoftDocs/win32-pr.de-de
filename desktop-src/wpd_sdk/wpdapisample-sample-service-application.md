---
description: Wpdservicesapisample-Anwendung
ms.assetid: 857753f7-bca1-4f4a-a8f9-0b2232e2f0dc
title: Wpdservicesapisample-Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54cbf6c6e4647744ae45f43b5d4139cbf7f9dc55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347379"
---
# <a name="wpdservicesapisample-application"></a><span data-ttu-id="c1919-103">Wpdservicesapisample-Anwendung</span><span class="sxs-lookup"><span data-stu-id="c1919-103">WpdServicesApiSample Application</span></span>

<span data-ttu-id="c1919-104">Ein Geräte Dienst ist eine Erweiterung eines funktionalen Objekts: Zusätzlich zur logischen Gruppierung von Gerätefunktionen bietet ein Geräte Dienst Anwendungen die Möglichkeit, diese Funktionen Programm gesteuert zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="c1919-104">A device service is an extension of a functional object: In addition to logically grouping device capabilities, a device service provides applications with the ability to programmatically discover those capabilities.</span></span>

<span data-ttu-id="c1919-105">Die Beispielanwendung wpdservicesapisample ist eine Befehlszeilen-Desktop Anwendung, mit der Sie kontaktdienste auf Geräten untersuchen können, die mit Ihrem Computer verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="c1919-105">The WpdServicesApiSample sample application is a command-line desktop application that you can use to explore Contacts services on devices attached to your computer.</span></span> <span data-ttu-id="c1919-106">Sie können diese Dienste durchsuchen, indem Sie unterstützt: Formate, Ereignisse, Methoden und abstrakte Dienste auflisten.</span><span class="sxs-lookup"><span data-stu-id="c1919-106">You can explore these services by listing supported: formats, events, methods, and abstract services.</span></span> <span data-ttu-id="c1919-107">Sie können diese Anwendung auch verwenden, um die Eigenschaften für einen bestimmten Kontakt Dienst abzurufen und Methoden aufzurufen, die von diesem Dienst unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="c1919-107">You can also use this application retrieve the properties on a given Contact service and to invoke methods supported by that service.</span></span>

<span data-ttu-id="c1919-108">Wenn Sie noch kein Gerät haben, das Kontakte Dienste unterstützt, können Sie wpdservicesapisample weiterhin ausführen, wenn Sie zunächst den wpdservicesampledriver installieren, der im Windows-Treiberkit enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="c1919-108">If you don't yet have a device that supports Contacts services, you can still run the WpdServicesApiSample if you first install the WpdServiceSampleDriver that is included in the Windows Driver Kit.</span></span>

<span data-ttu-id="c1919-109">Die Beispielanwendung wpdservicesapisample umfasst die folgenden Dateien:</span><span class="sxs-lookup"><span data-stu-id="c1919-109">The WpdServicesApiSample sample application includes the following files:</span></span>



| <span data-ttu-id="c1919-110">**File**</span><span class="sxs-lookup"><span data-stu-id="c1919-110">**File**</span></span>                | <span data-ttu-id="c1919-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c1919-111">**Description**</span></span>                                                                                                                                                                                           |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1919-112">"Contentenumeration. cpp"</span><span class="sxs-lookup"><span data-stu-id="c1919-112">ContentEnumeration.cpp</span></span>  | <span data-ttu-id="c1919-113">Enthält Methoden, die den Inhalt eines bestimmten Contacts-Dienstanbieter aufzählen.</span><span class="sxs-lookup"><span data-stu-id="c1919-113">Contains methods that enumerate the content on a given Contacts service.</span></span>                                                                                                                                  |
| <span data-ttu-id="c1919-114">Contentproperties. cpp</span><span class="sxs-lookup"><span data-stu-id="c1919-114">ContentProperties.cpp</span></span>   | <span data-ttu-id="c1919-115">Enthält Methoden, die Eigenschaften für einen bestimmten Kontakt Dienst lesen und schreiben.</span><span class="sxs-lookup"><span data-stu-id="c1919-115">Contains methods that read and write properties on a given Contacts service.</span></span>                                                                                                                              |
| <span data-ttu-id="c1919-116">Servicecapabili. cpp</span><span class="sxs-lookup"><span data-stu-id="c1919-116">ServiceCapabilities.cpp</span></span> | <span data-ttu-id="c1919-117">Enthält die Methoden, mit denen die unterstützten Formate, Ereignisse und abstrakten Dienste abgerufen werden, die von einem bestimmten Kontakt Dienst unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="c1919-117">Contains the methods that retrieve the supported formats, events, and abstract services that are supported by a given Contacts service.</span></span>                                                                   |
| <span data-ttu-id="c1919-118">Serviceenumeration. cpp</span><span class="sxs-lookup"><span data-stu-id="c1919-118">ServiceEnumeration.cpp</span></span>  | <span data-ttu-id="c1919-119">Enthält die Hilfsfunktionen, die Geräteinformationen abrufen, z. b. den Geräte freundlichen Namen oder die unterstützten kontaktdienste.</span><span class="sxs-lookup"><span data-stu-id="c1919-119">Contains the helper functions that retrieve device information such as the device-friendly name or the supported Contacts services.</span></span>                                                                       |
| <span data-ttu-id="c1919-120">Servicemethods. cpp</span><span class="sxs-lookup"><span data-stu-id="c1919-120">ServiceMethods.cpp</span></span>      | <span data-ttu-id="c1919-121">Enthält die Methoden, die Methoden abrufen und aufrufen, die von einem bestimmten Kontakt Dienst unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="c1919-121">Contains the methods that retrieve and invoke methods supported by a given Contacts service.</span></span>                                                                                                              |
| <span data-ttu-id="c1919-122">stdafx.cpp</span><span class="sxs-lookup"><span data-stu-id="c1919-122">Stdafx.cpp</span></span>              | <span data-ttu-id="c1919-123">Schließt die Standard Dateien ein.</span><span class="sxs-lookup"><span data-stu-id="c1919-123">Includes the standard files.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="c1919-124">Wpdserviceapisample. cpp</span><span class="sxs-lookup"><span data-stu-id="c1919-124">WpdServiceApiSample.cpp</span></span> | <span data-ttu-id="c1919-125">Hostet die **\_ Tmain** -Start Funktion, die die lokale **domenu** -Funktion aufruft, die eine Liste der verfügbaren Geräte und Tasks anzeigt und die Funktion aufruft, die für die Menü Auswahl des Benutzers geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="c1919-125">Hosts the **\_tmain** startup function, which calls the local **DoMenu** function, which displays a list of available devices and tasks and calls the function appropriate for the user's menu selection.</span></span> |



 


## <a name="related-topics"></a><span data-ttu-id="c1919-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c1919-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1919-127">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c1919-127">Samples</span></span>](sample.md)
</dt> </dl>

 

 



