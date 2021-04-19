---
description: Fügt ein alternatives Wort und seine Position in das iwordsink-Objekt ein.
ms.assetid: 5C8A9B30-F9B5-42E9-ADAC-A11230F0C2FA
title: Iwordsink::P utaltword-Methode (Search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutAltWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 21fd9eb9ac5a1bf0f52d6574595dc495432d7ec9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344262"
---
# <a name="iwordsinkputaltword-method"></a><span data-ttu-id="c9200-103">Iwordsink::P utaltword-Methode</span><span class="sxs-lookup"><span data-stu-id="c9200-103">IWordSink::PutAltWord method</span></span>

<span data-ttu-id="c9200-104">Fügt ein alternatives Wort und seine Position in das [**iwordsink**](iwordsink.md) -Objekt ein.</span><span class="sxs-lookup"><span data-stu-id="c9200-104">Puts an alternative word and its position in the [**IWordSink**](iwordsink.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9200-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9200-105">Syntax</span></span>


```C++
HRESULT PutAltWord(
  [in]       ULONG cwc,
  [in] const WCHAR *pwcInBuf,
  [in]       ULONG cwcSrcLen,
  [in]       ULONG cwcSrcPos
);
```



## <a name="parameters"></a><span data-ttu-id="c9200-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9200-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9200-107">*CWC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9200-107">*cwc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9200-108">Die Anzahl der Zeichen in *pwcinbuf*.</span><span class="sxs-lookup"><span data-stu-id="c9200-108">The number of characters in *pwcInBuf*.</span></span>

</dd> <dt>

<span data-ttu-id="c9200-109">*pwcinbuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9200-109">*pwcInBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9200-110">Ein Zeiger auf einen Puffer, der eine alternative Form eines Worts aus dem Quelltext enthält.</span><span class="sxs-lookup"><span data-stu-id="c9200-110">A pointer to a buffer that contains an alternative form of a word from the source text.</span></span> <span data-ttu-id="c9200-111">Dieser Parameter wird nicht von **putaltword** geändert.</span><span class="sxs-lookup"><span data-stu-id="c9200-111">This parameter is not modified by **PutAltWord**.</span></span> <span data-ttu-id="c9200-112">Sie können den *ptextsource* -Parameter nach Bedarf von [**iwordbreaker:: breaktext**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) übergeben.</span><span class="sxs-lookup"><span data-stu-id="c9200-112">You can pass the *pTextSource* parameter from [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) as appropriate.</span></span>

</dd> <dt>

<span data-ttu-id="c9200-113">*cwcsrclen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9200-113">*cwcSrcLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9200-114">Die Anzahl der Zeichen im Quell Text Puffer (angegeben durch den *ptextsource* -Parameter für [**iwordbreaker:: breaktext**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)), die dem in *pwcinbuf* enthaltenen Wort entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c9200-114">The number of characters in the source text buffer (indicated by the *pTextSource* parameter to [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)) that correspond to the word contained in *pwcInBuf*.</span></span>

</dd> <dt>

<span data-ttu-id="c9200-115">*cwcsrcpos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9200-115">*cwcSrcPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9200-116">Die Anfangsposition des Worts in *pwcinbuf* im Quell Text Puffer (angegeben durch den *ptextsource* -Parameter für [**iwordbreaker:: breaktext**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span><span class="sxs-lookup"><span data-stu-id="c9200-116">The starting position of the word in *pwcInBuf* in the source text buffer (indicated by the *pTextSource* parameter to [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9200-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c9200-117">Return value</span></span>

<span data-ttu-id="c9200-118">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c9200-118">This method can return one of these values.</span></span>



| <span data-ttu-id="c9200-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c9200-119">Return code</span></span>                                                                                              | <span data-ttu-id="c9200-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c9200-120">Description</span></span>                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c9200-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c9200-121"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="c9200-122">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="c9200-122">The operation was completed successfully.</span></span> <span data-ttu-id="c9200-123">Gibt auch an, dass noch kein Text mehr verarbeitet werden muss.</span><span class="sxs-lookup"><span data-stu-id="c9200-123">Also indicates that no more text remains to be processed.</span></span><br/>                                            |
| <dl> <span data-ttu-id="c9200-124"><dt>**Sprache \_ \_großes \_ Wort**</dt></span><span class="sxs-lookup"><span data-stu-id="c9200-124"><dt>**LANGUAGE\_S\_LARGE\_WORD** </dt></span></span> </dl> | <span data-ttu-id="c9200-125">Der Wert von *CWC* ist größer als der Wert für *ulmaxumkensize* , der in [**iwordbreaker:: init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init)angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c9200-125">Value of *cwc* is larger than the value for *ulMaxTokenSize* that is specified in [**IWordBreaker::Init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init).</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="c9200-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c9200-126">Remarks</span></span>

<span data-ttu-id="c9200-127">**Putaltword** stellt eine alternative Form eines Worts in [**iwordsink**](iwordsink.md)dar.</span><span class="sxs-lookup"><span data-stu-id="c9200-127">**PutAltWord** puts an alternative form of a word in the [**IWordSink**](iwordsink.md).</span></span> <span data-ttu-id="c9200-128">Das Wort wird an derselben Position wie das ursprüngliche Wort in der Text Quelle abgelegt (*ptextsource* in [**iwordbreaker:: breaktext**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span><span class="sxs-lookup"><span data-stu-id="c9200-128">The word is put in the same position as the original word in the text source (*pTextSource* in [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span></span> <span data-ttu-id="c9200-129">Standardmäßig beendet **putaltword** Wörter mit einem **wordrep- \_ \_** Break-Break-Typ aus dem Enumerationstyp " [**wordrep \_ break \_ Type**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) ".</span><span class="sxs-lookup"><span data-stu-id="c9200-129">By default, **PutAltWord** terminates words with a **WORDREP\_BREAK\_EOW** break type from the [**WORDREP\_BREAK\_TYPE**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) enumerated type.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9200-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c9200-130">Requirements</span></span>



| <span data-ttu-id="c9200-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c9200-131">Requirement</span></span> | <span data-ttu-id="c9200-132">Wert</span><span class="sxs-lookup"><span data-stu-id="c9200-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c9200-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c9200-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c9200-134">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9200-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c9200-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c9200-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c9200-136">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9200-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c9200-137">Header</span><span class="sxs-lookup"><span data-stu-id="c9200-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9200-138"><dt>Search. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9200-138"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9200-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9200-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9200-140">**Iwordsink**</span><span class="sxs-lookup"><span data-stu-id="c9200-140">**IWordSink**</span></span>](iwordsink.md)
</dt> </dl>

 

 
