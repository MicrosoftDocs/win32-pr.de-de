---
description: Die get \_ masknum-Methode ruft den SMPTE-Code zum Löschen der Löschung ab.
ms.assetid: 49710d40-acc0-453e-ac9c-882794a0b82d
title: 'Idxtjpeg:: get_MaskNum-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_MaskNum
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 869809fdea6e1c329088abca50a1670239554327
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370637"
---
# <a name="idxtjpegget_masknum-method"></a><span data-ttu-id="98a19-103">Idxtjpeg:: get \_ masknum-Methode</span><span class="sxs-lookup"><span data-stu-id="98a19-103">IDxtJpeg::get\_MaskNum method</span></span>

> [!Note]  
> <span data-ttu-id="98a19-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="98a19-104">\[Deprecated.</span></span> <span data-ttu-id="98a19-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="98a19-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="98a19-106">Die- `get_MaskNum` Methode ruft den SMPTE-Code zum Löschen der Löschung ab.</span><span class="sxs-lookup"><span data-stu-id="98a19-106">The `get_MaskNum` method retrieves the SMPTE wipe code of the wipe.</span></span>

## <a name="syntax"></a><span data-ttu-id="98a19-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="98a19-107">Syntax</span></span>


```C++
HRESULT get_MaskNum(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="98a19-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="98a19-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98a19-109">*PVal* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="98a19-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="98a19-110">Empfängt den Code zum Löschen von SMPTE.</span><span class="sxs-lookup"><span data-stu-id="98a19-110">Receives the SMPTE wipe code.</span></span> <span data-ttu-id="98a19-111">Eine Liste der unterstützten SMPTE-Wipes finden Sie unter [SMPTE](smpte-wipe-transition.md)-Zurücksetzungs Übergang.</span><span class="sxs-lookup"><span data-stu-id="98a19-111">For a list of supported SMPTE wipes, see [SMPTE Wipe Transition](smpte-wipe-transition.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98a19-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="98a19-112">Return value</span></span>

<span data-ttu-id="98a19-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="98a19-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="98a19-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="98a19-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="98a19-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98a19-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="98a19-116">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="98a19-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="98a19-117">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="98a19-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="98a19-118">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="98a19-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="98a19-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98a19-119">Requirements</span></span>



| <span data-ttu-id="98a19-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="98a19-120">Requirement</span></span> | <span data-ttu-id="98a19-121">Wert</span><span class="sxs-lookup"><span data-stu-id="98a19-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98a19-122">Header</span><span class="sxs-lookup"><span data-stu-id="98a19-122">Header</span></span><br/>  | <dl> <span data-ttu-id="98a19-123"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="98a19-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="98a19-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="98a19-124">Library</span></span><br/> | <dl> <span data-ttu-id="98a19-125"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="98a19-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98a19-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98a19-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98a19-127">**Idxtjpeg-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="98a19-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




