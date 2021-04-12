---
description: Diese Methode gibt ein Gerät zurück, das den Videodaten zugeordnet ist.
ms.assetid: 9A61159B-C383-4770-AD8F-9F69F720E3E2
title: 'Ivideoframenative:: getdevice-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVideoFrameNative.GetDevice
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: d012ae79b1cb2c83e916dc74113cc3d0560da4c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393517"
---
# <a name="ivideoframenativegetdevice-method"></a><span data-ttu-id="bb49d-103">Ivideoframenative:: getdevice-Methode</span><span class="sxs-lookup"><span data-stu-id="bb49d-103">IVideoFrameNative::GetDevice method</span></span>

<span data-ttu-id="bb49d-104">Diese Methode gibt ein Gerät zurück, das den Videodaten zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="bb49d-104">This method returns a device associated with the video data.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb49d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb49d-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [in]  REFIID riid,
  [out] LPVOID *ppv
);
```



## <a name="parameters"></a><span data-ttu-id="bb49d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb49d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb49d-107">*riid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb49d-107">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb49d-108">Die IID des abzurufenden Geräts.</span><span class="sxs-lookup"><span data-stu-id="bb49d-108">The IID of the device to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="bb49d-109">*PPV* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bb49d-109">*ppv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb49d-110">Wenn diese Methode erfolgreich zurückgegeben wird, enthält Sie den im *riid* -Parameter angeforderten Geräte Zeiger.</span><span class="sxs-lookup"><span data-stu-id="bb49d-110">When this method returns successfully, contains the device pointer requested in *riid* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb49d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bb49d-111">Return value</span></span>

<span data-ttu-id="bb49d-112">Gibt \_ beim erfolgreichen Abschluss S OK zurück.</span><span class="sxs-lookup"><span data-stu-id="bb49d-112">Returns S\_OK on successful completion.</span></span>

## <a name="see-also"></a><span data-ttu-id="bb49d-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb49d-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb49d-114">**Ivideoframenative**</span><span class="sxs-lookup"><span data-stu-id="bb49d-114">**IVideoFrameNative**</span></span>](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative)
</dt> </dl>

 

 



