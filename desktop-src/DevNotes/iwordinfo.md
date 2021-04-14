---
description: Die iwordinfo-Schnittstelle ist eine Japanisch-spezifische Sprachressourcen Komponente. Das-Objekt analysiert Text und identifiziert einzelne Wörter, wobei entweder die Wörter in der Zeichenfolge zurückgegeben werden oder die Wörterbuch Formen (root) der Wörter im Text der Zeichenfolge zurückgegeben werden.
ms.assetid: 760d9c78-d564-40a2-b2e4-d538c32361ed
title: Iwordinfo-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordInfo
- IWordInfo.BreakText
api_type:
- COM
api_location:
- Msir3jp.dll
ms.openlocfilehash: 9d685f2aa1b4ba4d31f221812c12729e4e689360
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522976"
---
# <a name="iwordinfo-interface"></a><span data-ttu-id="9d677-104">Iwordinfo-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9d677-104">IWordInfo interface</span></span>

<span data-ttu-id="9d677-105">\[Diese Schnittstelle ist veraltet und wird unter Windows Vista nicht unterstützt.\]</span><span class="sxs-lookup"><span data-stu-id="9d677-105">\[This interface is obsolete and is not supported on Windows Vista.\]</span></span>

<span data-ttu-id="9d677-106">Die **iwordinfo** -Schnittstelle ist eine Japanisch-spezifische Sprachressourcen Komponente.</span><span class="sxs-lookup"><span data-stu-id="9d677-106">The **IWordInfo** interface is a Japanese-specific language resource component.</span></span> <span data-ttu-id="9d677-107">Das-Objekt analysiert Text und identifiziert einzelne Wörter, wobei entweder die Wörter in der Zeichenfolge zurückgegeben werden oder die Wörterbuch Formen (root) der Wörter im Text der Zeichenfolge zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9d677-107">The object parses text and identifies individual words, returning either the words in the string or returns the dictionary (root) forms of the words in the text of the string.</span></span>

## <a name="members"></a><span data-ttu-id="9d677-108">Member</span><span class="sxs-lookup"><span data-stu-id="9d677-108">Members</span></span>

<span data-ttu-id="9d677-109">Die **iwordinfo** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="9d677-109">The **IWordInfo** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9d677-110">**Iwordinfo** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9d677-110">**IWordInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="9d677-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="9d677-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9d677-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="9d677-112">Methods</span></span>

<span data-ttu-id="9d677-113">Die **iwordinfo** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="9d677-113">The **IWordInfo** interface has these methods.</span></span>



| <span data-ttu-id="9d677-114">Methode</span><span class="sxs-lookup"><span data-stu-id="9d677-114">Method</span></span>        | <span data-ttu-id="9d677-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9d677-115">Description</span></span>                                                                                                                                 |
|:--------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d677-116">**Halte Text**</span><span class="sxs-lookup"><span data-stu-id="9d677-116">**BreakText**</span></span> | <span data-ttu-id="9d677-117">Analysiert Text, um die Wörter zu identifizieren, und stellt die Ergebnisse für das [wordsink](/previous-versions//ms691570(v=vs.85)) -Objekt bereit.</span><span class="sxs-lookup"><span data-stu-id="9d677-117">Parses text to identify words and provides the results to the [WordSink](/previous-versions//ms691570(v=vs.85)) object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9d677-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d677-118">Remarks</span></span>

<span data-ttu-id="9d677-119">Diese Schnittstelle wird verwendet, um japanische Wort Umbrüche oder Wörterbuch Formulare für den zu analysierenden Text abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9d677-119">This interface is used to retrieve Japanese word breaks or dictionary forms for the text to be analyzed.</span></span> <span data-ttu-id="9d677-120">Die Wörterbuch Form eines Worts ist die unflexions Form des Worts.</span><span class="sxs-lookup"><span data-stu-id="9d677-120">The dictionary form of a word is the uninflected form of the word.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d677-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d677-121">Requirements</span></span>



| <span data-ttu-id="9d677-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d677-122">Requirement</span></span> | <span data-ttu-id="9d677-123">Wert</span><span class="sxs-lookup"><span data-stu-id="9d677-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d677-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9d677-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9d677-125">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d677-125">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="9d677-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9d677-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9d677-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d677-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9d677-128">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="9d677-128">End of client support</span></span><br/>    | <span data-ttu-id="9d677-129">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9d677-129">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="9d677-130">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="9d677-130">End of server support</span></span><br/>    | <span data-ttu-id="9d677-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9d677-131">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="9d677-132">DLL</span><span class="sxs-lookup"><span data-stu-id="9d677-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d677-133"><dt>Msir3jp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d677-133"><dt>Msir3jp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d677-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d677-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d677-135">**WordInfo**</span><span class="sxs-lookup"><span data-stu-id="9d677-135">**WordInfo**</span></span>](wordinfo-coclass.md)
</dt> <dt>

<span data-ttu-id="9d677-136">[Wordsink](/previous-versions//ms691570(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9d677-136">[WordSink](/previous-versions//ms691570(v=vs.85))</span></span>
</dt> </dl>

 

 
