---
description: Das- <folderType> Element gibt eine GUID für den Ordnertyp an. Dieses Element ist erforderlich, wenn das <templateInfo> Element vorhanden ist, andernfalls ist es optional. Dieses Element hat keine Attribute und keine untergeordneten Elemente.
title: foldertype-Element (Bibliotheks Schema)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 240550F0-B6AC-470e-8BF1-DB5A4068226B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c6d94906fa8c0debfa1ee49d95f5acd47aea2526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977857"
---
# <a name="foldertype-element-library-schema"></a><span data-ttu-id="12aeb-105">foldertype-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="12aeb-105">folderType Element (Library Schema)</span></span>

<span data-ttu-id="12aeb-106">Das- <folderType> Element gibt eine GUID für den Ordnertyp an.</span><span class="sxs-lookup"><span data-stu-id="12aeb-106">The <folderType> element specifies a GUID for the folder type.</span></span> <span data-ttu-id="12aeb-107">Dieses Element ist erforderlich, wenn das <templateInfo> Element vorhanden ist, andernfalls ist es optional.</span><span class="sxs-lookup"><span data-stu-id="12aeb-107">This element is required if the <templateInfo> element exists, otherwise it is optional.</span></span> <span data-ttu-id="12aeb-108">Dieses Element hat keine Attribute und keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="12aeb-108">This element has no attributes and no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="12aeb-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="12aeb-109">Syntax</span></span>


