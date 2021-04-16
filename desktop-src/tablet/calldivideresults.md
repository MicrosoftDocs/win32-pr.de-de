---
description: Ruft Analyseergebnisse aus dem InkDivider-Objekt ab.
ms.assetid: 7fc2bb5a-172f-4f4e-84dd-e31925f86982
title: Calldivideresults-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivideResults
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 11878e6a0ac953b9b7eb27ce21bb67001f9d88d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127820"
---
# <a name="calldivideresults-function"></a><span data-ttu-id="f0cde-103">Calldivideresults-Funktion</span><span class="sxs-lookup"><span data-stu-id="f0cde-103">CallDivideResults function</span></span>

<span data-ttu-id="f0cde-104">Ruft Analyseergebnisse aus dem [**InkDivider**](inkdivider-class.md) -Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="f0cde-104">Retrieves analysis results from the [**InkDivider**](inkdivider-class.md) object.</span></span>

<span data-ttu-id="f0cde-105">Diese Funktion ist nicht für die Verwendung durch den Anwendungscode vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="f0cde-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0cde-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0cde-106">Syntax</span></span>


```C++
HRESULT WINAPI CallDivideResults(
  _In_  INT_PTR   hDivider,
  _Out_ int       aWordStrokeIds[],
  _Out_ int       aLineStrokeIds[],
  _Out_ int       aParagraphStrokeIds[],
  _Out_ int       aDrawingStrokeIds[],
  _Out_ SAFEARRAY **pastrWords,
  _Out_ SAFEARRAY **pastrLines,
  _Out_ SAFEARRAY **pastrParagraphs,
  _Out_ int       *aWordRotationCenterX,
  _Out_ int       *aWordRotationCenterY,
  _Out_ float     *aWordAngle,
  _Out_ int       *aLineRotationCenterX,
  _Out_ int       *aLineRotationCenterY,
  _Out_ float     *aLineAngle
);
```



## <a name="parameters"></a><span data-ttu-id="f0cde-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0cde-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0cde-108">*hdivider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0cde-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0cde-109">Ein Handle für das [**InkDivider**](inkdivider-class.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="f0cde-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="f0cde-110">*awordstrokeids* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f0cde-110">*aWordStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0cde-111">Ein Array von Bezeichner, die dem Wort zugeordnet sind, das an die [**InkDivider**](inkdivider-class.md) -Klasse weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="f0cde-111">An array of identifiers associated with the word that is passed in to the [**InkDivider**](inkdivider-class.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="f0cde-112">*alinestrokeids* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f0cde-112">*aLineStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0cde-113">Ein Array von [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) -Eigenschaften für die [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekte, die der Zeile zugeordnet sind, die an die [**InkDivider**](inkdivider-class.md) -Klasse weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="f0cde-113">An array of [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) properties for the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects associated with the line that is passed in to the [**InkDivider**](inkdivider-class.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="f0cde-114">*aparagphstrokeids* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f0cde-114">*aParagraphStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0cde-115">Ein Array der [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) -Eigenschaften für die [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekte, die dem Absatz der [**InkDivider**](inkdivider-class.md) -Klasse zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f0cde-115">An array of the [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) properties for the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects associated with the paragraph from the [**InkDivider**](inkdivider-class.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="f0cde-116">*adrawingstrokeids* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f0cde-116">*aDrawingStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0cde-117">Ein Array von [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) -Eigenschaften für die [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekte, die der Zeichnung aus der [**InkDivider**](inkdivider-class.md) -Klasse zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f0cde-117">An array of [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) properties for the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects associated with the drawing from the [**InkDivider**](inkdivider-class.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="f0cde-118">*paarwörter* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f0cde-118">*pastrWords* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0cde-119">Ein Array von Wörtern, das von der Ink-Analyse zurückgegeben wird</span><span class="sxs-lookup"><span data-stu-id="f0cde-119">An array of words returned from ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="f0cde-120">*Paare* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f0cde-120">*pastrLines* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0cde-121">Ein Array von Zeilen, die von der Ink-Analyse zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="f0cde-121">An array of lines returned from ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="f0cde-122">*Paare* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f0cde-122">*pastrParagraphs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0cde-123">Ein Array von Absätzen, die von der Ink-Analyse zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="f0cde-123">An array of paragraphs returned from ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="f0cde-124">*awordrotationcenterx* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f0cde-124">*aWordRotationCenterX* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0cde-125">Ein Array von den Mittelpunkten der Wörter entlang der x-Achse aus der Ink-Analyse.</span><span class="sxs-lookup"><span data-stu-id="f0cde-125">An array of the center points of the words along the x-axis from ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="f0cde-126">*awordrotationcentery* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f0cde-126">*aWordRotationCenterY* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0cde-127">Ein Array von den Mittelpunkten der Wörter entlang der y-Achse aus der Ink-Analyse.</span><span class="sxs-lookup"><span data-stu-id="f0cde-127">An array of the center points of the words along the y-axis from ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="f0cde-128">*awordangle* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f0cde-128">*aWordAngle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0cde-129">Ein Array mit den Winkeln, nach denen die Wörter für optimale Analyseergebnisse gedreht werden.</span><span class="sxs-lookup"><span data-stu-id="f0cde-129">An array containing the angles by which to rotate the words for best analysis results.</span></span>

