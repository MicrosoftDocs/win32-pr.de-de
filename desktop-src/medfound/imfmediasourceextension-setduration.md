---
description: Legt die Dauer der Medienquelle in 100-Nanosecond-Einheiten fest.
ms.assetid: dc3dc600-ca81-40da-9edb-0af283ba9221
title: 'Imfmediasourceextension:: setduration-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.SetDuration
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: ae669bf19f531034eacafac7fb89f3c07fa1e0e9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106365232"
---
# <a name="imfmediasourceextensionsetduration-method"></a><span data-ttu-id="7d3d0-103">Imfmediasourceextension:: setduration-Methode</span><span class="sxs-lookup"><span data-stu-id="7d3d0-103">IMFMediaSourceExtension::SetDuration method</span></span>

<span data-ttu-id="7d3d0-104">Legt die Dauer der Medienquelle in 100-Nanosecond-Einheiten fest.</span><span class="sxs-lookup"><span data-stu-id="7d3d0-104">Sets the duration of the media source in 100-nanosecond units.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d3d0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d3d0-105">Syntax</span></span>


```C++
HRESULT SetDuration(
  [in] double duration
);
```



## <a name="parameters"></a><span data-ttu-id="7d3d0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d3d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d3d0-107">*Dauer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7d3d0-107">*duration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d3d0-108">Die Dauer der Medienquelle in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="7d3d0-108">The duration of the media source in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d3d0-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7d3d0-109">Return value</span></span>

<span data-ttu-id="7d3d0-110">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="7d3d0-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7d3d0-111">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7d3d0-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d3d0-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d3d0-112">Requirements</span></span>



| <span data-ttu-id="7d3d0-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d3d0-113">Requirement</span></span> | <span data-ttu-id="7d3d0-114">Wert</span><span class="sxs-lookup"><span data-stu-id="7d3d0-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d3d0-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7d3d0-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7d3d0-116">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="7d3d0-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7d3d0-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7d3d0-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7d3d0-118">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7d3d0-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="7d3d0-119">IDL</span><span class="sxs-lookup"><span data-stu-id="7d3d0-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7d3d0-120"><dt>MF mediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7d3d0-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d3d0-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d3d0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d3d0-122">**Imfmediasourceextension**</span><span class="sxs-lookup"><span data-stu-id="7d3d0-122">**IMFMediaSourceExtension**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




