---
description: Die getmedialength-Methode ruft die Medien Länge dieses Quell Objekts ab.
ms.assetid: 70298d8f-67e7-4774-a7ae-f0b48e4afda7
title: 'Iamtimelinesrc:: getmedialength-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaLength
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5cd896ed0890a199f85838a01c4c6ebec6d0895d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372110"
---
# <a name="iamtimelinesrcgetmedialength-method"></a><span data-ttu-id="828f9-103">Iamtimelinesrc:: getmedialength-Methode</span><span class="sxs-lookup"><span data-stu-id="828f9-103">IAMTimelineSrc::GetMediaLength method</span></span>

> [!Note]  
> <span data-ttu-id="828f9-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="828f9-104">\[Deprecated.</span></span> <span data-ttu-id="828f9-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="828f9-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="828f9-106">Die- `GetMediaLength` Methode ruft die Medien Länge dieses Quell Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="828f9-106">The `GetMediaLength` method retrieves the media length of this source object.</span></span>

## <a name="syntax"></a><span data-ttu-id="828f9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="828f9-107">Syntax</span></span>


```C++
HRESULT GetMediaLength(
   REFERENCE_TIME *pLength
);
```



## <a name="parameters"></a><span data-ttu-id="828f9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="828f9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="828f9-109">*pLength*</span><span class="sxs-lookup"><span data-stu-id="828f9-109">*pLength*</span></span> 
</dt> <dd>

<span data-ttu-id="828f9-110">Empfängt die Medien Länge in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="828f9-110">Receives the media length in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="828f9-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="828f9-111">Return value</span></span>

<span data-ttu-id="828f9-112">Gibt einen der folgenden **HRESULT** -Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="828f9-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="828f9-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="828f9-113">Return code</span></span>                                                                                     | <span data-ttu-id="828f9-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="828f9-114">Description</span></span>                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="828f9-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="828f9-115"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="828f9-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="828f9-116">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="828f9-117"><dt>**E \_ notbestimmt**</dt></span><span class="sxs-lookup"><span data-stu-id="828f9-117"><dt>**E\_NOTDETERMINED**</dt></span></span> </dl> | <span data-ttu-id="828f9-118">Für dieses Objekt sind keine Medien Zeiten festgelegt.</span><span class="sxs-lookup"><span data-stu-id="828f9-118">Media times are not set on this object.</span></span><br/> |
| <dl> <span data-ttu-id="828f9-119"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="828f9-119"><dt>**E\_POINTER**</dt></span></span> </dl>       | <span data-ttu-id="828f9-120">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="828f9-120">**NULL** pointer argument.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="828f9-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="828f9-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="828f9-122">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="828f9-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="828f9-123">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="828f9-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="828f9-124">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="828f9-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="828f9-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="828f9-125">Requirements</span></span>



| <span data-ttu-id="828f9-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="828f9-126">Requirement</span></span> | <span data-ttu-id="828f9-127">Wert</span><span class="sxs-lookup"><span data-stu-id="828f9-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="828f9-128">Header</span><span class="sxs-lookup"><span data-stu-id="828f9-128">Header</span></span><br/>  | <dl> <span data-ttu-id="828f9-129"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="828f9-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="828f9-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="828f9-130">Library</span></span><br/> | <dl> <span data-ttu-id="828f9-131"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="828f9-131"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="828f9-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="828f9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="828f9-133">**Iamtimelinesrc-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="828f9-133">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="828f9-134">**Iamtimelinesrc:: setmedialength**</span><span class="sxs-lookup"><span data-stu-id="828f9-134">**IAMTimelineSrc::SetMediaLength**</span></span>](iamtimelinesrc-setmedialength.md)
</dt> <dt>

[<span data-ttu-id="828f9-135">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="828f9-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




