---
description: 'Die TranslateAccelerator-Methode weist die Eigenschaften Seite an, eine Tastatureingabe zu verarbeiten. Diese Methode implementiert die IPropertyPage:: TranslateAccelerator-Methode.'
ms.assetid: 2da214c9-35dc-470c-9b7f-2f4ef6bcd40a
title: Cbasepropertypage. TranslateAccelerator-Methode (cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.TranslateAccelerator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3116e85eec8fbf3a00bf434a1f88c8cac662ed0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355272"
---
# <a name="cbasepropertypagetranslateaccelerator-method"></a><span data-ttu-id="16d8f-104">Cbasepropertypage. TranslateAccelerator-Methode</span><span class="sxs-lookup"><span data-stu-id="16d8f-104">CBasePropertyPage.TranslateAccelerator method</span></span>

<span data-ttu-id="16d8f-105">Die- `TranslateAccelerator` Methode weist die Eigenschaften Seite an, eine Tastatureingabe zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="16d8f-105">The `TranslateAccelerator` method instructs the property page to process a keystroke.</span></span> <span data-ttu-id="16d8f-106">Diese Methode implementiert die **IPropertyPage:: TranslateAccelerator** -Methode.</span><span class="sxs-lookup"><span data-stu-id="16d8f-106">This method implements the **IPropertyPage::TranslateAccelerator** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="16d8f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="16d8f-107">Syntax</span></span>


```C++
HRESULT TranslateAccelerator(
   LPMSG lpMsg
);
```



## <a name="parameters"></a><span data-ttu-id="16d8f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="16d8f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16d8f-109">*lpmsg*</span><span class="sxs-lookup"><span data-stu-id="16d8f-109">*lpMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="16d8f-110">Zeiger auf eine **msg** -Struktur, die den zu verarbeitenden Tastatur Strich beschreibt.</span><span class="sxs-lookup"><span data-stu-id="16d8f-110">Pointer to a **MSG** structure describing the keystroke to process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16d8f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="16d8f-111">Return value</span></span>

<span data-ttu-id="16d8f-112">Gibt "E \_ notimpl" zurück.</span><span class="sxs-lookup"><span data-stu-id="16d8f-112">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="16d8f-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="16d8f-113">Remarks</span></span>

<span data-ttu-id="16d8f-114">Überschreiben Sie diese Methode, wenn Sie für die Eigenschaften Seite Tastaturbeschleuniger bereitstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="16d8f-114">Override this method if you want to provide keyboard accelerators for the property page.</span></span>

## <a name="requirements"></a><span data-ttu-id="16d8f-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16d8f-115">Requirements</span></span>



| <span data-ttu-id="16d8f-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="16d8f-116">Requirement</span></span> | <span data-ttu-id="16d8f-117">Wert</span><span class="sxs-lookup"><span data-stu-id="16d8f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16d8f-118">Header</span><span class="sxs-lookup"><span data-stu-id="16d8f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="16d8f-119"><dt>Cprop. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="16d8f-119"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="16d8f-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="16d8f-120">Library</span></span><br/> | <dl> <span data-ttu-id="16d8f-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="16d8f-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16d8f-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16d8f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16d8f-123">**Cbasepropertypage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="16d8f-123">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




