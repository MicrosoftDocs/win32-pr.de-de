---
title: Security-Element (systempropertiestype)
description: Identifiziert den Benutzer, der das Ereignis protokolliert hat.
ms.assetid: f421b0c3-96ea-440c-a3b2-0ddd8f327eec
keywords:
- Sicherheitselement-Ereignisprotokoll
topic_type:
- apiref
api_name:
- Security
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b793193d7afdfde5fd515252a024432ed45ff8b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105795"
---
# <a name="security-systempropertiestype-element"></a><span data-ttu-id="eda83-104">Security-Element (systempropertiestype)</span><span class="sxs-lookup"><span data-stu-id="eda83-104">Security (SystemPropertiesType) Element</span></span>

<span data-ttu-id="eda83-105">Identifiziert den Benutzer, der das Ereignis protokolliert hat.</span><span class="sxs-lookup"><span data-stu-id="eda83-105">Identifies the user that logged the event.</span></span>

``` syntax
<xs:element name="Security">
    <xs:complexType>
        <xs:attribute name="UserID"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="eda83-106">Das **Security** -Element wird durch den komplexen [**systempropertiestype**](eventschema-systempropertiestype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="eda83-106">The **Security** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="eda83-107">Attributes</span><span class="sxs-lookup"><span data-stu-id="eda83-107">Attributes</span></span>



| <span data-ttu-id="eda83-108">Name</span><span class="sxs-lookup"><span data-stu-id="eda83-108">Name</span></span>   | <span data-ttu-id="eda83-109">type</span><span class="sxs-lookup"><span data-stu-id="eda83-109">Type</span></span>   | <span data-ttu-id="eda83-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eda83-110">Description</span></span>                                                          |
|--------|--------|----------------------------------------------------------------------|
| <span data-ttu-id="eda83-111">UserID</span><span class="sxs-lookup"><span data-stu-id="eda83-111">UserID</span></span> | <span data-ttu-id="eda83-112">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="eda83-112">string</span></span> | <span data-ttu-id="eda83-113">Die Sicherheits-ID (SID) des Benutzers in Form einer Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="eda83-113">The security identifier (SID) of the user in string form.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="eda83-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eda83-114">Requirements</span></span>



| <span data-ttu-id="eda83-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eda83-115">Requirement</span></span> | <span data-ttu-id="eda83-116">Wert</span><span class="sxs-lookup"><span data-stu-id="eda83-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="eda83-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eda83-117">Minimum supported client</span></span><br/> | <span data-ttu-id="eda83-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eda83-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="eda83-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eda83-119">Minimum supported server</span></span><br/> | <span data-ttu-id="eda83-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eda83-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eda83-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eda83-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="eda83-122">**Übergeordnetes Element**</span><span class="sxs-lookup"><span data-stu-id="eda83-122">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="eda83-123">**System (EventType)**</span><span class="sxs-lookup"><span data-stu-id="eda83-123">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





