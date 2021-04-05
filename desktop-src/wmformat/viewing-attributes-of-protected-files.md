---
title: Anzeigen der Attribute geschützter Dateien
description: Anzeigen der Attribute geschützter Dateien
ms.assetid: fbfa1a1b-afd0-4f61-86ae-488716e16355
keywords:
- Windows Media-Format-SDK, Anzeigen von Attributen geschützter Dateien
- Windows Media-Format-SDK, Attribute geschützter Dateien
- Windows Media-Format-SDK, geschützte Dateien
- Advanced Systems Format (ASF), Anzeigen von Attributen geschützter Dateien
- ASF (Advanced Systems Format), Anzeigen von Attributen geschützter Dateien
- Advanced Systems Format (ASF), Attribute geschützter Dateien
- ASF (Advanced Systems Format), Attribute geschützter Dateien
- Advanced Systems Format (ASF), geschützte Dateien
- ASF (Advanced Systems Format), geschützte Dateien
- Digital Rights Management (DRM), Anzeigen der Attribute geschützter Dateien
- DRM (Digital Rights Management), Anzeigen der Attribute geschützter Dateien
- Digital Rights Management (DRM), Attribute geschützter Dateien
- DRM (Digital Rights Management), Attribute geschützter Dateien
- Digital Rights Management (DRM), geschützte Dateien
- DRM (Digital Rights Management), geschützte Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 642e9f580c3dffa1d3785985d548a5f971cfc218
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723397"
---
# <a name="viewing-attributes-of-protected-files"></a><span data-ttu-id="78f55-118">Anzeigen der Attribute geschützter Dateien</span><span class="sxs-lookup"><span data-stu-id="78f55-118">Viewing Attributes of Protected Files</span></span>

<span data-ttu-id="78f55-119">In einigen Szenarien müssen Sie möglicherweise bestimmte DRM-Attribute in einer Datei abrufen, ohne tatsächlich auf den Inhalt der Datei zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="78f55-119">In some scenarios, you may need to retrieve certain DRM attributes in a file without actually accessing the contents of the file.</span></span> <span data-ttu-id="78f55-120">Diese Funktion ist beispielsweise bei Anwendungen nützlich, die Datei Batches auf verschiedene Weise auf der Grundlage von Informationen im Dateiheader verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="78f55-120">This capability is useful, for example, in applications that process batches of files in different ways based on information in the file header.</span></span> <span data-ttu-id="78f55-121">In früheren Versionen des SDK für den Windows Media-Format mussten Anwendungen eine Verknüpfung mit der statischen DRM-Bibliothek herstellen, um geschützte Dateien zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="78f55-121">In previous versions of the Windows Media Format SDK, applications were required to link to the DRM static library in order to open any protected file.</span></span> <span data-ttu-id="78f55-122">Anwendungen, die keine DRM-Bibliothek haben, können die [**iwmdrmeditor:: getdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) -Schnittstelle für das Metadaten-Editor-Objekt verwenden, um bestimmte DRM-Attribute zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="78f55-122">Applications that do not have the DRM library can use the [**IWMDRMEditor::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) interface on the metadata editor object to examine certain DRM attributes.</span></span>

> [!Note]  
> <span data-ttu-id="78f55-123">DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="78f55-123">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="78f55-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="78f55-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78f55-125">**DRM-Attribut Liste**</span><span class="sxs-lookup"><span data-stu-id="78f55-125">**DRM Attribute List**</span></span>](drm-attribute-list.md)
</dt> <dt>

[<span data-ttu-id="78f55-126">**Aktivieren DRM-Unterstützung**</span><span class="sxs-lookup"><span data-stu-id="78f55-126">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="78f55-127">**Iwmdrmeditor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="78f55-127">**IWMDRMEditor Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)
</dt> </dl>

 

 