```
<!-- folderType -->
    <xs:element name="templateInfo" minOccurs="0">
      <xs:complexType>
        <xs:all>
          <xs:element name="folderType" minOccurs="0"/>
        </xs:all>
      </xs:complexType>
    </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="12aeb-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="12aeb-110">Element Information</span></span>



| <span data-ttu-id="12aeb-111">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="12aeb-111">Parent Element</span></span>                                                           | <span data-ttu-id="12aeb-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="12aeb-112">Child Elements</span></span> |
|--------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="12aeb-113">templateingefo-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="12aeb-113">templateInfo Element (Library Schema)</span></span>](schema-library-templateinfo.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="12aeb-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="12aeb-114">Remarks</span></span>

<span data-ttu-id="12aeb-115">Wenn Sie einen Ordnertyp festlegen, werden die Spalten und Details, die standardmäßig in Windows Explorer angezeigt werden, bestimmt</span><span class="sxs-lookup"><span data-stu-id="12aeb-115">Setting a folder type determines the columns and details that appear in Windows Explorer by default.</span></span> <span data-ttu-id="12aeb-116">Ordnertyp-IDs ([**foldertypeid**](foldertypeid.md)) sind GUIDs, die in "shlguid. h" definiert sind.</span><span class="sxs-lookup"><span data-stu-id="12aeb-116">Folder type identifiers ([**FOLDERTYPEID**](foldertypeid.md)) are GUIDs defined in Shlguid.h.</span></span> <span data-ttu-id="12aeb-117">In der folgenden Tabelle sind die GUIDs der allgemeinen Ordner Typen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="12aeb-117">The following table lists the GUIDs of common folder types.</span></span>



| <span data-ttu-id="12aeb-118">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="12aeb-118">Folder Type</span></span>      | <span data-ttu-id="12aeb-119">GUID</span><span class="sxs-lookup"><span data-stu-id="12aeb-119">GUID</span></span>                                   |
|------------------|----------------------------------------|
| <span data-ttu-id="12aeb-120">Generische Bibliothek</span><span class="sxs-lookup"><span data-stu-id="12aeb-120">Generic Library</span></span>  | <span data-ttu-id="12aeb-121">{5f4eab9a-6833-4f61-899d-31cf46979d49}</span><span class="sxs-lookup"><span data-stu-id="12aeb-121">{5f4eab9a-6833-4f61-899d-31cf46979d49}</span></span> |
| <span data-ttu-id="12aeb-122">Benutzer Bibliotheken</span><span class="sxs-lookup"><span data-stu-id="12aeb-122">Users Libraries</span></span>  | <span data-ttu-id="12aeb-123">{C4D98F09-6124-4fe0-9942-826416082DA9}</span><span class="sxs-lookup"><span data-stu-id="12aeb-123">{C4D98F09-6124-4fe0-9942-826416082DA9}</span></span> |
| <span data-ttu-id="12aeb-124">Ordner "Dokumente"</span><span class="sxs-lookup"><span data-stu-id="12aeb-124">Documents Folder</span></span> | <span data-ttu-id="12aeb-125">{7d49d726-3c21-4f 05-99aa-f dc2c9474656}</span><span class="sxs-lookup"><span data-stu-id="12aeb-125">{7D49D726-3C21-4F05-99AA-FDC2C9474656}</span></span> |
| <span data-ttu-id="12aeb-126">Ordner "Bilder"</span><span class="sxs-lookup"><span data-stu-id="12aeb-126">Pictures Folder</span></span>  | <span data-ttu-id="12aeb-127">{B3690E58-E961-423B-B687-386EBFD83239}</span><span class="sxs-lookup"><span data-stu-id="12aeb-127">{B3690E58-E961-423B-B687-386EBFD83239}</span></span> |
| <span data-ttu-id="12aeb-128">Ordner "Videos"</span><span class="sxs-lookup"><span data-stu-id="12aeb-128">Videos Folder</span></span>    | <span data-ttu-id="12aeb-129">{5fa96407-7e77-483c-ac93-691d05850de8}</span><span class="sxs-lookup"><span data-stu-id="12aeb-129">{5fa96407-7e77-483c-ac93-691d05850de8}</span></span> |
| <span data-ttu-id="12aeb-130">Ordner "Games"</span><span class="sxs-lookup"><span data-stu-id="12aeb-130">Games Folder</span></span>     | <span data-ttu-id="12aeb-131">{b689b0d0-76d3-4cbb-87f7-585d0e0ce070}</span><span class="sxs-lookup"><span data-stu-id="12aeb-131">{b689b0d0-76d3-4cbb-87f7-585d0e0ce070}</span></span> |
| <span data-ttu-id="12aeb-132">Ordner "Musik"</span><span class="sxs-lookup"><span data-stu-id="12aeb-132">Music Folder</span></span>     | <span data-ttu-id="12aeb-133">{94d6ddcc-4a68-4175-A374-bd584a510 B78}</span><span class="sxs-lookup"><span data-stu-id="12aeb-133">{94d6ddcc-4a68-4175-a374-bd584a510b78}</span></span> |
| <span data-ttu-id="12aeb-134">Kontakte</span><span class="sxs-lookup"><span data-stu-id="12aeb-134">Contacts</span></span>         | <span data-ttu-id="12aeb-135">{DE2B70EC-9BF7-4A93-BD3D-243F7881D492}</span><span class="sxs-lookup"><span data-stu-id="12aeb-135">{DE2B70EC-9BF7-4A93-BD3D-243F7881D492}</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="12aeb-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="12aeb-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12aeb-137">iconReference-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="12aeb-137">iconReference Element (Library Schema)</span></span>](schema-library-iconreference.md)
</dt> <dt>

[<span data-ttu-id="12aeb-138">islibrarypinned-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="12aeb-138">isLibraryPinned Element (Library Schema)</span></span>](schema-library-islibrarypinned.md)
</dt> <dt>

[<span data-ttu-id="12aeb-139">librarydescription-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="12aeb-139">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md)
</dt> <dt>

[<span data-ttu-id="12aeb-140">Name-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="12aeb-140">name Element (Library Schema)</span></span>](schema-library-name.md)
</dt> <dt>

[<span data-ttu-id="12aeb-141">Besitzer-SID-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="12aeb-141">ownerSID Element (Library Schema)</span></span>](schema-library-ownersid.md)
</dt> <dt>

[<span data-ttu-id="12aeb-142">PropertyStore-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="12aeb-142">propertyStore Element (Library Schema)</span></span>](schema-library-propertystore.md)
</dt> <dt>

[<span data-ttu-id="12aeb-143">searchconnectordescription-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="12aeb-143">searchConnectorDescription Element (Library Schema)</span></span>](schema-library-searchconnectordescription.md)
</dt> <dt>

[<span data-ttu-id="12aeb-144">searchconnectordescriptionlist-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="12aeb-144">searchConnectorDescriptionList Element (Library Schema)</span></span>](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="12aeb-145">templateingefo-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="12aeb-145">templateInfo Element (Library Schema)</span></span>](schema-library-templateinfo.md)
</dt> <dt>

[<span data-ttu-id="12aeb-146">Version-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="12aeb-146">version Element (Library Schema)</span></span>](schema-library-version.md)
</dt> </dl>

 

 



