---
description: Die SetPalette-Methode installiert eine Palette für das Fenster.
ms.assetid: 64fa0d3a-c2eb-4e58-8b8d-c8e5ec3bb479
title: Cbasewindow. SetPalette-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.SetPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f246fe8401e1f671f5935ff7d7454093ea1d3179
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369990"
---
# <a name="cbasewindowsetpalette-method-winutilh"></a><span data-ttu-id="08df4-103">Cbasewindow. SetPalette-Methode (winutil. h)</span><span class="sxs-lookup"><span data-stu-id="08df4-103">CBaseWindow.SetPalette method (Winutil.h)</span></span>

<span data-ttu-id="08df4-104">Mit der- `SetPalette` Methode wird eine Palette für das-Fenster installiert.</span><span class="sxs-lookup"><span data-stu-id="08df4-104">The `SetPalette` method installs a palette for the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="08df4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="08df4-105">Syntax</span></span>


```C++
virtual HRESULT SetPalette(
   HPALETTE hPalette
);
```



## <a name="parameters"></a><span data-ttu-id="08df4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="08df4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08df4-107">*hPalette*</span><span class="sxs-lookup"><span data-stu-id="08df4-107">*hPalette*</span></span> 
</dt> <dd>

<span data-ttu-id="08df4-108">Handle für die neue Palette.</span><span class="sxs-lookup"><span data-stu-id="08df4-108">Handle to the new palette.</span></span> <span data-ttu-id="08df4-109">Darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="08df4-109">Cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08df4-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="08df4-110">Return value</span></span>

<span data-ttu-id="08df4-111">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="08df4-111">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="08df4-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="08df4-112">Return code</span></span>                                                                             | <span data-ttu-id="08df4-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="08df4-113">Description</span></span>                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="08df4-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="08df4-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="08df4-115">Ein interner-Befehl von " **gdiflush** " hat einen Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="08df4-115">An internal call to **GdiFlush** returned an error.</span></span><br/> |
| <dl> <span data-ttu-id="08df4-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="08df4-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="08df4-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="08df4-117">Success.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="08df4-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08df4-118">Remarks</span></span>

<span data-ttu-id="08df4-119">Wenn der Wert der [**cbasewindow:: m \_ bnorealize**](cbasewindow-m-bnorealize.md) -Element Variablen **false** (Standardeinstellung) ist, wählt diese Methode die Palette aus und erkennt Sie.</span><span class="sxs-lookup"><span data-stu-id="08df4-119">If the value of the [**CBaseWindow::m\_bNoRealize**](cbasewindow-m-bnorealize.md) member variable is **FALSE** (the default), this method selects the palette and realizes it.</span></span> <span data-ttu-id="08df4-120">Andernfalls wird die Palette ausgewählt, aber nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="08df4-120">Otherwise, it selects the palette but does not realize it.</span></span> <span data-ttu-id="08df4-121">Das Objekt löscht keine zuvor verwendete Palette.</span><span class="sxs-lookup"><span data-stu-id="08df4-121">The object does not delete any previous palette that it was using.</span></span> <span data-ttu-id="08df4-122">Der Aufrufer ist für das Löschen von Paletten verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="08df4-122">The caller is responsible for deleting palettes.</span></span>

<span data-ttu-id="08df4-123">Jeder Thread kann diese Methode sicher aufzurufen, nicht nur den Thread, der das Fenster besitzt.</span><span class="sxs-lookup"><span data-stu-id="08df4-123">Any thread can safely call this method, not just the thread that owns the window.</span></span> <span data-ttu-id="08df4-124">Das Fenster sendet eine private Nachricht an sich selbst, wodurch ein Aufrufvorgang der [**cbasewindow:: onpalettechange**](cbasewindow-onpalettechange.md) -Methode ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="08df4-124">The window sends a private message to itself, which triggers a call to the [**CBaseWindow::OnPaletteChange**](cbasewindow-onpalettechange.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="08df4-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08df4-125">Requirements</span></span>



| <span data-ttu-id="08df4-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08df4-126">Requirement</span></span> | <span data-ttu-id="08df4-127">Wert</span><span class="sxs-lookup"><span data-stu-id="08df4-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08df4-128">Header</span><span class="sxs-lookup"><span data-stu-id="08df4-128">Header</span></span><br/>  | <dl> <span data-ttu-id="08df4-129"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="08df4-129"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="08df4-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="08df4-130">Library</span></span><br/> | <dl> <span data-ttu-id="08df4-131">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="08df4-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08df4-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08df4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08df4-133">**Cbasewindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="08df4-133">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