</dd> <dt>

<span data-ttu-id="f0cde-130">*alinerotationcenterx* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f0cde-130">*aLineRotationCenterX* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0cde-131">Ein Array, das die Mittelpunkte der Linien entlang der x-Achse enthält.</span><span class="sxs-lookup"><span data-stu-id="f0cde-131">An array containing the center points of the lines along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="f0cde-132">*alinerotationcentery* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f0cde-132">*aLineRotationCenterY* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0cde-133">Ein Array, das die Mittelpunkte der Linien entlang der y-Achse enthält.</span><span class="sxs-lookup"><span data-stu-id="f0cde-133">An array containing the center points of the lines along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="f0cde-134">*alineangle* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f0cde-134">*aLineAngle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0cde-135">Ein Array, das die Winkel enthält, nach denen die Linien für optimale Analyseergebnisse gedreht werden.</span><span class="sxs-lookup"><span data-stu-id="f0cde-135">An array containing the angles by which to rotate the lines for best analysis results.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0cde-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f0cde-136">Return value</span></span>

<span data-ttu-id="f0cde-137">Diese Funktion kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f0cde-137">This function can return one of these values.</span></span>



| <span data-ttu-id="f0cde-138">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f0cde-138">Return code</span></span>                                                                                   | <span data-ttu-id="f0cde-139">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f0cde-139">Description</span></span>                                                       |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="f0cde-140"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f0cde-140"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f0cde-141">Die Funktion wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f0cde-141">The function succeeded.</span></span><br/>                                |
| <dl> <span data-ttu-id="f0cde-142"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="f0cde-142"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="f0cde-143">Der *hdivider* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="f0cde-143">The *hDivider* parameter is invalid.</span></span><br/>                   |
| <dl> <span data-ttu-id="f0cde-144"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="f0cde-144"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f0cde-145">Es konnte nicht genügend Arbeitsspeicher belegt werden, um die Ergebnisse zu speichern.</span><span class="sxs-lookup"><span data-stu-id="f0cde-145">Could not allocate enough memory to store the results.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f0cde-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f0cde-146">Remarks</span></span>

<span data-ttu-id="f0cde-147">Um Speicher Verluste zu vermeiden, müssen Sie die Ressourcen für " *paarweise*", " *paarweise*" und " *paarweise*" freigeben.</span><span class="sxs-lookup"><span data-stu-id="f0cde-147">To avoid memory leaks you must release the resources for *pastrWords*, *pastrLines*, and *pastrParagraphs*.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0cde-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0cde-148">Requirements</span></span>



| <span data-ttu-id="f0cde-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0cde-149">Requirement</span></span> | <span data-ttu-id="f0cde-150">Wert</span><span class="sxs-lookup"><span data-stu-id="f0cde-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f0cde-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f0cde-151">Minimum supported client</span></span><br/> | <span data-ttu-id="f0cde-152">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0cde-152">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="f0cde-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f0cde-153">Minimum supported server</span></span><br/> | <span data-ttu-id="f0cde-154">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f0cde-154">None supported</span></span><br/>                                                             |
| <span data-ttu-id="f0cde-155">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f0cde-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="f0cde-156"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0cde-156"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




