---
title: Body (sendemailtype)-Element
description: Enthält den Text im Textkörper der e-Mail-Nachricht.
ms.assetid: fac6ddd5-6f73-427b-b213-ab946512c87a
keywords:
- Body-Element Taskplaner
topic_type:
- apiref
api_name:
- Body
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4659f2ff03f69b6bba40d9cd16e9b68515cc8889
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339341"
---
# <a name="body-sendemailtype-element"></a><span data-ttu-id="ffa97-104">Body (sendemailtype)-Element</span><span class="sxs-lookup"><span data-stu-id="ffa97-104">Body (sendEmailType) Element</span></span>

<span data-ttu-id="ffa97-105">Enthält den Text im Textkörper der e-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="ffa97-105">Contains the text in the body of the email message.</span></span>

``` syntax
<xs:element name="Body"
    type="string"
 />
```

<span data-ttu-id="ffa97-106">Das **Body** -Element wird durch den komplexen [**sendemailtype**](taskschedulerschema-sendemailtype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="ffa97-106">The **Body** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ffa97-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="ffa97-107">Parent element</span></span>



| <span data-ttu-id="ffa97-108">Element</span><span class="sxs-lookup"><span data-stu-id="ffa97-108">Element</span></span>                                                                              | <span data-ttu-id="ffa97-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="ffa97-109">Derived from</span></span>                                                           | <span data-ttu-id="ffa97-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ffa97-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="ffa97-111">**SendEmail (Aktionsgruppe)**</span><span class="sxs-lookup"><span data-stu-id="ffa97-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="ffa97-112">**sendemailtype**</span><span class="sxs-lookup"><span data-stu-id="ffa97-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="ffa97-113">Stellt eine Aktion dar, die eine e-Mail-Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="ffa97-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ffa97-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ffa97-114">Remarks</span></span>

<span data-ttu-id="ffa97-115">Informationen zur C++-Entwicklung finden Sie unter [**Text-Eigenschaft von iemailaction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body).</span><span class="sxs-lookup"><span data-stu-id="ffa97-115">For C++ development, see [**Body Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body).</span></span>

<span data-ttu-id="ffa97-116">Informationen zur Skript Entwicklung finden Sie unter [**emailaction. Body**](emailaction-body.md).</span><span class="sxs-lookup"><span data-stu-id="ffa97-116">For script development, see [**EmailAction.Body**](emailaction-body.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ffa97-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ffa97-117">Requirements</span></span>



| <span data-ttu-id="ffa97-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ffa97-118">Requirement</span></span> | <span data-ttu-id="ffa97-119">Wert</span><span class="sxs-lookup"><span data-stu-id="ffa97-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ffa97-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ffa97-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ffa97-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ffa97-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ffa97-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ffa97-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ffa97-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ffa97-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





