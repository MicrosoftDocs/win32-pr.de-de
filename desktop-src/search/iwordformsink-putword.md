---
description: Legt das ursprüngliche Word-Formular in das iwordformsink-Objekt ein.
ms.assetid: 333A3109-6C0A-42AE-9E10-87F53C7F737C
title: Iwordformsink::P utword-Methode (Search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordFormSink.PutWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 438cb41e50f264bd373ae2ef8e84598b651b0352
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340161"
---
# <a name="iwordformsinkputword-method"></a><span data-ttu-id="22eec-103">Iwordformsink::P utword-Methode</span><span class="sxs-lookup"><span data-stu-id="22eec-103">IWordFormSink::PutWord method</span></span>

<span data-ttu-id="22eec-104">Legt das ursprüngliche Word-Formular in das [**iwordformsink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) -Objekt ein.</span><span class="sxs-lookup"><span data-stu-id="22eec-104">Puts the original word form in the [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="22eec-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="22eec-105">Syntax</span></span>


```C++
HRESULT PutWord(
  [in] const WCHAR *pwcInBuf ,
  [in]       ULONG cwc
);
```



## <a name="parameters"></a><span data-ttu-id="22eec-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="22eec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22eec-107">*pwcinbuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22eec-107">*pwcInBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22eec-108">Ein Zeiger auf einen Puffer, der die endgültige alternative Form eines Worts enthält, bei der es sich immer um das ursprüngliche Wort handelt.</span><span class="sxs-lookup"><span data-stu-id="22eec-108">A pointer to a buffer that contains the final alternative form of a word, which is always the original word.</span></span>

</dd> <dt>

<span data-ttu-id="22eec-109">*CWC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22eec-109">*cwc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22eec-110">Die Anzahl der Zeichen in *pwcinbuf*.</span><span class="sxs-lookup"><span data-stu-id="22eec-110">The number of characters in *pwcInBuf*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22eec-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22eec-111">Return value</span></span>

<span data-ttu-id="22eec-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="22eec-112">This method can return one of these values.</span></span>



| <span data-ttu-id="22eec-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="22eec-113">Return code</span></span>                                                                          | <span data-ttu-id="22eec-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22eec-114">Description</span></span>                                           |
|--------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="22eec-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="22eec-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="22eec-116">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="22eec-116">The operation was completed successfully.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="22eec-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22eec-117">Remarks</span></span>

<span data-ttu-id="22eec-118">**Putword** wird von der [**generatewordforms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) -Methode der [**istemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) -Implementierung aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="22eec-118">**PutWord** is called from the [**GenerateWordForms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) method of the [**IStemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) implementation.</span></span> <span data-ttu-id="22eec-119">Diese Methode verarbeitet die ursprüngliche Form eines Worts und wird zuletzt aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="22eec-119">This method handles the original form of a word and is called last.</span></span> <span data-ttu-id="22eec-120">Alle vorherigen Alternativen Formulare für ein Wort werden durch Aufrufen von [**iwordformsink::P utaltword**](iwordformsink-putphrase.md)in das [**iwordformsink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) -Objekt eingefügt.</span><span class="sxs-lookup"><span data-stu-id="22eec-120">All preceding alternative forms for a word are put in the [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) object by calling [**IWordFormSink::PutAltWord**](iwordformsink-putphrase.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="22eec-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22eec-121">Requirements</span></span>



| <span data-ttu-id="22eec-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22eec-122">Requirement</span></span> | <span data-ttu-id="22eec-123">Wert</span><span class="sxs-lookup"><span data-stu-id="22eec-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="22eec-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="22eec-124">Minimum supported client</span></span><br/> | <span data-ttu-id="22eec-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="22eec-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="22eec-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="22eec-126">Minimum supported server</span></span><br/> | <span data-ttu-id="22eec-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="22eec-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="22eec-128">Header</span><span class="sxs-lookup"><span data-stu-id="22eec-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="22eec-129"><dt>Search. h</dt></span><span class="sxs-lookup"><span data-stu-id="22eec-129"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22eec-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22eec-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22eec-131">**Iwordformsink**</span><span class="sxs-lookup"><span data-stu-id="22eec-131">**IWordFormSink**</span></span>](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink)
</dt> </dl>

 

 
