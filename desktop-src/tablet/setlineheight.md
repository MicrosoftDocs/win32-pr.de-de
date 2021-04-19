---
description: Legt die LineHeight-Eigenschaft für das InkDivider-Objekt fest.
ms.assetid: ce5e40c5-faa1-4d66-94f4-d5bd1a11ee4c
title: SetLineHeight-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetLineHeight
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: be4045e01ac890471536d95768668b633d8f2249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362599"
---
# <a name="setlineheight-function"></a><span data-ttu-id="1bca4-103">SetLineHeight-Funktion</span><span class="sxs-lookup"><span data-stu-id="1bca4-103">SetLineHeight function</span></span>

<span data-ttu-id="1bca4-104">Legt die [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) -Eigenschaft für das [**InkDivider**](inkdivider-class.md) -Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="1bca4-104">Sets the [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) property on the [**InkDivider**](inkdivider-class.md) object.</span></span>

<span data-ttu-id="1bca4-105">Diese Hilfsfunktion ist nicht für die Verwendung durch den Anwendungscode vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="1bca4-105">This helper function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bca4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bca4-106">Syntax</span></span>


```C++
HRESULT WINAPI SetLineHeight(
  _In_ INT_PTR hDivider,
  _In_ LONG    lLineHeight
);
```



## <a name="parameters"></a><span data-ttu-id="1bca4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1bca4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bca4-108">*hdivider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1bca4-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bca4-109">Ein Handle für das [**InkDivider**](inkdivider-class.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="1bca4-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="1bca4-110">*llineheight* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1bca4-110">*lLineHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bca4-111">Die [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) -Eigenschaft des [**InkDivider**](inkdivider-class.md) -Objekts in HIMETRIC-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="1bca4-111">The [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) property of the [**InkDivider**](inkdivider-class.md) object, in HIMETRIC units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bca4-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1bca4-112">Return value</span></span>

<span data-ttu-id="1bca4-113">Diese Funktion kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="1bca4-113">This function can return one of these values.</span></span>



| <span data-ttu-id="1bca4-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1bca4-114">Return code</span></span>                                                                                  | <span data-ttu-id="1bca4-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1bca4-115">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="1bca4-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1bca4-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="1bca4-117">Die Funktion wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1bca4-117">The function succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="1bca4-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="1bca4-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="1bca4-119">Der *pdivider* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="1bca4-119">The *pDivider* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1bca4-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1bca4-120">Requirements</span></span>



| <span data-ttu-id="1bca4-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1bca4-121">Requirement</span></span> | <span data-ttu-id="1bca4-122">Wert</span><span class="sxs-lookup"><span data-stu-id="1bca4-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1bca4-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1bca4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1bca4-124">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1bca4-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="1bca4-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1bca4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1bca4-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1bca4-126">None supported</span></span><br/>                                                             |
| <span data-ttu-id="1bca4-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1bca4-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="1bca4-128"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1bca4-128"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 
