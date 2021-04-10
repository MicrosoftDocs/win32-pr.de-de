---
title: Metadata-Element (instrumentationmanifest)
description: Enthält globale Werte, auf die in anderen Manifesten verwiesen werden kann.
ms.assetid: 5bf3bb1e-47c9-4d6e-86e3-3316e21b76b3
keywords:
- Metadatenelement-Ereignisprotokoll
topic_type:
- apiref
api_name:
- metadata
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c14dc8772dee66fcce9ff07e9918c11b463aa414
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102931"
---
# <a name="metadata-instrumentationmanifest-element"></a><span data-ttu-id="5df9c-104">Metadata-Element (instrumentationmanifest)</span><span class="sxs-lookup"><span data-stu-id="5df9c-104">metadata (instrumentationManifest) Element</span></span>

<span data-ttu-id="5df9c-105">Enthält globale Werte, auf die in anderen Manifesten verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="5df9c-105">Contains global values that you can reference in other manifests.</span></span> <span data-ttu-id="5df9c-106">Ein Beispiel finden Sie in der Winmeta.xml-Datei, die im \\ Ordner include des Windows SDK enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="5df9c-106">For an example, see the Winmeta.xml file included in the \\Include folder of the Windows SDK.</span></span>

``` syntax
<xs:element name="metadata"
    type="MetadataType"
 />
```

<span data-ttu-id="5df9c-107">Das **Metadatenelement** wird durch das [**instrumentationmanifest**](eventmanifestschema-instrumentationmanifest-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="5df9c-107">The **metadata** element is defined by the [**instrumentationManifest**](eventmanifestschema-instrumentationmanifest-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="5df9c-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5df9c-108">Remarks</span></span>

<span data-ttu-id="5df9c-109">Obwohl Sie ein Manifest erstellen können, das einen Metadatenabschnitt enthält, wird es vom Dienst nicht verwendet. die einzigen Metadaten, die der Dienst erkennt, sind die Metadaten, die in der Winmeta.xml-Datei gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="5df9c-109">Although you can create a manifest that contains a metadata section, the service will not use it; the only metadata that the service recognizes is the metadata found in the Winmeta.xml file.</span></span>

## <a name="requirements"></a><span data-ttu-id="5df9c-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5df9c-110">Requirements</span></span>



| <span data-ttu-id="5df9c-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5df9c-111">Requirement</span></span> | <span data-ttu-id="5df9c-112">Wert</span><span class="sxs-lookup"><span data-stu-id="5df9c-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5df9c-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5df9c-113">Minimum supported client</span></span><br/> | <span data-ttu-id="5df9c-114">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5df9c-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5df9c-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5df9c-115">Minimum supported server</span></span><br/> | <span data-ttu-id="5df9c-116">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5df9c-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5df9c-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5df9c-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="5df9c-118">**Übergeordnetes Element**</span><span class="sxs-lookup"><span data-stu-id="5df9c-118">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="5df9c-119">**instrumentationmanifest**</span><span class="sxs-lookup"><span data-stu-id="5df9c-119">**instrumentationManifest**</span></span>](eventmanifestschema-instrumentationmanifest-element.md)
</dt> </dl>

 

 





