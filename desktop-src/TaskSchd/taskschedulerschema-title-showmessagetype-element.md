---
title: Title (showmessagetype)-Element
description: Enthält den Titel des Meldungs Felds.
ms.assetid: 089d2043-41ed-4050-b794-af24ab7ac8b9
keywords:
- Title-Element Taskplaner
topic_type:
- apiref
api_name:
- Title
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca5baa7135579ff673ba9b01a672a126924d1d49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103110"
---
# <a name="title-showmessagetype-element"></a><span data-ttu-id="3f08c-104">Title (showmessagetype)-Element</span><span class="sxs-lookup"><span data-stu-id="3f08c-104">Title (showMessageType) Element</span></span>

<span data-ttu-id="3f08c-105">Enthält den Titel des Meldungs Felds.</span><span class="sxs-lookup"><span data-stu-id="3f08c-105">Contains the title of the message box.</span></span>

``` syntax
<xs:element name="Title"
    type="nonEmptyString"
 />
```

<span data-ttu-id="3f08c-106">Das **Title** -Element wird durch den komplexen Typ " [**showmessagetype**](taskschedulerschema-showmessagetype-complextype.md) " definiert.</span><span class="sxs-lookup"><span data-stu-id="3f08c-106">The **Title** element is defined by the [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="3f08c-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="3f08c-107">Parent element</span></span>



| <span data-ttu-id="3f08c-108">Element</span><span class="sxs-lookup"><span data-stu-id="3f08c-108">Element</span></span>                                                                                  | <span data-ttu-id="3f08c-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="3f08c-109">Derived from</span></span>                                                               | <span data-ttu-id="3f08c-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3f08c-110">Description</span></span>                                               |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="3f08c-111">**ShowMessage (Aktionsgruppe)**</span><span class="sxs-lookup"><span data-stu-id="3f08c-111">**ShowMessage (actionGroup)**</span></span>](taskschedulerschema-showmessage-actiongroup-element.md) | [<span data-ttu-id="3f08c-112">**showmessagetype**</span><span class="sxs-lookup"><span data-stu-id="3f08c-112">**showMessageType**</span></span>](taskschedulerschema-showmessagetype-complextype.md) | <span data-ttu-id="3f08c-113">Stellt eine Aktion dar, die ein Meldungs Feld anzeigt.</span><span class="sxs-lookup"><span data-stu-id="3f08c-113">Represents an action that shows a message box.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3f08c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3f08c-114">Remarks</span></span>

<span data-ttu-id="3f08c-115">Informationen zur C++-Entwicklung finden Sie unter [**Title-Eigenschaft von ishowmessageaction**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title).</span><span class="sxs-lookup"><span data-stu-id="3f08c-115">For C++ development, see [**Title Property of IShowMessageAction**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title).</span></span>

<span data-ttu-id="3f08c-116">Informationen zur Skript Entwicklung finden Sie unter [**showmessageaction. Title**](showmessageaction-title.md).</span><span class="sxs-lookup"><span data-stu-id="3f08c-116">For script development, see [**ShowMessageAction.Title**](showmessageaction-title.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3f08c-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3f08c-117">Requirements</span></span>



| <span data-ttu-id="3f08c-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3f08c-118">Requirement</span></span> | <span data-ttu-id="3f08c-119">Wert</span><span class="sxs-lookup"><span data-stu-id="3f08c-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3f08c-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3f08c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3f08c-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3f08c-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3f08c-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3f08c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3f08c-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3f08c-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





