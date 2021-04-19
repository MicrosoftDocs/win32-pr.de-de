---
description: Die get \_ streamtypeb-Methode ruft eine Zeichenfolge ab, die die GUID des Medientyps für den aktuellen Stream darstellt.
ms.assetid: 99ae4b52-4449-4b7c-babf-1a6cba479499
title: 'Imediadet:: get_StreamTypeB-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamTypeB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fd1cdf4bbadfa769654f20792cf2fda17dbe2806
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367771"
---
# <a name="imediadetget_streamtypeb-method"></a><span data-ttu-id="27afd-103">Imediadet:: get \_ streamtypeb-Methode</span><span class="sxs-lookup"><span data-stu-id="27afd-103">IMediaDet::get\_StreamTypeB method</span></span>

> [!Note]  
> <span data-ttu-id="27afd-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="27afd-104">\[Deprecated.</span></span> <span data-ttu-id="27afd-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="27afd-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="27afd-106">Die- `get_StreamTypeB` Methode ruft eine Zeichenfolge ab, die die GUID des Medientyps für den aktuellen Stream darstellt.</span><span class="sxs-lookup"><span data-stu-id="27afd-106">The `get_StreamTypeB` method retrieves a string representing the GUID of the media type for the current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="27afd-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="27afd-107">Syntax</span></span>


```C++
HRESULT get_StreamTypeB(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="27afd-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="27afd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27afd-109">*PVal* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="27afd-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="27afd-110">Empfängt eine Zeichen folgen Darstellung der Medientyp-GUID.</span><span class="sxs-lookup"><span data-stu-id="27afd-110">Receives a string representation of the media type GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27afd-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="27afd-111">Return value</span></span>

<span data-ttu-id="27afd-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="27afd-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="27afd-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="27afd-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="27afd-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27afd-114">Remarks</span></span>

<span data-ttu-id="27afd-115">Der zurückgegebene **BSTR** ist wie folgt formatiert: `{73647561-0000-0010-8000-00AA00389B71}`</span><span class="sxs-lookup"><span data-stu-id="27afd-115">The returned **BSTR** is formatted like the following: `{73647561-0000-0010-8000-00AA00389B71}`</span></span>

<span data-ttu-id="27afd-116">Die-Methode ordnet Speicher für die Zeichenfolge zu.</span><span class="sxs-lookup"><span data-stu-id="27afd-116">The method allocates memory for the string.</span></span> <span data-ttu-id="27afd-117">Die Anwendung muss **SysFreeString** aufzurufen, um den Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="27afd-117">The application must call **SysFreeString** to free the memory.</span></span>

<span data-ttu-id="27afd-118">Bevor Sie diese Methode aufrufen, legen Sie den Dateinamen und den Stream durch Aufrufen von [**imediadet::p UT \_ filename**](imediadet-put-filename.md) und [**imediadet::p UT \_ currentstream**](imediadet-put-currentstream.md)fest.</span><span class="sxs-lookup"><span data-stu-id="27afd-118">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="27afd-119">Wenn sich der Medien Detektor im bitmapingmodus befindet, gibt diese Methode E \_ invalidArg zurück.</span><span class="sxs-lookup"><span data-stu-id="27afd-119">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="27afd-120">Weitere Informationen finden Sie unter [**imediadet:: enterbitmapgrabmode**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="27afd-120">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="27afd-121">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="27afd-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="27afd-122">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="27afd-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="27afd-123">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="27afd-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="27afd-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27afd-124">Requirements</span></span>



| <span data-ttu-id="27afd-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27afd-125">Requirement</span></span> | <span data-ttu-id="27afd-126">Wert</span><span class="sxs-lookup"><span data-stu-id="27afd-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27afd-127">Header</span><span class="sxs-lookup"><span data-stu-id="27afd-127">Header</span></span><br/>  | <dl> <span data-ttu-id="27afd-128"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="27afd-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="27afd-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="27afd-129">Library</span></span><br/> | <dl> <span data-ttu-id="27afd-130"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="27afd-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27afd-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27afd-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27afd-132">**Imediadet-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="27afd-132">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="27afd-133">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="27afd-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




