---
title: Komplexer XmlType-Typ
description: Definiert ein XML-Fragment.
ms.assetid: ac6ce2a2-4584-4181-9a39-aceab85d5c51
keywords:
- Ereignisprotokoll für komplexen XmlType-Typ
topic_type:
- apiref
api_name:
- XmlType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a4a4d71d7f4f2685d6c5f1c0626392c79436b68d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391893"
---
# <a name="xmltype-complex-type"></a><span data-ttu-id="d4d08-104">Komplexer XmlType-Typ</span><span class="sxs-lookup"><span data-stu-id="d4d08-104">XmlType Complex Type</span></span>

<span data-ttu-id="d4d08-105">Definiert ein XML-Fragment.</span><span class="sxs-lookup"><span data-stu-id="d4d08-105">Defines an XML fragment.</span></span> <span data-ttu-id="d4d08-106">Eine beliebige Schema Instanz ist zulässig. der Knoten der obersten Ebene im Fragment muss ein Namespace-Attribut enthalten.</span><span class="sxs-lookup"><span data-stu-id="d4d08-106">Any schema instance is allowed; the top-level node in the fragment must contain a namespace attribute.</span></span>

``` syntax
<xs:complexType name="XmlType">
    <xs:sequence>
        <xs:any
            processContents="skip"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="requirements"></a><span data-ttu-id="d4d08-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4d08-107">Requirements</span></span>



| <span data-ttu-id="d4d08-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4d08-108">Requirement</span></span> | <span data-ttu-id="d4d08-109">Wert</span><span class="sxs-lookup"><span data-stu-id="d4d08-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d4d08-110">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d4d08-110">Minimum supported client</span></span><br/> | <span data-ttu-id="d4d08-111">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d4d08-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d4d08-112">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d4d08-112">Minimum supported server</span></span><br/> | <span data-ttu-id="d4d08-113">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d4d08-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





