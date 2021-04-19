---
description: Die makeidentitypalette-Methode versucht, eine &\# 0034;-Identitäts Palette zu erstellen &\# 0034; definiert als eine, die direkt der im Anzeigegerät ausgewählten Palette zugeordnet ist.
ms.assetid: 08a0cf67-f43f-44c0-bfb3-6527fd434ea4
title: Cimagepalette. makeidentitypalette-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.MakeIdentityPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e105652108e74907375408f0bd8946c69194202
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370532"
---
# <a name="cimagepalettemakeidentitypalette-method"></a><span data-ttu-id="d4ee7-103">Cimagepalette. makeidentitypalette-Methode</span><span class="sxs-lookup"><span data-stu-id="d4ee7-103">CImagePalette.MakeIdentityPalette method</span></span>

<span data-ttu-id="d4ee7-104">Die `MakeIdentityPalette` Methode versucht, eine "Identitäts Palette" als eine zu definieren, die direkt der im Anzeigegerät ausgewählten Palette zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d4ee7-104">The `MakeIdentityPalette` method attempts to make an "identity palette," defined as one that maps directly to the palette selected in the display device.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4ee7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4ee7-105">Syntax</span></span>


```C++
HRESULT MakeIdentityPalette(
   PALETTEENTRY *pEntry,
   INT          iColours,
   LPSTR        szDevice
);
```



## <a name="parameters"></a><span data-ttu-id="d4ee7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4ee7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4ee7-107">*Pentry*</span><span class="sxs-lookup"><span data-stu-id="d4ee7-107">*pEntry*</span></span> 
</dt> <dd>

<span data-ttu-id="d4ee7-108">Zeiger auf ein Array von paletteneinträgen.</span><span class="sxs-lookup"><span data-stu-id="d4ee7-108">Pointer to an array of palette entries.</span></span>

</dd> <dt>

<span data-ttu-id="d4ee7-109">*icolours*</span><span class="sxs-lookup"><span data-stu-id="d4ee7-109">*iColours*</span></span> 
</dt> <dd>

<span data-ttu-id="d4ee7-110">Anzahl der Paletteneinträge in *Pentry*.</span><span class="sxs-lookup"><span data-stu-id="d4ee7-110">Number of palette entries in *pEntry*.</span></span>

</dd> <dt>

<span data-ttu-id="d4ee7-111">*szdevice*</span><span class="sxs-lookup"><span data-stu-id="d4ee7-111">*szDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="d4ee7-112">Zeiger auf eine Zeichenfolge, die den Namen des Anzeige Geräts enthält, wie von der GDI-Funktion " **EnumDisplayDevices** " zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d4ee7-112">Pointer to a string that contains the name of the display device, as returned by the GDI **EnumDisplayDevices** function.</span></span> <span data-ttu-id="d4ee7-113">Legen Sie diesen Parameter auf **null** fest, um das Haupt Anzeigegerät zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d4ee7-113">To use the main display device, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4ee7-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d4ee7-114">Return value</span></span>

<span data-ttu-id="d4ee7-115">Gibt \_ bei Erfolg s OK oder \_ false zurück.</span><span class="sxs-lookup"><span data-stu-id="d4ee7-115">Returns S\_OK if successful or S\_FALSE if unsuccessful.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4ee7-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4ee7-116">Remarks</span></span>

<span data-ttu-id="d4ee7-117">Diese Methode vergleicht die reservierten Einträge in der Systempalette mit den entsprechenden Einträgen im *Pentry* -Array.</span><span class="sxs-lookup"><span data-stu-id="d4ee7-117">This method compares the reserved entries in the system palette against the corresponding entries in the *pEntry* array.</span></span> <span data-ttu-id="d4ee7-118">Wenn Sie genau übereinstimmen, legt die-Methode das PC- \_ nocollapse-Flag in den restlichen (nicht reservierten) paletteneinträgen in *Pentry* fest.</span><span class="sxs-lookup"><span data-stu-id="d4ee7-118">If they match exactly, the method sets the PC\_NOCOLLAPSE flag in the remaining (non-reserved) palette entries in *pEntry*.</span></span> <span data-ttu-id="d4ee7-119">Mit diesem Flag wird verhindert, dass der GDI logische Paletteneinträge zu System paletteneinträgen zuordnet.</span><span class="sxs-lookup"><span data-stu-id="d4ee7-119">This flag prevents GDI from trying map logical palette entries to system palette entries.</span></span>

<span data-ttu-id="d4ee7-120">Die [**cimagepalette:: makepalette**](cimagepalette-makepalette.md) -Methode ruft diese Methode auf.</span><span class="sxs-lookup"><span data-stu-id="d4ee7-120">The [**CImagePalette::MakePalette**](cimagepalette-makepalette.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4ee7-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4ee7-121">Requirements</span></span>



| <span data-ttu-id="d4ee7-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4ee7-122">Requirement</span></span> | <span data-ttu-id="d4ee7-123">Wert</span><span class="sxs-lookup"><span data-stu-id="d4ee7-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4ee7-124">Header</span><span class="sxs-lookup"><span data-stu-id="d4ee7-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d4ee7-125"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d4ee7-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d4ee7-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d4ee7-126">Library</span></span><br/> | <dl> <span data-ttu-id="d4ee7-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d4ee7-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4ee7-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4ee7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4ee7-129">**Cimagepalette-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d4ee7-129">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




