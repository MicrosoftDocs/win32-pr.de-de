---
title: komplexer showmessagetype-Typ
description: Definiert die Elemente, die eine Aktion darstellen, die ein Meldungs Feld anzeigt.
ms.assetid: eb841d9f-0be2-433b-9002-5e41c6ee78f9
keywords:
- komplexer showmessagetype-Typ Taskplaner
topic_type:
- apiref
api_name:
- showMessageType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d65ed893bce63c95fffcf237d3a3a95ebb1550d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956760"
---
# <a name="showmessagetype-complex-type"></a><span data-ttu-id="a9f32-104">komplexer showmessagetype-Typ</span><span class="sxs-lookup"><span data-stu-id="a9f32-104">showMessageType Complex Type</span></span>

<span data-ttu-id="a9f32-105">Definiert die Elemente, die eine Aktion darstellen, die ein Meldungs Feld anzeigt.</span><span class="sxs-lookup"><span data-stu-id="a9f32-105">Defines the elements that represent an action that shows a message box.</span></span>

``` syntax
<xs:complexType name="showMessageType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Title"
                    type="nonEmptyString"
                 />
                <xs:element name="Body"
                    type="nonEmptyString"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="a9f32-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a9f32-106">Child elements</span></span>



| <span data-ttu-id="a9f32-107">Element</span><span class="sxs-lookup"><span data-stu-id="a9f32-107">Element</span></span>                                                            | <span data-ttu-id="a9f32-108">type</span><span class="sxs-lookup"><span data-stu-id="a9f32-108">Type</span></span>           | <span data-ttu-id="a9f32-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a9f32-109">Description</span></span>                                                               |
|--------------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="a9f32-110">**Text**</span><span class="sxs-lookup"><span data-stu-id="a9f32-110">**Body**</span></span>](taskschedulerschema-body-showmessagetype-element.md)   | <span data-ttu-id="a9f32-111">nonEmptyString</span><span class="sxs-lookup"><span data-stu-id="a9f32-111">nonEmptyString</span></span> | <span data-ttu-id="a9f32-112">Gibt den Text an, der im Textkörper des Meldungs Felds angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a9f32-112">Specifies the text to display in the body of the message box.</span></span> <br/> |
| [<span data-ttu-id="a9f32-113">**Titel**</span><span class="sxs-lookup"><span data-stu-id="a9f32-113">**Title**</span></span>](taskschedulerschema-title-showmessagetype-element.md) | <span data-ttu-id="a9f32-114">nonEmptyString</span><span class="sxs-lookup"><span data-stu-id="a9f32-114">nonEmptyString</span></span> | <span data-ttu-id="a9f32-115">Gibt den Titel des Meldungs Felds an.</span><span class="sxs-lookup"><span data-stu-id="a9f32-115">Specifies the title of the message box.</span></span> <br/>                       |



## <a name="requirements"></a><span data-ttu-id="a9f32-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9f32-116">Requirements</span></span>



| <span data-ttu-id="a9f32-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a9f32-117">Requirement</span></span> | <span data-ttu-id="a9f32-118">Wert</span><span class="sxs-lookup"><span data-stu-id="a9f32-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a9f32-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a9f32-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a9f32-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9f32-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a9f32-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a9f32-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a9f32-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9f32-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





