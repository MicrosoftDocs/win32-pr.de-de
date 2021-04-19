---
description: Die gezmartrecompressformat-Methode ruft das aktuelle Komprimierungs Format für die intelligente Neukomprimierung ab.
ms.assetid: 2d420fe9-691d-4cc9-a8de-363a4be1b364
title: 'Iamtimelinegroup:: gezmartrecompressformat-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetSmartRecompressFormat
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8560bb9d8da6904cf74b62ffd238b234e9c74ed6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358108"
---
# <a name="iamtimelinegroupgetsmartrecompressformat-method"></a><span data-ttu-id="2e148-103">Iamtimelinegroup:: gezmartrecompressformat-Methode</span><span class="sxs-lookup"><span data-stu-id="2e148-103">IAMTimelineGroup::GetSmartRecompressFormat method</span></span>

> [!Note]  
> <span data-ttu-id="2e148-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="2e148-104">\[Deprecated.</span></span> <span data-ttu-id="2e148-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="2e148-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2e148-106">Die- `GetSmartRecompressFormat` Methode ruft das aktuelle Komprimierungs Format für die intelligente Neukomprimierung ab.</span><span class="sxs-lookup"><span data-stu-id="2e148-106">The `GetSmartRecompressFormat` method retrieves the current compression format for smart recompression.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e148-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e148-107">Syntax</span></span>


```C++
HRESULT GetSmartRecompressFormat(
   long **ppFormat
);
```



## <a name="parameters"></a><span data-ttu-id="2e148-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e148-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e148-109">*ppformat*</span><span class="sxs-lookup"><span data-stu-id="2e148-109">*ppFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="2e148-110">Empfängt einen Zeiger auf eine [**SCompFmt0**](scompfmt0.md) -Struktur, die als Zeiger auf einen Long-Typ umgewandelt wird.</span><span class="sxs-lookup"><span data-stu-id="2e148-110">Receives a pointer to an [**SCompFmt0**](scompfmt0.md) structure, cast as a pointer to a long.</span></span> <span data-ttu-id="2e148-111">Wenn die Methode fehlschlägt, wird der Wert auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2e148-111">If the method fails, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e148-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e148-112">Return value</span></span>

<span data-ttu-id="2e148-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="2e148-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2e148-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2e148-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e148-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e148-115">Remarks</span></span>

<span data-ttu-id="2e148-116">Wenn die Anwendung kein intelligentes Komprimierungs Format festgelegt hat (durch Aufrufen von [**iamtimelinegroup:: setionmartrecompressformat**](iamtimelinegroup-setsmartrecompressformat.md)), ist das von dieser Methode zurückgegebene Format ungültig.</span><span class="sxs-lookup"><span data-stu-id="2e148-116">If the application has not set a smart compression format (by calling [**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md)), the format returned by this method will be invalid.</span></span> <span data-ttu-id="2e148-117">Rufen Sie die [**iamtimelinegroup:: issmartrecompressformatset**](iamtimelinegroup-issmartrecompressformatset.md) -Methode auf, um zu bestimmen, ob ein Komprimierungs Format festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="2e148-117">Call the [**IAMTimelineGroup::IsSmartRecompressFormatSet**](iamtimelinegroup-issmartrecompressformatset.md) method to determine whether a compression format was set.</span></span>

<span data-ttu-id="2e148-118">Wenn die Methode erfolgreich ausgeführt wird, muss der Aufrufer den zurückgegebenen Medientyp freigeben und die [**SCompFmt0**](scompfmt0.md) -Struktur löschen:</span><span class="sxs-lookup"><span data-stu-id="2e148-118">If the method succeeds, the caller must free the returned media type and delete the [**SCompFmt0**](scompfmt0.md) structure:</span></span>


```C++
if (pFormat) {
    FreeMediaType(pFormat->MediaType);
    delete pFormat;
}
```



> [!Note]  
> <span data-ttu-id="2e148-119">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="2e148-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2e148-120">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="2e148-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2e148-121">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2e148-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2e148-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e148-122">Requirements</span></span>



| <span data-ttu-id="2e148-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e148-123">Requirement</span></span> | <span data-ttu-id="2e148-124">Wert</span><span class="sxs-lookup"><span data-stu-id="2e148-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e148-125">Header</span><span class="sxs-lookup"><span data-stu-id="2e148-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2e148-126"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="2e148-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2e148-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2e148-127">Library</span></span><br/> | <dl> <span data-ttu-id="2e148-128"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="2e148-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e148-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e148-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e148-130">**Iamtimelinegroup-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="2e148-130">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="2e148-131">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="2e148-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




