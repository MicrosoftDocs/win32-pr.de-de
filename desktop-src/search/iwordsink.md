---
description: Behandelt Wörter, die von Wort Umbrüchen während der Index Zeit und der Abfragezeit identifiziert werden.
ms.assetid: 220FCAE5-D22D-45ED-9689-E78C0D8E0BB3
title: Iwordsink-Schnittstelle (Search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 2eab8eee4f7b07b0f712e68d7ad05b970506b00b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344672"
---
# <a name="iwordsink-interface"></a><span data-ttu-id="2c762-103">Iwordsink-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="2c762-103">IWordSink interface</span></span>

<span data-ttu-id="2c762-104">Behandelt Wörter, die von Wort Umbrüchen während der Index Zeit und der Abfragezeit identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="2c762-104">Handles words identified by word breaks during both index time and query time.</span></span>

## <a name="members"></a><span data-ttu-id="2c762-105">Member</span><span class="sxs-lookup"><span data-stu-id="2c762-105">Members</span></span>

<span data-ttu-id="2c762-106">Die **iwordsink** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="2c762-106">The **IWordSink** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2c762-107">**Iwordsink** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2c762-107">**IWordSink** also has these types of members:</span></span>

-   [<span data-ttu-id="2c762-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="2c762-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2c762-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="2c762-109">Methods</span></span>

<span data-ttu-id="2c762-110">Die **iwordsink** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="2c762-110">The **IWordSink** interface has these methods.</span></span>



| <span data-ttu-id="2c762-111">Methode</span><span class="sxs-lookup"><span data-stu-id="2c762-111">Method</span></span>                                             | <span data-ttu-id="2c762-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2c762-112">Description</span></span>                                                                                                                             |
|:---------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c762-113">**Endaltphrase**</span><span class="sxs-lookup"><span data-stu-id="2c762-113">**EndAltPhrase**</span></span>](iwordsink-endaltphrase.md)     | <span data-ttu-id="2c762-114">Gibt das Ende des abschließenden Ausdrucks in einer Sequenz alternativer Ausdrücke an, die eine Wörter Trennung während der Index Zeit generiert.</span><span class="sxs-lookup"><span data-stu-id="2c762-114">Indicates the end of the final phrase in a sequence of alternative phrases that a word breaker generates during index time.</span></span><br/>  |
| [<span data-ttu-id="2c762-115">**Putaltword**</span><span class="sxs-lookup"><span data-stu-id="2c762-115">**PutAltWord**</span></span>](iwordsink-putaltword.md)         | <span data-ttu-id="2c762-116">Fügt ein alternatives Wort und seine Position in das **iwordsink** -Objekt ein.</span><span class="sxs-lookup"><span data-stu-id="2c762-116">Puts an alternative word and its position in the **IWordSink** object.</span></span><br/>                                                       |
| [<span data-ttu-id="2c762-117">**Putbreak**</span><span class="sxs-lookup"><span data-stu-id="2c762-117">**PutBreak**</span></span>](iwordsink-putbreak.md)             | <span data-ttu-id="2c762-118">Versetzt nach dem vorangehenden Wort einen Umbruch.</span><span class="sxs-lookup"><span data-stu-id="2c762-118">Puts a break after the preceding word.</span></span><br/>                                                                                       |
| [<span data-ttu-id="2c762-119">**Putword**</span><span class="sxs-lookup"><span data-stu-id="2c762-119">**PutWord**</span></span>](iwordsink-putword.md)               | <span data-ttu-id="2c762-120">Fügt ein Wort und seine Position in das **iwordsink** -Objekt ein.</span><span class="sxs-lookup"><span data-stu-id="2c762-120">Puts a word and its position in the **IWordSink** object.</span></span><br/>                                                                    |
| [<span data-ttu-id="2c762-121">**Startaltphrase**</span><span class="sxs-lookup"><span data-stu-id="2c762-121">**StartAltPhrase**</span></span>](iwordsink-startaltphrase.md) | <span data-ttu-id="2c762-122">Gibt die Begrenzung zwischen Ausdrücken in einer Sequenz alternativer Ausdrücke an, die eine Wörter Trennung während der Index Zeit generiert.</span><span class="sxs-lookup"><span data-stu-id="2c762-122">Indicates the boundary between phrases in a sequence of alternative phrases that a word breaker generates during index time.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2c762-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2c762-123">Remarks</span></span>

<span data-ttu-id="2c762-124">Windows Search erstellt und Initialisiert Instanzen des **iwordsink** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="2c762-124">Windows Search creates and initializes instances of the **IWordSink** object.</span></span> <span data-ttu-id="2c762-125">Das **iwordsink** -Objekt empfängt den *fquery* -Parameter während der Initialisierung und verwendet diesen Parameter, um den Wort Umbruch Kontext zu bestimmen, in dem das-Objekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2c762-125">The **IWordSink** object receives the *fQuery* parameter during initialization and uses this parameter to determine the word-breaking context in which the object is used.</span></span>

<span data-ttu-id="2c762-126">[**Iwordbreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) -Implementierungen erhalten einen Zeiger auf das **iwordsink** -Objekt in der [**iwordbreaker:: breaktext**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) -Methode.</span><span class="sxs-lookup"><span data-stu-id="2c762-126">[**IWordBreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) implementations receive a pointer to the **IWordSink** object in the [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c762-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c762-127">Requirements</span></span>



| <span data-ttu-id="2c762-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c762-128">Requirement</span></span> | <span data-ttu-id="2c762-129">Wert</span><span class="sxs-lookup"><span data-stu-id="2c762-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2c762-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2c762-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2c762-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c762-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2c762-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2c762-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2c762-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c762-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2c762-134">Header</span><span class="sxs-lookup"><span data-stu-id="2c762-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c762-135"><dt>Search. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c762-135"><dt>Search.h</dt></span></span> </dl> |



 

 
