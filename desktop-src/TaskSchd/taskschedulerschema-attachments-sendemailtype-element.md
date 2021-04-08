---
title: Anhänge (sendemailtype)-Element
description: Enthält eine Liste der Anlagen in der e-Mail-Nachricht.
ms.assetid: 5ae22481-af70-42eb-a964-e63d800be17d
keywords:
- Anhänge-Element Taskplaner
topic_type:
- apiref
api_name:
- Attachments
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 67eed8f82f0caa27f44070bd109d4fa4560472eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742769"
---
# <a name="attachments-sendemailtype-element"></a><span data-ttu-id="3ec7d-104">Anhänge (sendemailtype)-Element</span><span class="sxs-lookup"><span data-stu-id="3ec7d-104">Attachments (sendEmailType) Element</span></span>

<span data-ttu-id="3ec7d-105">Enthält eine Liste der Anlagen in der e-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="3ec7d-105">Contains a list of attachments in the email message.</span></span>

``` syntax
<xs:element name="Attachments"
    type="attachmentsType"
 />
```

<span data-ttu-id="3ec7d-106">Das **Anhänge** -Element wird durch den komplexen [**sendemailtype**](taskschedulerschema-sendemailtype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="3ec7d-106">The **Attachments** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="3ec7d-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="3ec7d-107">Parent element</span></span>



| <span data-ttu-id="3ec7d-108">Element</span><span class="sxs-lookup"><span data-stu-id="3ec7d-108">Element</span></span>                                                                              | <span data-ttu-id="3ec7d-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="3ec7d-109">Derived from</span></span>                                                           | <span data-ttu-id="3ec7d-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3ec7d-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="3ec7d-111">**SendEmail (Aktionsgruppe)**</span><span class="sxs-lookup"><span data-stu-id="3ec7d-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="3ec7d-112">**sendemailtype**</span><span class="sxs-lookup"><span data-stu-id="3ec7d-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="3ec7d-113">Stellt eine Aktion dar, die eine e-Mail-Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="3ec7d-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="3ec7d-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3ec7d-114">Child elements</span></span>



| <span data-ttu-id="3ec7d-115">Element</span><span class="sxs-lookup"><span data-stu-id="3ec7d-115">Element</span></span>                                                          | <span data-ttu-id="3ec7d-116">type</span><span class="sxs-lookup"><span data-stu-id="3ec7d-116">Type</span></span>                                                                    | <span data-ttu-id="3ec7d-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3ec7d-117">Description</span></span>                                                                                |
|------------------------------------------------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3ec7d-118">**Datei**</span><span class="sxs-lookup"><span data-stu-id="3ec7d-118">**File**</span></span>](taskschedulerschema-file-attachmentstype-element.md) | [<span data-ttu-id="3ec7d-119">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="3ec7d-119">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="3ec7d-120">Gibt den Pfad zu einer Datei an, die als Anlage in einer e-Mail-Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="3ec7d-120">Specifies the path to a file that is sent as an attachment in an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3ec7d-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3ec7d-121">Remarks</span></span>

<span data-ttu-id="3ec7d-122">Informationen zur C++-Entwicklung finden Sie unter [**der Eigenschaft "Anhänge" von iemailaction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).</span><span class="sxs-lookup"><span data-stu-id="3ec7d-122">For C++ development, see [**Attachments Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).</span></span>

<span data-ttu-id="3ec7d-123">Informationen zur Skript Entwicklung finden Sie unter [**emailaction. Anhänge**](emailaction-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="3ec7d-123">For script development, see [**EmailAction.Attachments**](emailaction-attachments.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3ec7d-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3ec7d-124">Requirements</span></span>



| <span data-ttu-id="3ec7d-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3ec7d-125">Requirement</span></span> | <span data-ttu-id="3ec7d-126">Wert</span><span class="sxs-lookup"><span data-stu-id="3ec7d-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3ec7d-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3ec7d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3ec7d-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3ec7d-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3ec7d-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3ec7d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3ec7d-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3ec7d-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





