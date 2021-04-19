---
description: Die Methode "Aktualisierungs Methode" aktualisiert das Videoformat des Objekts entsprechend der angegebenen Anzeige.
ms.assetid: cc2bdfeb-80f1-4fb6-859d-977d644a5e08
title: Cimagedisplay. erfrischend Display Type-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.RefreshDisplayType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9f8010dcfe490363903ff455bedb61254b69b825
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366744"
---
# <a name="cimagedisplayrefreshdisplaytype-method"></a><span data-ttu-id="be80e-103">Cimagedisplay. erfrischend Display Type-Methode</span><span class="sxs-lookup"><span data-stu-id="be80e-103">CImageDisplay.RefreshDisplayType method</span></span>

<span data-ttu-id="be80e-104">Die `RefreshDisplayType` -Methode aktualisiert das Videoformat des Objekts entsprechend der angegebenen Anzeige.</span><span class="sxs-lookup"><span data-stu-id="be80e-104">The `RefreshDisplayType` method updates the object's video format to match the specified display.</span></span>

## <a name="syntax"></a><span data-ttu-id="be80e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="be80e-105">Syntax</span></span>


```C++
HRESULT RefreshDisplayType(
   LPSTR szDeviceName
);
```



## <a name="parameters"></a><span data-ttu-id="be80e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="be80e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be80e-107">*szdevicename*</span><span class="sxs-lookup"><span data-stu-id="be80e-107">*szDeviceName*</span></span> 
</dt> <dd>

<span data-ttu-id="be80e-108">Zeiger auf eine Zeichenfolge, die den Namen des Anzeige Geräts enthält, wie von der GDI-Funktion " **EnumDisplayDevices** " zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="be80e-108">Pointer to a string that contains the name of the display device, as returned by the GDI **EnumDisplayDevices** function.</span></span> <span data-ttu-id="be80e-109">Legen Sie diesen Parameter auf **null** fest, um das Haupt Anzeigegerät zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="be80e-109">To use the main display device, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be80e-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="be80e-110">Return value</span></span>

<span data-ttu-id="be80e-111">Gibt \_ bei Erfolg S OK zurück, oder E \_ schlägt fehl, wenn er nicht erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="be80e-111">Returns S\_OK if successful, or E\_FAIL if unsuccessful.</span></span>

## <a name="remarks"></a><span data-ttu-id="be80e-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be80e-112">Remarks</span></span>

<span data-ttu-id="be80e-113">Diese Methode initialisiert den **m- \_ Anzeige** Member mit einem Videotyp, der dem Anzeigemodus auf dem angegebenen Gerät entspricht.</span><span class="sxs-lookup"><span data-stu-id="be80e-113">This method initializes the **m\_Display** member to a video type that corresponds to the display mode on the specified device.</span></span>

<span data-ttu-id="be80e-114">Ruft diese Methode immer dann auf, wenn eine "WM \_ Display Changed"-Meldung empfangen wird, oder um ein sekundäres Anzeigegerät anzugeben.</span><span class="sxs-lookup"><span data-stu-id="be80e-114">Call this method whenever a WM\_DISPLAYCHANGED message is received, or to specify a secondary display device.</span></span>

## <a name="requirements"></a><span data-ttu-id="be80e-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be80e-115">Requirements</span></span>



| <span data-ttu-id="be80e-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be80e-116">Requirement</span></span> | <span data-ttu-id="be80e-117">Wert</span><span class="sxs-lookup"><span data-stu-id="be80e-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be80e-118">Header</span><span class="sxs-lookup"><span data-stu-id="be80e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="be80e-119"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be80e-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="be80e-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="be80e-120">Library</span></span><br/> | <dl> <span data-ttu-id="be80e-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="be80e-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be80e-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be80e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be80e-123">**Cimagedisplay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="be80e-123">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




