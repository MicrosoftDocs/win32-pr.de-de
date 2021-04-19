---
description: Mit der Put \_ repliplatey-Methode wird angegeben, wie oft das Muster für das Löschen vertikal repliziert wird.
ms.assetid: f27e0d54-1d0f-42fe-9638-39f68b97f9c7
title: Idxtjpeg::p ut_ReplicateY-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_ReplicateY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1ac5016635cb8e6f5b81b99f1ea67f0282878d8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369716"
---
# <a name="idxtjpegput_replicatey-method"></a><span data-ttu-id="22fbc-103">Idxtjpeg::p UT \_ replialisiey-Methode</span><span class="sxs-lookup"><span data-stu-id="22fbc-103">IDxtJpeg::put\_ReplicateY method</span></span>

> [!Note]  
> <span data-ttu-id="22fbc-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="22fbc-104">\[Deprecated.</span></span> <span data-ttu-id="22fbc-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="22fbc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="22fbc-106">Die- `put_ReplicateY` Methode gibt an, wie oft das Abbild für die Löschung vertikal repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="22fbc-106">The `put_ReplicateY` method specifies the number of times the wipe pattern is replicated vertically.</span></span>

## <a name="syntax"></a><span data-ttu-id="22fbc-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="22fbc-107">Syntax</span></span>


```C++
HRESULT put_ReplicateY(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="22fbc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="22fbc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22fbc-109">*NewVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22fbc-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22fbc-110">Gibt an, wie oft das Muster für die Löschung vertikal repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="22fbc-110">The number of times the wipe pattern is replicated vertically.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22fbc-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22fbc-111">Return value</span></span>

<span data-ttu-id="22fbc-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="22fbc-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="22fbc-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="22fbc-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="22fbc-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22fbc-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="22fbc-115">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="22fbc-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="22fbc-116">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="22fbc-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="22fbc-117">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="22fbc-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="22fbc-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22fbc-118">Requirements</span></span>



| <span data-ttu-id="22fbc-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22fbc-119">Requirement</span></span> | <span data-ttu-id="22fbc-120">Wert</span><span class="sxs-lookup"><span data-stu-id="22fbc-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22fbc-121">Header</span><span class="sxs-lookup"><span data-stu-id="22fbc-121">Header</span></span><br/>  | <dl> <span data-ttu-id="22fbc-122"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="22fbc-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="22fbc-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="22fbc-123">Library</span></span><br/> | <dl> <span data-ttu-id="22fbc-124"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="22fbc-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22fbc-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22fbc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22fbc-126">**Idxtjpeg-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="22fbc-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




