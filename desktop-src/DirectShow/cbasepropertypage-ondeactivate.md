---
description: Die ondeaktivieren-Methode wird aufgerufen, wenn das Dialogfeld Fenster zerstört wird.
ms.assetid: 47320e61-324f-4f64-abe1-38fe70e82787
title: Cbasepropertypage. ondeaktiviert-Methode (cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnDeactivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27191e4895c911d3d13a795306eee2b0ad6989ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354811"
---
# <a name="cbasepropertypageondeactivate-method"></a><span data-ttu-id="36d85-103">Cbasepropertypage. ondeaktivieren-Methode</span><span class="sxs-lookup"><span data-stu-id="36d85-103">CBasePropertyPage.OnDeactivate method</span></span>

<span data-ttu-id="36d85-104">Die- `OnDeactivate` Methode wird aufgerufen, wenn das Dialogfeld Fenster zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="36d85-104">The `OnDeactivate` method is called when the dialog box window is destroyed.</span></span>

## <a name="syntax"></a><span data-ttu-id="36d85-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="36d85-105">Syntax</span></span>


```C++
virtual HRESULT OnDeactivate();
```



## <a name="parameters"></a><span data-ttu-id="36d85-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="36d85-106">Parameters</span></span>

<span data-ttu-id="36d85-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="36d85-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="36d85-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="36d85-108">Return value</span></span>

<span data-ttu-id="36d85-109">Die Basisklassen Implementierung gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="36d85-109">The base-class implementation returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="36d85-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="36d85-110">Remarks</span></span>

<span data-ttu-id="36d85-111">Die [**cbasepropertypage::D eaktivierungs**](cbasepropertypage-deactivate.md) -Methode ruft die- `OnDeactivate` Methode auf.</span><span class="sxs-lookup"><span data-stu-id="36d85-111">The [**CBasePropertyPage::Deactivate**](cbasepropertypage-deactivate.md) method calls the `OnDeactivate` method.</span></span> <span data-ttu-id="36d85-112">`OnDeactivate`Überschreiben Sie, um alle Ressourcen freizugeben, die von der abgeleiteten Klasse in der [**cbasepropertypage:: onaktivierungs**](cbasepropertypage-onactivate.md) -Methode abgerufen wurden, oder, um andere Aufgaben nach Bedarf auszuführen.</span><span class="sxs-lookup"><span data-stu-id="36d85-112">Override `OnDeactivate` to release any resources that the derived class obtained in the [**CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md) method, or to perform other tasks as needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="36d85-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="36d85-113">Requirements</span></span>



| <span data-ttu-id="36d85-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="36d85-114">Requirement</span></span> | <span data-ttu-id="36d85-115">Wert</span><span class="sxs-lookup"><span data-stu-id="36d85-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36d85-116">Header</span><span class="sxs-lookup"><span data-stu-id="36d85-116">Header</span></span><br/>  | <dl> <span data-ttu-id="36d85-117"><dt>Cprop. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="36d85-117"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="36d85-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="36d85-118">Library</span></span><br/> | <dl> <span data-ttu-id="36d85-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="36d85-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36d85-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36d85-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36d85-121">**Cbasepropertypage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="36d85-121">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




