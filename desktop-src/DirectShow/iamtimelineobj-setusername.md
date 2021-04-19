---
description: Die setUserName-Methode legt einen von der Anwendung definierten Namen für das Objekt fest.
ms.assetid: 6f071884-519a-465f-8273-ab1be58dda8b
title: 'Iamtimelineobj:: setUserName-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetUserName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8ec39aece23d38be6fbe2e69f7ded8bc738e04c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372640"
---
# <a name="iamtimelineobjsetusername-method"></a><span data-ttu-id="b8a8f-103">Iamtimelineobj:: setUserName-Methode</span><span class="sxs-lookup"><span data-stu-id="b8a8f-103">IAMTimelineObj::SetUserName method</span></span>

> [!Note]  
> <span data-ttu-id="b8a8f-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="b8a8f-104">\[Deprecated.</span></span> <span data-ttu-id="b8a8f-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="b8a8f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b8a8f-106">Die `SetUserName` -Methode legt einen Anwendungs definierten Namen für das-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="b8a8f-106">The `SetUserName` method sets an application-defined name for the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8a8f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8a8f-107">Syntax</span></span>


```C++
HRESULT SetUserName(
   BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="b8a8f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8a8f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8a8f-109">*NewVal*</span><span class="sxs-lookup"><span data-stu-id="b8a8f-109">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="b8a8f-110">Zeichenfolge mit breit Zeichen, die den Namen enthält.</span><span class="sxs-lookup"><span data-stu-id="b8a8f-110">Wide-character string that contains the name.</span></span> <span data-ttu-id="b8a8f-111">Zeichen folgen, die länger als 256 Zeichen sind, werden möglicherweise abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="b8a8f-111">Strings longer than 256 characters might be truncated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8a8f-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b8a8f-112">Return value</span></span>

<span data-ttu-id="b8a8f-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="b8a8f-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b8a8f-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b8a8f-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8a8f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8a8f-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b8a8f-116">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="b8a8f-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b8a8f-117">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="b8a8f-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b8a8f-118">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b8a8f-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b8a8f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8a8f-119">Requirements</span></span>



| <span data-ttu-id="b8a8f-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8a8f-120">Requirement</span></span> | <span data-ttu-id="b8a8f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="b8a8f-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8a8f-122">Header</span><span class="sxs-lookup"><span data-stu-id="b8a8f-122">Header</span></span><br/>  | <dl> <span data-ttu-id="b8a8f-123"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="b8a8f-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b8a8f-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b8a8f-124">Library</span></span><br/> | <dl> <span data-ttu-id="b8a8f-125"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="b8a8f-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8a8f-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8a8f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8a8f-127">**Iamtimelineobj-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b8a8f-127">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="b8a8f-128">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="b8a8f-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




