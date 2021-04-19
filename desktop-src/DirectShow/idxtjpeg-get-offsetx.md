---
description: Die get \_ OffsetX-Methode ruft den horizontalen Offset des Ursprungs der Löschung ab.
ms.assetid: 0ca97bb9-9359-4098-9e80-1847da4154ec
title: 'Idxtjpeg:: get_OffsetX-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_OffsetX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d18d8ede94700f2de2fe49e44031675c7c91c930
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355992"
---
# <a name="idxtjpegget_offsetx-method"></a><span data-ttu-id="deeed-103">Idxtjpeg:: get \_ OffsetX-Methode</span><span class="sxs-lookup"><span data-stu-id="deeed-103">IDxtJpeg::get\_OffsetX method</span></span>

> [!Note]  
> <span data-ttu-id="deeed-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="deeed-104">\[Deprecated.</span></span> <span data-ttu-id="deeed-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="deeed-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="deeed-106">Die- `get_OffsetX` Methode ruft den horizontalen Offset des Ursprungs der Löschung ab.</span><span class="sxs-lookup"><span data-stu-id="deeed-106">The `get_OffsetX` method retrieves the horizontal offset of the wipe origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="deeed-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="deeed-107">Syntax</span></span>


```C++
HRESULT get_OffsetX(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="deeed-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="deeed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="deeed-109">*PVal* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="deeed-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="deeed-110">Empfängt den horizontalen Offset des Ursprungs der Löschung in Pixel.</span><span class="sxs-lookup"><span data-stu-id="deeed-110">Receives the horizontal offset of the wipe origin, in pixels.</span></span> <span data-ttu-id="deeed-111">Der Mittelpunkt der Löschung wird um diesen Betrag versetzt.</span><span class="sxs-lookup"><span data-stu-id="deeed-111">The center of the wipe is offset by this amount.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="deeed-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="deeed-112">Return value</span></span>

<span data-ttu-id="deeed-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="deeed-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="deeed-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="deeed-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="deeed-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="deeed-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="deeed-116">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="deeed-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="deeed-117">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="deeed-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="deeed-118">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="deeed-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="deeed-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="deeed-119">Requirements</span></span>



| <span data-ttu-id="deeed-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="deeed-120">Requirement</span></span> | <span data-ttu-id="deeed-121">Wert</span><span class="sxs-lookup"><span data-stu-id="deeed-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="deeed-122">Header</span><span class="sxs-lookup"><span data-stu-id="deeed-122">Header</span></span><br/>  | <dl> <span data-ttu-id="deeed-123"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="deeed-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="deeed-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="deeed-124">Library</span></span><br/> | <dl> <span data-ttu-id="deeed-125"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="deeed-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="deeed-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="deeed-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="deeed-127">**Idxtjpeg-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="deeed-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




