---
description: Die Methode initialierwindow initialisiert das Fenster.
ms.assetid: 0cf07714-6846-4271-8095-bc4ab865171f
title: CBaseWindow.Initialierwindow-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.InitialiseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 75668846c700c33a26b7bb7ad2af2a3fd6e8eea2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371108"
---
# <a name="cbasewindowinitialisewindow-method"></a><span data-ttu-id="17062-103">CBaseWindow.Initialierwindow-Methode</span><span class="sxs-lookup"><span data-stu-id="17062-103">CBaseWindow.InitialiseWindow method</span></span>

<span data-ttu-id="17062-104">Die- `InitialiseWindow` Methode initialisiert das-Fenster.</span><span class="sxs-lookup"><span data-stu-id="17062-104">The `InitialiseWindow` method initializes the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="17062-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="17062-105">Syntax</span></span>


```C++
virtual HRESULT InitialiseWindow(
   HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="17062-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="17062-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17062-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="17062-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="17062-108">Handle für das Fenster.</span><span class="sxs-lookup"><span data-stu-id="17062-108">Handle to the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17062-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="17062-109">Return value</span></span>

<span data-ttu-id="17062-110">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="17062-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="17062-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17062-111">Remarks</span></span>

<span data-ttu-id="17062-112">Standardmäßig ruft diese Methode ein Handle für den Gerätekontext des Fensters ab und erstellt einen kompatiblen Arbeitsspeicher-DC.</span><span class="sxs-lookup"><span data-stu-id="17062-112">By default, this method retrieves a handle to the window's device context (DC) and creates a compatible memory DC.</span></span> <span data-ttu-id="17062-113">Wenn der Wert des [**cbasewindow:: m \_ bdogetdc**](cbasewindow-m-bdogetdc.md) -Flags **false** ist, ruft diese Methode jedoch nicht die Geräte Kontexte ab.</span><span class="sxs-lookup"><span data-stu-id="17062-113">If the value of the [**CBaseWindow::m\_bDoGetDC**](cbasewindow-m-bdogetdc.md) flag is **FALSE**, however, this method does not retrieve the device contexts.</span></span> <span data-ttu-id="17062-114">Der Arbeitsspeicher-Domänen Controller eignet sich für die Auswahl von Bitmaps, bevor diese im Fenster ausgeblendet werden.</span><span class="sxs-lookup"><span data-stu-id="17062-114">The memory DC is useful for selecting bitmaps before blitting them to the window.</span></span>

<span data-ttu-id="17062-115">Die [**cbasewindow::D okreatewindow**](cbasewindow-docreatewindow.md) -Methode ruft diese Methode auf.</span><span class="sxs-lookup"><span data-stu-id="17062-115">The [**CBaseWindow::DoCreateWindow**](cbasewindow-docreatewindow.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="17062-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17062-116">Requirements</span></span>



| <span data-ttu-id="17062-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17062-117">Requirement</span></span> | <span data-ttu-id="17062-118">Wert</span><span class="sxs-lookup"><span data-stu-id="17062-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17062-119">Header</span><span class="sxs-lookup"><span data-stu-id="17062-119">Header</span></span><br/>  | <dl> <span data-ttu-id="17062-120"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="17062-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="17062-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="17062-121">Library</span></span><br/> | <dl> <span data-ttu-id="17062-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="17062-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17062-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17062-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17062-124">**Cbasewindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="17062-124">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




