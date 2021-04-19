---
description: Verwaltet die Seite der Anwendung der automatischen vollständigen Integration des Text Eingabe Bereichs.
ms.assetid: 02601258-d867-4c01-b094-bf9ff96d2f6e
title: Itipauescompleteprovider-Schnittstelle (tipauabcomplete. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 3c300e2724ccabbc8388ef647f8f0145531cfc8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355440"
---
# <a name="itipautocompleteprovider-interface"></a><span data-ttu-id="449a2-103">Itipauescompleteprovider-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="449a2-103">ITipAutocompleteProvider interface</span></span>

<span data-ttu-id="449a2-104">Verwaltet die Seite der Anwendung der automatischen vollständigen Integration des Text Eingabe Bereichs.</span><span class="sxs-lookup"><span data-stu-id="449a2-104">Manages the application's side of the Text Input Panel auto complete integration.</span></span>

## <a name="members"></a><span data-ttu-id="449a2-105">Member</span><span class="sxs-lookup"><span data-stu-id="449a2-105">Members</span></span>

<span data-ttu-id="449a2-106">Die **itipauescompleteprovider** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="449a2-106">The **ITipAutocompleteProvider** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="449a2-107">**Itipautocompleteprovider** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="449a2-107">**ITipAutocompleteProvider** also has these types of members:</span></span>

-   [<span data-ttu-id="449a2-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="449a2-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="449a2-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="449a2-109">Methods</span></span>

<span data-ttu-id="449a2-110">Die **itipaudecompleteprovider** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="449a2-110">The **ITipAutocompleteProvider** interface has these methods.</span></span>



| <span data-ttu-id="449a2-111">Methode</span><span class="sxs-lookup"><span data-stu-id="449a2-111">Method</span></span>                                                                  | <span data-ttu-id="449a2-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="449a2-112">Description</span></span>                                                                                                          |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="449a2-113">**Auftritt**</span><span class="sxs-lookup"><span data-stu-id="449a2-113">**Show**</span></span>](itipautocompleteprovider-show.md)                           | <span data-ttu-id="449a2-114">Hiermit wird die Liste der Auto Vervollständigen angezeigt oder ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="449a2-114">Displays or hides the auto complete list.</span></span><br/>                                                                 |
| [<span data-ttu-id="449a2-115">**Updatepzudingtext**</span><span class="sxs-lookup"><span data-stu-id="449a2-115">**UpdatePendingText**</span></span>](itipautocompleteprovider-updatependingtext.md) | <span data-ttu-id="449a2-116">Wird vom Auto Vervollständigen-Client verwendet, um die Anwendung über den Text zu benachrichtigen, den ein Benutzer in den Eingabebereich eingegeben hat.</span><span class="sxs-lookup"><span data-stu-id="449a2-116">Used by the auto complete client to notify the application of the text a user has inked into Input Panel.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="449a2-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="449a2-117">Requirements</span></span>



| <span data-ttu-id="449a2-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="449a2-118">Requirement</span></span> | <span data-ttu-id="449a2-119">Wert</span><span class="sxs-lookup"><span data-stu-id="449a2-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="449a2-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="449a2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="449a2-121">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="449a2-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="449a2-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="449a2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="449a2-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="449a2-123">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="449a2-124">Header</span><span class="sxs-lookup"><span data-stu-id="449a2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="449a2-125"><dt>Tipautocomplete. h (erfordert auch "pinputpanel \_ i. c")</dt></span><span class="sxs-lookup"><span data-stu-id="449a2-125"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="449a2-126">DLL</span><span class="sxs-lookup"><span data-stu-id="449a2-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="449a2-127"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="449a2-127"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="449a2-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="449a2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="449a2-129">Verweis auf Text Eingabe Panel</span><span class="sxs-lookup"><span data-stu-id="449a2-129">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> <dt>

[<span data-ttu-id="449a2-130">**Itipauwebcompleteclient-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="449a2-130">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> </dl>

 

