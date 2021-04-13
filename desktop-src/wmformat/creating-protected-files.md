---
title: Erstellen geschützter Dateien
description: Erstellen geschützter Dateien
ms.assetid: 5237e797-72ec-402e-81ec-ab379747e464
keywords:
- Windows Media-Format-SDK, erstellen geschützter Dateien
- Windows Media-Format-SDK, geschützte Dateien
- Advanced Systems Format (ASF), erstellen geschützter Dateien
- ASF (Advanced Systems Format), erstellen geschützter Dateien
- Advanced Systems Format (ASF), geschützte Dateien
- ASF (Advanced Systems Format), geschützte Dateien
- Advanced Systems Format (ASF), wmstubdrm. lib
- ASF (Advanced Systems Format), wmstubdrm. lib
- Wmstubdrm. lib, erstellen geschützter Dateien
- Wmstubdrm. lib, geschützte Dateien
- Digital Rights Management (DRM), wmstubdrm. lib
- DRM (Digital Rights Management), wmstubdrm. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160a14d96da924bdb2a307bc804514a1ec3de083
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314261"
---
# <a name="creating-protected-files"></a><span data-ttu-id="c15bc-115">Erstellen geschützter Dateien</span><span class="sxs-lookup"><span data-stu-id="c15bc-115">Creating Protected Files</span></span>

<span data-ttu-id="c15bc-116">Um geschützte digitale Mediendateien mithilfe von DRM Version 1 oder DRM Version 7 und höher zu erstellen, verknüpfen Sie eine Verknüpfung mit der Datei "wmstubdrm. lib", die Sie von Microsoft erhalten haben, und erstellen Sie das Writer-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c15bc-116">To create protected digital media files using either DRM version 1 or DRM versions 7 and later, link to the WMStubDRM.lib file that you obtained from Microsoft, and create the writer object.</span></span> <span data-ttu-id="c15bc-117">Verwenden Sie für den Schutz von Version 1 die [**iwmheaderinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) -Schnittstelle zum Festlegen der DRM-Attribute, die Sie anwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="c15bc-117">For version 1 protection, use the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface to set the DRM attributes you want to apply.</span></span> <span data-ttu-id="c15bc-118">Verwenden Sie für die Versionen 7 und höher die [**iwmdrmwriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) -Schnittstellen Methoden.</span><span class="sxs-lookup"><span data-stu-id="c15bc-118">For versions 7 and later, use the [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) interface methods.</span></span>

<span data-ttu-id="c15bc-119">In den folgenden Themen wird ausführlich beschrieben, wie Sie Dateien schützen.</span><span class="sxs-lookup"><span data-stu-id="c15bc-119">The following topics describe in detail how to protect files.</span></span>

-   [<span data-ttu-id="c15bc-120">Schützen von Dateien mit DRM-Version 1</span><span class="sxs-lookup"><span data-stu-id="c15bc-120">Protecting Files with DRM Version 1</span></span>](protecting-files-with-drm-version-1.md)
-   [<span data-ttu-id="c15bc-121">Schützen von Dateien mit DRM-Version 7 oder höher</span><span class="sxs-lookup"><span data-stu-id="c15bc-121">Protecting Files with DRM Version 7 or Later</span></span>](protecting-files-with-drm-version-7-or-later.md)

> [!Note]  
> <span data-ttu-id="c15bc-122">DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c15bc-122">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c15bc-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c15bc-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c15bc-124">**DRM-Attribut Liste**</span><span class="sxs-lookup"><span data-stu-id="c15bc-124">**DRM Attribute List**</span></span>](drm-attribute-list.md)
</dt> <dt>

[<span data-ttu-id="c15bc-125">**DRM-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="c15bc-125">**DRM Properties**</span></span>](drm-properties.md)
</dt> <dt>

[<span data-ttu-id="c15bc-126">**DRM-Versionen**</span><span class="sxs-lookup"><span data-stu-id="c15bc-126">**DRM Versions**</span></span>](drm-versions.md)
</dt> <dt>

[<span data-ttu-id="c15bc-127">**Aktivieren DRM-Unterstützung**</span><span class="sxs-lookup"><span data-stu-id="c15bc-127">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="c15bc-128">**Abrufen der erforderlichen DRM-Bibliothek**</span><span class="sxs-lookup"><span data-stu-id="c15bc-128">**Obtaining the Required DRM Library**</span></span>](obtaining-the-required-drm-library.md)
</dt> <dt>

[<span data-ttu-id="c15bc-129">**Geschützte Dateien werden gelesen.**</span><span class="sxs-lookup"><span data-stu-id="c15bc-129">**Reading Protected Files**</span></span>](reading-protected-files.md)
</dt> </dl>

 

 




