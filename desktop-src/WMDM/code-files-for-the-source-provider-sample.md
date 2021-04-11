---
title: Code Dateien für das Beispiel des Quell Anbieters
description: Code Dateien für das Beispiel des Quell Anbieters
ms.assetid: bd6bfc98-a805-4e04-8a80-7af42ed3dbef
keywords:
- Windows Media Device Manager, Beispiele
- Device Manager, Beispiele
- Windows Media Device Manager, Dienstanbieter Beispiel
- Beispiel für Device Manager, Dienstanbieter
- Dienstanbieter, Beispiele
- Beispiele, Dienstanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64b8af4b34310ae183ce55b2e52d3dd346dc6665
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100726"
---
# <a name="code-files-for-the-source-provider-sample"></a><span data-ttu-id="5f878-109">Code Dateien für das Beispiel des Quell Anbieters</span><span class="sxs-lookup"><span data-stu-id="5f878-109">Code Files for the Source Provider Sample</span></span>

<span data-ttu-id="5f878-110">Das Beispiel Quell Anbieter Projekt enthält die folgenden Quell Code Dateien mit zugeordneten Headern:</span><span class="sxs-lookup"><span data-stu-id="5f878-110">The sample source provider project includes the following source code files, with associated headers:</span></span>



| <span data-ttu-id="5f878-111">Datei</span><span class="sxs-lookup"><span data-stu-id="5f878-111">File</span></span>                   | <span data-ttu-id="5f878-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5f878-112">Description</span></span>                                                                                                                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f878-113">hdsppch. cpp</span><span class="sxs-lookup"><span data-stu-id="5f878-113">hdsppch.cpp</span></span>            | <span data-ttu-id="5f878-114">Schließt Standard-ATL-Dateien ein.</span><span class="sxs-lookup"><span data-stu-id="5f878-114">Includes standard ATL files.</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="5f878-115">Schlüssel. c</span><span class="sxs-lookup"><span data-stu-id="5f878-115">key.c</span></span>                  | <span data-ttu-id="5f878-116">Enthält einen dummyauthentifizierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="5f878-116">Contains a dummy authentication key.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="5f878-117">loghelp. cpp</span><span class="sxs-lookup"><span data-stu-id="5f878-117">loghelp.cpp</span></span>            | <span data-ttu-id="5f878-118">Enthält Funktionen, die Aktivitäten und Fehler mithilfe der **wmdmlogger** -Klasse protokollieren, die in der WMDMLOG.dll Systemdatei implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="5f878-118">Contains functions that log activity and errors by using the **WMDMLogger** class, which is implemented in the WMDMLOG.dll system file.</span></span>                                                                         |
| <span data-ttu-id="5f878-119">Mdserviceprovider. cpp</span><span class="sxs-lookup"><span data-stu-id="5f878-119">MDServiceProvider.cpp</span></span>  | <span data-ttu-id="5f878-120">Implementiert die cmdserviceprovider-Klasse, die die [**imdserviceprovider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider) -und die icomponentauthenticate-Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="5f878-120">Implements a class, CMDServiceProvider, that implements the [**IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider) and IComponentAuthenticate interfaces.</span></span>                                                             |
| <span data-ttu-id="5f878-121">mdsp. cpp</span><span class="sxs-lookup"><span data-stu-id="5f878-121">mdsp.cpp</span></span>               | <span data-ttu-id="5f878-122">Der DLL-Einstiegspunkt und der Registrierungscode.</span><span class="sxs-lookup"><span data-stu-id="5f878-122">DLL entry point and registration code.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="5f878-123">Mdspdevice. cpp</span><span class="sxs-lookup"><span data-stu-id="5f878-123">MDSPDevice.cpp</span></span>         | <span data-ttu-id="5f878-124">Implementiert eine Klasse, cmdspdevice, die die Schnittstellen [**IMDSPDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2), [**imdspdevicecontrol**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevicecontrol)und **ISpecifyPropertyPages** implementiert.</span><span class="sxs-lookup"><span data-stu-id="5f878-124">Implements a class, CMDSPDevice, that implements the [**IMDSPDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2), [**IMDSPDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevicecontrol), and **ISpecifyPropertyPages** interfaces.</span></span>                          |
| <span data-ttu-id="5f878-125">Mdspenum Device. cpp</span><span class="sxs-lookup"><span data-stu-id="5f878-125">MDSPEnumDevice.cpp</span></span>     | <span data-ttu-id="5f878-126">Implementiert die Klasse "cmdspenum Device", die die [**imdspenumschlag Device**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice) -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="5f878-126">Implements a class, CMDSPEnumDevice, that implements the [**IMDSPEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice) interface.</span></span>                                                                                                  |
| <span data-ttu-id="5f878-127">Mdspenum Storage. cpp</span><span class="sxs-lookup"><span data-stu-id="5f878-127">MDSPEnumStorage.cpp</span></span>    | <span data-ttu-id="5f878-128">Implementiert eine Klasse, cmdspenumschlag Storage, die die [**imdspenumschlag Storage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage) -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="5f878-128">Implements a class, CMDSPEnumStorage, that implements the [**IMDSPEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage) interface.</span></span>                                                                                               |
| <span data-ttu-id="5f878-129">Mdspstorage. cpp</span><span class="sxs-lookup"><span data-stu-id="5f878-129">MDSPStorage.cpp</span></span>        | <span data-ttu-id="5f878-130">Implementiert eine Klasse, cmdspstorage, die die Schnittstellen [**IMDSPStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2), [**imdspobjectinfo**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobjectinfo)und [**imdspobject**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject) implementiert.</span><span class="sxs-lookup"><span data-stu-id="5f878-130">Implements a class, CMDSPStorage, that implements the [**IMDSPStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2), [**IMDSPObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobjectinfo), and [**IMDSPObject**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject) interfaces.</span></span>                    |
| <span data-ttu-id="5f878-131">Mdspstorageglobals. cpp</span><span class="sxs-lookup"><span data-stu-id="5f878-131">MDSPStorageGlobals.cpp</span></span> | <span data-ttu-id="5f878-132">Implementiert eine Klasse, cmdspstorageglobals, die die [**imdspstorageglobals**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals) -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="5f878-132">Implements a class, CMDSPStorageGlobals, that implements the [**IMDSPStorageGlobals**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals) interface.</span></span>                                                                                      |
| <span data-ttu-id="5f878-133">Mdsputil. cpp</span><span class="sxs-lookup"><span data-stu-id="5f878-133">MDSPutil.cpp</span></span>           | <span data-ttu-id="5f878-134">Enthält verschiedene Hilfsprogrammfunktionen für die Verwaltung von Geräten und Dateien.</span><span class="sxs-lookup"><span data-stu-id="5f878-134">Contains various utility functions for device and file management.</span></span>                                                                                                                                              |
| <span data-ttu-id="5f878-135">PropPage. cpp</span><span class="sxs-lookup"><span data-stu-id="5f878-135">proppage.cpp</span></span>           | <span data-ttu-id="5f878-136">Implementiert eine Klasse, CPropPage, die die ATL-Klassen **IPropertyPageImpl** (zum Implementieren von IPropertyPage) und **CDialogImpl** erbt, die die ATL-Klasse CDialogImpl erbt (zum Verwalten von Fenstern und Nachrichten).</span><span class="sxs-lookup"><span data-stu-id="5f878-136">Implements a class, CPropPage, that inherits the ATL classes **IPropertyPageImpl** (to implement IPropertyPage) and **CDialogImpl**, which inherits the ATL class CDialogImpl (to manage windows and messages).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="5f878-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5f878-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f878-138">**Beispiel Dienstanbieter**</span><span class="sxs-lookup"><span data-stu-id="5f878-138">**Sample Service Provider**</span></span>](sample-service-provider.md)
</dt> </dl>

 

 




