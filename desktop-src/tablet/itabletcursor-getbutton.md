---
description: Ruft das angegebene Schaltflächen Objekt aus einem Tablet Tablettstift ab.
ms.assetid: 83a26703-4501-4f43-9e86-c5c753347012
title: 'Itabletcursor:: getbutton-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetButton
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 0b9e8e1337cacdb26d8c124d10e0a886748e70fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349352"
---
# <a name="itabletcursorgetbutton-method"></a><span data-ttu-id="9645e-103">Itabletcursor:: getbutton-Methode</span><span class="sxs-lookup"><span data-stu-id="9645e-103">ITabletCursor::GetButton method</span></span>

<span data-ttu-id="9645e-104">Ruft das angegebene Schaltflächen Objekt aus einem Tablet Tablettstift ab.</span><span class="sxs-lookup"><span data-stu-id="9645e-104">Retrieves the specified button object from a tablet stylus.</span></span>

## <a name="syntax"></a><span data-ttu-id="9645e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9645e-105">Syntax</span></span>


```C++
HRESULT GetButton(
  [in]  ULONG               iButton,
  [out] ITabletCursorButton **ppButton
);
```



## <a name="parameters"></a><span data-ttu-id="9645e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9645e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9645e-107">*iButton* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9645e-107">*iButton* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9645e-108">Der Bezeichner der abzurufenden Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="9645e-108">Identifier of the button to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="9645e-109">*ppbutton* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9645e-109">*ppButton* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9645e-110">Das durch den *iButton* -Parameter angegebene Schaltflächen Objekt.</span><span class="sxs-lookup"><span data-stu-id="9645e-110">The button object specified by the *iButton* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9645e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9645e-111">Return value</span></span>

<span data-ttu-id="9645e-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="9645e-112">This method can return one of these values.</span></span>



| <span data-ttu-id="9645e-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9645e-113">Return code</span></span>                                                                            | <span data-ttu-id="9645e-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9645e-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="9645e-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9645e-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="9645e-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="9645e-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="9645e-117"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="9645e-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="9645e-118">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="9645e-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9645e-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9645e-119">Requirements</span></span>



| <span data-ttu-id="9645e-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9645e-120">Requirement</span></span> | <span data-ttu-id="9645e-121">Wert</span><span class="sxs-lookup"><span data-stu-id="9645e-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9645e-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9645e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9645e-123">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9645e-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9645e-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9645e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9645e-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9645e-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9645e-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9645e-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="9645e-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9645e-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9645e-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9645e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9645e-129">**Itabletcursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="9645e-129">**ITabletCursor Interface**</span></span>](itabletcursor.md)
</dt> </dl>

 

 




