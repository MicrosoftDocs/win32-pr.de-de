---
title: komplexer restarttype-Typ
description: Definiert die untergeordneten Elemente und Sequenz Informationen für das restartonfailure-Element.
ms.assetid: 3a192955-8a33-42b9-a974-faa9a3789f58
keywords:
- komplexer restarttype-Typ Taskplaner
topic_type:
- apiref
api_name:
- restartType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f83dcac376fcdd8d2059649350502111f5a732f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519127"
---
# <a name="restarttype-complex-type"></a><span data-ttu-id="78278-104">komplexer restarttype-Typ</span><span class="sxs-lookup"><span data-stu-id="78278-104">restartType Complex Type</span></span>

<span data-ttu-id="78278-105">Definiert die untergeordneten Elemente und Sequenz Informationen für das [restartonfailure](taskschedulerschema-restartonfailure-settingstype-element.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="78278-105">Defines the child elements and sequence information for the [RestartOnFailure](taskschedulerschema-restartonfailure-settingstype-element.md) element.</span></span>

``` syntax
<xs:complexType name="restartType">
    <xs:all>
        <xs:element name="Interval">
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="PT1M"
                     />
                    <xs:maxInclusive
                        value="P31D"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="Count">
            <xs:simpleType>
                <xs:restriction
                    base="unsignedByte"
                >
                    <xs:minInclusive
                        value="1"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="78278-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="78278-106">Child elements</span></span>



| <span data-ttu-id="78278-107">Element</span><span class="sxs-lookup"><span data-stu-id="78278-107">Element</span></span>                                                              | <span data-ttu-id="78278-108">type</span><span class="sxs-lookup"><span data-stu-id="78278-108">Type</span></span> | <span data-ttu-id="78278-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="78278-109">Description</span></span>                                        |
|----------------------------------------------------------------------|------|----------------------------------------------------|
| [<span data-ttu-id="78278-110">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="78278-110">**Count**</span></span>](taskschedulerschema-count-restarttype-element.md)       |      | <span data-ttu-id="78278-111">Anzahl der Versuche, den Task neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="78278-111">Number of attempts to restart the task.</span></span><br/> |
| [<span data-ttu-id="78278-112">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="78278-112">**Interval**</span></span>](taskschedulerschema-interval-restarttype-element.md) |      | <span data-ttu-id="78278-113">Gibt an, wie lange versucht wird, die Aufgabe zu starten.</span><span class="sxs-lookup"><span data-stu-id="78278-113">How long to try to start the task.</span></span><br/>      |



## <a name="requirements"></a><span data-ttu-id="78278-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78278-114">Requirements</span></span>



| <span data-ttu-id="78278-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78278-115">Requirement</span></span> | <span data-ttu-id="78278-116">Wert</span><span class="sxs-lookup"><span data-stu-id="78278-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="78278-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="78278-117">Minimum supported client</span></span><br/> | <span data-ttu-id="78278-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="78278-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="78278-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="78278-119">Minimum supported server</span></span><br/> | <span data-ttu-id="78278-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="78278-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="78278-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78278-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78278-122">Komplexe Typen von Taskplaner Schemas</span><span class="sxs-lookup"><span data-stu-id="78278-122">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="78278-123">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="78278-123">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





