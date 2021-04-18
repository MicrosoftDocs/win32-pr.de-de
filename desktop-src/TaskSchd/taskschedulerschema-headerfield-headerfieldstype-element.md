---
title: Headerfield (headerfieldstype)-Element
description: Enthält ein Feld für einen Header in einer e-Mail-Nachricht.
ms.assetid: ec6fc593-8798-4dd0-b589-48657b7cdeb1
keywords:
- Headerfield-Element Taskplaner
topic_type:
- apiref
api_name:
- HeaderField
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f7ac79a16bb0464f6e81d90eba38384a3c2b483
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341041"
---
# <a name="headerfield-headerfieldstype-element"></a><span data-ttu-id="f0a42-104">Headerfield (headerfieldstype)-Element</span><span class="sxs-lookup"><span data-stu-id="f0a42-104">HeaderField (headerFieldsType) Element</span></span>

<span data-ttu-id="f0a42-105">Enthält ein Feld für einen Header in einer e-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="f0a42-105">Contains a field for a header in an email message.</span></span>

``` syntax
<xs:element name="HeaderField"
    type="headerFieldType"
 />
```

<span data-ttu-id="f0a42-106">Das **headerfield** -Element wird durch den komplexen [**headerfieldstype**](taskschedulerschema-headerfieldstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="f0a42-106">The **HeaderField** element is defined by the [**headerFieldsType**](taskschedulerschema-headerfieldstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f0a42-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="f0a42-107">Parent element</span></span>



| <span data-ttu-id="f0a42-108">Element</span><span class="sxs-lookup"><span data-stu-id="f0a42-108">Element</span></span>                                                                        | <span data-ttu-id="f0a42-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="f0a42-109">Derived from</span></span>                                                                 | <span data-ttu-id="f0a42-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f0a42-110">Description</span></span>                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f0a42-111">**Headerfields**</span><span class="sxs-lookup"><span data-stu-id="f0a42-111">**HeaderFields**</span></span>](taskschedulerschema-headerfields-sendemailtype-element.md) | [<span data-ttu-id="f0a42-112">**headerfieldstype**</span><span class="sxs-lookup"><span data-stu-id="f0a42-112">**headerFieldsType**</span></span>](taskschedulerschema-headerfieldstype-complextype.md) | <span data-ttu-id="f0a42-113">Gibt die Header Felder und deren Werte an, die im Header der e-Mail-Nachricht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f0a42-113">Specifies the header fields and their values used in the header of the email message.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="f0a42-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f0a42-114">Child elements</span></span>



| <span data-ttu-id="f0a42-115">Element</span><span class="sxs-lookup"><span data-stu-id="f0a42-115">Element</span></span>                                                            | <span data-ttu-id="f0a42-116">type</span><span class="sxs-lookup"><span data-stu-id="f0a42-116">Type</span></span>                                                                    | <span data-ttu-id="f0a42-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f0a42-117">Description</span></span>                                                            |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="f0a42-118">**Name**</span><span class="sxs-lookup"><span data-stu-id="f0a42-118">**Name**</span></span>](taskschedulerschema-name-headerfieldtype-element.md)   | [<span data-ttu-id="f0a42-119">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="f0a42-119">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="f0a42-120">Gibt den Namen des Header Felds in einer e-Mail-Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="f0a42-120">Specifies the name of the header field in an email message.</span></span><br/> |
| [<span data-ttu-id="f0a42-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="f0a42-121">**Value**</span></span>](taskschedulerschema-value-headerfieldtype-element.md) | <span data-ttu-id="f0a42-122">**string**</span><span class="sxs-lookup"><span data-stu-id="f0a42-122">**string**</span></span>                                                              | <span data-ttu-id="f0a42-123">Gibt den Wert eines Header Felds in einer e-Mail-Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="f0a42-123">Specifies the value of a header field in an email message.</span></span><br/>  |



## <a name="remarks"></a><span data-ttu-id="f0a42-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f0a42-124">Remarks</span></span>

<span data-ttu-id="f0a42-125">Informationen zur C++-Entwicklung finden Sie unter [**headerfields-Eigenschaft von iemailaction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields).</span><span class="sxs-lookup"><span data-stu-id="f0a42-125">For C++ development, see [**HeaderFields Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields).</span></span>

<span data-ttu-id="f0a42-126">Informationen zur Skript Entwicklung finden Sie unter [**emailaction. headerfields**](emailaction-headerfields.md).</span><span class="sxs-lookup"><span data-stu-id="f0a42-126">For script development, see [**EmailAction.HeaderFields**](emailaction-headerfields.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f0a42-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0a42-127">Requirements</span></span>



| <span data-ttu-id="f0a42-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0a42-128">Requirement</span></span> | <span data-ttu-id="f0a42-129">Wert</span><span class="sxs-lookup"><span data-stu-id="f0a42-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f0a42-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f0a42-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f0a42-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0a42-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f0a42-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f0a42-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f0a42-133">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0a42-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





