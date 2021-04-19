---
description: Die onaktivierungs-Methode wird aufgerufen, wenn die Eigenschaften Seite aktiviert wird.
ms.assetid: aff843d4-cfb2-4255-a59c-0579f1cd24bd
title: Cbasepropertypage. onaktivierungs-Methode (cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnActivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5093cb2ac71e8010bc689e4517b3d8bb758c8436
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369115"
---
# <a name="cbasepropertypageonactivate-method"></a><span data-ttu-id="59531-103">Cbasepropertypage. onaktivierungs-Methode</span><span class="sxs-lookup"><span data-stu-id="59531-103">CBasePropertyPage.OnActivate method</span></span>

<span data-ttu-id="59531-104">Die- `OnActivate` Methode wird aufgerufen, wenn die Eigenschaften Seite aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="59531-104">The `OnActivate` method is called when the property page is activated.</span></span>

## <a name="syntax"></a><span data-ttu-id="59531-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="59531-105">Syntax</span></span>


```C++
virtual HRESULT OnActivate();
```



## <a name="parameters"></a><span data-ttu-id="59531-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="59531-106">Parameters</span></span>

<span data-ttu-id="59531-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="59531-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="59531-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="59531-108">Return value</span></span>

<span data-ttu-id="59531-109">Die Basisklassen Implementierung gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="59531-109">The base-class implementation returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="59531-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="59531-110">Remarks</span></span>

<span data-ttu-id="59531-111">Die [**cbasepropertypage:: Aktivierungs**](cbasepropertypage-activate.md) -Methode ruft die- `OnActivate` Methode auf.</span><span class="sxs-lookup"><span data-stu-id="59531-111">The [**CBasePropertyPage::Activate**](cbasepropertypage-activate.md) method calls the `OnActivate` method.</span></span> <span data-ttu-id="59531-112">Überschreiben Sie in der abgeleiteten Klasse, `OnActivate` um das Dialogfeld zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="59531-112">In your derived class, override `OnActivate` to initialize the dialog box.</span></span>

## <a name="examples"></a><span data-ttu-id="59531-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="59531-113">Examples</span></span>

<span data-ttu-id="59531-114">Im folgenden Beispiel wird ein TrackBar-Steuerelement initialisiert.</span><span class="sxs-lookup"><span data-stu-id="59531-114">The following example initializes a trackbar control.</span></span> <span data-ttu-id="59531-115">In diesem Beispiel wird davon ausgegangen, dass **m \_ powningfilter** ein Zeiger auf eine benutzerdefinierte Schnittstelle für den Filter ist, der der Eigenschaften Seite zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="59531-115">This example assumes that **m\_pOwningFilter** is a pointer to a custom interface on the filter associated with the property page.</span></span> <span data-ttu-id="59531-116">(Verwenden Sie die [**cbasepropertypage:: OnConnect**](cbasepropertypage-onconnect.md) -Methode, um solche Zeiger zu initialisieren.)</span><span class="sxs-lookup"><span data-stu-id="59531-116">(Use the [**CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) method to initialize such pointers.)</span></span>


```C++
HRESULT CMyProp::OnActivate(void)
{
    ASSERT(m_pOwningFilter != NULL);
    m_pOwningFilter->GetSomeProperty(&m_lOldVal);
    
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETRANGE, 0, MAKELONG(0, 100));
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETTICFREQ, 10, 0);
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETPOS, 1, m_lOldVal);
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="59531-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="59531-117">Requirements</span></span>



| <span data-ttu-id="59531-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="59531-118">Requirement</span></span> | <span data-ttu-id="59531-119">Wert</span><span class="sxs-lookup"><span data-stu-id="59531-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59531-120">Header</span><span class="sxs-lookup"><span data-stu-id="59531-120">Header</span></span><br/>  | <dl> <span data-ttu-id="59531-121"><dt>Cprop. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59531-121"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="59531-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="59531-122">Library</span></span><br/> | <dl> <span data-ttu-id="59531-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="59531-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59531-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59531-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59531-125">**Cbasepropertypage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="59531-125">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




