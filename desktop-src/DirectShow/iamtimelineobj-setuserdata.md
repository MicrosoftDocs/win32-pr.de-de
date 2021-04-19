---
description: Mit der setUserData-Methode werden von der Anwendung definierte persistente Daten festgelegt.
ms.assetid: 195d8e92-a25c-40ff-8cc7-c1f05bdd76ab
title: 'Iamtimelineobj:: setUserData-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetUserData
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7e09aafd614234827a704d8b9997f27981eb7c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367720"
---
# <a name="iamtimelineobjsetuserdata-method"></a><span data-ttu-id="c438f-103">Iamtimelineobj:: setUserData-Methode</span><span class="sxs-lookup"><span data-stu-id="c438f-103">IAMTimelineObj::SetUserData method</span></span>

> [!Note]  
> <span data-ttu-id="c438f-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="c438f-104">\[Deprecated.</span></span> <span data-ttu-id="c438f-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="c438f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c438f-106">Die `SetUserData` -Methode legt von der Anwendung definierte persistente Daten fest.</span><span class="sxs-lookup"><span data-stu-id="c438f-106">The `SetUserData` method sets application-defined persistent data.</span></span>

## <a name="syntax"></a><span data-ttu-id="c438f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c438f-107">Syntax</span></span>


```C++
HRESULT SetUserData(
   BYTE *pData,
   long Size
);
```



## <a name="parameters"></a><span data-ttu-id="c438f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c438f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c438f-109">*pData*</span><span class="sxs-lookup"><span data-stu-id="c438f-109">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="c438f-110">Zeiger auf einen Puffer, der die Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="c438f-110">Pointer to a buffer containing the data.</span></span>

</dd> <dt>

<span data-ttu-id="c438f-111">*Größe*</span><span class="sxs-lookup"><span data-stu-id="c438f-111">*Size*</span></span> 
</dt> <dd>

<span data-ttu-id="c438f-112">Größe der Daten in Bytes.</span><span class="sxs-lookup"><span data-stu-id="c438f-112">Size of the data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c438f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c438f-113">Return value</span></span>

<span data-ttu-id="c438f-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="c438f-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c438f-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c438f-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c438f-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c438f-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c438f-117">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="c438f-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c438f-118">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="c438f-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c438f-119">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c438f-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c438f-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c438f-120">Requirements</span></span>



| <span data-ttu-id="c438f-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c438f-121">Requirement</span></span> | <span data-ttu-id="c438f-122">Wert</span><span class="sxs-lookup"><span data-stu-id="c438f-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c438f-123">Header</span><span class="sxs-lookup"><span data-stu-id="c438f-123">Header</span></span><br/>  | <dl> <span data-ttu-id="c438f-124"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="c438f-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c438f-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c438f-125">Library</span></span><br/> | <dl> <span data-ttu-id="c438f-126"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="c438f-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c438f-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c438f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c438f-128">**Iamtimelineobj-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c438f-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="c438f-129">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="c438f-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




