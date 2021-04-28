---
description: 'IXml2Dex::WriteXMLPart-Methode: Nicht implementiert.'
ms.assetid: d0fc571f-79f5-448a-8082-6e5f7f48118f
title: IXml2Dex::WriteXMLPart-Methode
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
ms.openlocfilehash: 957fa74f09a79f94e2e0feb35c418a711c91c1b0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084358"
---
# <a name="ixml2dexwritexmlpart-method"></a><span data-ttu-id="d5dc4-103">IXml2Dex::WriteXMLPart-Methode</span><span class="sxs-lookup"><span data-stu-id="d5dc4-103">IXml2Dex::WriteXMLPart method</span></span>

> [!Note]  
> <span data-ttu-id="d5dc4-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="d5dc4-104">\[Deprecated.</span></span> <span data-ttu-id="d5dc4-105">Diese API wird möglicherweise aus zukünftigen Versionen von Windows entfernt.\]</span><span class="sxs-lookup"><span data-stu-id="d5dc4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d5dc4-106">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="d5dc4-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5dc4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5dc4-107">Syntax</span></span>


```C++
HRESULT WriteXMLPart(
   IUnknown *pTimeline,
   double   dStart,
   double   dEnd,
   BSTR     FileName
);
```



## <a name="parameters"></a><span data-ttu-id="d5dc4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5dc4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5dc4-109">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="d5dc4-109">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="d5dc4-110">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="d5dc4-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="d5dc4-111">*dStart*</span><span class="sxs-lookup"><span data-stu-id="d5dc4-111">*dStart*</span></span> 
</dt> <dd>

<span data-ttu-id="d5dc4-112">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="d5dc4-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="d5dc4-113">*dEnd*</span><span class="sxs-lookup"><span data-stu-id="d5dc4-113">*dEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="d5dc4-114">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="d5dc4-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="d5dc4-115">*FileName*</span><span class="sxs-lookup"><span data-stu-id="d5dc4-115">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="d5dc4-116">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="d5dc4-116">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5dc4-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d5dc4-117">Return value</span></span>

<span data-ttu-id="d5dc4-118">Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.**</span><span class="sxs-lookup"><span data-stu-id="d5dc4-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d5dc4-119">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d5dc4-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5dc4-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5dc4-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d5dc4-121">Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="d5dc4-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d5dc4-122">Um Qedit.h zu erhalten, laden Sie das Microsoft Windows SDK Update für Windows Vista und .NET Framework [3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5dc4-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d5dc4-123">Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d5dc4-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="d5dc4-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d5dc4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5dc4-125">**IXml2Dex-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="d5dc4-125">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> </dl>

 

 



