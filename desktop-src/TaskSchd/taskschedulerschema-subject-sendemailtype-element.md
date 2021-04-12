---
title: Subject (sendemailtype)-Element
description: Enthält den Betreff der e-Mail-Nachricht.
ms.assetid: 2ccaa983-4dca-4e45-ba8d-2a93e23f7e8c
keywords:
- Subject-Element Taskplaner
topic_type:
- apiref
api_name:
- Subject
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b3b4871f8d61603ea77c7699a9993d29e2fc0187
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519119"
---
# <a name="subject-sendemailtype-element"></a><span data-ttu-id="48a3c-104">Subject (sendemailtype)-Element</span><span class="sxs-lookup"><span data-stu-id="48a3c-104">Subject (sendEmailType) Element</span></span>

<span data-ttu-id="48a3c-105">Enthält den Betreff der e-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="48a3c-105">Contains the subject of the email message.</span></span>

``` syntax
<xs:element name="Subject"
    type="string"
 />
```

<span data-ttu-id="48a3c-106">Das **Subject** -Element wird durch den komplexen [**sendemailtype**](taskschedulerschema-sendemailtype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="48a3c-106">The **Subject** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="48a3c-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="48a3c-107">Parent element</span></span>



| <span data-ttu-id="48a3c-108">Element</span><span class="sxs-lookup"><span data-stu-id="48a3c-108">Element</span></span>                                                                              | <span data-ttu-id="48a3c-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="48a3c-109">Derived from</span></span>                                                           | <span data-ttu-id="48a3c-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48a3c-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="48a3c-111">**SendEmail (Aktionsgruppe)**</span><span class="sxs-lookup"><span data-stu-id="48a3c-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="48a3c-112">**sendemailtype**</span><span class="sxs-lookup"><span data-stu-id="48a3c-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="48a3c-113">Stellt eine Aktion dar, die eine e-Mail-Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="48a3c-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="48a3c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48a3c-114">Remarks</span></span>

<span data-ttu-id="48a3c-115">Informationen zur C++-Entwicklung finden Sie [**unter Subject-Eigenschaft von iemailaction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject).</span><span class="sxs-lookup"><span data-stu-id="48a3c-115">For C++ development, see [**Subject Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject).</span></span>

<span data-ttu-id="48a3c-116">Informationen zur Skript Entwicklung finden Sie [**unter emailaction. Subject**](emailaction-subject.md).</span><span class="sxs-lookup"><span data-stu-id="48a3c-116">For script development, see [**EmailAction.Subject**](emailaction-subject.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="48a3c-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48a3c-117">Requirements</span></span>



| <span data-ttu-id="48a3c-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48a3c-118">Requirement</span></span> | <span data-ttu-id="48a3c-119">Wert</span><span class="sxs-lookup"><span data-stu-id="48a3c-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="48a3c-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48a3c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="48a3c-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48a3c-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="48a3c-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48a3c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="48a3c-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48a3c-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





