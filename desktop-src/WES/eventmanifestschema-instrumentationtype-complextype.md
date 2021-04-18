---
title: Komplexer InstrumentationType-Typ
description: Definiert den Inhalt des Instrumentations Abschnitts des Manifests.
ms.assetid: dbbb978d-50dd-44c0-8bd1-3e48b41afb88
keywords:
- Instrumentierungstyp komplexer Typ EventLog
topic_type:
- apiref
api_name:
- InstrumentationType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1679ae310a996458aad3e25aba74955036094e00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340373"
---
# <a name="instrumentationtype-complex-type"></a><span data-ttu-id="ee034-104">Komplexer InstrumentationType-Typ</span><span class="sxs-lookup"><span data-stu-id="ee034-104">InstrumentationType Complex Type</span></span>

<span data-ttu-id="ee034-105">Definiert den Inhalt des Instrumentations Abschnitts des Manifests.</span><span class="sxs-lookup"><span data-stu-id="ee034-105">Defines the contents of the instrumentation section of the manifest.</span></span>

``` syntax
<xs:complexType name="InstrumentationType">
    <xs:sequence>
        <xs:element name="events"
            type="EventsType"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="ee034-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ee034-106">Child elements</span></span>



| <span data-ttu-id="ee034-107">Element</span><span class="sxs-lookup"><span data-stu-id="ee034-107">Element</span></span>                                                                  | <span data-ttu-id="ee034-108">type</span><span class="sxs-lookup"><span data-stu-id="ee034-108">Type</span></span>                                                             | <span data-ttu-id="ee034-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ee034-109">Description</span></span>                                                        |
|--------------------------------------------------------------------------|------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="ee034-110">**events**</span><span class="sxs-lookup"><span data-stu-id="ee034-110">**events**</span></span>](eventmanifestschema-events-instrumentationtype-element.md) | [<span data-ttu-id="ee034-111">**Eventstype**</span><span class="sxs-lookup"><span data-stu-id="ee034-111">**EventsType**</span></span>](eventmanifestschema-eventstype-complextype.md) | <span data-ttu-id="ee034-112">Enthält eine Liste der Anbieter, die das Manifest definiert.</span><span class="sxs-lookup"><span data-stu-id="ee034-112">Contains a list of providers that the manifest defines.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="ee034-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee034-113">Requirements</span></span>



| <span data-ttu-id="ee034-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee034-114">Requirement</span></span> | <span data-ttu-id="ee034-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ee034-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ee034-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ee034-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ee034-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ee034-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ee034-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ee034-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ee034-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ee034-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





