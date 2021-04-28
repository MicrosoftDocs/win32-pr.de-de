---
description: 'IXml2Dex::CreateGraphFromFile-Methode: Nicht implementiert.'
ms.assetid: b476e0c9-1432-4644-8002-154797a2a594
title: IXml2Dex::CreateGraphFromFile-Methode
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
ms.openlocfilehash: a79b4115dddb0e15adb4284bbefd245aba088d5f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084418"
---
# <a name="ixml2dexcreategraphfromfile-method"></a><span data-ttu-id="d03a4-103">IXml2Dex::CreateGraphFromFile-Methode</span><span class="sxs-lookup"><span data-stu-id="d03a4-103">IXml2Dex::CreateGraphFromFile method</span></span>

> [!Note]  
> <span data-ttu-id="d03a4-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="d03a4-104">\[Deprecated.</span></span> <span data-ttu-id="d03a4-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="d03a4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d03a4-106">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="d03a4-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="d03a4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d03a4-107">Syntax</span></span>


```C++
HRESULT CreateGraphFromFile(
   IUnknown **ppGraph,
   IUnknown *pTimeline,
   BSTR     FileName
);
```



## <a name="parameters"></a><span data-ttu-id="d03a4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d03a4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d03a4-109">*ppGraph*</span><span class="sxs-lookup"><span data-stu-id="d03a4-109">*ppGraph*</span></span> 
</dt> <dd>

<span data-ttu-id="d03a4-110">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="d03a4-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="d03a4-111">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="d03a4-111">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="d03a4-112">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="d03a4-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="d03a4-113">*FileName*</span><span class="sxs-lookup"><span data-stu-id="d03a4-113">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="d03a4-114">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="d03a4-114">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d03a4-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d03a4-115">Return value</span></span>

<span data-ttu-id="d03a4-116">Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d03a4-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d03a4-117">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d03a4-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d03a4-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d03a4-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d03a4-119">Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.</span><span class="sxs-lookup"><span data-stu-id="d03a4-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d03a4-120">Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="d03a4-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d03a4-121">Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d03a4-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="d03a4-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d03a4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d03a4-123">**IXml2Dex-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="d03a4-123">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> </dl>

 

 



