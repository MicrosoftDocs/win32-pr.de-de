---
description: Die getvendorstring-Methode ruft den Namen des Anbieters ab. Bei den Renderengine-Objekten, die von DirectShow bereitgestellt werden, ist die Hersteller Zeichenfolge &\# 0034; Microsoft Corporation&\# 0034;.
ms.assetid: d0a4c525-67dc-419a-b4d6-8cd51888fd8a
title: 'Unenderengine:: getvendorstring-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetVendorString
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: abf339b73fa058c6554965c16428774ad1fdd32c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358670"
---
# <a name="irenderenginegetvendorstring-method"></a><span data-ttu-id="78199-104">Unenderengine:: getvendorstring-Methode</span><span class="sxs-lookup"><span data-stu-id="78199-104">IRenderEngine::GetVendorString method</span></span>

> [!Note]  
> <span data-ttu-id="78199-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="78199-105">\[Deprecated.</span></span> <span data-ttu-id="78199-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="78199-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="78199-107">Die- `GetVendorString` Methode ruft den Namen des Anbieters ab.</span><span class="sxs-lookup"><span data-stu-id="78199-107">The `GetVendorString` method retrieves the name of the vendor.</span></span> <span data-ttu-id="78199-108">Bei den Renderengine-Objekten, die von DirectShow bereitgestellt werden, lautet die Hersteller Zeichenfolge "Microsoft Corporation".</span><span class="sxs-lookup"><span data-stu-id="78199-108">For the render engine objects that are provided by DirectShow, the vendor string is "Microsoft Corporation".</span></span>

## <a name="syntax"></a><span data-ttu-id="78199-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="78199-109">Syntax</span></span>


```C++
HRESULT GetVendorString(
  [out, retval] BSTR *pVendorID
);
```



## <a name="parameters"></a><span data-ttu-id="78199-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="78199-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78199-111">*pvendorid* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="78199-111">*pVendorID* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="78199-112">Empfängt ein **BSTR** , das die Hersteller Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="78199-112">Receives a **BSTR** containing the vendor string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78199-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="78199-113">Return value</span></span>

<span data-ttu-id="78199-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="78199-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="78199-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="78199-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="78199-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78199-116">Remarks</span></span>

<span data-ttu-id="78199-117">Die-Methode ordnet Speicher für die Zeichenfolge zu.</span><span class="sxs-lookup"><span data-stu-id="78199-117">The method allocates memory for the string.</span></span> <span data-ttu-id="78199-118">Die Anwendung muss **SysFreeString** aufzurufen, um den Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="78199-118">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="78199-119">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="78199-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="78199-120">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="78199-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="78199-121">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="78199-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="78199-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78199-122">Requirements</span></span>



| <span data-ttu-id="78199-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78199-123">Requirement</span></span> | <span data-ttu-id="78199-124">Wert</span><span class="sxs-lookup"><span data-stu-id="78199-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="78199-125">Header</span><span class="sxs-lookup"><span data-stu-id="78199-125">Header</span></span><br/>  | <dl> <span data-ttu-id="78199-126"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="78199-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="78199-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="78199-127">Library</span></span><br/> | <dl> <span data-ttu-id="78199-128"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="78199-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78199-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78199-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78199-130">**Schnittstelle ""**</span><span class="sxs-lookup"><span data-stu-id="78199-130">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="78199-131">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="78199-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




