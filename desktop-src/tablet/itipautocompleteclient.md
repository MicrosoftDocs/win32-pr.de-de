---
description: Ermöglicht dem Client, das Auto Vervollständigen-Anbieter Objekt der Anwendung für den Text Eingabebereich aufzurufen.
ms.assetid: 448b8136-ebcb-4116-9a81-a77a37d69e24
title: Itipautcompleteclient-Schnittstelle (tipauabcomplete. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 7b9dad38d0e3f169019934b7e60a09096aced1b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362725"
---
# <a name="itipautocompleteclient-interface"></a><span data-ttu-id="d3b97-103">Itipauwebcompleteclient-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d3b97-103">ITipAutocompleteClient interface</span></span>

<span data-ttu-id="d3b97-104">Ermöglicht dem Client, das Auto Vervollständigen-Anbieter Objekt der Anwendung für den Text Eingabebereich aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d3b97-104">Enables the client to call the application's Text Input Panel auto complete provider object.</span></span>

## <a name="members"></a><span data-ttu-id="d3b97-105">Member</span><span class="sxs-lookup"><span data-stu-id="d3b97-105">Members</span></span>

<span data-ttu-id="d3b97-106">Die **itipautecompleteclient** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d3b97-106">The **ITipAutocompleteClient** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d3b97-107">**Itipautocompleteclient** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d3b97-107">**ITipAutocompleteClient** also has these types of members:</span></span>

-   [<span data-ttu-id="d3b97-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="d3b97-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d3b97-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="d3b97-109">Methods</span></span>

<span data-ttu-id="d3b97-110">Die **itipaudecompleteclient** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="d3b97-110">The **ITipAutocompleteClient** interface has these methods.</span></span>



| <span data-ttu-id="d3b97-111">Methode</span><span class="sxs-lookup"><span data-stu-id="d3b97-111">Method</span></span>                                                              | <span data-ttu-id="d3b97-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d3b97-112">Description</span></span>                                                                                                                                                          |
|:--------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d3b97-113">**Adviseprovider**</span><span class="sxs-lookup"><span data-stu-id="d3b97-113">**AdviseProvider**</span></span>](itipautocompleteclient-adviseprovider.md)     | <span data-ttu-id="d3b97-114">Registriert den Anbieter beim Client, damit der Client das Auto Vervollständigen-Anbieter Objekt der Anwendung abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="d3b97-114">Registers the provider with the client to enable the client to call the application's auto complete provider object.</span></span><br/>                                      |
| [<span data-ttu-id="d3b97-115">**Preferredrects**</span><span class="sxs-lookup"><span data-stu-id="d3b97-115">**PreferredRects**</span></span>](itipautocompleteclient-preferredrects.md)     | <span data-ttu-id="d3b97-116">Ermöglicht dem Client, vorzuschlagen, wo die Auto Vervollständigen-Liste positioniert werden soll, um die überlappenden Eingabebereich zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="d3b97-116">Allows the client to suggest where to position the auto complete list to avoid overlapping the Input Panel.</span></span><br/>                                               |
| [<span data-ttu-id="d3b97-117">**Requestshowui**</span><span class="sxs-lookup"><span data-stu-id="d3b97-117">**RequestShowUI**</span></span>](itipautocompleteclient-requestshowui.md)       | <span data-ttu-id="d3b97-118">Bestimmt, ob der Eingabebereich bereit ist, die Auto Vervollständigen-Liste angezeigt zu haben.</span><span class="sxs-lookup"><span data-stu-id="d3b97-118">Determines whether Input Panel is ready to have the auto complete list shown.</span></span><br/>                                                                             |
| [<span data-ttu-id="d3b97-119">**Unadviseprovider**</span><span class="sxs-lookup"><span data-stu-id="d3b97-119">**UnadviseProvider**</span></span>](itipautocompleteclient-unadviseprovider.md) | <span data-ttu-id="d3b97-120">Hebt die Registrierung des zugeordneten Anbieters auf.</span><span class="sxs-lookup"><span data-stu-id="d3b97-120">Unregisters the associated provider.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="d3b97-121">**Userselection**</span><span class="sxs-lookup"><span data-stu-id="d3b97-121">**UserSelection**</span></span>](itipautocompleteclient-userselection.md)       | <span data-ttu-id="d3b97-122">Benachrichtigt den Eingabebereich, dass der Benutzer etwas in der Liste Auto vervollständigen ausgewählt und den verbleibenden Text verworfen hat, der noch nicht eingefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="d3b97-122">Notifies the Input Panel that the user has selected something in the auto complete list and to discard all remaining text that has not yet been inserted.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d3b97-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3b97-123">Requirements</span></span>



| <span data-ttu-id="d3b97-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d3b97-124">Requirement</span></span> | <span data-ttu-id="d3b97-125">Wert</span><span class="sxs-lookup"><span data-stu-id="d3b97-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3b97-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d3b97-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d3b97-127">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3b97-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="d3b97-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d3b97-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d3b97-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d3b97-129">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="d3b97-130">Header</span><span class="sxs-lookup"><span data-stu-id="d3b97-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3b97-131"><dt>Tipautocomplete. h (erfordert auch "pinputpanel \_ i. c")</dt></span><span class="sxs-lookup"><span data-stu-id="d3b97-131"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d3b97-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d3b97-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3b97-133"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3b97-133"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



 

