---
description: 'Mit der Methode "aktivieren" wird das Dialogfeld Fenster erstellt. Diese Methode implementiert die IPropertyPage:: Aktivierungs-Methode.'
ms.assetid: 8f030dc5-1d14-46b5-9d40-7f07a1177dbe
title: Cbasepropertypage. Aktivierungs-Methode (cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Activate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4b851cfc4490d25e7e30dfd2cf0e7c33b0e76224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368425"
---
# <a name="cbasepropertypageactivate-method"></a><span data-ttu-id="3dfea-104">Cbasepropertypage. Aktivierungs-Methode</span><span class="sxs-lookup"><span data-stu-id="3dfea-104">CBasePropertyPage.Activate method</span></span>

<span data-ttu-id="3dfea-105">Mit der- `Activate` Methode wird das Dialogfeld Fenster erstellt.</span><span class="sxs-lookup"><span data-stu-id="3dfea-105">The `Activate` method creates the dialog box window.</span></span> <span data-ttu-id="3dfea-106">Diese Methode implementiert die **IPropertyPage:: Aktivierungs** -Methode.</span><span class="sxs-lookup"><span data-stu-id="3dfea-106">This method implements the **IPropertyPage::Activate** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dfea-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3dfea-107">Syntax</span></span>


```C++
HRESULT Activate(
   HWND    hwndParent,
   LPCRECT prect,
   BOOL    fModal
);
```



## <a name="parameters"></a><span data-ttu-id="3dfea-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3dfea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dfea-109">*hwndParent*</span><span class="sxs-lookup"><span data-stu-id="3dfea-109">*hwndParent*</span></span> 
</dt> <dd>

<span data-ttu-id="3dfea-110">Handle für das übergeordnete Fenster des Dialog Felds.</span><span class="sxs-lookup"><span data-stu-id="3dfea-110">Handle to the parent window of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="3dfea-111">*vorab ausführen*</span><span class="sxs-lookup"><span data-stu-id="3dfea-111">*prect*</span></span> 
</dt> <dd>

<span data-ttu-id="3dfea-112">Ein Zeiger auf eine **Rect** -Struktur, die Positionsinformationen für das Dialogfeld enthält.</span><span class="sxs-lookup"><span data-stu-id="3dfea-112">Pointer to a **RECT** structure that contains positioning information for the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="3dfea-113">*für den modalen*</span><span class="sxs-lookup"><span data-stu-id="3dfea-113">*fModal*</span></span> 
</dt> <dd>

<span data-ttu-id="3dfea-114">Boolescher Wert, der angibt, ob der Dialogfeld Rahmen Modal (**true**) oder nicht modelliert (**false**) ist.</span><span class="sxs-lookup"><span data-stu-id="3dfea-114">Boolean value indicating whether the dialog box frame is modal (**TRUE**) or modeless (**FALSE**).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dfea-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3dfea-115">Return value</span></span>

<span data-ttu-id="3dfea-116">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3dfea-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="3dfea-117">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="3dfea-117">Possible values include the following.</span></span>



| <span data-ttu-id="3dfea-118">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="3dfea-118">Return code</span></span>                                                                                   | <span data-ttu-id="3dfea-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3dfea-119">Description</span></span>                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="3dfea-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3dfea-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3dfea-121">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="3dfea-121">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="3dfea-122"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="3dfea-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3dfea-123">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="3dfea-123">Insufficient memory.</span></span><br/>       |
| <dl> <span data-ttu-id="3dfea-124"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="3dfea-124"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="3dfea-125">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="3dfea-125">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="3dfea-126"><dt>**E \_ unerwartet**</dt></span><span class="sxs-lookup"><span data-stu-id="3dfea-126"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="3dfea-127">Unerwarteter Fehler.</span><span class="sxs-lookup"><span data-stu-id="3dfea-127">Unexpected failure.</span></span><br/>        |



 

## <a name="requirements"></a><span data-ttu-id="3dfea-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3dfea-128">Requirements</span></span>



| <span data-ttu-id="3dfea-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3dfea-129">Requirement</span></span> | <span data-ttu-id="3dfea-130">Wert</span><span class="sxs-lookup"><span data-stu-id="3dfea-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dfea-131">Header</span><span class="sxs-lookup"><span data-stu-id="3dfea-131">Header</span></span><br/>  | <dl> <span data-ttu-id="3dfea-132"><dt>Cprop. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3dfea-132"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="3dfea-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3dfea-133">Library</span></span><br/> | <dl> <span data-ttu-id="3dfea-134">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="3dfea-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dfea-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3dfea-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dfea-136">**Cbasepropertypage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="3dfea-136">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> <dt>

[<span data-ttu-id="3dfea-137">**Cbasepropertypage:: onaktivierungs**</span><span class="sxs-lookup"><span data-stu-id="3dfea-137">**CBasePropertyPage::OnActivate**</span></span>](cbasepropertypage-onactivate.md)
</dt> </dl>

 

 




