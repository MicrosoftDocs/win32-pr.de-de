---
description: Die get \_ OffsetX-Methode ruft den horizontalen Offset des Ziel Rechtecks ab.
ms.assetid: a9d8c81b-f978-4b47-9c7f-12cee7c2c40d
title: 'Idxtcompositor:: get_OffsetX-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.get_OffsetX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f8e2f21956e67b42158f4e646d33aa6e3e90d9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372701"
---
# <a name="idxtcompositorget_offsetx-method"></a><span data-ttu-id="4d958-103">Idxtcompositor:: get \_ OffsetX-Methode</span><span class="sxs-lookup"><span data-stu-id="4d958-103">IDxtCompositor::get\_OffsetX method</span></span>

> [!Note]  
> <span data-ttu-id="4d958-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="4d958-104">\[Deprecated.</span></span> <span data-ttu-id="4d958-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="4d958-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4d958-106">Die- `get_OffsetX` Methode ruft den horizontalen Offset des Ziel Rechtecks ab.</span><span class="sxs-lookup"><span data-stu-id="4d958-106">The `get_OffsetX` method retrieves the horizontal offset of the target rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d958-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d958-107">Syntax</span></span>


```C++
HRESULT get_OffsetX(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="4d958-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d958-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d958-109">*PVal* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="4d958-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="4d958-110">Empfängt den horizontalen Offset des Ziel Rechtecks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="4d958-110">Receives the horizontal offset of the target rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d958-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4d958-111">Return value</span></span>

<span data-ttu-id="4d958-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="4d958-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4d958-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4d958-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d958-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4d958-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4d958-115">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="4d958-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4d958-116">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="4d958-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4d958-117">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4d958-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4d958-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4d958-118">Requirements</span></span>



| <span data-ttu-id="4d958-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4d958-119">Requirement</span></span> | <span data-ttu-id="4d958-120">Wert</span><span class="sxs-lookup"><span data-stu-id="4d958-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d958-121">Header</span><span class="sxs-lookup"><span data-stu-id="4d958-121">Header</span></span><br/>  | <dl> <span data-ttu-id="4d958-122"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="4d958-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4d958-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4d958-123">Library</span></span><br/> | <dl> <span data-ttu-id="4d958-124"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="4d958-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d958-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d958-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d958-126">**Idxtcompositor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="4d958-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




