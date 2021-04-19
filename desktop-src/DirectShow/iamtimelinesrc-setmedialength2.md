---
description: 'Die SetMediaLength2-Methode gibt die Dauer der Quelldatei an. Diese Methode entspricht iamtimelinesrc:: setmedialength, aber nimmt einen reftime-Wert an.'
ms.assetid: 1a1dcf23-2041-4791-bce7-0ecbe33df592
title: 'Iamtimelinesrc:: SetMediaLength2-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaLength2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4deb42cdd917fe7d79a420b15247b4bdf5ee52bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365525"
---
# <a name="iamtimelinesrcsetmedialength2-method"></a><span data-ttu-id="65355-104">Iamtimelinesrc:: SetMediaLength2-Methode</span><span class="sxs-lookup"><span data-stu-id="65355-104">IAMTimelineSrc::SetMediaLength2 method</span></span>

> [!Note]  
> <span data-ttu-id="65355-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="65355-105">\[Deprecated.</span></span> <span data-ttu-id="65355-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="65355-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="65355-107">Die- `SetMediaLength2` Methode gibt die Dauer der Quelldatei an.</span><span class="sxs-lookup"><span data-stu-id="65355-107">The `SetMediaLength2` method specifies the duration of the source file.</span></span> <span data-ttu-id="65355-108">Diese Methode entspricht [**iamtimelinesrc:: setmedialength**](iamtimelinesrc-setmedialength.md), aber nimmt einen [**reftime**](reftime.md) -Wert an.</span><span class="sxs-lookup"><span data-stu-id="65355-108">This method is equivalent to [**IAMTimelineSrc::SetMediaLength**](iamtimelinesrc-setmedialength.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="65355-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="65355-109">Syntax</span></span>


```C++
HRESULT SetMediaLength2(
   REFTIME Length
);
```



## <a name="parameters"></a><span data-ttu-id="65355-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="65355-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65355-111">*Länge*</span><span class="sxs-lookup"><span data-stu-id="65355-111">*Length*</span></span> 
</dt> <dd>

<span data-ttu-id="65355-112">Medien Länge in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="65355-112">Media length, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65355-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="65355-113">Return value</span></span>

<span data-ttu-id="65355-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="65355-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="65355-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="65355-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="65355-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="65355-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="65355-117">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="65355-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="65355-118">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="65355-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="65355-119">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="65355-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="65355-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="65355-120">Requirements</span></span>



| <span data-ttu-id="65355-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="65355-121">Requirement</span></span> | <span data-ttu-id="65355-122">Wert</span><span class="sxs-lookup"><span data-stu-id="65355-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65355-123">Header</span><span class="sxs-lookup"><span data-stu-id="65355-123">Header</span></span><br/>  | <dl> <span data-ttu-id="65355-124"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="65355-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="65355-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="65355-125">Library</span></span><br/> | <dl> <span data-ttu-id="65355-126"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="65355-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65355-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65355-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65355-128">**Iamtimelinesrc-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="65355-128">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="65355-129">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="65355-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




