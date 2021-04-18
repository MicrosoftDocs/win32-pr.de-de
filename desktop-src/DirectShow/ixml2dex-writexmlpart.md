---
description: Nicht implementiert.
ms.assetid: d0fc571f-79f5-448a-8082-6e5f7f48118f
title: 'IXml2Dex:: Write texmlpart-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteXMLPart
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8f194fe409d8ea94f786fe3802b2c758a1a00520
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344177"
---
# <a name="ixml2dexwritexmlpart-method"></a><span data-ttu-id="8dc35-103">IXml2Dex:: Write texmlpart-Methode</span><span class="sxs-lookup"><span data-stu-id="8dc35-103">IXml2Dex::WriteXMLPart method</span></span>

> [!Note]  
> <span data-ttu-id="8dc35-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="8dc35-104">\[Deprecated.</span></span> <span data-ttu-id="8dc35-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="8dc35-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8dc35-106">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="8dc35-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dc35-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8dc35-107">Syntax</span></span>


```C++
HRESULT WriteXMLPart(
   IUnknown *pTimeline,
   double   dStart,
   double   dEnd,
   BSTR     FileName
);
```



## <a name="parameters"></a><span data-ttu-id="8dc35-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8dc35-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8dc35-109">*ptimeline*</span><span class="sxs-lookup"><span data-stu-id="8dc35-109">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="8dc35-110">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="8dc35-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="8dc35-111">*dstart*</span><span class="sxs-lookup"><span data-stu-id="8dc35-111">*dStart*</span></span> 
</dt> <dd>

<span data-ttu-id="8dc35-112">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="8dc35-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="8dc35-113">*unabhängiges*</span><span class="sxs-lookup"><span data-stu-id="8dc35-113">*dEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="8dc35-114">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="8dc35-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="8dc35-115">*FileName*</span><span class="sxs-lookup"><span data-stu-id="8dc35-115">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="8dc35-116">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="8dc35-116">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8dc35-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8dc35-117">Return value</span></span>

<span data-ttu-id="8dc35-118">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="8dc35-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8dc35-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8dc35-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8dc35-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8dc35-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8dc35-121">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="8dc35-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8dc35-122">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="8dc35-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8dc35-123">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8dc35-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="8dc35-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8dc35-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dc35-125">**IXml2Dex-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8dc35-125">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> </dl>

 

 



