---
description: Das- <folderType> Element gibt die GUID für den Ordnertyp an. Dieses Element ist erforderlich, wenn das- <templateInfo> Element vorhanden ist. Sie verfügt über keine Attribute und keine untergeordneten Elemente.
ms.assetid: 2361bbf5-adeb-4189-a8ff-5fdd1c9b0ec6
title: foldertype-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7d2a9e7f83dbe225427a8370cd8f5e948a46cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484403"
---
# <a name="foldertype-element-search-connector-schema"></a><span data-ttu-id="6ce66-105">foldertype-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="6ce66-105">folderType Element (Search Connector Schema)</span></span>

<span data-ttu-id="6ce66-106">Das- <folderType> Element gibt die GUID für den Ordnertyp an.</span><span class="sxs-lookup"><span data-stu-id="6ce66-106">The <folderType> element specifies GUID for the folder type.</span></span> <span data-ttu-id="6ce66-107">Dieses Element ist erforderlich, wenn das- <templateInfo> Element vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6ce66-107">This element is required if the <templateInfo> element exists.</span></span> <span data-ttu-id="6ce66-108">Sie verfügt über keine Attribute und keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="6ce66-108">It has no attributes and no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ce66-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ce66-109">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="6ce66-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="6ce66-110">Element Information</span></span>



| <span data-ttu-id="6ce66-111">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="6ce66-111">Parent Element</span></span>                                                                         | <span data-ttu-id="6ce66-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6ce66-112">Child Elements</span></span> |
|----------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="6ce66-113">templateingefo-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="6ce66-113">templateInfo Element (Search Connector Schema)</span></span>](search-schema-sconn-templateinfo.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="6ce66-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ce66-114">Remarks</span></span>

<span data-ttu-id="6ce66-115">Die Standard-GUID ist {8faf9629-1980-46ff-8023-9dceab9c3ee3}, ein allgemeiner Ordnertyp für Verbund Suchconnectors (OpenSearch).</span><span class="sxs-lookup"><span data-stu-id="6ce66-115">The default GUID is {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}, a general folder type for federated search (OpenSearch) connectors.</span></span>

## <a name="example-of-a-foldertype-element"></a><span data-ttu-id="6ce66-116">Beispiel für ein foldertype-Element</span><span class="sxs-lookup"><span data-stu-id="6ce66-116">Example of a folderType Element</span></span>


```
<!-- templateInfo and folderType -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 



