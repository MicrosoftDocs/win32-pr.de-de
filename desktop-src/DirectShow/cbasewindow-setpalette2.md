---
description: Die SetPalette-Methode installiert eine Palette für das Fenster. Diese Methode hat keine Parameter.
ms.assetid: 86eb34c6-85ff-4a40-8085-ea55dbc2727e
title: Cbasewindow. SetPalette-Methode (winutil. h)-keine Parameter
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
ms.openlocfilehash: 1203b6aeedd39eb82d7188c4e5d5503b01d167fe
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104219730"
---
# <a name="cbasewindowsetpalette-method-winutilh---no-parameters"></a><span data-ttu-id="c62d7-104">Cbasewindow. SetPalette-Methode (winutil. h)-keine Parameter</span><span class="sxs-lookup"><span data-stu-id="c62d7-104">CBaseWindow.SetPalette method (Winutil.h) - No parameters</span></span>

<span data-ttu-id="c62d7-105">Mit der- `SetPalette` Methode wird eine Palette für das-Fenster installiert.</span><span class="sxs-lookup"><span data-stu-id="c62d7-105">The `SetPalette` method installs a palette for the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="c62d7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c62d7-106">Syntax</span></span>


```C++
HRESULT SetPalette();
```



## <a name="parameters"></a><span data-ttu-id="c62d7-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c62d7-107">Parameters</span></span>

<span data-ttu-id="c62d7-108">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c62d7-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c62d7-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c62d7-109">Return value</span></span>

<span data-ttu-id="c62d7-110">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="c62d7-110">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="c62d7-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c62d7-111">Return code</span></span>                                                                             | <span data-ttu-id="c62d7-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c62d7-112">Description</span></span>                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="c62d7-113"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="c62d7-113"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="c62d7-114">Ein interner-Befehl von " **gdiflush** " hat einen Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c62d7-114">An internal call to **GdiFlush** returned an error.</span></span><br/> |
| <dl> <span data-ttu-id="c62d7-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c62d7-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="c62d7-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="c62d7-116">Success.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="c62d7-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c62d7-117">Remarks</span></span>

<span data-ttu-id="c62d7-118">Die von der [**cbasewindow:: m \_ hpalette**](cbasewindow-m-hpalette.md) -Member-Variable angegebene Palette ist ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="c62d7-118">The palette given by the [**CBaseWindow::m\_hPalette**](cbasewindow-m-hpalette.md) member variable is selected.</span></span> <span data-ttu-id="c62d7-119">Der Aufrufer muss die Gültigkeit von **m \_ hpalette** sicherstellen.</span><span class="sxs-lookup"><span data-stu-id="c62d7-119">The caller must ensure the validity of **m\_hPalette**.</span></span>

<span data-ttu-id="c62d7-120">Wenn der Wert der [**cbasewindow:: m \_ bnorealize**](cbasewindow-m-bnorealize.md) -Element Variablen **false** (Standardeinstellung) ist, wählt diese Methode die Palette aus und erkennt Sie.</span><span class="sxs-lookup"><span data-stu-id="c62d7-120">If the value of the [**CBaseWindow::m\_bNoRealize**](cbasewindow-m-bnorealize.md) member variable is **FALSE** (the default), this method selects the palette and realizes it.</span></span> <span data-ttu-id="c62d7-121">Andernfalls wird die Palette ausgewählt, aber nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="c62d7-121">Otherwise, it selects the palette but does not realize it.</span></span> <span data-ttu-id="c62d7-122">Das Objekt löscht keine zuvor verwendete Palette.</span><span class="sxs-lookup"><span data-stu-id="c62d7-122">The object does not delete any previous palette that it was using.</span></span> <span data-ttu-id="c62d7-123">Der Aufrufer ist für das Löschen von Paletten verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="c62d7-123">The caller is responsible for deleting palettes.</span></span>

<span data-ttu-id="c62d7-124">Jeder Thread kann diese Methode sicher aufzurufen, nicht nur den Thread, der das Fenster besitzt.</span><span class="sxs-lookup"><span data-stu-id="c62d7-124">Any thread can safely call this method, not just the thread that owns the window.</span></span> <span data-ttu-id="c62d7-125">Das Fenster sendet eine private Nachricht an sich selbst, wodurch ein Aufrufvorgang der [**cbasewindow:: onpalettechange**](cbasewindow-onpalettechange.md) -Methode ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="c62d7-125">The window sends a private message to itself, which triggers a call to the [**CBaseWindow::OnPaletteChange**](cbasewindow-onpalettechange.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c62d7-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c62d7-126">Requirements</span></span>

| <span data-ttu-id="c62d7-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c62d7-127">Requirement</span></span> | <span data-ttu-id="c62d7-128">Wert</span><span class="sxs-lookup"><span data-stu-id="c62d7-128">Value</span></span> |
|-|-|
| <span data-ttu-id="c62d7-129">Header</span><span class="sxs-lookup"><span data-stu-id="c62d7-129">Header</span></span> | <span data-ttu-id="c62d7-130">Winutil. h (Include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="c62d7-130">Winutil.h (include Streams.h)</span></span> |
| <span data-ttu-id="c62d7-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c62d7-131">Library</span></span>| <span data-ttu-id="c62d7-132">"Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds)</span><span class="sxs-lookup"><span data-stu-id="c62d7-132">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="c62d7-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c62d7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c62d7-134">**Cbasewindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c62d7-134">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




