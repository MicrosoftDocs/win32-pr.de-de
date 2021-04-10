---
title: BCC (sendemailtype)-Element
description: Enthält die in der Bcc-Zeile einer e-Mail-Nachricht verwendeten e-Mail-Adressen.
ms.assetid: c80407d0-3b3f-4efe-91de-7a3a7abc996f
keywords:
- BCC-Element Taskplaner
topic_type:
- apiref
api_name:
- Bcc
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f262b8f5d74018a4622f915def85df5e16108cdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104349"
---
# <a name="bcc-sendemailtype-element"></a><span data-ttu-id="f28ec-104">BCC (sendemailtype)-Element</span><span class="sxs-lookup"><span data-stu-id="f28ec-104">Bcc (sendEmailType) Element</span></span>

<span data-ttu-id="f28ec-105">Enthält die in der Bcc-Zeile einer e-Mail-Nachricht verwendeten e-Mail-Adressen.</span><span class="sxs-lookup"><span data-stu-id="f28ec-105">Contains the email addresses used on the Bcc line of an email message.</span></span>

``` syntax
<xs:element name="Bcc"
    type="string"
 />
```

<span data-ttu-id="f28ec-106">Das **Bcc** -Element wird durch den komplexen [**sendemailtype**](taskschedulerschema-sendemailtype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="f28ec-106">The **Bcc** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f28ec-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="f28ec-107">Parent element</span></span>



| <span data-ttu-id="f28ec-108">Element</span><span class="sxs-lookup"><span data-stu-id="f28ec-108">Element</span></span>                                                                              | <span data-ttu-id="f28ec-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="f28ec-109">Derived from</span></span>                                                           | <span data-ttu-id="f28ec-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f28ec-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="f28ec-111">**SendEmail (Aktionsgruppe)**</span><span class="sxs-lookup"><span data-stu-id="f28ec-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="f28ec-112">**sendemailtype**</span><span class="sxs-lookup"><span data-stu-id="f28ec-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="f28ec-113">Stellt eine Aktion dar, die eine e-Mail-Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="f28ec-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f28ec-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f28ec-114">Remarks</span></span>

<span data-ttu-id="f28ec-115">Informationen zur C++-Entwicklung finden Sie unter [**Bcc-Eigenschaft von iemailaction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc).</span><span class="sxs-lookup"><span data-stu-id="f28ec-115">For C++ development, see [**Bcc Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc).</span></span>

<span data-ttu-id="f28ec-116">Informationen zur Skript Entwicklung finden Sie unter [**emailaction. BCC**](emailaction-bcc.md).</span><span class="sxs-lookup"><span data-stu-id="f28ec-116">For script development, see [**EmailAction.Bcc**](emailaction-bcc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f28ec-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f28ec-117">Requirements</span></span>



| <span data-ttu-id="f28ec-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f28ec-118">Requirement</span></span> | <span data-ttu-id="f28ec-119">Wert</span><span class="sxs-lookup"><span data-stu-id="f28ec-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f28ec-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f28ec-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f28ec-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f28ec-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f28ec-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f28ec-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f28ec-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f28ec-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





