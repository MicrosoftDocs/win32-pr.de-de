---
description: Die get \_ filename-Methode ruft den Namen der Quelldatei ab, die derzeit vom Medien Erkennungs Modul verwendet wird.
ms.assetid: 68f0f1ea-74a2-4b65-9f1d-8699326d9d04
title: 'Imediadet:: get_filename-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_Filename
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 95a350dde3dfdc1c6046c8e31b8a2d9e62684788
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369171"
---
# <a name="imediadetget_filename-method"></a><span data-ttu-id="cf7eb-103">Imediadet:: get \_ filename-Methode</span><span class="sxs-lookup"><span data-stu-id="cf7eb-103">IMediaDet::get\_Filename method</span></span>

> [!Note]  
> <span data-ttu-id="cf7eb-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="cf7eb-104">\[Deprecated.</span></span> <span data-ttu-id="cf7eb-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="cf7eb-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="cf7eb-106">Die- `get_Filename` Methode ruft den Namen der Quelldatei ab, die derzeit vom Medien Erkennungs Modul verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cf7eb-106">The `get_Filename` method retrieves the name of the source file currently used by the media detector.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf7eb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf7eb-107">Syntax</span></span>


```C++
HRESULT get_Filename(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="cf7eb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf7eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf7eb-109">*PVal* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="cf7eb-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="cf7eb-110">Empfängt den Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="cf7eb-110">Receives the file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf7eb-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf7eb-111">Return value</span></span>

<span data-ttu-id="cf7eb-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="cf7eb-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cf7eb-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cf7eb-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf7eb-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf7eb-114">Remarks</span></span>

<span data-ttu-id="cf7eb-115">Die-Methode ordnet Speicher für die Zeichenfolge zu.</span><span class="sxs-lookup"><span data-stu-id="cf7eb-115">The method allocates memory for the string.</span></span> <span data-ttu-id="cf7eb-116">Die Anwendung muss **SysFreeString** aufzurufen, um den Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="cf7eb-116">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="cf7eb-117">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="cf7eb-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="cf7eb-118">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="cf7eb-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="cf7eb-119">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cf7eb-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cf7eb-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf7eb-120">Requirements</span></span>



| <span data-ttu-id="cf7eb-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf7eb-121">Requirement</span></span> | <span data-ttu-id="cf7eb-122">Wert</span><span class="sxs-lookup"><span data-stu-id="cf7eb-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf7eb-123">Header</span><span class="sxs-lookup"><span data-stu-id="cf7eb-123">Header</span></span><br/>  | <dl> <span data-ttu-id="cf7eb-124"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="cf7eb-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="cf7eb-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cf7eb-125">Library</span></span><br/> | <dl> <span data-ttu-id="cf7eb-126"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="cf7eb-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf7eb-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf7eb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf7eb-128">**Imediadet-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="cf7eb-128">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="cf7eb-129">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="cf7eb-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




