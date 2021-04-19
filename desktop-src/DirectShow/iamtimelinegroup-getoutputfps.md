---
description: Die getoutputfps-Methode ruft die Ausgabe Frame Rate dieser Gruppe ab.
ms.assetid: e6dfa4a9-4d44-4ce7-9aec-3564fd337ff6
title: 'Iamtimelinegroup:: getoutputfps-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetOutputFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2f02e7db36e5ea61e3c738b4c2d92678674bfcec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372002"
---
# <a name="iamtimelinegroupgetoutputfps-method"></a><span data-ttu-id="3fbe6-103">Iamtimelinegroup:: getoutputfps-Methode</span><span class="sxs-lookup"><span data-stu-id="3fbe6-103">IAMTimelineGroup::GetOutputFPS method</span></span>

> [!Note]  
> <span data-ttu-id="3fbe6-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="3fbe6-104">\[Deprecated.</span></span> <span data-ttu-id="3fbe6-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="3fbe6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3fbe6-106">Die- `GetOutputFPS` Methode ruft die Ausgabe Frame Rate dieser Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="3fbe6-106">The `GetOutputFPS` method retrieves the output frame rate of this group.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fbe6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3fbe6-107">Syntax</span></span>


```C++
HRESULT GetOutputFPS(
   double *pFPS
);
```



## <a name="parameters"></a><span data-ttu-id="3fbe6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3fbe6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fbe6-109">*pfps*</span><span class="sxs-lookup"><span data-stu-id="3fbe6-109">*pFPS*</span></span> 
</dt> <dd>

<span data-ttu-id="3fbe6-110">Empfängt die Ausgabe Frame Rate in Frames pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="3fbe6-110">Receives the output frame rate, in frames per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fbe6-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3fbe6-111">Return value</span></span>

<span data-ttu-id="3fbe6-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="3fbe6-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3fbe6-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3fbe6-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fbe6-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3fbe6-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3fbe6-115">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="3fbe6-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3fbe6-116">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="3fbe6-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3fbe6-117">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3fbe6-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3fbe6-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3fbe6-118">Requirements</span></span>



| <span data-ttu-id="3fbe6-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3fbe6-119">Requirement</span></span> | <span data-ttu-id="3fbe6-120">Wert</span><span class="sxs-lookup"><span data-stu-id="3fbe6-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3fbe6-121">Header</span><span class="sxs-lookup"><span data-stu-id="3fbe6-121">Header</span></span><br/>  | <dl> <span data-ttu-id="3fbe6-122"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="3fbe6-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3fbe6-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3fbe6-123">Library</span></span><br/> | <dl> <span data-ttu-id="3fbe6-124"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="3fbe6-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fbe6-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3fbe6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fbe6-126">**Iamtimelinegroup-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="3fbe6-126">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="3fbe6-127">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="3fbe6-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




