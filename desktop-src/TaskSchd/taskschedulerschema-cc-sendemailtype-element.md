---
title: CC (sendemailtype)-Element
description: Enthält die in der CC-Zeile einer e-Mail-Nachricht verwendeten e-Mail-Adressen.
ms.assetid: cb8bc5b3-c352-43e3-bf28-d2090a519c7f
keywords:
- CC-Element Taskplaner
topic_type:
- apiref
api_name:
- Cc
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0bc49f2d7eebc2fbb1b5818fee2efa0e54f579a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477793"
---
# <a name="cc-sendemailtype-element"></a><span data-ttu-id="d131b-104">CC (sendemailtype)-Element</span><span class="sxs-lookup"><span data-stu-id="d131b-104">Cc (sendEmailType) Element</span></span>

<span data-ttu-id="d131b-105">Enthält die in der CC-Zeile einer e-Mail-Nachricht verwendeten e-Mail-Adressen.</span><span class="sxs-lookup"><span data-stu-id="d131b-105">Contains the email addresses used on the Cc line of an email message.</span></span>

``` syntax
<xs:element name="Cc"
    type="string"
 />
```

<span data-ttu-id="d131b-106">Das **CC** -Element wird durch den komplexen [**sendemailtype**](taskschedulerschema-sendemailtype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="d131b-106">The **Cc** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="d131b-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="d131b-107">Parent element</span></span>



| <span data-ttu-id="d131b-108">Element</span><span class="sxs-lookup"><span data-stu-id="d131b-108">Element</span></span>                                                                              | <span data-ttu-id="d131b-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="d131b-109">Derived from</span></span>                                                           | <span data-ttu-id="d131b-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d131b-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="d131b-111">**SendEmail (Aktionsgruppe)**</span><span class="sxs-lookup"><span data-stu-id="d131b-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="d131b-112">**sendemailtype**</span><span class="sxs-lookup"><span data-stu-id="d131b-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="d131b-113">Stellt eine Aktion dar, die eine e-Mail-Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="d131b-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d131b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d131b-114">Remarks</span></span>

<span data-ttu-id="d131b-115">Informationen zur C++-Entwicklung finden Sie unter [**der CC-Eigenschaft von iemailaction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc).</span><span class="sxs-lookup"><span data-stu-id="d131b-115">For C++ development, see [**Cc Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc).</span></span>

<span data-ttu-id="d131b-116">Informationen zur Skript Entwicklung finden Sie unter [**EmailAction.CC**](emailaction-cc.md).</span><span class="sxs-lookup"><span data-stu-id="d131b-116">For script development, see [**EmailAction.Cc**](emailaction-cc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d131b-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d131b-117">Requirements</span></span>



| <span data-ttu-id="d131b-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d131b-118">Requirement</span></span> | <span data-ttu-id="d131b-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d131b-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d131b-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d131b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d131b-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d131b-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d131b-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d131b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d131b-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d131b-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





