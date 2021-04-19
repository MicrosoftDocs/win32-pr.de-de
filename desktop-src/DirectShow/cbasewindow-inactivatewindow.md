---
description: Die inactivatewindow-Methode aktiviert das Fenster. In der Basisklasse blendet diese Methode das Fenster aus.
ms.assetid: b575d4fd-dee1-4ae5-abb4-e92ae361e82a
title: Cbasewindow. inactivatewindow-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.InactivateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d1c5e925a3d9b510918636a221d5ad6e1b7da736
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371110"
---
# <a name="cbasewindowinactivatewindow-method"></a><span data-ttu-id="4cc94-104">Cbasewindow. inactivatewindow-Methode</span><span class="sxs-lookup"><span data-stu-id="4cc94-104">CBaseWindow.InactivateWindow method</span></span>

<span data-ttu-id="4cc94-105">Mit der- `InactivateWindow` Methode wird das Fenster deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="4cc94-105">The `InactivateWindow` method inactivates the window.</span></span> <span data-ttu-id="4cc94-106">In der Basisklasse blendet diese Methode das Fenster aus.</span><span class="sxs-lookup"><span data-stu-id="4cc94-106">In the base class, this method hides the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cc94-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4cc94-107">Syntax</span></span>


```C++
virtual HRESULT InactivateWindow();
```



## <a name="parameters"></a><span data-ttu-id="4cc94-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4cc94-108">Parameters</span></span>

<span data-ttu-id="4cc94-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="4cc94-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4cc94-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4cc94-110">Return value</span></span>

<span data-ttu-id="4cc94-111">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="4cc94-111">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="4cc94-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="4cc94-112">Return code</span></span>                                                                             | <span data-ttu-id="4cc94-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4cc94-113">Description</span></span>                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="4cc94-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4cc94-114"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="4cc94-115">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="4cc94-115">Success.</span></span><br/>                    |
| <dl> <span data-ttu-id="4cc94-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="4cc94-116"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="4cc94-117">Das Fenster ist bereits inaktiv.</span><span class="sxs-lookup"><span data-stu-id="4cc94-117">Window is already inactive.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4cc94-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4cc94-118">Requirements</span></span>



| <span data-ttu-id="4cc94-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4cc94-119">Requirement</span></span> | <span data-ttu-id="4cc94-120">Wert</span><span class="sxs-lookup"><span data-stu-id="4cc94-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cc94-121">Header</span><span class="sxs-lookup"><span data-stu-id="4cc94-121">Header</span></span><br/>  | <dl> <span data-ttu-id="4cc94-122"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4cc94-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4cc94-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4cc94-123">Library</span></span><br/> | <dl> <span data-ttu-id="4cc94-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="4cc94-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cc94-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4cc94-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cc94-126">**Cbasewindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="4cc94-126">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




