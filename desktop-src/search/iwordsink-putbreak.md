---
description: Versetzt nach dem vorangehenden Wort einen Umbruch.
ms.assetid: C8622067-D8CE-4099-8B9F-941720F4706B
title: Iwordsink::P utbreak-Methode (Search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutBreak
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: c6407f1307b4860960c5202af13de736c7921139
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342929"
---
# <a name="iwordsinkputbreak-method"></a><span data-ttu-id="9c067-103">Iwordsink::P utbreak-Methode</span><span class="sxs-lookup"><span data-stu-id="9c067-103">IWordSink::PutBreak method</span></span>

<span data-ttu-id="9c067-104">Versetzt nach dem vorangehenden Wort einen Umbruch.</span><span class="sxs-lookup"><span data-stu-id="9c067-104">Puts a break after the preceding word.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c067-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c067-105">Syntax</span></span>


```C++
HRESULT PutBreak(
  [in] WORDREP_BREAK_TYPE breakType
);
```



## <a name="parameters"></a><span data-ttu-id="9c067-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c067-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c067-107">*breaktyp* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9c067-107">*breakType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c067-108">Ein Wert aus dem [**wordrep- \_ \_ unterbruchtyp**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) , der den Typ der Unterbrechung angibt, den die wordsink nach dem vorangehenden Wort einfügt.</span><span class="sxs-lookup"><span data-stu-id="9c067-108">A value from [**WORDREP\_BREAK\_TYPE**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) that indicates the type of break that the WordSink inserts after the preceding word.</span></span> <span data-ttu-id="9c067-109">Jede Unterbrechung nimmt eine eindeutige Position im Index auf.</span><span class="sxs-lookup"><span data-stu-id="9c067-109">Each break occupies a unique position in the index.</span></span> <span data-ttu-id="9c067-110">Daher wird durch Einfügen von Unterbrechungen zwischen Wörtern der relative Abstand zwischen Wörtern geändert.</span><span class="sxs-lookup"><span data-stu-id="9c067-110">Therefore, inserting breaks between words changes the relative distance between words.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c067-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9c067-111">Return value</span></span>

<span data-ttu-id="9c067-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="9c067-112">This method can return one of these values.</span></span>



| <span data-ttu-id="9c067-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9c067-113">Return code</span></span>                                                                          | <span data-ttu-id="9c067-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9c067-114">Description</span></span>                                          |
|--------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="9c067-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9c067-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="9c067-116">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="9c067-116">The operation was completed successfully.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9c067-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9c067-117">Remarks</span></span>

<span data-ttu-id="9c067-118">Die Methoden [**iwordsink putword**](iwordsink-putword.md) und [**iwordsink::P utaltword**](iwordsink-putaltword.md) fügen automatisch einen Ende der Wort Umbruch (EOW, der durch das wordrep \_ break \_ EOW-Element des Enumerationstyps der [**wordrep \_ \_**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) -Enumeration gekennzeichnet ist) nach jedem Wort ein.</span><span class="sxs-lookup"><span data-stu-id="9c067-118">The [**IWordSinkPutWord**](iwordsink-putword.md) and [**IWordSink::PutAltWord**](iwordsink-putaltword.md) methods automatically insert an end-of-word break (EOW, indicated by the WORDREP\_BREAK\_EOW element of the [**WORDREP\_BREAK\_TYPE**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) enumerated type) after each word.</span></span> <span data-ttu-id="9c067-119">Ruft die **putbreak** -Methode auf, um einen anderen Bruchtyp als das Wort Ende einzufügen.</span><span class="sxs-lookup"><span data-stu-id="9c067-119">Call the **PutBreak** method to insert a break type other than end of word.</span></span> <span data-ttu-id="9c067-120">Diese Methode ändert nicht den Quell Text Puffer (*psourcetext*) oder erhöht die Zeichen Anzahl (*CWC*).</span><span class="sxs-lookup"><span data-stu-id="9c067-120">This method does not change the source text buffer (*pSourceText*) or increment the character count (*cwc*).</span></span> <span data-ttu-id="9c067-121">Allerdings wird die aktuelle Position im Index erhöht und wirkt sich auf die Abfrageergebnisse aus.</span><span class="sxs-lookup"><span data-stu-id="9c067-121">However, it does increment the current position in the index and affects query results.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c067-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9c067-122">Requirements</span></span>



| <span data-ttu-id="9c067-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9c067-123">Requirement</span></span> | <span data-ttu-id="9c067-124">Wert</span><span class="sxs-lookup"><span data-stu-id="9c067-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9c067-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9c067-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9c067-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9c067-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9c067-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9c067-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9c067-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9c067-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9c067-129">Header</span><span class="sxs-lookup"><span data-stu-id="9c067-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c067-130"><dt>Search. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c067-130"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c067-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c067-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c067-132">**Iwordsink**</span><span class="sxs-lookup"><span data-stu-id="9c067-132">**IWordSink**</span></span>](iwordsink.md)
</dt> </dl>

 

 
