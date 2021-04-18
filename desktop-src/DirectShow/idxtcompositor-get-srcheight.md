---
description: Die get \_ srcHeight-Methode ruft die Höhe des Quell Rechtecks ab.
ms.assetid: 3c6647b3-dfca-490d-a3d5-9aa6988e387d
title: 'Idxtcompositor:: get_SrcHeight-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.get_SrcHeight
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b3ad874d7c02a9c9300af7fe3dbc69f6d351bba8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371237"
---
# <a name="idxtcompositorget_srcheight-method"></a><span data-ttu-id="506a8-103">Idxtcompositor:: get \_ srcHeight-Methode</span><span class="sxs-lookup"><span data-stu-id="506a8-103">IDxtCompositor::get\_SrcHeight method</span></span>

> [!Note]  
> <span data-ttu-id="506a8-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="506a8-104">\[Deprecated.</span></span> <span data-ttu-id="506a8-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="506a8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="506a8-106">Die- `get_SrcHeight` Methode ruft die Höhe des Quell Rechtecks ab.</span><span class="sxs-lookup"><span data-stu-id="506a8-106">The `get_SrcHeight` method retrieves the height of the source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="506a8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="506a8-107">Syntax</span></span>


```C++
HRESULT get_SrcHeight(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="506a8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="506a8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="506a8-109">*PVal* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="506a8-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="506a8-110">Empfängt die Höhe des Quell Rechtecks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="506a8-110">Receives the height of the source rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="506a8-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="506a8-111">Return value</span></span>

<span data-ttu-id="506a8-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="506a8-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="506a8-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="506a8-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="506a8-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="506a8-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="506a8-115">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="506a8-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="506a8-116">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="506a8-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="506a8-117">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="506a8-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="506a8-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="506a8-118">Requirements</span></span>



| <span data-ttu-id="506a8-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="506a8-119">Requirement</span></span> | <span data-ttu-id="506a8-120">Wert</span><span class="sxs-lookup"><span data-stu-id="506a8-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="506a8-121">Header</span><span class="sxs-lookup"><span data-stu-id="506a8-121">Header</span></span><br/>  | <dl> <span data-ttu-id="506a8-122"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="506a8-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="506a8-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="506a8-123">Library</span></span><br/> | <dl> <span data-ttu-id="506a8-124"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="506a8-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="506a8-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="506a8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="506a8-126">**Idxtcompositor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="506a8-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




