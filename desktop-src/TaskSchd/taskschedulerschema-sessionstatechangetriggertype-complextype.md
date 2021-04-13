---
title: komplexer sessionstatechangetriggertype-Typ
description: Definiert die Elemente, die zum Erstellen eines Task Auslösers für die Konsolen Verbindung oder die Verbindung, Remote Verbindung oder Verbindung oder Arbeitsstations Sperre und-Sperre verwendet werden.
ms.assetid: 0d452476-1e1f-417d-a97a-5f39d80145f2
keywords:
- komplexer sessionstatechangetriggertype-Typ Taskplaner
topic_type:
- apiref
api_name:
- sessionStateChangeTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a8eb3ad02aef3f5bbbc078f8eafa52f3439819cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341298"
---
# <a name="sessionstatechangetriggertype-complex-type"></a><span data-ttu-id="5c969-104">komplexer sessionstatechangetriggertype-Typ</span><span class="sxs-lookup"><span data-stu-id="5c969-104">sessionStateChangeTriggerType Complex Type</span></span>

<span data-ttu-id="5c969-105">Definiert die Elemente, die zum Erstellen eines Task Auslösers für die Konsolen Verbindung oder die Verbindung, Remote Verbindung oder Verbindung oder Arbeitsstations Sperre und-Sperre verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5c969-105">Defines the elements used to create a task trigger for console connect or disconnect, remote connect or disconnect, or workstation lock or unlock notifications.</span></span>

``` syntax
<xs:complexType name="sessionStateChangeTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="UserId"
                    type="nonEmptyString"
                    minOccurs="0"
                 />
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
                <xs:element name="StateChange"
                    type="sessionStateChangeType"
                    minOccurs="1"
                    maxOccurs="1"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="5c969-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5c969-106">Child elements</span></span>



| <span data-ttu-id="5c969-107">Element</span><span class="sxs-lookup"><span data-stu-id="5c969-107">Element</span></span>                                                                                      | <span data-ttu-id="5c969-108">type</span><span class="sxs-lookup"><span data-stu-id="5c969-108">Type</span></span>                                                                                    | <span data-ttu-id="5c969-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5c969-109">Description</span></span>                                                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c969-110">**Verzögern**</span><span class="sxs-lookup"><span data-stu-id="5c969-110">**Delay**</span></span>](taskschedulerschema-delay-sessionstatechangetriggertype-element.md)             | <span data-ttu-id="5c969-111">duration</span><span class="sxs-lookup"><span data-stu-id="5c969-111">duration</span></span>                                                                                | <span data-ttu-id="5c969-112">Gibt einen Wert an, der die Länge der Verzögerung angibt, bevor ein Task gestartet wird, wenn eine Terminal Server-Sitzungs Zustandsänderung erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="5c969-112">Specifies a value that indicates the length of the delay before a task is started when a Terminal Server session state change is detected.</span></span><br/> |
| [<span data-ttu-id="5c969-113">**StateChange**</span><span class="sxs-lookup"><span data-stu-id="5c969-113">**StateChange**</span></span>](taskschedulerschema-statechange-sessionstatechangetriggertype-element.md) | [<span data-ttu-id="5c969-114">**sessionstatechangetype**</span><span class="sxs-lookup"><span data-stu-id="5c969-114">**sessionStateChangeType**</span></span>](taskschedulerschema-sessionstatechangetype-simpletype.md) | <span data-ttu-id="5c969-115">Gibt die Art der Terminal Server-Sitzungs Änderung an, die einen Task Start auslöst.</span><span class="sxs-lookup"><span data-stu-id="5c969-115">Specifies the kind of Terminal Server session change that would trigger a task launch.</span></span><br/>                                                     |
| [<span data-ttu-id="5c969-116">**UserID**</span><span class="sxs-lookup"><span data-stu-id="5c969-116">**UserId**</span></span>](taskschedulerschema-userid-sessionstatechangetriggertype-element.md)           | [<span data-ttu-id="5c969-117">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="5c969-117">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)                 | <span data-ttu-id="5c969-118">Gibt den Benutzer für die Terminal Server Sitzung an.</span><span class="sxs-lookup"><span data-stu-id="5c969-118">Specifies the user for the Terminal Server session.</span></span> <span data-ttu-id="5c969-119">Wenn eine Sitzungs Zustandsänderung für diesen Benutzer erkannt wird, wird eine Aufgabe gestartet.</span><span class="sxs-lookup"><span data-stu-id="5c969-119">When a session state change is detected for this user, a task is started.</span></span><br/>              |



## <a name="requirements"></a><span data-ttu-id="5c969-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c969-120">Requirements</span></span>



| <span data-ttu-id="5c969-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5c969-121">Requirement</span></span> | <span data-ttu-id="5c969-122">Wert</span><span class="sxs-lookup"><span data-stu-id="5c969-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5c969-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5c969-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5c969-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c969-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5c969-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5c969-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5c969-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c969-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





