---
description: Gibt die Begrenzung zwischen Ausdrücken in einer Sequenz alternativer Ausdrücke an, die eine Wörter Trennung während der Index Zeit generiert.
ms.assetid: 3F3B6761-887B-426E-A44F-E636397180C7
title: 'Iwordsink:: startaltphrase-Methode (Search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.StartAltPhrase
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: e4e35c5ed75016292dd420e7a832c6cfb780284a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214447"
---
# <a name="iwordsinkstartaltphrase-method"></a><span data-ttu-id="32c19-103">Iwordsink:: startaltphrase-Methode</span><span class="sxs-lookup"><span data-stu-id="32c19-103">IWordSink::StartAltPhrase method</span></span>

<span data-ttu-id="32c19-104">Gibt die Begrenzung zwischen Ausdrücken in einer Sequenz alternativer Ausdrücke an, die eine Wörter Trennung während der Index Zeit generiert.</span><span class="sxs-lookup"><span data-stu-id="32c19-104">Indicates the boundary between phrases in a sequence of alternative phrases that a word breaker generates during index time.</span></span>

## <a name="syntax"></a><span data-ttu-id="32c19-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="32c19-105">Syntax</span></span>


```C++
HRESULT StartAltPhrase();
```



## <a name="parameters"></a><span data-ttu-id="32c19-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="32c19-106">Parameters</span></span>

<span data-ttu-id="32c19-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="32c19-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="32c19-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="32c19-108">Return value</span></span>

<span data-ttu-id="32c19-109">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="32c19-109">This method can return one of these values.</span></span>



| <span data-ttu-id="32c19-110">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="32c19-110">Return code</span></span>                                                                                           | <span data-ttu-id="32c19-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="32c19-111">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="32c19-112"><dt>**nur wbreak \_ E- \_ Abfrage \_**</dt></span><span class="sxs-lookup"><span data-stu-id="32c19-112"><dt>**WBREAK\_E\_QUERY\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="32c19-113">[**Startaltphrase**](iwordsink-startaltphrase.md) wird während der Abfragezeit aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="32c19-113">[**StartAltPhrase**](iwordsink-startaltphrase.md) is called during query time.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="32c19-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="32c19-114">Remarks</span></span>

<span data-ttu-id="32c19-115">Jeder Alternative Ausdruck beginnt mit einem **startaltphrase** -Befehl.</span><span class="sxs-lookup"><span data-stu-id="32c19-115">Each alternative phrase starts with a **StartAltPhrase** call.</span></span> <span data-ttu-id="32c19-116">Der Ausdruck wird durch nachfolgende Aufrufe der [**iwordsink::P utword**](iwordsink-putword.md) -Methode oder der [**iwordsink::P utaltword**](iwordsink-putaltword.md) -Methode in das [**iwordsink**](iwordsink.md) -Objekt eingefügt.</span><span class="sxs-lookup"><span data-stu-id="32c19-116">The phrase is put in the [**IWordSink**](iwordsink.md) object through subsequent calls to the [**IWordSink::PutWord**](iwordsink-putword.md) or [**IWordSink::PutAltWord**](iwordsink-putaltword.md) method.</span></span> <span data-ttu-id="32c19-117">Der endgültige Alternative Ausdruck in einer Sequenz von Ausdrücken wird mit einem-Rückruf der [**iwordsink:: endaltphrase**](iwordsink-endaltphrase.md) -Methode beendet.</span><span class="sxs-lookup"><span data-stu-id="32c19-117">The final alternative phrase in a sequence of phrases is terminated with a call to the [**IWordSink::EndAltPhrase**](iwordsink-endaltphrase.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="32c19-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="32c19-118">Requirements</span></span>



| <span data-ttu-id="32c19-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="32c19-119">Requirement</span></span> | <span data-ttu-id="32c19-120">Wert</span><span class="sxs-lookup"><span data-stu-id="32c19-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="32c19-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="32c19-121">Minimum supported client</span></span><br/> | <span data-ttu-id="32c19-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="32c19-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="32c19-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="32c19-123">Minimum supported server</span></span><br/> | <span data-ttu-id="32c19-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="32c19-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="32c19-125">Header</span><span class="sxs-lookup"><span data-stu-id="32c19-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="32c19-126"><dt>Search. h</dt></span><span class="sxs-lookup"><span data-stu-id="32c19-126"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32c19-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32c19-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32c19-128">**Iwordsink**</span><span class="sxs-lookup"><span data-stu-id="32c19-128">**IWordSink**</span></span>](iwordsink.md)
</dt> </dl>

 

 




