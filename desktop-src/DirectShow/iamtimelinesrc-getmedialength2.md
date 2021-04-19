---
description: 'Die GetMediaLength2-Methode ruft die Medien Länge dieses Quell Objekts ab. Diese Methode entspricht iamtimelinesrc:: getmedialength, erfordert jedoch reftime-Werte.'
ms.assetid: 96685e00-4e16-4205-a6ad-8b83cf2f8c29
title: 'Iamtimelinesrc:: GetMediaLength2-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaLength2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: caee510db9ddeda1923327176a634a9011601e4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357319"
---
# <a name="iamtimelinesrcgetmedialength2-method"></a><span data-ttu-id="9e638-104">Iamtimelinesrc:: GetMediaLength2-Methode</span><span class="sxs-lookup"><span data-stu-id="9e638-104">IAMTimelineSrc::GetMediaLength2 method</span></span>

> [!Note]  
> <span data-ttu-id="9e638-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="9e638-105">\[Deprecated.</span></span> <span data-ttu-id="9e638-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="9e638-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9e638-107">Die- `GetMediaLength2` Methode ruft die Medien Länge dieses Quell Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="9e638-107">The `GetMediaLength2` method retrieves the media length of this source object.</span></span> <span data-ttu-id="9e638-108">Diese Methode entspricht [**iamtimelinesrc:: getmedialength**](iamtimelinesrc-getmedialength.md), erfordert jedoch [**reftime**](reftime.md) -Werte.</span><span class="sxs-lookup"><span data-stu-id="9e638-108">This method is equivalent to [**IAMTimelineSrc::GetMediaLength**](iamtimelinesrc-getmedialength.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e638-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e638-109">Syntax</span></span>


```C++
HRESULT GetMediaLength2(
   REFTIME *pLength
);
```



## <a name="parameters"></a><span data-ttu-id="9e638-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e638-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e638-111">*pLength*</span><span class="sxs-lookup"><span data-stu-id="9e638-111">*pLength*</span></span> 
</dt> <dd>

<span data-ttu-id="9e638-112">Empfängt die Medien Länge in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="9e638-112">Receives the media length in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e638-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9e638-113">Return value</span></span>

<span data-ttu-id="9e638-114">Gibt einen der folgenden **HRESULT** -Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="9e638-114">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="9e638-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9e638-115">Return code</span></span>                                                                                     | <span data-ttu-id="9e638-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e638-116">Description</span></span>                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="9e638-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9e638-117"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="9e638-118">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="9e638-118">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="9e638-119"><dt>**E \_ notbestimmt**</dt></span><span class="sxs-lookup"><span data-stu-id="9e638-119"><dt>**E\_NOTDETERMINED**</dt></span></span> </dl> | <span data-ttu-id="9e638-120">Für dieses Objekt sind keine Medien Zeiten festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9e638-120">Media times are not set on this object.</span></span><br/> |
| <dl> <span data-ttu-id="9e638-121"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="9e638-121"><dt>**E\_POINTER**</dt></span></span> </dl>       | <span data-ttu-id="9e638-122">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="9e638-122">**NULL** pointer argument.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="9e638-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e638-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9e638-124">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="9e638-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9e638-125">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="9e638-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9e638-126">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9e638-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9e638-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9e638-127">Requirements</span></span>



| <span data-ttu-id="9e638-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9e638-128">Requirement</span></span> | <span data-ttu-id="9e638-129">Wert</span><span class="sxs-lookup"><span data-stu-id="9e638-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e638-130">Header</span><span class="sxs-lookup"><span data-stu-id="9e638-130">Header</span></span><br/>  | <dl> <span data-ttu-id="9e638-131"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="9e638-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9e638-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9e638-132">Library</span></span><br/> | <dl> <span data-ttu-id="9e638-133"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="9e638-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e638-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e638-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e638-135">**Iamtimelinesrc-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="9e638-135">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="9e638-136">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="9e638-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




