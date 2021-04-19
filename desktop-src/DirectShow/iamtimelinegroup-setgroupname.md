---
description: Mit der setgroupname-Methode wird der von der Anwendung definierte Name der Gruppe festgelegt.
ms.assetid: e1d8a91b-d5b9-42a4-9b98-582e1a57ac51
title: 'Iamtimelinegroup:: setgroupname-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetGroupName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 327bf0384ce484353ac41c069ddf580c674b0b45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369975"
---
# <a name="iamtimelinegroupsetgroupname-method"></a><span data-ttu-id="105f2-103">Iamtimelinegroup:: setgroupname-Methode</span><span class="sxs-lookup"><span data-stu-id="105f2-103">IAMTimelineGroup::SetGroupName method</span></span>

> [!Note]  
> <span data-ttu-id="105f2-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="105f2-104">\[Deprecated.</span></span> <span data-ttu-id="105f2-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="105f2-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="105f2-106">`SetGroupName`Mit der-Methode wird der von der Anwendung definierte Name der Gruppe festgelegt.</span><span class="sxs-lookup"><span data-stu-id="105f2-106">The `SetGroupName` method sets the application-defined name of the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="105f2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="105f2-107">Syntax</span></span>


```C++
HRESULT SetGroupName(
   BSTR pGroupName
);
```



## <a name="parameters"></a><span data-ttu-id="105f2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="105f2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="105f2-109">*pgroupname*</span><span class="sxs-lookup"><span data-stu-id="105f2-109">*pGroupName*</span></span> 
</dt> <dd>

<span data-ttu-id="105f2-110">**BSTR** , das den Namen der Gruppe angibt.</span><span class="sxs-lookup"><span data-stu-id="105f2-110">**BSTR** that specifies the name of the group.</span></span> <span data-ttu-id="105f2-111">Die maximale Länge des Namens beträgt 256 Zeichen und umfasst das NULL-Terminator.</span><span class="sxs-lookup"><span data-stu-id="105f2-111">The maximum length of the name is 256 characters, incuding the null terminator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="105f2-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="105f2-112">Return value</span></span>

<span data-ttu-id="105f2-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="105f2-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="105f2-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="105f2-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="105f2-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="105f2-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="105f2-116">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="105f2-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="105f2-117">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="105f2-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="105f2-118">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="105f2-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="105f2-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="105f2-119">Requirements</span></span>



| <span data-ttu-id="105f2-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="105f2-120">Requirement</span></span> | <span data-ttu-id="105f2-121">Wert</span><span class="sxs-lookup"><span data-stu-id="105f2-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="105f2-122">Header</span><span class="sxs-lookup"><span data-stu-id="105f2-122">Header</span></span><br/>  | <dl> <span data-ttu-id="105f2-123"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="105f2-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="105f2-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="105f2-124">Library</span></span><br/> | <dl> <span data-ttu-id="105f2-125"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="105f2-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="105f2-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="105f2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="105f2-127">**Iamtimelinegroup-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="105f2-127">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="105f2-128">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="105f2-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




