---
description: Ruft die ID-Eigenschaften für die IInkStrokeDisp-Objekte des entsprechenden Worts, der Zeile, des Absatzes oder der Zeichnung ab, die durch eine Handschrift Analyse bestimmt werden.
ms.assetid: f05ffa3b-2a47-46fe-bb8f-e682aa094b69
title: Calldivideresultstrokeids-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivideResultsStrokeIds
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: ee690c9564df3b8c75eca6eec8eeb88b7531f4ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344630"
---
# <a name="calldivideresultsstrokeids-function"></a><span data-ttu-id="024b6-103">Calldivideresultstrokeids-Funktion</span><span class="sxs-lookup"><span data-stu-id="024b6-103">CallDivideResultsStrokeIds function</span></span>

<span data-ttu-id="024b6-104">Ruft die [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) -Eigenschaften für die [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekte des entsprechenden Worts, der Zeile, des Absatzes oder der Zeichnung ab, die durch eine Handschrift Analyse bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="024b6-104">Retrieves the [**Id**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) properties for the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects of the corresponding word, line, paragraph, or drawing determined by ink analysis.</span></span>

<span data-ttu-id="024b6-105">Diese Funktion ist nicht für die Verwendung durch den Anwendungscode vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="024b6-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="024b6-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="024b6-106">Syntax</span></span>


```C++
HRESULT WINAPI CallDivideResultsStrokeIds(
  _In_  INT_PTR hDivider,
  _Out_ int     aWordStrokeIds[],
  _Out_ int     aLineStrokeIds[],
  _Out_ int     aParagraphStrokeIds[],
  _Out_ int     aDrawingStrokeIds[]
);
```



## <a name="parameters"></a><span data-ttu-id="024b6-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="024b6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="024b6-108">*hdivider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="024b6-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="024b6-109">Ein Handle für das [Divider](the-divider-object.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="024b6-109">A handle to the [Divider](the-divider-object.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="024b6-110">*awordstrokeids \[ \]* \[out\]</span><span class="sxs-lookup"><span data-stu-id="024b6-110">*aWordStrokeIds\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="024b6-111">Ein Array der Strich-IDs der frei Hand Eingaben im Wort.</span><span class="sxs-lookup"><span data-stu-id="024b6-111">An array of the stroke IDs of the ink in the word.</span></span>

</dd> <dt>

<span data-ttu-id="024b6-112">*alinestrokeids \[ \]* \[out\]</span><span class="sxs-lookup"><span data-stu-id="024b6-112">*aLineStrokeIds\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="024b6-113">Ein Array der Strich-IDs der frei Hand Eingabe in der Zeile.</span><span class="sxs-lookup"><span data-stu-id="024b6-113">An array of the stroke IDs of the ink in the line.</span></span>

</dd> <dt>

<span data-ttu-id="024b6-114">*aparagphstrokeids \[ \]* \[out\]</span><span class="sxs-lookup"><span data-stu-id="024b6-114">*aParagraphStrokeIds\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="024b6-115">Ein Array der Strich-IDs der frei Hand Eingaben im Absatz.</span><span class="sxs-lookup"><span data-stu-id="024b6-115">An array of the stroke IDs of the ink in the paragraph.</span></span>

</dd> <dt>

<span data-ttu-id="024b6-116">*adrawingstrokeids \[ \]* \[out\]</span><span class="sxs-lookup"><span data-stu-id="024b6-116">*aDrawingStrokeIds\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="024b6-117">Ein Array der Strich-IDs der frei Hand Eingaben in der Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="024b6-117">An array of the stroke IDs of the ink in the drawing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="024b6-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="024b6-118">Return value</span></span>

<span data-ttu-id="024b6-119">Diese Funktion kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="024b6-119">This function can return one of these values.</span></span>



| <span data-ttu-id="024b6-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="024b6-120">Return code</span></span>                                                                                  | <span data-ttu-id="024b6-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="024b6-121">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="024b6-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="024b6-122"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="024b6-123">Die Funktion wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="024b6-123">The function succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="024b6-124"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="024b6-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="024b6-125">Der *hdivider* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="024b6-125">The *hDivider* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="024b6-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="024b6-126">Requirements</span></span>



| <span data-ttu-id="024b6-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="024b6-127">Requirement</span></span> | <span data-ttu-id="024b6-128">Wert</span><span class="sxs-lookup"><span data-stu-id="024b6-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="024b6-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="024b6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="024b6-130">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="024b6-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="024b6-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="024b6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="024b6-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="024b6-132">None supported</span></span><br/>                                                             |
| <span data-ttu-id="024b6-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="024b6-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="024b6-134"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="024b6-134"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




