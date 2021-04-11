---
description: Diese Methode gibt eine-Schnittstelle zurück, die Zugriff auf die Videodaten bereitstellt.
ms.assetid: 084F020F-A6F5-4982-BA4B-A8F8D6182868
title: 'Ivideoframenative:: GetData-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVideoFrameNative.GetData
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: c612d2d34e23b393921f83f7dbe9e189aa366b30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958933"
---
# <a name="ivideoframenativegetdata-method"></a><span data-ttu-id="bb00f-103">Ivideoframenative:: GetData-Methode</span><span class="sxs-lookup"><span data-stu-id="bb00f-103">IVideoFrameNative::GetData method</span></span>

<span data-ttu-id="bb00f-104">Diese Methode gibt eine-Schnittstelle zurück, die Zugriff auf die Videodaten bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="bb00f-104">This method returns an interface that provides access to the video data.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb00f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb00f-105">Syntax</span></span>


```C++
HRESULT GetData(
  [in]  REFIID riid,
  [out] LPVOID *ppv
);
```



## <a name="parameters"></a><span data-ttu-id="bb00f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb00f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb00f-107">*riid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb00f-107">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb00f-108">Die IID der abzurufenden Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="bb00f-108">The IID of the interface to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="bb00f-109">*PPV* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bb00f-109">*ppv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb00f-110">Wenn diese Methode erfolgreich zurückgegeben wird, enthält Sie den im *riid* -Parameter angeforderten Schnittstellen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="bb00f-110">When this method returns successfully, contains the interface pointer requested in *riid* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb00f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bb00f-111">Return value</span></span>

<span data-ttu-id="bb00f-112">Gibt \_ beim erfolgreichen Abschluss S OK zurück.</span><span class="sxs-lookup"><span data-stu-id="bb00f-112">Returns S\_OK on successful completion.</span></span> <span data-ttu-id="bb00f-113">Gibt E \_ nointerface zurück, wenn die angeforderte Schnittstelle nicht gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="bb00f-113">Returns E\_NOINTERFACE if the requested interface can't be found.</span></span>

## <a name="see-also"></a><span data-ttu-id="bb00f-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb00f-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb00f-115">**Ivideoframenative**</span><span class="sxs-lookup"><span data-stu-id="bb00f-115">**IVideoFrameNative**</span></span>](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative)
</dt> </dl>

 

 



