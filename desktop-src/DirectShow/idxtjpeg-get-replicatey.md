---
description: Die get \_ Repli-Methode ruft die Häufigkeit ab, mit der das Muster für das Löschen vertikal repliziert wird.
ms.assetid: 347e1ffa-bb39-4980-b8af-5806a23d1334
title: 'Idxtjpeg:: get_ReplicateY-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_ReplicateY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8ae5c68d153b64783f84a6c4c4a8ba7f5d5f0f24
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352147"
---
# <a name="idxtjpegget_replicatey-method"></a><span data-ttu-id="e61aa-103">Idxtjpeg:: get \_ replialisiey-Methode</span><span class="sxs-lookup"><span data-stu-id="e61aa-103">IDxtJpeg::get\_ReplicateY method</span></span>

> [!Note]  
> <span data-ttu-id="e61aa-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="e61aa-104">\[Deprecated.</span></span> <span data-ttu-id="e61aa-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="e61aa-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e61aa-106">Die- `get_ReplicateY` Methode ruft die Häufigkeit ab, mit der das Muster für das Löschen vertikal repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="e61aa-106">The `get_ReplicateY` method retrieves the number of times the wipe pattern is replicated vertically.</span></span>

## <a name="syntax"></a><span data-ttu-id="e61aa-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e61aa-107">Syntax</span></span>


```C++
HRESULT get_ReplicateY(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="e61aa-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e61aa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e61aa-109">*PVal* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="e61aa-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e61aa-110">Empfängt die Häufigkeit, mit der das Muster für das Löschen vertikal repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="e61aa-110">Receives the number of times the wipe pattern is replicated vertically.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e61aa-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e61aa-111">Return value</span></span>

<span data-ttu-id="e61aa-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="e61aa-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e61aa-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e61aa-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e61aa-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e61aa-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e61aa-115">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="e61aa-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e61aa-116">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="e61aa-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e61aa-117">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e61aa-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e61aa-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e61aa-118">Requirements</span></span>



| <span data-ttu-id="e61aa-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e61aa-119">Requirement</span></span> | <span data-ttu-id="e61aa-120">Wert</span><span class="sxs-lookup"><span data-stu-id="e61aa-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e61aa-121">Header</span><span class="sxs-lookup"><span data-stu-id="e61aa-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e61aa-122"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="e61aa-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e61aa-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e61aa-123">Library</span></span><br/> | <dl> <span data-ttu-id="e61aa-124"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="e61aa-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e61aa-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e61aa-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e61aa-126">**Idxtjpeg-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="e61aa-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




