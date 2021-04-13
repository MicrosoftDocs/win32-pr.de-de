---
title: Server (sendemailtype)-Element
description: Enthält den e-Mail-Server zum Senden der e-Mail-Nachricht.
ms.assetid: 4c6084d1-70c5-4d8b-8fcb-ab4cd8aab441
keywords:
- Server-Element Taskplaner
topic_type:
- apiref
api_name:
- Server
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5fc57ddf5deee52ff9b118a8267eec4069108030
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391631"
---
# <a name="server-sendemailtype-element"></a><span data-ttu-id="ac8cf-104">Server (sendemailtype)-Element</span><span class="sxs-lookup"><span data-stu-id="ac8cf-104">Server (sendEmailType) Element</span></span>

<span data-ttu-id="ac8cf-105">Enthält den e-Mail-Server zum Senden der e-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="ac8cf-105">Contains the email server used to send the email message.</span></span>

``` syntax
<xs:element name="Server"
    type="nonEmptyString"
 />
```

<span data-ttu-id="ac8cf-106">Das **Server** -Element wird durch den komplexen [**sendemailtype**](taskschedulerschema-sendemailtype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="ac8cf-106">The **Server** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ac8cf-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="ac8cf-107">Parent element</span></span>



| <span data-ttu-id="ac8cf-108">Element</span><span class="sxs-lookup"><span data-stu-id="ac8cf-108">Element</span></span>                                                                              | <span data-ttu-id="ac8cf-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="ac8cf-109">Derived from</span></span>                                                           | <span data-ttu-id="ac8cf-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ac8cf-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="ac8cf-111">**SendEmail (Aktionsgruppe)**</span><span class="sxs-lookup"><span data-stu-id="ac8cf-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="ac8cf-112">**sendemailtype**</span><span class="sxs-lookup"><span data-stu-id="ac8cf-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="ac8cf-113">Stellt eine Aktion dar, die eine e-Mail-Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="ac8cf-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ac8cf-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac8cf-114">Remarks</span></span>

<span data-ttu-id="ac8cf-115">Informationen zur C++-Entwicklung finden Sie unter [**Server-Eigenschaft von iemailaction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server).</span><span class="sxs-lookup"><span data-stu-id="ac8cf-115">For C++ development, see [**Server Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server).</span></span>

<span data-ttu-id="ac8cf-116">Informationen zur Skript Entwicklung finden Sie unter [**emailaction. Server**](emailaction-server.md).</span><span class="sxs-lookup"><span data-stu-id="ac8cf-116">For script development, see [**EmailAction.Server**](emailaction-server.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ac8cf-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac8cf-117">Requirements</span></span>



| <span data-ttu-id="ac8cf-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac8cf-118">Requirement</span></span> | <span data-ttu-id="ac8cf-119">Wert</span><span class="sxs-lookup"><span data-stu-id="ac8cf-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ac8cf-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ac8cf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ac8cf-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac8cf-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ac8cf-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ac8cf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ac8cf-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac8cf-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





