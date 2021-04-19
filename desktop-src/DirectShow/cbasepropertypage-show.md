---
description: 'Die Show-Methode zeigt das Dialogfeld an oder blendet es aus. Diese Methode implementiert die IPropertyPage:: Show-Methode.'
ms.assetid: 03796779-ed41-4b68-852d-6b1849a9dc10
title: Cbasepropertypage. Show-Methode (cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Show
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1dadd1c187773df3ca41ac0e1e4daf06fb54761b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365690"
---
# <a name="cbasepropertypageshow-method"></a><span data-ttu-id="8543e-104">Cbasepropertypage. Show-Methode</span><span class="sxs-lookup"><span data-stu-id="8543e-104">CBasePropertyPage.Show method</span></span>

<span data-ttu-id="8543e-105">Die- `Show` Methode zeigt das Dialogfeld an oder blendet es aus.</span><span class="sxs-lookup"><span data-stu-id="8543e-105">The `Show` method shows or hides the dialog box.</span></span> <span data-ttu-id="8543e-106">Diese Methode implementiert die [IPropertyPage:: Show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) -Methode.</span><span class="sxs-lookup"><span data-stu-id="8543e-106">This method implements the [IPropertyPage::Show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8543e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8543e-107">Syntax</span></span>

```C++
HRESULT Show(
   UINT nCmdShow
);
```
## <a name="parameters"></a><span data-ttu-id="8543e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8543e-108">Parameters</span></span>

<span data-ttu-id="8543e-109">*nCmdShow*</span><span class="sxs-lookup"><span data-stu-id="8543e-109">*nCmdShow*</span></span>

<span data-ttu-id="8543e-110">Typ: **[uint](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8543e-110">Type: **[UINT](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8543e-111">Ein Wert, der angibt, ob das Fenster angezeigt oder ausgeblendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8543e-111">Value that specifies whether to show or hide the window.</span></span> <span data-ttu-id="8543e-112">Weitere Informationen finden Sie unter der [IPropertyPage:: Show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) -Methode.</span><span class="sxs-lookup"><span data-stu-id="8543e-112">For more information, see the [IPropertyPage::Show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) method.</span></span>

## <a name="return-value"></a><span data-ttu-id="8543e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8543e-113">Return value</span></span>

<span data-ttu-id="8543e-114">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8543e-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="8543e-115">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="8543e-115">Possible values include the following.</span></span>

| <span data-ttu-id="8543e-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="8543e-116">Return code</span></span>                                                                                  | <span data-ttu-id="8543e-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8543e-117">Description</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="8543e-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8543e-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="8543e-119">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="8543e-119">Success.</span></span><br/>            |
| <dl> <span data-ttu-id="8543e-120"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="8543e-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="8543e-121">Ungültiges Argument.</span><span class="sxs-lookup"><span data-stu-id="8543e-121">Invalid argument.</span></span><br/>   |
| <dl> <span data-ttu-id="8543e-122"><dt>**E \_ unerwartet**</dt></span><span class="sxs-lookup"><span data-stu-id="8543e-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="8543e-123">Unerwarteter Fehler.</span><span class="sxs-lookup"><span data-stu-id="8543e-123">Unexpected failure.</span></span><br/> |

## <a name="requirements"></a><span data-ttu-id="8543e-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8543e-124">Requirements</span></span>

| <span data-ttu-id="8543e-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8543e-125">Requirement</span></span> | <span data-ttu-id="8543e-126">Wert</span><span class="sxs-lookup"><span data-stu-id="8543e-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8543e-127">Header</span><span class="sxs-lookup"><span data-stu-id="8543e-127">Header</span></span>  | <dl> <span data-ttu-id="8543e-128"><dt>Cprop. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8543e-128"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="8543e-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8543e-129">Library</span></span> | <dl> <span data-ttu-id="8543e-130">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="8543e-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="8543e-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8543e-131">See also</span></span>

[<span data-ttu-id="8543e-132">Cbasepropertypage-Klasse</span><span class="sxs-lookup"><span data-stu-id="8543e-132">CBasePropertyPage Class</span></span>](cbasepropertypage.md)
