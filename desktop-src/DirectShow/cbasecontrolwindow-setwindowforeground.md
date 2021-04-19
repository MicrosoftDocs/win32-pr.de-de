---
description: Mit der setwindowfore-Methode wird das Videofenster in den Vordergrund verschoben, und der Fokus erhält optional den Fokus.
ms.assetid: 41c26bff-0023-41ad-bca8-8f0c43c94814
title: Cbasecontrolwindow. setwindowvorder-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetWindowForeground
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 52c9a37f23b555e140bfd541cf0b5e8e782f8d51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369281"
---
# <a name="cbasecontrolwindowsetwindowforeground-method"></a><span data-ttu-id="73a14-103">Cbasecontrolwindow. setwindowvorder Grund-Methode</span><span class="sxs-lookup"><span data-stu-id="73a14-103">CBaseControlWindow.SetWindowForeground method</span></span>

<span data-ttu-id="73a14-104">Die `SetWindowForeground` -Methode verschiebt das Videofenster in den Vordergrund und gibt ihm optional den Fokus.</span><span class="sxs-lookup"><span data-stu-id="73a14-104">The `SetWindowForeground` method moves the video window to the foreground and optionally gives it focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="73a14-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="73a14-105">Syntax</span></span>


```C++
HRESULT SetWindowForeground(
   long Focus
);
```



## <a name="parameters"></a><span data-ttu-id="73a14-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="73a14-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73a14-107">*Fokus*</span><span class="sxs-lookup"><span data-stu-id="73a14-107">*Focus*</span></span> 
</dt> <dd>

<span data-ttu-id="73a14-108">Ein Wert, der angibt, ob das Videofenster den Fokus erhält.</span><span class="sxs-lookup"><span data-stu-id="73a14-108">Value that specifies whether the video window will get focus.</span></span> <span data-ttu-id="73a14-109">Der Wert 1 gibt dem Fenster Fokus und 0 nicht.</span><span class="sxs-lookup"><span data-stu-id="73a14-109">A value of  1 gives the window focus and 0 does not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73a14-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="73a14-110">Return value</span></span>

<span data-ttu-id="73a14-111">Gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="73a14-111">Returns one of the following values.</span></span>



| <span data-ttu-id="73a14-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="73a14-112">Return code</span></span>                                                                                           | <span data-ttu-id="73a14-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="73a14-113">Description</span></span>                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="73a14-114"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="73a14-114"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="73a14-115">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="73a14-115">The method succeeded.</span></span><br/>                                          |
| <dl> <span data-ttu-id="73a14-116"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="73a14-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="73a14-117">Der Fokus ist nicht gleich 1 oder 0.</span><span class="sxs-lookup"><span data-stu-id="73a14-117">Focus doesn't equal  1 or 0.</span></span><br/>                                   |
| <dl> <span data-ttu-id="73a14-118"><dt>**VFW \_ E \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="73a14-118"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="73a14-119">Der aktuelle Filter ist nicht mit einem kompletten Filter Diagramm verbunden.</span><span class="sxs-lookup"><span data-stu-id="73a14-119">The current filter isn't connected to a complete filter graph.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="73a14-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73a14-120">Requirements</span></span>



| <span data-ttu-id="73a14-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73a14-121">Requirement</span></span> | <span data-ttu-id="73a14-122">Wert</span><span class="sxs-lookup"><span data-stu-id="73a14-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73a14-123">Header</span><span class="sxs-lookup"><span data-stu-id="73a14-123">Header</span></span><br/>  | <dl> <span data-ttu-id="73a14-124"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="73a14-124"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="73a14-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="73a14-125">Library</span></span><br/> | <dl> <span data-ttu-id="73a14-126">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="73a14-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73a14-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73a14-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73a14-128">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="73a14-128">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




