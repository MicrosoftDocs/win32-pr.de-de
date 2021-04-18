---
description: Die getconnectedmediatype-Methode ruft den Medientyp für die Verbindung mit der Eingabe-PIN der Sample Grabber ab.
ms.assetid: 65f5603a-1151-4ffd-a662-84e265663b04
title: 'Isamplegrabber:: getconnectedmediatype-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.GetConnectedMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 85e30820afdca865f438ac40521a9be540fd4a1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364595"
---
# <a name="isamplegrabbergetconnectedmediatype-method"></a><span data-ttu-id="b0056-103">Isamplegrabber:: getconnectedmediatype-Methode</span><span class="sxs-lookup"><span data-stu-id="b0056-103">ISampleGrabber::GetConnectedMediaType method</span></span>

> [!Note]  
> <span data-ttu-id="b0056-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="b0056-104">\[Deprecated.</span></span> <span data-ttu-id="b0056-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="b0056-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b0056-106">Die- `GetConnectedMediaType` Methode ruft den Medientyp für die Verbindung mit der Eingabe-PIN der Sample Grabber ab.</span><span class="sxs-lookup"><span data-stu-id="b0056-106">The `GetConnectedMediaType` method retrieves the media type for the connection on the input pin of the Sample Grabber.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0056-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0056-107">Syntax</span></span>


```C++
HRESULT GetConnectedMediaType(
   AM_MEDIA_TYPE *pType
);
```



## <a name="parameters"></a><span data-ttu-id="b0056-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0056-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0056-109">*pType*</span><span class="sxs-lookup"><span data-stu-id="b0056-109">*pType*</span></span> 
</dt> <dd>

<span data-ttu-id="b0056-110">Zeiger auf eine vom Aufrufer zugeordnete Objekt- [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur.</span><span class="sxs-lookup"><span data-stu-id="b0056-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure allocated by the caller.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0056-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b0056-111">Return value</span></span>

<span data-ttu-id="b0056-112">Gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="b0056-112">Returns one of the following values.</span></span>



| <span data-ttu-id="b0056-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b0056-113">Return code</span></span>                                                                                           | <span data-ttu-id="b0056-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b0056-114">Description</span></span>                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="b0056-115"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="b0056-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="b0056-116">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="b0056-116">**NULL** pointer argument.</span></span><br/>   |
| <dl> <span data-ttu-id="b0056-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b0056-117"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="b0056-118">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="b0056-118">Success.</span></span><br/>                     |
| <dl> <span data-ttu-id="b0056-119"><dt>**VFW \_ E \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="b0056-119"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="b0056-120">Der Filter ist nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="b0056-120">The filter is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b0056-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0056-121">Remarks</span></span>

<span data-ttu-id="b0056-122">Mit dieser Methode wird der Medientyp in die von " *pType*" angegebene **\_ Medientyp \_** -Struktur kopiert.</span><span class="sxs-lookup"><span data-stu-id="b0056-122">This method copies the media type into the **AM\_MEDIA\_TYPE** structure specified by *pType*.</span></span> <span data-ttu-id="b0056-123">Der Aufrufer muss den Format Block des Medientyps freigeben.</span><span class="sxs-lookup"><span data-stu-id="b0056-123">The caller must free the format block of the media type.</span></span> <span data-ttu-id="b0056-124">Sie können die Funktion " **CoTaskMemFree** " oder die Funktion " [**freemediatype**](freemediatype.md) " in der Basisklassen Bibliothek verwenden.</span><span class="sxs-lookup"><span data-stu-id="b0056-124">You can use the **CoTaskMemFree** function, or the [**FreeMediaType**](freemediatype.md) function in the base-class library.</span></span>

> [!Note]  
> <span data-ttu-id="b0056-125">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="b0056-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b0056-126">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="b0056-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b0056-127">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b0056-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b0056-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0056-128">Requirements</span></span>



| <span data-ttu-id="b0056-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b0056-129">Requirement</span></span> | <span data-ttu-id="b0056-130">Wert</span><span class="sxs-lookup"><span data-stu-id="b0056-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0056-131">Header</span><span class="sxs-lookup"><span data-stu-id="b0056-131">Header</span></span><br/>  | <dl> <span data-ttu-id="b0056-132"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="b0056-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b0056-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b0056-133">Library</span></span><br/> | <dl> <span data-ttu-id="b0056-134"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="b0056-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0056-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0056-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0056-136">Verwenden der Beispiel-Grabber</span><span class="sxs-lookup"><span data-stu-id="b0056-136">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="b0056-137">**Isamplegrabber-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b0056-137">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




