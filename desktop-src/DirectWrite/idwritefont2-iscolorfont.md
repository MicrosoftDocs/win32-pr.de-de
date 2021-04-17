---
title: IDWriteFont2 iscolorfont-Methode
description: Ermöglicht die Ermittlung, ob ein farbrenderingpfad möglicherweise erforderlich ist.
ms.assetid: E21BB773-923E-461B-B966-A186ACD0164A
keywords:
- Iscolorfont-Methode, direktes Schreiben
- Iscolorfont-Methode Direct Write, IDWriteFont2-Schnittstelle
- IDWriteFont2 Interface Direct Write, iscolorfont-Methode
topic_type:
- apiref
api_name:
- IDWriteFont2.IsColorFont
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 353499c5e1c00ae37e585ecc6be47e5a2033d795
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392044"
---
# <a name="idwritefont2iscolorfont-method"></a><span data-ttu-id="bc12e-106">IDWriteFont2:: iscolorfont-Methode</span><span class="sxs-lookup"><span data-stu-id="bc12e-106">IDWriteFont2::IsColorFont method</span></span>

<span data-ttu-id="bc12e-107">Ermöglicht die Ermittlung, ob ein farbrenderingpfad möglicherweise erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="bc12e-107">Enables determining if a color rendering path is potentially necessary.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc12e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc12e-108">Syntax</span></span>


```C++
BOOL IsColorFont();
```



## <a name="parameters"></a><span data-ttu-id="bc12e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc12e-109">Parameters</span></span>

<span data-ttu-id="bc12e-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="bc12e-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bc12e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc12e-111">Return value</span></span>

<span data-ttu-id="bc12e-112">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="bc12e-112">Type: **BOOL**</span></span>

<span data-ttu-id="bc12e-113">Gibt " **true** " zurück, wenn die Schriftart Farbinformationen (colr-und CPAL-Tabellen) aufweist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="bc12e-113">Returns **TRUE** if the font has color information (COLR and CPAL tables); otherwise **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc12e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc12e-114">Requirements</span></span>



| <span data-ttu-id="bc12e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc12e-115">Requirement</span></span> | <span data-ttu-id="bc12e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="bc12e-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc12e-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bc12e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bc12e-118">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="bc12e-118">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="bc12e-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bc12e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bc12e-120">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="bc12e-120">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="bc12e-121">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="bc12e-121">Minimum supported phone</span></span><br/>  | <span data-ttu-id="bc12e-122">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]</span><span class="sxs-lookup"><span data-stu-id="bc12e-122">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="bc12e-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bc12e-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="bc12e-124"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc12e-124"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="bc12e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="bc12e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc12e-126"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc12e-126"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bc12e-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc12e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc12e-128">**IDWriteFont2**</span><span class="sxs-lookup"><span data-stu-id="bc12e-128">**IDWriteFont2**</span></span>](idwritefont2.md)
</dt> </dl>

 

 





