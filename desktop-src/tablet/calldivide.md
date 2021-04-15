---
description: Ruft Analyse Informationen aus dem InkDivider-Objekt ab.
ms.assetid: 1b073da4-80f4-48f4-8ff6-b21793c173a8
title: Calldivide-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivide
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 0084811ee471bee8fe67653dace49fa83642a7fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524403"
---
# <a name="calldivide-function"></a><span data-ttu-id="85d66-103">Calldivide-Funktion</span><span class="sxs-lookup"><span data-stu-id="85d66-103">CallDivide function</span></span>

<span data-ttu-id="85d66-104">Ruft Analyse Informationen aus dem [**InkDivider**](inkdivider-class.md) -Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="85d66-104">Retrieves analysis information from the [**InkDivider**](inkdivider-class.md) object.</span></span>

<span data-ttu-id="85d66-105">Diese Funktion ist nicht für die Verwendung durch den Anwendungscode vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="85d66-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="85d66-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="85d66-106">Syntax</span></span>


```C++
HRESULT WINAPI CallDivide(
  _In_  INT_PTR hDivider,
  _In_  int     *pWordSize,
  _In_  int     *pLineSize,
  _In_  int     *pParagraphSize,
  _In_  int     *pDrawingSize,
  _Out_ int     *pWordCount,
  _Out_ int     *pLineCount,
  _Out_ int     *pParagraphCount
);
```



## <a name="parameters"></a><span data-ttu-id="85d66-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="85d66-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85d66-108">*hdivider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85d66-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85d66-109">Ein Handle für das [**InkDivider**](inkdivider-class.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="85d66-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="85d66-110">*pwordsize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85d66-110">*pWordSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85d66-111">Die Größe des vom [**InkDivider**](inkdivider-class.md) -Objekt zurückgegebenen Worts.</span><span class="sxs-lookup"><span data-stu-id="85d66-111">The size of the word returned by the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="85d66-112">*plinesize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85d66-112">*pLineSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85d66-113">Die Größe der Zeile, die vom [**InkDivider**](inkdivider-class.md) -Objekt zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="85d66-113">The size of the line returned by the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="85d66-114">*pparagphsize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85d66-114">*pParagraphSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85d66-115">Die Größe des vom [**InkDivider**](inkdivider-class.md) -Objekt zurückgegebenen Absatzes.</span><span class="sxs-lookup"><span data-stu-id="85d66-115">The size of the paragraph returned by the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="85d66-116">*pdrawingsize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85d66-116">*pDrawingSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85d66-117">Die Größe der Zeichnung, die vom [**InkDivider**](inkdivider-class.md) -Objekt zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="85d66-117">The size of the drawing returned by the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="85d66-118">*pwordcount* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="85d66-118">*pWordCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85d66-119">Die Anzahl der von der Ink-Analyse zurückgegebenen Wörter.</span><span class="sxs-lookup"><span data-stu-id="85d66-119">The number of words returned by ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="85d66-120">*plinecount* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="85d66-120">*pLineCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85d66-121">Die Anzahl der Zeilen, die von der Ink-Analyse zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="85d66-121">The number of lines returned by ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="85d66-122">*pparagphcount* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="85d66-122">*pParagraphCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85d66-123">Die Anzahl von Absätzen, die von der Ink-Analyse zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="85d66-123">The number of paragraphs returned by ink analysis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85d66-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="85d66-124">Return value</span></span>

<span data-ttu-id="85d66-125">Diese Funktion kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="85d66-125">This function can return one of these values.</span></span>



| <span data-ttu-id="85d66-126">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="85d66-126">Return code</span></span>                                                                                  | <span data-ttu-id="85d66-127">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="85d66-127">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="85d66-128"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="85d66-128"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="85d66-129">Die Funktion, die unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="85d66-129">The function suceeded.</span></span><br/>              |
| <dl> <span data-ttu-id="85d66-130"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="85d66-130"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="85d66-131">Mindestens ein Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="85d66-131">One or more parameters are invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="85d66-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85d66-132">Requirements</span></span>



| <span data-ttu-id="85d66-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85d66-133">Requirement</span></span> | <span data-ttu-id="85d66-134">Wert</span><span class="sxs-lookup"><span data-stu-id="85d66-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="85d66-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="85d66-135">Minimum supported client</span></span><br/> | <span data-ttu-id="85d66-136">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85d66-136">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="85d66-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="85d66-137">Minimum supported server</span></span><br/> | <span data-ttu-id="85d66-138">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="85d66-138">None supported</span></span><br/>                                                             |
| <span data-ttu-id="85d66-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="85d66-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="85d66-140"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85d66-140"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




