---
title: Body-Element (showmessagetype)
description: Enthält den Text, der im Textkörper des Meldungs Felds angezeigt werden soll.
ms.assetid: 69ea872a-7ca1-4464-9380-b35f74c9cb8e
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
ms.openlocfilehash: 3486601153f8e9dd7dac14f83800dae00a79a9f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477469"
---
# <a name="body-showmessagetype-element"></a><span data-ttu-id="bb1c3-104">Body-Element (showmessagetype)</span><span class="sxs-lookup"><span data-stu-id="bb1c3-104">Body (showMessageType) Element</span></span>

<span data-ttu-id="bb1c3-105">Enthält den Text, der im Textkörper des Meldungs Felds angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bb1c3-105">Contains the text to display in the body of the message box.</span></span>

``` syntax
<xs:element name="Body"
    type="nonEmptyString"
 />
```

<span data-ttu-id="bb1c3-106">Das **Body** -Element wird durch den komplexen Typ " [**showmessagetype**](taskschedulerschema-showmessagetype-complextype.md) " definiert.</span><span class="sxs-lookup"><span data-stu-id="bb1c3-106">The **Body** element is defined by the [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="bb1c3-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="bb1c3-107">Parent element</span></span>



| <span data-ttu-id="bb1c3-108">Element</span><span class="sxs-lookup"><span data-stu-id="bb1c3-108">Element</span></span>                                                                                  | <span data-ttu-id="bb1c3-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="bb1c3-109">Derived from</span></span>                                                               | <span data-ttu-id="bb1c3-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bb1c3-110">Description</span></span>                                               |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="bb1c3-111">**ShowMessage (Aktionsgruppe)**</span><span class="sxs-lookup"><span data-stu-id="bb1c3-111">**ShowMessage (actionGroup)**</span></span>](taskschedulerschema-showmessage-actiongroup-element.md) | [<span data-ttu-id="bb1c3-112">**showmessagetype**</span><span class="sxs-lookup"><span data-stu-id="bb1c3-112">**showMessageType**</span></span>](taskschedulerschema-showmessagetype-complextype.md) | <span data-ttu-id="bb1c3-113">Stellt eine Aktion dar, die ein Meldungs Feld anzeigt.</span><span class="sxs-lookup"><span data-stu-id="bb1c3-113">Represents an action that shows a message box.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="bb1c3-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bb1c3-114">Remarks</span></span>

<span data-ttu-id="bb1c3-115">Informationen zur C++-Entwicklung finden Sie unter [**MessageBody-Eigenschaft von ishowmessageaction**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody).</span><span class="sxs-lookup"><span data-stu-id="bb1c3-115">For C++ development, see [**MessageBody Property of IShowMessageAction**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody).</span></span>

<span data-ttu-id="bb1c3-116">Informationen zur Skript Entwicklung finden Sie unter [**showmessageaction. MessageBody**](showmessageaction-messagebody.md).</span><span class="sxs-lookup"><span data-stu-id="bb1c3-116">For script development, see [**ShowMessageAction.MessageBody**](showmessageaction-messagebody.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bb1c3-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb1c3-117">Requirements</span></span>



| <span data-ttu-id="bb1c3-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb1c3-118">Requirement</span></span> | <span data-ttu-id="bb1c3-119">Wert</span><span class="sxs-lookup"><span data-stu-id="bb1c3-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bb1c3-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bb1c3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bb1c3-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bb1c3-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bb1c3-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bb1c3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bb1c3-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bb1c3-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





