---
description: Ruft den Beziehungstyp ab, den dieser icontextlink darstellt.
ms.assetid: 03c13eba-1493-4fb7-b684-f15147e5a0eb
title: 'Icontextlink:: getcontextlinkdirection-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetContextLinkDirection
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 47ad3e6c8d28126c010e5cc1c1419b99d9cde4c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214673"
---
# <a name="icontextlinkgetcontextlinkdirection-method"></a><span data-ttu-id="cb50c-103">Icontextlink:: getcontextlinkdirection-Methode</span><span class="sxs-lookup"><span data-stu-id="cb50c-103">IContextLink::GetContextLinkDirection method</span></span>

<span data-ttu-id="cb50c-104">Ruft den Beziehungstyp ab, den dieser [**icontextlink**](icontextlink.md) darstellt.</span><span class="sxs-lookup"><span data-stu-id="cb50c-104">Retrieves the type of relationship this [**IContextLink**](icontextlink.md) represents.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb50c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb50c-105">Syntax</span></span>


```C++
HRESULT GetContextLinkDirection(
  [out] ContextLinkDirection *pContextLinkDirection
);
```



## <a name="parameters"></a><span data-ttu-id="cb50c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb50c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb50c-107">*pcontextlinkdirection* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cb50c-107">*pContextLinkDirection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb50c-108">Die Richtung, die dieser [**icontextlink**](icontextlink.md) darstellt.</span><span class="sxs-lookup"><span data-stu-id="cb50c-108">The direction this [**IContextLink**](icontextlink.md) represents.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb50c-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb50c-109">Return value</span></span>

<span data-ttu-id="cb50c-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="cb50c-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cb50c-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cb50c-111">Requirements</span></span>



| <span data-ttu-id="cb50c-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cb50c-112">Requirement</span></span> | <span data-ttu-id="cb50c-113">Wert</span><span class="sxs-lookup"><span data-stu-id="cb50c-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb50c-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cb50c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="cb50c-115">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cb50c-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cb50c-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cb50c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="cb50c-117">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cb50c-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="cb50c-118">Header</span><span class="sxs-lookup"><span data-stu-id="cb50c-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb50c-119"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="cb50c-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="cb50c-120">DLL</span><span class="sxs-lookup"><span data-stu-id="cb50c-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb50c-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb50c-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="cb50c-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb50c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb50c-123">**Icontextlink**</span><span class="sxs-lookup"><span data-stu-id="cb50c-123">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="cb50c-124">**ContextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="cb50c-124">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="cb50c-125">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="cb50c-125">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




