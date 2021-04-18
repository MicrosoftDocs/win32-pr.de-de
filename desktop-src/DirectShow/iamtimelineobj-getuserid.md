---
description: Die GetUserID-Methode ruft den von der Anwendung definierten Bezeichner des Objekts ab.
ms.assetid: 68a20dfa-990e-47de-ae02-1d3182b7f13f
title: 'Iamtimelineobj:: GetUserID-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetUserID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f5d6c07fd826f2045ddc9f54445bc96feb5a7c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371964"
---
# <a name="iamtimelineobjgetuserid-method"></a><span data-ttu-id="b88d0-103">Iamtimelineobj:: GetUserID-Methode</span><span class="sxs-lookup"><span data-stu-id="b88d0-103">IAMTimelineObj::GetUserID method</span></span>

> [!Note]  
> <span data-ttu-id="b88d0-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="b88d0-104">\[Deprecated.</span></span> <span data-ttu-id="b88d0-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="b88d0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b88d0-106">Die `GetUserID` -Methode ruft den von der Anwendung definierten Bezeichner des Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="b88d0-106">The `GetUserID` method retrieves the object's application-defined identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="b88d0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b88d0-107">Syntax</span></span>


```C++
HRESULT GetUserID(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="b88d0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b88d0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b88d0-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="b88d0-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="b88d0-110">Empfängt den von der Anwendung definierten Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="b88d0-110">Receives the application-defined identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b88d0-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b88d0-111">Return value</span></span>

<span data-ttu-id="b88d0-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="b88d0-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b88d0-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b88d0-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b88d0-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b88d0-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b88d0-115">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="b88d0-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b88d0-116">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="b88d0-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b88d0-117">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b88d0-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b88d0-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b88d0-118">Requirements</span></span>



| <span data-ttu-id="b88d0-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b88d0-119">Requirement</span></span> | <span data-ttu-id="b88d0-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b88d0-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b88d0-121">Header</span><span class="sxs-lookup"><span data-stu-id="b88d0-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b88d0-122"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="b88d0-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b88d0-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b88d0-123">Library</span></span><br/> | <dl> <span data-ttu-id="b88d0-124"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="b88d0-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b88d0-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b88d0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b88d0-126">**Iamtimelineobj-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b88d0-126">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="b88d0-127">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="b88d0-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




