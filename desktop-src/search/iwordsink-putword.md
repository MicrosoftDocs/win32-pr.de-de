---
description: Fügt ein Wort und seine Position in das iwordsink-Objekt ein.
ms.assetid: 3D645BF6-895E-46E2-92A3-3E301CD228D8
title: Iwordsink::P utword-Methode (Search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 5f622e09c2b82bc8de986dafcc83247617caec75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339755"
---
# <a name="iwordsinkputword-method"></a><span data-ttu-id="75e96-103">Iwordsink::P utword-Methode</span><span class="sxs-lookup"><span data-stu-id="75e96-103">IWordSink::PutWord method</span></span>

<span data-ttu-id="75e96-104">Fügt ein Wort und seine Position in das [**iwordsink**](iwordsink.md) -Objekt ein.</span><span class="sxs-lookup"><span data-stu-id="75e96-104">Puts a word and its position in the [**IWordSink**](iwordsink.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="75e96-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="75e96-105">Syntax</span></span>


```C++
HRESULT PutWord(
  [in]       ULONG cwc,
  [in] const WCHAR *pwcInBuf,
  [in]       ULONG cwcSrcLen,
  [in]       ULONG cwcSrcPos
);
```



## <a name="parameters"></a><span data-ttu-id="75e96-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="75e96-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75e96-107">*CWC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75e96-107">*cwc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75e96-108">Die Anzahl der Zeichen in *pwcinbuf*.</span><span class="sxs-lookup"><span data-stu-id="75e96-108">The number of characters in *pwcInBuf*.</span></span>

</dd> <dt>

<span data-ttu-id="75e96-109">*pwcinbuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75e96-109">*pwcInBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75e96-110">Ein Zeiger auf einen Puffer, der eine alternative Form eines Worts aus dem Quelltext enthält.</span><span class="sxs-lookup"><span data-stu-id="75e96-110">A pointer to a buffer that contains an alternative form of a word from the source text.</span></span> <span data-ttu-id="75e96-111">Dieser Parameter wird nicht von **putword** geändert.</span><span class="sxs-lookup"><span data-stu-id="75e96-111">This parameter is not modified by **PutWord**.</span></span> <span data-ttu-id="75e96-112">Sie können den *ptextsource* -Parameter nach Bedarf von [**iwordbreaker:: breaktext**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) übergeben.</span><span class="sxs-lookup"><span data-stu-id="75e96-112">You can pass the *pTextSource* parameter from [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) as appropriate.</span></span>

</dd> <dt>

<span data-ttu-id="75e96-113">*cwcsrclen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75e96-113">*cwcSrcLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75e96-114">Die Anzahl der Zeichen im Quell Text Puffer (angegeben durch den *ptextsource* -Parameter für [**iwordbreaker:: breaktext**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)), die dem in *pwcinbuf* enthaltenen Wort entsprechen.</span><span class="sxs-lookup"><span data-stu-id="75e96-114">The number of characters in the source text buffer (indicated by the *pTextSource* parameter to [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)) that correspond to the word contained in *pwcInBuf*.</span></span>

</dd> <dt>

<span data-ttu-id="75e96-115">*cwcsrcpos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75e96-115">*cwcSrcPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75e96-116">Die Anfangsposition des Worts in *pwcinbuf* im Quell Text Puffer (angegeben durch den *ptextsource* -Parameter für [**iwordbreaker:: breaktext**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span><span class="sxs-lookup"><span data-stu-id="75e96-116">The starting position of the word in *pwcInBuf* in the source text buffer (indicated by the *pTextSource* parameter to [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75e96-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="75e96-117">Return value</span></span>

<span data-ttu-id="75e96-118">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="75e96-118">This method can return one of these values.</span></span>



| <span data-ttu-id="75e96-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="75e96-119">Return code</span></span>                                                                                              | <span data-ttu-id="75e96-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75e96-120">Description</span></span>                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="75e96-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="75e96-121"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="75e96-122">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="75e96-122">The operation was completed successfully.</span></span> <span data-ttu-id="75e96-123">Gibt auch an, dass kein Text mehr zum Auffüllen des Puffers verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="75e96-123">Also indicates that no more text is available to refill the buffer.</span></span><br/>                                  |
| <dl> <span data-ttu-id="75e96-124"><dt>**Sprache \_ \_großes \_ Wort**</dt></span><span class="sxs-lookup"><span data-stu-id="75e96-124"><dt>**LANGUAGE\_S\_LARGE\_WORD** </dt></span></span> </dl> | <span data-ttu-id="75e96-125">Der Wert von *CWC* ist größer als der Wert für *ulmaxumkensize* , der in [**iwordbreaker:: init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init)angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="75e96-125">Value of *cwc* is larger than the value for *ulMaxTokenSize* that is specified in [**IWordBreaker::Init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init).</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="75e96-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75e96-126">Remarks</span></span>

<span data-ttu-id="75e96-127">Es wird empfohlen, dass die **iwordsink::P utword** -Methode immer das ursprüngliche Wort enthält, wie es in *ptextsource* gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="75e96-127">We recommend that the **IWordSink::PutWord** method always contain the original word as found in *pTextSource*.</span></span> <span data-ttu-id="75e96-128">Alternative Formen des Worts werden mithilfe von [**iwordsink::P utaltword**](iwordsink-putaltword.md)an wordsink übermittelt.</span><span class="sxs-lookup"><span data-stu-id="75e96-128">Alternative forms of the word are passed to WordSink by using [**IWordSink::PutAltWord**](iwordsink-putaltword.md).</span></span> <span data-ttu-id="75e96-129">Außerdem wird empfohlen, dass die Wörter in *pwcinbuf* so genau wie möglich mit dem Quelltext übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="75e96-129">We also recommend that the words in *pwcInBuf* match the source text as closely as possible.</span></span> <span data-ttu-id="75e96-130">Behalten Sie z. b. Groß-/Kleinschreibung und Akzente bei.</span><span class="sxs-lookup"><span data-stu-id="75e96-130">For example, retain capitalization and accents where possible.</span></span>

<span data-ttu-id="75e96-131">Dieser Rückruf muss für jedes aus *ptextsource* abgerufene Wort mit Ausnahme derjenigen erfolgen, für die der [**iwordsink::P utaltword**](iwordsink-putaltword.md) -Befehl durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="75e96-131">This call must be made for every word retrieved from *pTextSource* except those for which the [**IWordSink::PutAltWord**](iwordsink-putaltword.md) call was made.</span></span> <span data-ttu-id="75e96-132">Das Wort wird mit einem EOW-Zeichen beendet, wenn es in der wordsink gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="75e96-132">The word is terminated with an EOW character when it is saved to the WordSink.</span></span>

## <a name="requirements"></a><span data-ttu-id="75e96-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="75e96-133">Requirements</span></span>



| <span data-ttu-id="75e96-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="75e96-134">Requirement</span></span> | <span data-ttu-id="75e96-135">Wert</span><span class="sxs-lookup"><span data-stu-id="75e96-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="75e96-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="75e96-136">Minimum supported client</span></span><br/> | <span data-ttu-id="75e96-137">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="75e96-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="75e96-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="75e96-138">Minimum supported server</span></span><br/> | <span data-ttu-id="75e96-139">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="75e96-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="75e96-140">Header</span><span class="sxs-lookup"><span data-stu-id="75e96-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="75e96-141"><dt>Search. h</dt></span><span class="sxs-lookup"><span data-stu-id="75e96-141"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75e96-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75e96-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75e96-143">**Iwordsink**</span><span class="sxs-lookup"><span data-stu-id="75e96-143">**IWordSink**</span></span>](iwordsink.md)
</dt> </dl>

 

 
