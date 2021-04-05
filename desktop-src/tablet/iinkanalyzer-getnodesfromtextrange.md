---
description: Ruft eine Auflistung von icontextnode-Objekten ab, die für den angegebenen Textbereich für die angegebenen Kontext Knoten relevant sind.
ms.assetid: 39a5dd52-7007-4395-8668-261eca78a090
title: 'Iinkanalyzer:: GetNodesFromTextRange-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetNodesFromTextRange
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ada60a64bb4e7d8b4604b18982630dabd7e44256
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751809"
---
# <a name="iinkanalyzergetnodesfromtextrange-method"></a><span data-ttu-id="7a521-103">Iinkanalyzer:: GetNodesFromTextRange-Methode</span><span class="sxs-lookup"><span data-stu-id="7a521-103">IInkAnalyzer::GetNodesFromTextRange method</span></span>

<span data-ttu-id="7a521-104">Ruft eine Auflistung von [**icontextnode**](icontextnode.md) -Objekten ab, die für den angegebenen Textbereich für die angegebenen Kontext Knoten relevant sind.</span><span class="sxs-lookup"><span data-stu-id="7a521-104">Retrieves a collection of [**IContextNode**](icontextnode.md) objects that are relevant to the specified text range for the specified context nodes.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a521-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a521-105">Syntax</span></span>


```C++
HRESULT GetNodesFromTextRange(
  [in, out] LONG          *plStart,
  [in, out] LONG          *plLength,
  [out]     IContextNodes **ppContextNodes,
  [in]      IContextNodes *pNodesToSearch = defaultvalue
);
```



## <a name="parameters"></a><span data-ttu-id="7a521-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a521-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a521-107">*plstart* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7a521-107">*plStart* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a521-108">Ein Verweis auf den Anfang des Text Bereichs im *pnoentstosearch* -Teil der erkannten Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="7a521-108">A reference to the start of the text range in the *pNodesToSearch* portion of the recognized string.</span></span>

</dd> <dt>

<span data-ttu-id="7a521-109">*pllength* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7a521-109">*plLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a521-110">Ein Verweis auf die Länge des Text Bereichs im *pnoentstosearch* -Teil der erkannten Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="7a521-110">A reference to the length of the text range in the *pNodesToSearch* portion of the recognized string.</span></span>

</dd> <dt>

<span data-ttu-id="7a521-111">*ppcontextnodes* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7a521-111">*ppContextNodes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a521-112">Ein Zeiger auf die [**icontextnode**](icontextnode.md) -Objekte, die für den angegebenen Textbereich für die angegebenen Kontext Knoten relevant sind.</span><span class="sxs-lookup"><span data-stu-id="7a521-112">A pointer to the [**IContextNode**](icontextnode.md) objects that are relevant to the specified text range for the specified context nodes.</span></span>

</dd> <dt>

<span data-ttu-id="7a521-113">*pnodebug Search* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7a521-113">*pNodesToSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a521-114">Die [**icontextnode**](icontextnode.md) -Objekte, auf die die Suche beschränkt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7a521-114">The [**IContextNode**](icontextnode.md) objects to which to limit the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a521-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a521-115">Return value</span></span>

<span data-ttu-id="7a521-116">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="7a521-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7a521-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a521-117">Remarks</span></span>

<span data-ttu-id="7a521-118">Der angegebene Textbereich muss relativ zum " *pnodebug Search* "-Teil der erkannten Zeichenfolge des " [**iinkanalyzer**](iinkanalyzer.md)" und nicht zur erkannten Zeichenfolge des gesamten " **iinkanalyzer**" sein.</span><span class="sxs-lookup"><span data-stu-id="7a521-118">The specified text range should be relative to the *pNodesToSearch* portion of the recognized string of the [**IInkAnalyzer**](iinkanalyzer.md), rather than to the recognized string of the entire **IInkAnalyzer**.</span></span>

<span data-ttu-id="7a521-119">Diese Methode ändert die Werte der *plstart* -und *pllength* -Parameter, indem der Textbereich auf die nächstgelegenen Wortgrenzen erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="7a521-119">This method modifies the values of the *plStart* and *plLength* parameters by expanding the text range to the nearest word boundaries.</span></span>

<span data-ttu-id="7a521-120">Wenn die erkannte Zeichenfolge z. b. "I am late" lautet und Sie diese Methode mit den Parameterwerten 6 für *plstart* und 1 für *pllength* aufrufen, was dem Buchstaben "a" in "Late" entspricht, gibt diese Methode eine Auflistung mit einem einzelnen [**icontextnode**](icontextnode.md), dem InkWord oder textword zurück, das dem Wort "Late" entspricht.</span><span class="sxs-lookup"><span data-stu-id="7a521-120">For example, if the recognized string is "I am late" and you call this method using the parameter values of 6 for *plStart* and 1 for *plLength*, which corresponds to the letter "a" in "late", this method returns a collection containing a single [**IContextNode**](icontextnode.md), the InkWord or TextWord that corresponds to the word "late".</span></span> <span data-ttu-id="7a521-121">In diesem Beispiel ändert diese Methode auch den Wert von *plstart* in 5 und den Wert von *pllength* in 4, was dem Wort "Late" entspricht.</span><span class="sxs-lookup"><span data-stu-id="7a521-121">For this example, this method also modifies the value of *plStart* to 5 and the value of *plLength* to 4, which corresponds to the word "late".</span></span>

> [!Note]  
> <span data-ttu-id="7a521-122">Der *plstart* -Parameter ist relativ zur erkannten Zeichenfolge des *pnodebug Search* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="7a521-122">The *plStart* parameter is relative to the recognized string of the *pNodesToSearch* parameter.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7a521-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a521-123">Requirements</span></span>



| <span data-ttu-id="7a521-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a521-124">Requirement</span></span> | <span data-ttu-id="7a521-125">Wert</span><span class="sxs-lookup"><span data-stu-id="7a521-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a521-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7a521-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7a521-127">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7a521-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7a521-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7a521-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7a521-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7a521-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7a521-130">Header</span><span class="sxs-lookup"><span data-stu-id="7a521-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a521-131"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7a521-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7a521-132">DLL</span><span class="sxs-lookup"><span data-stu-id="7a521-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a521-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a521-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="7a521-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a521-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a521-135">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="7a521-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> </dl>

 

 




