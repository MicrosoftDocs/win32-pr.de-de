---
description: Fügt dem InkDivider-Objekt ein neues IInkStrokeDisp-Objekt hinzu, das weitergegeben wurde.
ms.assetid: d5b82244-68d5-4137-aaf4-d3232f7c0779
title: Addonestroke-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddOneStroke
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 0af3913f2579363afbb0c3985ad0f40f58051eac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483998"
---
# <a name="addonestroke-function"></a><span data-ttu-id="5b1c7-103">Addonestroke-Funktion</span><span class="sxs-lookup"><span data-stu-id="5b1c7-103">AddOneStroke function</span></span>

<span data-ttu-id="5b1c7-104">Fügt dem [**InkDivider**](inkdivider-class.md) -Objekt ein neues [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt hinzu, das weitergegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="5b1c7-104">Adds a new [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object to the [**InkDivider**](inkdivider-class.md) object that was passed in.</span></span>

<span data-ttu-id="5b1c7-105">Diese Funktion ist nicht für die Verwendung durch den Anwendungscode vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="5b1c7-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b1c7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b1c7-106">Syntax</span></span>


```C++
HRESULT WINAPI AddOneStroke(
  _In_ INT_PTR hDivider,
  _In_ int     strokeId,
  _In_ int     cPoints,
  _In_ POINT   *aPoints
);
```



## <a name="parameters"></a><span data-ttu-id="5b1c7-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b1c7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b1c7-108">*hdivider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b1c7-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b1c7-109">Ein Handle für das [**InkDivider**](inkdivider-class.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="5b1c7-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="5b1c7-110">*strokeid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b1c7-110">*strokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b1c7-111">Die [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) des [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekts, das dem [**InkDivider**](inkdivider-class.md) -Objekt hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5b1c7-111">The [**Id**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) of the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object to be added to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="5b1c7-112">*CPoints* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b1c7-112">*cPoints* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b1c7-113">Die Anzahl der Pakete, die das neue [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt bilden.</span><span class="sxs-lookup"><span data-stu-id="5b1c7-113">The number of packets that make up the new [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="5b1c7-114">*apoints* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b1c7-114">*aPoints* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b1c7-115">Das Array von Paketen, die das [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt in *strokeid* bilden.</span><span class="sxs-lookup"><span data-stu-id="5b1c7-115">The array of packets that make up the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object in *strokeId*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b1c7-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5b1c7-116">Return value</span></span>

<span data-ttu-id="5b1c7-117">Diese Funktion kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="5b1c7-117">This function can return one of these values.</span></span>



| <span data-ttu-id="5b1c7-118">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="5b1c7-118">Return code</span></span>                                                                                  | <span data-ttu-id="5b1c7-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5b1c7-119">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="5b1c7-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5b1c7-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="5b1c7-121">Die Funktion wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5b1c7-121">The function succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="5b1c7-122"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="5b1c7-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="5b1c7-123">Der *hdivider* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="5b1c7-123">The *hDivider* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5b1c7-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5b1c7-124">Requirements</span></span>



| <span data-ttu-id="5b1c7-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5b1c7-125">Requirement</span></span> | <span data-ttu-id="5b1c7-126">Wert</span><span class="sxs-lookup"><span data-stu-id="5b1c7-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5b1c7-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5b1c7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5b1c7-128">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5b1c7-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="5b1c7-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5b1c7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5b1c7-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5b1c7-130">None supported</span></span><br/>                                                             |
| <span data-ttu-id="5b1c7-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5b1c7-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="5b1c7-132"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b1c7-132"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




