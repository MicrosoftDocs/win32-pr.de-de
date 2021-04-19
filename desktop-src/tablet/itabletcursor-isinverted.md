---
description: Gibt an, ob der Tablettstift aufwärts unten ist.
ms.assetid: 04b05287-000d-455f-88e5-821c7fdb8119
title: 'Itabletcursor:: isinvertierte-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.IsInverted
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 041b81c38f3370421c96a4c0d66201254a715e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364072"
---
# <a name="itabletcursorisinverted-method"></a><span data-ttu-id="2abae-103">Itabletcursor:: isinvertierte-Methode</span><span class="sxs-lookup"><span data-stu-id="2abae-103">ITabletCursor::IsInverted method</span></span>

<span data-ttu-id="2abae-104">Gibt an, ob der Tablettstift aufwärts unten ist.</span><span class="sxs-lookup"><span data-stu-id="2abae-104">Indicates if the stylus is upside down.</span></span>

## <a name="syntax"></a><span data-ttu-id="2abae-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2abae-105">Syntax</span></span>


```C++
HRESULT IsInverted();
```



## <a name="parameters"></a><span data-ttu-id="2abae-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2abae-106">Parameters</span></span>

<span data-ttu-id="2abae-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="2abae-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2abae-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2abae-108">Return value</span></span>

<span data-ttu-id="2abae-109">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="2abae-109">This method can return one of these values.</span></span>



| <span data-ttu-id="2abae-110">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="2abae-110">Return code</span></span>                                                                             | <span data-ttu-id="2abae-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2abae-111">Description</span></span>                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="2abae-112"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2abae-112"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="2abae-113">Der Tablettstift ist invertiert.</span><span class="sxs-lookup"><span data-stu-id="2abae-113">The stylus is inverted.</span></span><br/>        |
| <dl> <span data-ttu-id="2abae-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="2abae-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="2abae-115">Der Tablettstift wird nicht invertiert.</span><span class="sxs-lookup"><span data-stu-id="2abae-115">The stylus is not inverted.</span></span><br/>    |
| <dl> <span data-ttu-id="2abae-116"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="2abae-116"><dt>**E\_FAIL**</dt></span></span> </dl>  | <span data-ttu-id="2abae-117">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="2abae-117">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2abae-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2abae-118">Requirements</span></span>



| <span data-ttu-id="2abae-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2abae-119">Requirement</span></span> | <span data-ttu-id="2abae-120">Wert</span><span class="sxs-lookup"><span data-stu-id="2abae-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2abae-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2abae-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2abae-122">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2abae-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2abae-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2abae-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2abae-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2abae-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="2abae-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2abae-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="2abae-126"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2abae-126"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2abae-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2abae-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2abae-128">**Itabletcursor**</span><span class="sxs-lookup"><span data-stu-id="2abae-128">**ITabletCursor**</span></span>](itabletcursor.md)
</dt> <dt>

[<span data-ttu-id="2abae-129">**Itabletcursor Button-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="2abae-129">**ITabletCursorButton Interface**</span></span>](itabletcursorbutton.md)
</dt> </dl>

 

 




