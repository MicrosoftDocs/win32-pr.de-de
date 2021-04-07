---
title: Benutzerdefinierte Metadaten
description: Benutzerdefinierte Metadaten
ms.assetid: 86132163-da56-416a-9539-874d18972932
keywords:
- Windows Media-Format-SDK, benutzerdefinierte Metadaten
- Advanced Systems Format (ASF), benutzerdefinierte Metadaten
- ASF (Advanced Systems Format), benutzerdefinierte Metadaten
- Windows Media-Format-SDK, IWMHeaderInfo3-Schnittstelle
- Advanced Systems Format (ASF), IWMHeaderInfo3-Schnittstelle
- ASF (Advanced Systems Format), IWMHeaderInfo3-Schnittstelle
- Metadaten, anpassen
- IWMHeaderInfo3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a795ab184e5bd6120278f61c0d3654679fd79c28
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "103724027"
---
# <a name="custom-metadata"></a><span data-ttu-id="255c0-111">Benutzerdefinierte Metadaten</span><span class="sxs-lookup"><span data-stu-id="255c0-111">Custom Metadata</span></span>

<span data-ttu-id="255c0-112">Zusätzlich zu den zahlreichen unterstützten Attributen, die mit dem Windows Media Format SDK bereitgestellt werden, können Sie Metadatenattribute ihren eigenen Spezifikationen erstellen.</span><span class="sxs-lookup"><span data-stu-id="255c0-112">In addition to the many supported attributes provided with the Windows Media Format SDK, you can create metadata attributes to your own specifications.</span></span> <span data-ttu-id="255c0-113">Beim Erstellen benutzerdefinierter Metadatenattribute sollten Sie eine leicht identifizierbare Benennungs Konvention verwenden, um einen Konflikt mit Attributen zu vermeiden, die von anderen Benutzern erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="255c0-113">When creating custom metadata attributes, you should use an easily identifiable naming convention to avoid possible conflict with attributes created by others.</span></span>

<span data-ttu-id="255c0-114">Es wird empfohlen, dass Sie die Methoden von [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) verwenden, um Ihre Metadaten aufgrund der zusätzlichen Flexibilität zu erstellen, die Sie über die Methoden von [**iwmheaderinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="255c0-114">It is recommended that you use the methods of [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) to create your metadata because of the added flexibility they provide over the methods of [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo).</span></span>

## <a name="related-topics"></a><span data-ttu-id="255c0-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="255c0-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="255c0-116">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="255c0-116">**Attributes**</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="255c0-117">**Metadatenfeatures**</span><span class="sxs-lookup"><span data-stu-id="255c0-117">**Metadata Features**</span></span>](metadata-features.md)
</dt> <dt>

[<span data-ttu-id="255c0-118">**Arbeiten mit Metadaten**</span><span class="sxs-lookup"><span data-stu-id="255c0-118">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




