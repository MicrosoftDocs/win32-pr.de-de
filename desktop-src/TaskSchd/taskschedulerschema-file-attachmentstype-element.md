---
title: File (attachmentstype)-Element
description: Enthält den Pfad zu einer Datei, die in einer e-Mail-Nachricht als Anlage gesendet wurde.
ms.assetid: a53f591b-ac59-43b4-8cc2-661e76d307cc
keywords:
- File-Element Taskplaner
topic_type:
- apiref
api_name:
- File
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ed07d4b31f9054f6caefcff0585d9683faa90c7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391764"
---
# <a name="file-attachmentstype-element"></a><span data-ttu-id="48924-104">File (attachmentstype)-Element</span><span class="sxs-lookup"><span data-stu-id="48924-104">File (attachmentsType) Element</span></span>

<span data-ttu-id="48924-105">Enthält den Pfad zu einer Datei, die in einer e-Mail-Nachricht als Anlage gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="48924-105">Contains the path to a file sent as an attachment in an email message.</span></span>

``` syntax
<xs:element name="File"
    type="nonEmptyString"
 />
```

<span data-ttu-id="48924-106">Das **File** -Element wird durch den komplexen [**attachmentstype**](taskschedulerschema-attachmentstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="48924-106">The **File** element is defined by the [**attachmentsType**](taskschedulerschema-attachmentstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="48924-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="48924-107">Parent element</span></span>



| <span data-ttu-id="48924-108">Element</span><span class="sxs-lookup"><span data-stu-id="48924-108">Element</span></span>                                                                                      | <span data-ttu-id="48924-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="48924-109">Derived from</span></span>                                                               | <span data-ttu-id="48924-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48924-110">Description</span></span>                                                     |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="48924-111">**Anlagen (sendemailtype)**</span><span class="sxs-lookup"><span data-stu-id="48924-111">**Attachments (sendEmailType)**</span></span>](taskschedulerschema-attachments-sendemailtype-element.md) | [<span data-ttu-id="48924-112">**attachmentstype**</span><span class="sxs-lookup"><span data-stu-id="48924-112">**attachmentsType**</span></span>](taskschedulerschema-attachmentstype-complextype.md) | <span data-ttu-id="48924-113">Enthält eine Liste der Anlagen in der e-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="48924-113">Contains a list of attachments in the email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="48924-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48924-114">Remarks</span></span>

<span data-ttu-id="48924-115">Informationen zur C++-Entwicklung finden Sie unter [**der Eigenschaft "Anhänge" von iemailaction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).</span><span class="sxs-lookup"><span data-stu-id="48924-115">For C++ development, see [**Attachments Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).</span></span>

<span data-ttu-id="48924-116">Informationen zur Skript Entwicklung finden Sie unter [**emailaction. Anhänge**](emailaction-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="48924-116">For script development, see [**EmailAction.Attachments**](emailaction-attachments.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="48924-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48924-117">Requirements</span></span>



| <span data-ttu-id="48924-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48924-118">Requirement</span></span> | <span data-ttu-id="48924-119">Wert</span><span class="sxs-lookup"><span data-stu-id="48924-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="48924-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48924-120">Minimum supported client</span></span><br/> | <span data-ttu-id="48924-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48924-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="48924-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48924-122">Minimum supported server</span></span><br/> | <span data-ttu-id="48924-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48924-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





