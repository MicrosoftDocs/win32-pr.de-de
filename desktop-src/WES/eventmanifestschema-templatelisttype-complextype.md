---
title: Komplexer templatelisttype-Typ
description: Definiert eine Liste von Vorlagen, die die Daten angeben, die in die Ereignisse eingeschlossen werden sollen. | Komplexer templatelisttype-Typ
ms.assetid: 7f676746-6773-4ae2-8330-60d432c29e3a
keywords:
- Datentyp "templatelisttype" (Ereignisprotokoll)
topic_type:
- apiref
api_name:
- TemplateListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a60b31fd88d05f00229f27a616a29483a29bd49d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761778"
---
# <a name="templatelisttype-complex-type"></a><span data-ttu-id="61145-105">Komplexer templatelisttype-Typ</span><span class="sxs-lookup"><span data-stu-id="61145-105">TemplateListType Complex Type</span></span>

<span data-ttu-id="61145-106">Definiert eine Liste von Vorlagen, die die Daten angeben, die in die Ereignisse eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="61145-106">Defines a list of templates that specify the data to include with the events.</span></span>

``` syntax
<xs:complexType name="TemplateListType">
    <xs:sequence>
        <xs:element name="template"
            type="TemplateItemType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="61145-107">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="61145-107">Child elements</span></span>



| <span data-ttu-id="61145-108">Element</span><span class="sxs-lookup"><span data-stu-id="61145-108">Element</span></span>                                                                   | <span data-ttu-id="61145-109">type</span><span class="sxs-lookup"><span data-stu-id="61145-109">Type</span></span>                                                                         | <span data-ttu-id="61145-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="61145-110">Description</span></span>                                                           |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="61145-111">**fungiert**</span><span class="sxs-lookup"><span data-stu-id="61145-111">**template**</span></span>](eventmanifestschema-template-templatelisttype-element.md) | [<span data-ttu-id="61145-112">**Templateitemtype**</span><span class="sxs-lookup"><span data-stu-id="61145-112">**TemplateItemType**</span></span>](eventmanifestschema-templateitemtype-complextype.md) | <span data-ttu-id="61145-113">Eine Vorlage, die die Daten definiert, die in einem Ereignis enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="61145-113">A template that defines the data to include with an event.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="61145-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61145-114">Requirements</span></span>



| <span data-ttu-id="61145-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61145-115">Requirement</span></span> | <span data-ttu-id="61145-116">Wert</span><span class="sxs-lookup"><span data-stu-id="61145-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="61145-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="61145-117">Minimum supported client</span></span><br/> | <span data-ttu-id="61145-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="61145-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="61145-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="61145-119">Minimum supported server</span></span><br/> | <span data-ttu-id="61145-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="61145-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





