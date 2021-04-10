---
title: From (sendemailtype)-Element
description: Enthält die e-Mail-Adresse des Absenders der e-Mail.
ms.assetid: b80733de-e050-4026-a2fe-f63833ec2660
keywords:
- From-Element Taskplaner
topic_type:
- apiref
api_name:
- From
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9f50704212fe6a4fec7ce0fc21bacd7ea33e402c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040394"
---
# <a name="from-sendemailtype-element"></a><span data-ttu-id="4b046-104">From (sendemailtype)-Element</span><span class="sxs-lookup"><span data-stu-id="4b046-104">From (sendEmailType) Element</span></span>

<span data-ttu-id="4b046-105">Enthält die e-Mail-Adresse des Absenders der e-Mail.</span><span class="sxs-lookup"><span data-stu-id="4b046-105">Contains the email address of the email sender.</span></span>

``` syntax
<xs:element name="From"
    type="string"
 />
```

<span data-ttu-id="4b046-106">Das **from** -Element wird durch den komplexen [**sendemailtype**](taskschedulerschema-sendemailtype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="4b046-106">The **From** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="4b046-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="4b046-107">Parent element</span></span>



| <span data-ttu-id="4b046-108">Element</span><span class="sxs-lookup"><span data-stu-id="4b046-108">Element</span></span>                                                                              | <span data-ttu-id="4b046-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="4b046-109">Derived from</span></span>                                                           | <span data-ttu-id="4b046-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b046-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="4b046-111">**SendEmail (Aktionsgruppe)**</span><span class="sxs-lookup"><span data-stu-id="4b046-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="4b046-112">**sendemailtype**</span><span class="sxs-lookup"><span data-stu-id="4b046-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="4b046-113">Stellt eine Aktion dar, die eine e-Mail-Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="4b046-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4b046-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4b046-114">Remarks</span></span>

<span data-ttu-id="4b046-115">Informationen zur C++-Entwicklung finden Sie unter [**From-Eigenschaft von iemailaction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from).</span><span class="sxs-lookup"><span data-stu-id="4b046-115">For C++ development, see [**From Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from).</span></span>

<span data-ttu-id="4b046-116">Informationen zur Skript Entwicklung finden Sie unter [**emailaction. from**](emailaction-from.md).</span><span class="sxs-lookup"><span data-stu-id="4b046-116">For script development, see [**EmailAction.From**](emailaction-from.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4b046-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b046-117">Requirements</span></span>



| <span data-ttu-id="4b046-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4b046-118">Requirement</span></span> | <span data-ttu-id="4b046-119">Wert</span><span class="sxs-lookup"><span data-stu-id="4b046-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4b046-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4b046-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4b046-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4b046-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4b046-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4b046-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4b046-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4b046-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





