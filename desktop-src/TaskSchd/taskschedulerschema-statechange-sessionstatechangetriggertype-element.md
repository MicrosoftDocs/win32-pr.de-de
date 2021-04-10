---
title: StateChange (sessionstatechangetriggertype)-Element
description: Enthält die Art der Sitzungs Änderung für Terminal Server, die einen Task Start auslöst.
ms.assetid: 0b17a4a5-caa7-4b58-a1a4-cbc7564838bb
keywords:
- StateChange-Element Taskplaner
topic_type:
- apiref
api_name:
- StateChange
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3991a767256184f23fbb9defda7e33465c0477e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106347"
---
# <a name="statechange-sessionstatechangetriggertype-element"></a><span data-ttu-id="b07b7-104">StateChange (sessionstatechangetriggertype)-Element</span><span class="sxs-lookup"><span data-stu-id="b07b7-104">StateChange (sessionStateChangeTriggerType) Element</span></span>

<span data-ttu-id="b07b7-105">Enthält die Art der Sitzungs Änderung für Terminal Server, die einen Task Start auslöst.</span><span class="sxs-lookup"><span data-stu-id="b07b7-105">Contains the kind of Terminal Server session change that would trigger a task launch.</span></span>

``` syntax
<xs:element name="StateChange"
    type="sessionStateChangeType"
 />
```

<span data-ttu-id="b07b7-106">Das **StateChange** -Element wird durch den komplexen Typ [**sessionstatechangetriggertype**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="b07b7-106">The **StateChange** element is defined by the [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="b07b7-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="b07b7-107">Parent element</span></span>



| <span data-ttu-id="b07b7-108">Element</span><span class="sxs-lookup"><span data-stu-id="b07b7-108">Element</span></span>                       | <span data-ttu-id="b07b7-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="b07b7-109">Derived from</span></span>                                                                                           | <span data-ttu-id="b07b7-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b07b7-110">Description</span></span>                                                                                     |
|-------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b07b7-111">**Sessionstatechange-Auslösers**</span><span class="sxs-lookup"><span data-stu-id="b07b7-111">**SessionStateChangeTrigger**</span></span> | [<span data-ttu-id="b07b7-112">**sessionstatechangetriggertype**</span><span class="sxs-lookup"><span data-stu-id="b07b7-112">**sessionStateChangeTriggerType**</span></span>](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | <span data-ttu-id="b07b7-113">Gibt einen-Endpunkt an, der einen Task startet, wenn sich der Status einer Terminal Server Sitzung ändert.</span><span class="sxs-lookup"><span data-stu-id="b07b7-113">Specifies a trigger that starts a task when a Terminal Server session changes state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b07b7-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b07b7-114">Remarks</span></span>

<span data-ttu-id="b07b7-115">Informationen zur C++-Entwicklung finden Sie unter [**StateChange-Eigenschaft von isessionstatechangelöst**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_statechange).</span><span class="sxs-lookup"><span data-stu-id="b07b7-115">For C++ development, see [**StateChange Property of ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_statechange).</span></span>

<span data-ttu-id="b07b7-116">Informationen zur Skript Entwicklung finden Sie unter [**sessionstatechange-Ereignis. StateChange**](sessionstatechangetrigger-statechange.md).</span><span class="sxs-lookup"><span data-stu-id="b07b7-116">For script development, see [**SessionStateChangeTrigger.StateChange**](sessionstatechangetrigger-statechange.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b07b7-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b07b7-117">Requirements</span></span>



| <span data-ttu-id="b07b7-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b07b7-118">Requirement</span></span> | <span data-ttu-id="b07b7-119">Wert</span><span class="sxs-lookup"><span data-stu-id="b07b7-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b07b7-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b07b7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b07b7-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b07b7-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b07b7-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b07b7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b07b7-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b07b7-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





