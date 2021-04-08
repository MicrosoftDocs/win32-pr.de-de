---
description: Fügt eine alternative Form eines Worts in das iwordformsink-Objekt ein.
ms.assetid: 4F6A3E88-A17C-4CA3-849D-FF0DC06D5DC3
title: Iwordformsink::P utaltword-Methode (Search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordFormSink.PutAltWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 43539bbf67e23bc37ca92f6a961b945ae581e746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750360"
---
# <a name="iwordformsinkputaltword-method"></a><span data-ttu-id="dbfaa-103">Iwordformsink::P utaltword-Methode</span><span class="sxs-lookup"><span data-stu-id="dbfaa-103">IWordFormSink::PutAltWord method</span></span>

<span data-ttu-id="dbfaa-104">Fügt eine alternative Form eines Worts in das [**iwordformsink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) -Objekt ein.</span><span class="sxs-lookup"><span data-stu-id="dbfaa-104">Puts an alternative form of a word in the [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbfaa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbfaa-105">Syntax</span></span>


```C++
HRESULT PutAltWord(
  [in] const WCHAR *pwcInBuf ,
  [in]       ULONG cwc
);
```



## <a name="parameters"></a><span data-ttu-id="dbfaa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dbfaa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbfaa-107">*pwcinbuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dbfaa-107">*pwcInBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbfaa-108">Ein Zeiger auf einen Puffer, der eine alternative Form eines Worts enthält.</span><span class="sxs-lookup"><span data-stu-id="dbfaa-108">A pointer to a buffer that contains an alternative form of a word.</span></span>

</dd> <dt>

<span data-ttu-id="dbfaa-109">*CWC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dbfaa-109">*cwc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbfaa-110">Die Anzahl der Zeichen in *pwcinbuf*.</span><span class="sxs-lookup"><span data-stu-id="dbfaa-110">The number of characters in *pwcInBuf*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbfaa-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dbfaa-111">Return value</span></span>

<span data-ttu-id="dbfaa-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="dbfaa-112">This method can return one of these values.</span></span>



| <span data-ttu-id="dbfaa-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="dbfaa-113">Return code</span></span>                                                                                              | <span data-ttu-id="dbfaa-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dbfaa-114">Description</span></span>                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dbfaa-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dbfaa-115"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="dbfaa-116">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="dbfaa-116">The operation was completed successfully.</span></span> <br/>                                                                                             |
| <dl> <span data-ttu-id="dbfaa-117"><dt>**Sprache \_ \_großes \_ Wort**</dt></span><span class="sxs-lookup"><span data-stu-id="dbfaa-117"><dt>**LANGUAGE\_S\_LARGE\_WORD** </dt></span></span> </dl> | <span data-ttu-id="dbfaa-118">Der Wert von *CWC* ist größer als der Wert für *ulmaxumkensize* , der in [**istemmer:: init**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-init)angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="dbfaa-118">Value of *cwc* is larger than the value for *ulMaxTokenSize* that is specified in [**IStemmer::Init**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-init).</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="dbfaa-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dbfaa-119">Remarks</span></span>

<span data-ttu-id="dbfaa-120">Diese Methode wird von der [**generatewordforms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) -Methode der [**istemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) -Implementierung aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="dbfaa-120">This method is called from the [**GenerateWordForms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) method of the [**IStemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) implementation.</span></span> <span data-ttu-id="dbfaa-121">Alle alternativen Formulare für ein Wort, mit Ausnahme des letzten, werden durch Aufrufen von **iwordformsink::P utaltword** in das [**iwordformsink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) -Objekt eingefügt.</span><span class="sxs-lookup"><span data-stu-id="dbfaa-121">All alternative forms for a word, except the last, are put in the [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) object by calling **IWordFormSink::PutAltWord**.</span></span> <span data-ttu-id="dbfaa-122">Die endgültige alternative Form eines Worts, bei der es sich immer um die ursprüngliche Form des Worts handelt, wird durch Aufrufen von [**iwordformsink::P utword**](iwordformsink-putword.md)behandelt.</span><span class="sxs-lookup"><span data-stu-id="dbfaa-122">The final alternative form of a word, which is always the original form of the word, is handled by calling [**IWordFormSink::PutWord**](iwordformsink-putword.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dbfaa-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dbfaa-123">Requirements</span></span>



| <span data-ttu-id="dbfaa-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dbfaa-124">Requirement</span></span> | <span data-ttu-id="dbfaa-125">Wert</span><span class="sxs-lookup"><span data-stu-id="dbfaa-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="dbfaa-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dbfaa-126">Minimum supported client</span></span><br/> | <span data-ttu-id="dbfaa-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dbfaa-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="dbfaa-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dbfaa-128">Minimum supported server</span></span><br/> | <span data-ttu-id="dbfaa-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dbfaa-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="dbfaa-130">Header</span><span class="sxs-lookup"><span data-stu-id="dbfaa-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbfaa-131"><dt>Search. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbfaa-131"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbfaa-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dbfaa-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbfaa-133">**Iwordformsink**</span><span class="sxs-lookup"><span data-stu-id="dbfaa-133">**IWordFormSink**</span></span>](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink)
</dt> </dl>

 

 
