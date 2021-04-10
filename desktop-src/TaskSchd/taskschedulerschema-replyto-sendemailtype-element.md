---
title: ReplyTo (sendemailtype)-Element
description: Enthält die e-Mail-Adressen, die in der e-Mail-Nachricht beantwortet werden.
ms.assetid: c09b72f6-de2c-41dc-942c-d6184863e33c
keywords:
- ReplyTo-Element Taskplaner
topic_type:
- apiref
api_name:
- ReplyTo
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 02055539d4557a60f182981f0d9cd7d3e1a63ca4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106358"
---
# <a name="replyto-sendemailtype-element"></a><span data-ttu-id="1b1d4-104">ReplyTo (sendemailtype)-Element</span><span class="sxs-lookup"><span data-stu-id="1b1d4-104">ReplyTo (sendEmailType) Element</span></span>

<span data-ttu-id="1b1d4-105">Enthält die e-Mail-Adressen, die in der e-Mail-Nachricht beantwortet werden.</span><span class="sxs-lookup"><span data-stu-id="1b1d4-105">Contains the email addresses that are replied to in the email message.</span></span>

``` syntax
<xs:element name="ReplyTo"
    type="string"
 />
```

<span data-ttu-id="1b1d4-106">Das **ReplyTo** -Element wird durch den komplexen [**sendemailtype**](taskschedulerschema-sendemailtype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="1b1d4-106">The **ReplyTo** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="1b1d4-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="1b1d4-107">Parent element</span></span>



| <span data-ttu-id="1b1d4-108">Element</span><span class="sxs-lookup"><span data-stu-id="1b1d4-108">Element</span></span>                                                                              | <span data-ttu-id="1b1d4-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="1b1d4-109">Derived from</span></span>                                                           | <span data-ttu-id="1b1d4-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1b1d4-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="1b1d4-111">**SendEmail (Aktionsgruppe)**</span><span class="sxs-lookup"><span data-stu-id="1b1d4-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="1b1d4-112">**sendemailtype**</span><span class="sxs-lookup"><span data-stu-id="1b1d4-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="1b1d4-113">Stellt eine Aktion dar, die eine e-Mail-Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="1b1d4-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1b1d4-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b1d4-114">Remarks</span></span>

<span data-ttu-id="1b1d4-115">Informationen zur C++-Entwicklung finden [**Sie unter ReplyTo-Eigenschaft von iemailaction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto).</span><span class="sxs-lookup"><span data-stu-id="1b1d4-115">For C++ development, see [**ReplyTo Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto).</span></span>

<span data-ttu-id="1b1d4-116">Informationen zur Skript Entwicklung finden [**Sie unter emailaction. ReplyTo**](emailaction-replyto.md).</span><span class="sxs-lookup"><span data-stu-id="1b1d4-116">For script development, see [**EmailAction.ReplyTo**](emailaction-replyto.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1b1d4-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b1d4-117">Requirements</span></span>



| <span data-ttu-id="1b1d4-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b1d4-118">Requirement</span></span> | <span data-ttu-id="1b1d4-119">Wert</span><span class="sxs-lookup"><span data-stu-id="1b1d4-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1b1d4-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1b1d4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1b1d4-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b1d4-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1b1d4-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1b1d4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1b1d4-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b1d4-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





