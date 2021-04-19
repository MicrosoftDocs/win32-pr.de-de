---
description: Nicht implementiert.
ms.assetid: b476e0c9-1432-4644-8002-154797a2a594
title: 'IXml2Dex:: kreategraphfromfile-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.CreateGraphFromFile
api_type:
- COM
api_location: ''
ms.openlocfilehash: 10a2e52716de77f9c62a51c87cbda550b92a8f90
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346394"
---
# <a name="ixml2dexcreategraphfromfile-method"></a><span data-ttu-id="ffe32-103">IXml2Dex:: kreategraphfromfile-Methode</span><span class="sxs-lookup"><span data-stu-id="ffe32-103">IXml2Dex::CreateGraphFromFile method</span></span>

> [!Note]  
> <span data-ttu-id="ffe32-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="ffe32-104">\[Deprecated.</span></span> <span data-ttu-id="ffe32-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="ffe32-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ffe32-106">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="ffe32-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffe32-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffe32-107">Syntax</span></span>


```C++
HRESULT CreateGraphFromFile(
   IUnknown **ppGraph,
   IUnknown *pTimeline,
   BSTR     FileName
);
```



## <a name="parameters"></a><span data-ttu-id="ffe32-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ffe32-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffe32-109">*ppgraph*</span><span class="sxs-lookup"><span data-stu-id="ffe32-109">*ppGraph*</span></span> 
</dt> <dd>

<span data-ttu-id="ffe32-110">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="ffe32-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="ffe32-111">*ptimeline*</span><span class="sxs-lookup"><span data-stu-id="ffe32-111">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="ffe32-112">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="ffe32-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="ffe32-113">*FileName*</span><span class="sxs-lookup"><span data-stu-id="ffe32-113">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="ffe32-114">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="ffe32-114">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffe32-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ffe32-115">Return value</span></span>

<span data-ttu-id="ffe32-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="ffe32-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ffe32-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ffe32-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffe32-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ffe32-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ffe32-119">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="ffe32-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ffe32-120">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="ffe32-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ffe32-121">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ffe32-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="ffe32-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ffe32-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffe32-123">**IXml2Dex-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ffe32-123">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> </dl>

 

 



