---
title: Headerfields (sendemailtype)-Element
description: Gibt die Header Felder und deren Werte an, die im Header der e-Mail-Nachricht verwendet werden.
ms.assetid: 6261f32e-3012-4ce7-b407-699374596333
keywords:
- Headerfields-Element Taskplaner
topic_type:
- apiref
api_name:
- HeaderFields
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d108f1c31b8253046ccdbf09312df4f54c7335d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518191"
---
# <a name="headerfields-sendemailtype-element"></a><span data-ttu-id="d1323-104">Headerfields (sendemailtype)-Element</span><span class="sxs-lookup"><span data-stu-id="d1323-104">HeaderFields (sendEmailType) Element</span></span>

<span data-ttu-id="d1323-105">Gibt die Header Felder und deren Werte an, die im Header der e-Mail-Nachricht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d1323-105">Specifies the header fields and their values used in the header of the email message.</span></span>

``` syntax
<xs:element name="HeaderFields"
    type="headerFieldsType"
 />
```

<span data-ttu-id="d1323-106">Das **headerfields** -Element wird durch den komplexen [**sendemailtype**](taskschedulerschema-sendemailtype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="d1323-106">The **HeaderFields** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="d1323-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="d1323-107">Parent element</span></span>



| <span data-ttu-id="d1323-108">Element</span><span class="sxs-lookup"><span data-stu-id="d1323-108">Element</span></span>                                                                              | <span data-ttu-id="d1323-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="d1323-109">Derived from</span></span>                                                           | <span data-ttu-id="d1323-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d1323-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="d1323-111">**SendEmail (Aktionsgruppe)**</span><span class="sxs-lookup"><span data-stu-id="d1323-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="d1323-112">**sendemailtype**</span><span class="sxs-lookup"><span data-stu-id="d1323-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="d1323-113">Stellt eine Aktion dar, die eine e-Mail-Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="d1323-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="d1323-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d1323-114">Child elements</span></span>



| <span data-ttu-id="d1323-115">Element</span><span class="sxs-lookup"><span data-stu-id="d1323-115">Element</span></span>                                                                         | <span data-ttu-id="d1323-116">type</span><span class="sxs-lookup"><span data-stu-id="d1323-116">Type</span></span>                                                                       | <span data-ttu-id="d1323-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d1323-117">Description</span></span>                                                    |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="d1323-118">**Headerfield**</span><span class="sxs-lookup"><span data-stu-id="d1323-118">**HeaderField**</span></span>](taskschedulerschema-headerfield-headerfieldstype-element.md) | [<span data-ttu-id="d1323-119">**headerfieldtype**</span><span class="sxs-lookup"><span data-stu-id="d1323-119">**headerFieldType**</span></span>](taskschedulerschema-headerfieldtype-complextype.md) | <span data-ttu-id="d1323-120">Enthält ein Feld für einen Header in einer e-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="d1323-120">Contains a field for a header in an email message.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="d1323-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d1323-121">Remarks</span></span>

<span data-ttu-id="d1323-122">Informationen zur C++-Entwicklung finden Sie unter [**headerfields-Eigenschaft von iemailaction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields).</span><span class="sxs-lookup"><span data-stu-id="d1323-122">For C++ development, see [**HeaderFields Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields).</span></span>

<span data-ttu-id="d1323-123">Informationen zur Skript Entwicklung finden Sie unter [**emailaction. headerfields**](emailaction-headerfields.md).</span><span class="sxs-lookup"><span data-stu-id="d1323-123">For script development, see [**EmailAction.HeaderFields**](emailaction-headerfields.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d1323-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1323-124">Requirements</span></span>



| <span data-ttu-id="d1323-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1323-125">Requirement</span></span> | <span data-ttu-id="d1323-126">Wert</span><span class="sxs-lookup"><span data-stu-id="d1323-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d1323-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d1323-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d1323-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d1323-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d1323-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d1323-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d1323-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d1323-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





