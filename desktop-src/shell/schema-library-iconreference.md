---
description: Das- <iconReference> Element gibt ein benutzerdefiniertes Symbol für diese Bibliothek an. Dieses Element ist optional und besitzt keine Attribute oder untergeordneten Elemente.
title: iconReference-Element (Bibliotheks Schema)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 7A35B014-1E01-4da2-AA64-4CFC3436C6D9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1f307ecd4fa523cc28881164869dca3329dfd698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994150"
---
# <a name="iconreference-element-library-schema"></a><span data-ttu-id="46873-104">iconReference-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="46873-104">iconReference Element (Library Schema)</span></span>

<span data-ttu-id="46873-105">Das- <iconReference> Element gibt ein benutzerdefiniertes Symbol für diese Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="46873-105">The <iconReference> element specifies a custom icon for this library.</span></span> <span data-ttu-id="46873-106">Dieses Element ist optional und besitzt keine Attribute oder untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="46873-106">This element is optional and has no attributes or child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="46873-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="46873-107">Syntax</span></span>


```
<!-- iconReference -->
    <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
```



## <a name="element-information"></a><span data-ttu-id="46873-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="46873-108">Element Information</span></span>



| <span data-ttu-id="46873-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="46873-109">Parent Element</span></span>                                                               | <span data-ttu-id="46873-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="46873-110">Child Elements</span></span> |
|------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="46873-111">librarydescription-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="46873-111">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="46873-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46873-112">Remarks</span></span>

<span data-ttu-id="46873-113">Der Symbol Verweis muss in einem Formular angegeben werden, das für die [**pathparser**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa) -Funktion geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="46873-113">The icon reference must be specified in a form suitable for the [**PathParseIconLocation**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa) function.</span></span> <span data-ttu-id="46873-114">Beispiel: `ModuleFileName,IconResourceIndex`.</span><span class="sxs-lookup"><span data-stu-id="46873-114">For example: `ModuleFileName,IconResourceIndex`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="46873-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="46873-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46873-116">foldertype-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="46873-116">folderType Element (Library Schema)</span></span>](schema-library-foldertype.md)
</dt> <dt>

[<span data-ttu-id="46873-117">islibrarypinned-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="46873-117">isLibraryPinned Element (Library Schema)</span></span>](schema-library-islibrarypinned.md)
</dt> <dt>

[<span data-ttu-id="46873-118">librarydescription-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="46873-118">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md)
</dt> <dt>

[<span data-ttu-id="46873-119">Name-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="46873-119">name Element (Library Schema)</span></span>](schema-library-name.md)
</dt> <dt>

[<span data-ttu-id="46873-120">Besitzer-SID-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="46873-120">ownerSID Element (Library Schema)</span></span>](schema-library-ownersid.md)
</dt> <dt>

[<span data-ttu-id="46873-121">PropertyStore-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="46873-121">propertyStore Element (Library Schema)</span></span>](schema-library-propertystore.md)
</dt> <dt>

[<span data-ttu-id="46873-122">searchconnectordescription-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="46873-122">searchConnectorDescription Element (Library Schema)</span></span>](schema-library-searchconnectordescription.md)
</dt> <dt>

[<span data-ttu-id="46873-123">searchconnectordescriptionlist-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="46873-123">searchConnectorDescriptionList Element (Library Schema)</span></span>](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="46873-124">templateingefo-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="46873-124">templateInfo Element (Library Schema)</span></span>](schema-library-templateinfo.md)
</dt> <dt>

[<span data-ttu-id="46873-125">Version-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="46873-125">version Element (Library Schema)</span></span>](schema-library-version.md)
</dt> </dl>

 

 



