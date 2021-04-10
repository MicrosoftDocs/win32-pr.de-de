---
description: Gibt das Ende des abschließenden Ausdrucks in einer Sequenz alternativer Ausdrücke an, die eine Wörter Trennung während der Index Zeit generiert.
ms.assetid: 50E4E208-A290-42B7-9152-9472C01B20D5
title: 'Iwordsink:: endaltphrase-Methode (Search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.EndAltPhrase
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 4056357de5e3e479124e8f9a91d9b3d906300709
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214448"
---
# <a name="iwordsinkendaltphrase-method"></a><span data-ttu-id="a729f-103">Iwordsink:: endaltphrase-Methode</span><span class="sxs-lookup"><span data-stu-id="a729f-103">IWordSink::EndAltPhrase method</span></span>

<span data-ttu-id="a729f-104">Gibt das Ende des abschließenden Ausdrucks in einer Sequenz alternativer Ausdrücke an, die eine Wörter Trennung während der Index Zeit generiert.</span><span class="sxs-lookup"><span data-stu-id="a729f-104">Indicates the end of the final phrase in a sequence of alternative phrases that a word breaker generates during index time.</span></span>

## <a name="syntax"></a><span data-ttu-id="a729f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a729f-105">Syntax</span></span>


```C++
HRESULT EndAltPhrase();
```



## <a name="parameters"></a><span data-ttu-id="a729f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a729f-106">Parameters</span></span>

<span data-ttu-id="a729f-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="a729f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a729f-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a729f-108">Return value</span></span>

<span data-ttu-id="a729f-109">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="a729f-109">This method can return one of these values.</span></span>



| <span data-ttu-id="a729f-110">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a729f-110">Return code</span></span>                                                                                           | <span data-ttu-id="a729f-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a729f-111">Description</span></span>                                                                            |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a729f-112"><dt>**nur wbreak \_ E- \_ Abfrage \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a729f-112"><dt>**WBREAK\_E\_QUERY\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="a729f-113">[**Endaltphrase**](iwordsink-endaltphrase.md) wird während der Abfragezeit aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="a729f-113">[**EndAltPhrase**](iwordsink-endaltphrase.md) is called during query time.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a729f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a729f-114">Remarks</span></span>

<span data-ttu-id="a729f-115">[**Iwordbreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) -Implementierungen wenden **iwordsink:: endaltphrase** von der [**iwordbreak:: breaktext**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) -Methode an, um eine Sequenz alternativer Ausdrücke zu beenden.</span><span class="sxs-lookup"><span data-stu-id="a729f-115">[**IWordBreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) implementations call **IWordSink::EndAltPhrase** from the [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) method to terminate a sequence of alternative phrases.</span></span> <span data-ttu-id="a729f-116">Die [**iwordsink:: startaltphrase**](iwordsink-startaltphrase.md) -Methode wird aufgerufen, um das Ende eines Ausdrucks und den Anfang eines anderen in einer Sequenz von Ausdrücken anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a729f-116">The [**IWordSink::StartAltPhrase**](iwordsink-startaltphrase.md) method is called to indicate the end of one phrase and the beginning of another in a sequence of phrases.</span></span> <span data-ttu-id="a729f-117">Nur der letzte Ausdruck in einer Sequenz wird mit einem-Befehl von **endaltphrase** beendet.</span><span class="sxs-lookup"><span data-stu-id="a729f-117">Only the last phrase in a sequence is terminated with a call to **EndAltPhrase**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a729f-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a729f-118">Requirements</span></span>



| <span data-ttu-id="a729f-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a729f-119">Requirement</span></span> | <span data-ttu-id="a729f-120">Wert</span><span class="sxs-lookup"><span data-stu-id="a729f-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a729f-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a729f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a729f-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a729f-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a729f-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a729f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a729f-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a729f-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a729f-125">Header</span><span class="sxs-lookup"><span data-stu-id="a729f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a729f-126"><dt>Search. h</dt></span><span class="sxs-lookup"><span data-stu-id="a729f-126"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a729f-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a729f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a729f-128">**Iwordsink**</span><span class="sxs-lookup"><span data-stu-id="a729f-128">**IWordSink**</span></span>](iwordsink.md)
</dt> </dl>

 

 
