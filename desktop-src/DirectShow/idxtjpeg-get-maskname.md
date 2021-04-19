---
description: Die get \_ maskname-Methode ruft den Namen einer JPEG-Datei ab, die als abzurufende Maske verwendet werden soll.
ms.assetid: b21913c0-4269-41f9-b2f0-ae69be9c0871
title: 'Idxtjpeg:: get_MaskName-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_MaskName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a00c8104ee19cac33a00ff9062006338a19e283b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370004"
---
# <a name="idxtjpegget_maskname-method"></a><span data-ttu-id="5f1cc-103">Idxtjpeg:: get \_ maskname-Methode</span><span class="sxs-lookup"><span data-stu-id="5f1cc-103">IDxtJpeg::get\_MaskName method</span></span>

> [!Note]  
> <span data-ttu-id="5f1cc-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="5f1cc-104">\[Deprecated.</span></span> <span data-ttu-id="5f1cc-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="5f1cc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5f1cc-106">Die- `get_MaskName` Methode ruft den Namen einer JPEG-Datei ab, die als abzurufende Maske verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5f1cc-106">The `get_MaskName` method retrieves the name of a JPEG file to be used as the wipe mask.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f1cc-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f1cc-107">Syntax</span></span>


```C++
HRESULT get_MaskName(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="5f1cc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f1cc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f1cc-109">*PVal* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="5f1cc-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5f1cc-110">Empfängt den Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="5f1cc-110">Receives the file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f1cc-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5f1cc-111">Return value</span></span>

<span data-ttu-id="5f1cc-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="5f1cc-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5f1cc-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5f1cc-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f1cc-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f1cc-114">Remarks</span></span>

<span data-ttu-id="5f1cc-115">Wenn der zurücksetzungübergang eines der integrierten SMPTE-setzt verwendet, die es unterstützt, ist der Wert dieser Eigenschaft eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="5f1cc-115">If the wipe transition is using one of the built-in SMPTE wipes that it supports, the value of this property is an empty string.</span></span>

<span data-ttu-id="5f1cc-116">Der Aufrufer muss die zurückgegebene Zeichenfolge mit der **sysfrestring** -Funktion freigeben.</span><span class="sxs-lookup"><span data-stu-id="5f1cc-116">The caller must release the returned string, using the **SysFreeString** function.</span></span>

> [!Note]  
> <span data-ttu-id="5f1cc-117">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="5f1cc-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5f1cc-118">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="5f1cc-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5f1cc-119">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5f1cc-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5f1cc-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f1cc-120">Requirements</span></span>



| <span data-ttu-id="5f1cc-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f1cc-121">Requirement</span></span> | <span data-ttu-id="5f1cc-122">Wert</span><span class="sxs-lookup"><span data-stu-id="5f1cc-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f1cc-123">Header</span><span class="sxs-lookup"><span data-stu-id="5f1cc-123">Header</span></span><br/>  | <dl> <span data-ttu-id="5f1cc-124"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="5f1cc-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5f1cc-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5f1cc-125">Library</span></span><br/> | <dl> <span data-ttu-id="5f1cc-126"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="5f1cc-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f1cc-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f1cc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f1cc-128">**Idxtjpeg-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5f1cc-128">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> <dt>

[<span data-ttu-id="5f1cc-129">**Idxtjpeg:: get \_ masknum**</span><span class="sxs-lookup"><span data-stu-id="5f1cc-129">**IDxtJpeg::get\_MaskNum**</span></span>](idxtjpeg-get-masknum.md)
</dt> </dl>

 

 




