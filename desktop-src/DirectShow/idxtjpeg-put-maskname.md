---
description: Die Put \_ maskname-Methode gibt den Namen einer JPEG-Datei an, die als abzurufende Maske verwendet werden soll.
ms.assetid: f2b93c1e-479e-46c1-afe3-25b0ef720ab3
title: Idxtjpeg::p ut_MaskName-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_MaskName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f74fe09572b95ff1508021b3fa2ae4f9888f2d5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367081"
---
# <a name="idxtjpegput_maskname-method"></a><span data-ttu-id="a0b82-103">Idxtjpeg::p UT \_ maskname-Methode</span><span class="sxs-lookup"><span data-stu-id="a0b82-103">IDxtJpeg::put\_MaskName method</span></span>

> [!Note]  
> <span data-ttu-id="a0b82-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="a0b82-104">\[Deprecated.</span></span> <span data-ttu-id="a0b82-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="a0b82-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a0b82-106">Die- `put_MaskName` Methode gibt den Namen einer JPEG-Datei an, die als abzurufende Maske verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0b82-106">The `put_MaskName` method specifies the name of a JPEG file to use as the wipe mask.</span></span> <span data-ttu-id="a0b82-107">Diese Maske wird anstelle einer der integrierten Masken für das Löschen verwendet.</span><span class="sxs-lookup"><span data-stu-id="a0b82-107">This mask will be used instead of one of the built-in wipe masks.</span></span> <span data-ttu-id="a0b82-108">Die Datei muss einen Farbverlauf von 8 Bits pro Pixel enthalten.</span><span class="sxs-lookup"><span data-stu-id="a0b82-108">The file must contain a monochrome, 8-bits-per-pixel gradient.</span></span> <span data-ttu-id="a0b82-109">Der Farbverlauf wird als Maske zum Definieren des Fortschritts der Löschung verwendet.</span><span class="sxs-lookup"><span data-stu-id="a0b82-109">The gradient is used as a mask to define the wipe's progression.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0b82-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0b82-110">Syntax</span></span>


```C++
HRESULT put_MaskName(
  [in] BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="a0b82-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0b82-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0b82-112">*NewVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0b82-112">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0b82-113">Gibt den Namen der Datei an.</span><span class="sxs-lookup"><span data-stu-id="a0b82-113">Specifies the name of the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0b82-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a0b82-114">Return value</span></span>

<span data-ttu-id="a0b82-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="a0b82-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a0b82-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a0b82-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0b82-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a0b82-117">Remarks</span></span>

<span data-ttu-id="a0b82-118">Legen Sie die **masknum** -Eigenschaft fest, um zu einer integrierten Maske zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="a0b82-118">To revert to a built-in mask, set the **MaskNum** property.</span></span>

> [!Note]  
> <span data-ttu-id="a0b82-119">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="a0b82-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a0b82-120">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="a0b82-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a0b82-121">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a0b82-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a0b82-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a0b82-122">Requirements</span></span>



| <span data-ttu-id="a0b82-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a0b82-123">Requirement</span></span> | <span data-ttu-id="a0b82-124">Wert</span><span class="sxs-lookup"><span data-stu-id="a0b82-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0b82-125">Header</span><span class="sxs-lookup"><span data-stu-id="a0b82-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a0b82-126"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="a0b82-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a0b82-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a0b82-127">Library</span></span><br/> | <dl> <span data-ttu-id="a0b82-128"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="a0b82-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0b82-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0b82-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0b82-130">**Idxtjpeg-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a0b82-130">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> <dt>

[<span data-ttu-id="a0b82-131">**Idxtjpeg::p UT- \_ masknum**</span><span class="sxs-lookup"><span data-stu-id="a0b82-131">**IDxtJpeg::put\_MaskNum**</span></span>](idxtjpeg-put-masknum.md)
</dt> </dl>

 

 




