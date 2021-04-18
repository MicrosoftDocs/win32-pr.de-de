---
description: Die get \_ currentstream-Methode ruft die streamnummer ab, die derzeit vom Medien Detektor verwendet wird.
ms.assetid: 0f590498-e639-4b6b-be1d-f1e4a36282cb
title: 'Imediadet:: get_CurrentStream-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_CurrentStream
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 98e664e88862a6bc124a88ac23cedf29e687d51e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372064"
---
# <a name="imediadetget_currentstream-method"></a><span data-ttu-id="0b371-103">Imediadet:: get \_ currentstream-Methode</span><span class="sxs-lookup"><span data-stu-id="0b371-103">IMediaDet::get\_CurrentStream method</span></span>

> [!Note]  
> <span data-ttu-id="0b371-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="0b371-104">\[Deprecated.</span></span> <span data-ttu-id="0b371-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="0b371-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0b371-106">Die- `get_CurrentStream` Methode ruft die streamnummer ab, die derzeit vom Medien Erkennungs Modul verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0b371-106">The `get_CurrentStream` method retrieves the stream number currently used by the media detector.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b371-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b371-107">Syntax</span></span>


```C++
HRESULT get_CurrentStream(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="0b371-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b371-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b371-109">*PVal* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="0b371-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="0b371-110">Empfängt die aktuelle streamnummer.</span><span class="sxs-lookup"><span data-stu-id="0b371-110">Receives the current stream number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b371-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0b371-111">Return value</span></span>

<span data-ttu-id="0b371-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="0b371-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0b371-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0b371-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b371-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b371-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0b371-115">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="0b371-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0b371-116">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="0b371-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0b371-117">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0b371-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0b371-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b371-118">Requirements</span></span>



| <span data-ttu-id="0b371-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b371-119">Requirement</span></span> | <span data-ttu-id="0b371-120">Wert</span><span class="sxs-lookup"><span data-stu-id="0b371-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b371-121">Header</span><span class="sxs-lookup"><span data-stu-id="0b371-121">Header</span></span><br/>  | <dl> <span data-ttu-id="0b371-122"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="0b371-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0b371-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0b371-123">Library</span></span><br/> | <dl> <span data-ttu-id="0b371-124"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="0b371-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b371-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b371-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b371-126">**Imediadet-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="0b371-126">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="0b371-127">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="0b371-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




