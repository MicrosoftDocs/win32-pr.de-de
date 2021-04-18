---
description: 'Die Hilfe Methode ruft die Hilfe der Eigenschaften Seite auf. Diese Methode implementiert die IPropertyPage:: Help-Methode.'
ms.assetid: 8fe72b2e-a9f1-435d-8eda-27056f112c6d
title: Cbasepropertypage. Help-Methode (cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Help
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b87c8ba76928fbf0e465a8b6a3a0aaf4730759f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360944"
---
# <a name="cbasepropertypagehelp-method"></a><span data-ttu-id="b59ea-104">Cbasepropertypage. Help-Methode</span><span class="sxs-lookup"><span data-stu-id="b59ea-104">CBasePropertyPage.Help method</span></span>

<span data-ttu-id="b59ea-105">Die- `Help` Methode ruft die Hilfe der Eigenschaften Seite auf.</span><span class="sxs-lookup"><span data-stu-id="b59ea-105">The `Help` method invokes the property page help.</span></span> <span data-ttu-id="b59ea-106">Diese Methode implementiert die **IPropertyPage:: Help** -Methode.</span><span class="sxs-lookup"><span data-stu-id="b59ea-106">This method implements the **IPropertyPage::Help** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b59ea-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b59ea-107">Syntax</span></span>


```C++
HRESULT Help(
   LPCWSTR lpszHelpDir
);
```



## <a name="parameters"></a><span data-ttu-id="b59ea-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b59ea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b59ea-109">*lpszhelpdir*</span><span class="sxs-lookup"><span data-stu-id="b59ea-109">*lpszHelpDir*</span></span> 
</dt> <dd>

<span data-ttu-id="b59ea-110">Zeiger auf die Zeichenfolge unter dem **helpDir** -Schlüssel in den CLSID-Informationen der Eigenschaften Seite in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="b59ea-110">Pointer to the string under the **HelpDir** key in the property page's CLSID information in the registry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b59ea-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b59ea-111">Return value</span></span>

<span data-ttu-id="b59ea-112">Gibt "E \_ notimpl" zurück.</span><span class="sxs-lookup"><span data-stu-id="b59ea-112">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b59ea-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b59ea-113">Remarks</span></span>

<span data-ttu-id="b59ea-114">In der-Basisklasse gibt die-Methode immer E \_ notimpl zurück.</span><span class="sxs-lookup"><span data-stu-id="b59ea-114">In the base class, the method always returns E\_NOTIMPL.</span></span> <span data-ttu-id="b59ea-115">Wenn die Methode fehlschlägt, ruft der Frame **IPropertyPage:: GetPageInfo** auf, um den Namen der Hilfedatei und des Kontext Bezeichners zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b59ea-115">When the method fails, the frame calls **IPropertyPage::GetPageInfo** to get the name of the help file and context identifier.</span></span> <span data-ttu-id="b59ea-116">Standardmäßig sind diese **null**-Werte.</span><span class="sxs-lookup"><span data-stu-id="b59ea-116">By default, these are **NULL**.</span></span> <span data-ttu-id="b59ea-117">Um Hilfe bereitzustellen, kann die abgeleitete Klasse entweder die- `Help` Methode oder die [**cbasepropertypage:: getpagumfo**](cbasepropertypage-getpageinfo.md) -Methode überschreiben.</span><span class="sxs-lookup"><span data-stu-id="b59ea-117">To provide help, therefore, the derived class can override either the `Help` method or the [**CBasePropertyPage::GetPageInfo**](cbasepropertypage-getpageinfo.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b59ea-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b59ea-118">Requirements</span></span>



| <span data-ttu-id="b59ea-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b59ea-119">Requirement</span></span> | <span data-ttu-id="b59ea-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b59ea-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b59ea-121">Header</span><span class="sxs-lookup"><span data-stu-id="b59ea-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b59ea-122"><dt>Cprop. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b59ea-122"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="b59ea-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b59ea-123">Library</span></span><br/> | <dl> <span data-ttu-id="b59ea-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b59ea-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b59ea-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b59ea-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b59ea-126">**Cbasepropertypage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b59ea-126">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




