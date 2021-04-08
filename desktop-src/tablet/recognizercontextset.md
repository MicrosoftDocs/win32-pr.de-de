---
description: Testet, ob das InkDivider-Objekt die inkrecognizercontext-Klasse zum Analysieren von Wörtern verwenden kann.
ms.assetid: fd848fcc-5258-401f-8b51-b9d57da173da
title: Erkennzercontextset-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognizerContextSet
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 51e75b810c2103afed2e8ac8a28706b9c9af5da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865812"
---
# <a name="recognizercontextset-function"></a><span data-ttu-id="bb5ab-103">Erkennzercontextset-Funktion</span><span class="sxs-lookup"><span data-stu-id="bb5ab-103">RecognizerContextSet function</span></span>

<span data-ttu-id="bb5ab-104">Testet, ob das [**InkDivider**](inkdivider-class.md) -Objekt die [**inkrecognizercontext**](inkrecognizercontext-class.md) -Klasse zum Analysieren von Wörtern verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="bb5ab-104">Tests whether the [**InkDivider**](inkdivider-class.md) object can use the [**InkRecognizerContext**](inkrecognizercontext-class.md) class to analyze words.</span></span>

<span data-ttu-id="bb5ab-105">Diese Funktion ist nicht für die Verwendung durch den Anwendungscode vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="bb5ab-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb5ab-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb5ab-106">Syntax</span></span>


```C++
HRESULT WINAPI RecognizerContextSet(
  _In_ INT_PTR hDivider
);
```



## <a name="parameters"></a><span data-ttu-id="bb5ab-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb5ab-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb5ab-108">*hdivider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb5ab-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb5ab-109">Ein Handle für das [**InkDivider**](inkdivider-class.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="bb5ab-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb5ab-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bb5ab-110">Return value</span></span>

<span data-ttu-id="bb5ab-111">Diese Funktion kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="bb5ab-111">This function can return one of these values.</span></span>



| <span data-ttu-id="bb5ab-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="bb5ab-112">Return code</span></span>                                                                                  | <span data-ttu-id="bb5ab-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bb5ab-113">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="bb5ab-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bb5ab-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="bb5ab-115">Die Funktion wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bb5ab-115">The function succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="bb5ab-116"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="bb5ab-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="bb5ab-117">Der *pdivider* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="bb5ab-117">The *pDivider* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bb5ab-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb5ab-118">Requirements</span></span>



| <span data-ttu-id="bb5ab-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb5ab-119">Requirement</span></span> | <span data-ttu-id="bb5ab-120">Wert</span><span class="sxs-lookup"><span data-stu-id="bb5ab-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb5ab-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bb5ab-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bb5ab-122">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bb5ab-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="bb5ab-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bb5ab-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bb5ab-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="bb5ab-124">None supported</span></span><br/>                                                             |
| <span data-ttu-id="bb5ab-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bb5ab-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="bb5ab-126"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb5ab-126"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




