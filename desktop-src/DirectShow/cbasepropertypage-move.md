---
description: 'Die Move-Methode positioniert und ändert die Größe des Dialog Felds. Diese Methode implementiert die IPropertyPage:: Move-Methode.'
ms.assetid: b6cabb5c-196d-489b-9dd4-194d26f4de83
title: Cbasepropertypage. Move-Methode (cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Move
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4d293f6ccb6a1bcd730ce997367c179f1747f66e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366748"
---
# <a name="cbasepropertypagemove-method"></a><span data-ttu-id="ee161-104">Cbasepropertypage. Move-Methode</span><span class="sxs-lookup"><span data-stu-id="ee161-104">CBasePropertyPage.Move method</span></span>

<span data-ttu-id="ee161-105">Die `Move` -Methode positioniert und ändert die Größe des Dialog Felds.</span><span class="sxs-lookup"><span data-stu-id="ee161-105">The `Move` method positions and resizes the dialog box.</span></span> <span data-ttu-id="ee161-106">Diese Methode implementiert die **IPropertyPage:: Move** -Methode.</span><span class="sxs-lookup"><span data-stu-id="ee161-106">This method implements the **IPropertyPage::Move** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee161-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee161-107">Syntax</span></span>


```C++
HRESULT Move(
   LPCRECT prect
);
```



## <a name="parameters"></a><span data-ttu-id="ee161-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee161-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee161-109">*vorab ausführen*</span><span class="sxs-lookup"><span data-stu-id="ee161-109">*prect*</span></span> 
</dt> <dd>

<span data-ttu-id="ee161-110">Ein Zeiger auf eine **Rect** -Struktur, die die Positionsinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="ee161-110">Pointer to a **RECT** structure containing the positioning information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee161-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ee161-111">Return value</span></span>

<span data-ttu-id="ee161-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ee161-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="ee161-113">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="ee161-113">Possible values include the following.</span></span>



| <span data-ttu-id="ee161-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ee161-114">Return code</span></span>                                                                                  | <span data-ttu-id="ee161-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ee161-115">Description</span></span>                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="ee161-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ee161-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="ee161-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="ee161-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="ee161-118"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="ee161-118"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="ee161-119">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="ee161-119">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="ee161-120"><dt>**E \_ unerwartet**</dt></span><span class="sxs-lookup"><span data-stu-id="ee161-120"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="ee161-121">Unerwarteter Fehler.</span><span class="sxs-lookup"><span data-stu-id="ee161-121">Unexpected failure.</span></span><br/>        |



 

## <a name="requirements"></a><span data-ttu-id="ee161-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee161-122">Requirements</span></span>



| <span data-ttu-id="ee161-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee161-123">Requirement</span></span> | <span data-ttu-id="ee161-124">Wert</span><span class="sxs-lookup"><span data-stu-id="ee161-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee161-125">Header</span><span class="sxs-lookup"><span data-stu-id="ee161-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ee161-126"><dt>Cprop. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee161-126"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="ee161-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ee161-127">Library</span></span><br/> | <dl> <span data-ttu-id="ee161-128">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ee161-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee161-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee161-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee161-130">**Cbasepropertypage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ee161-130">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




