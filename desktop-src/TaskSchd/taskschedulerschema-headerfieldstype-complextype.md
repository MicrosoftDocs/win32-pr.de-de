---
title: komplexer headerfieldstype-Typ
description: Definiert die Elemente, die die Felder für einen e-Mail-Header angeben.
ms.assetid: 1ad1b62d-5aca-4be4-b956-6f8c64761b2b
keywords:
- komplexer headerfieldstype-Typ Taskplaner
topic_type:
- apiref
api_name:
- headerFieldsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: edb783972217d0455eb2ee25fed31cf20e5b774b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475963"
---
# <a name="headerfieldstype-complex-type"></a><span data-ttu-id="d430f-104">komplexer headerfieldstype-Typ</span><span class="sxs-lookup"><span data-stu-id="d430f-104">headerFieldsType Complex Type</span></span>

<span data-ttu-id="d430f-105">Definiert die Elemente, die die Felder für einen e-Mail-Header angeben.</span><span class="sxs-lookup"><span data-stu-id="d430f-105">Defines the elements that specify the fields for an email header.</span></span>

``` syntax
<xs:complexType name="headerFieldsType">
    <xs:sequence>
        <xs:element name="HeaderField"
            type="headerFieldType"
            minOccurs="0"
            maxOccurs="32"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="d430f-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d430f-106">Child elements</span></span>



| <span data-ttu-id="d430f-107">Element</span><span class="sxs-lookup"><span data-stu-id="d430f-107">Element</span></span>                                                                         | <span data-ttu-id="d430f-108">type</span><span class="sxs-lookup"><span data-stu-id="d430f-108">Type</span></span>                                                                       | <span data-ttu-id="d430f-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d430f-109">Description</span></span>                                       |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="d430f-110">**Headerfield**</span><span class="sxs-lookup"><span data-stu-id="d430f-110">**HeaderField**</span></span>](taskschedulerschema-headerfield-headerfieldstype-element.md) | [<span data-ttu-id="d430f-111">**headerfieldtype**</span><span class="sxs-lookup"><span data-stu-id="d430f-111">**headerFieldType**</span></span>](taskschedulerschema-headerfieldtype-complextype.md) | <span data-ttu-id="d430f-112">Gibt ein Feld in einem e-Mail-Header an.</span><span class="sxs-lookup"><span data-stu-id="d430f-112">Specifies a field in an email header.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="d430f-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d430f-113">Requirements</span></span>



| <span data-ttu-id="d430f-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d430f-114">Requirement</span></span> | <span data-ttu-id="d430f-115">Wert</span><span class="sxs-lookup"><span data-stu-id="d430f-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d430f-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d430f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d430f-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d430f-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d430f-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d430f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d430f-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d430f-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





