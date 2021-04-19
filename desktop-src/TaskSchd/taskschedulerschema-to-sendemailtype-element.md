---
title: To (sendemailtype)-Element
description: Enthält die e-Mail-Adressen, an die die e-Mail gesendet wird.
ms.assetid: bf3aa878-967b-4ebd-9397-a2a499686a9f
keywords:
- To-Element Taskplaner
topic_type:
- apiref
api_name:
- To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b9e0643220915ecb1c8f2cd1fe842e0dc3f21d8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341995"
---
# <a name="to-sendemailtype-element"></a><span data-ttu-id="68da2-104">To (sendemailtype)-Element</span><span class="sxs-lookup"><span data-stu-id="68da2-104">To (sendEmailType) Element</span></span>

<span data-ttu-id="68da2-105">Enthält die e-Mail-Adressen, an die die e-Mail gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="68da2-105">Contains the email addresses to which the email will be sent.</span></span>

``` syntax
<xs:element name="To"
    type="string"
 />
```

<span data-ttu-id="68da2-106">Das **to** -Element wird durch den komplexen [**sendemailtype**](taskschedulerschema-sendemailtype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="68da2-106">The **To** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="68da2-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="68da2-107">Parent element</span></span>



| <span data-ttu-id="68da2-108">Element</span><span class="sxs-lookup"><span data-stu-id="68da2-108">Element</span></span>                                                                              | <span data-ttu-id="68da2-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="68da2-109">Derived from</span></span>                                                           | <span data-ttu-id="68da2-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="68da2-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="68da2-111">**SendEmail (Aktionsgruppe)**</span><span class="sxs-lookup"><span data-stu-id="68da2-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="68da2-112">**sendemailtype**</span><span class="sxs-lookup"><span data-stu-id="68da2-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="68da2-113">Stellt eine Aktion dar, die eine e-Mail-Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="68da2-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="68da2-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68da2-114">Remarks</span></span>

<span data-ttu-id="68da2-115">Informationen zur C++-Entwicklung finden [**Sie unter to-Eigenschaft von iemailaction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to).</span><span class="sxs-lookup"><span data-stu-id="68da2-115">For C++ development, see [**To Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to).</span></span>

<span data-ttu-id="68da2-116">Informationen zur Skript Entwicklung finden Sie unter [**EmailAction.to**](emailaction-to.md).</span><span class="sxs-lookup"><span data-stu-id="68da2-116">For script development, see [**EmailAction.To**](emailaction-to.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="68da2-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68da2-117">Requirements</span></span>



| <span data-ttu-id="68da2-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68da2-118">Requirement</span></span> | <span data-ttu-id="68da2-119">Wert</span><span class="sxs-lookup"><span data-stu-id="68da2-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="68da2-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="68da2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="68da2-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="68da2-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="68da2-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="68da2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="68da2-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="68da2-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





