---
description: Diese Methode gibt eine Schnittstelle zurück, die Zugriff auf die Audiodaten bereitstellt.
ms.assetid: 4FA7CC9D-D379-4C08-8D4F-5301ECCDF372
title: 'Iaudioframenative:: GetData-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAudioFrameNative.GetData
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: eb61bce5132c2029b6f53fdd1159ca50984ba936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129237"
---
# <a name="iaudioframenativegetdata-method"></a><span data-ttu-id="2edd9-103">Iaudioframenative:: GetData-Methode</span><span class="sxs-lookup"><span data-stu-id="2edd9-103">IAudioFrameNative::GetData method</span></span>

<span data-ttu-id="2edd9-104">Diese Methode gibt eine Schnittstelle zurück, die Zugriff auf die Audiodaten bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="2edd9-104">This method returns an interface that provides access to the audio data.</span></span>

## <a name="syntax"></a><span data-ttu-id="2edd9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2edd9-105">Syntax</span></span>


```C++
HRESULT GetData(
  [in]  REFIID riid,
  [out] LPVOID *ppv
);
```



## <a name="parameters"></a><span data-ttu-id="2edd9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2edd9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2edd9-107">*riid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2edd9-107">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2edd9-108">Typ: **refID**</span><span class="sxs-lookup"><span data-stu-id="2edd9-108">Type: **REFIID**</span></span>

<span data-ttu-id="2edd9-109">Die IID der abzurufenden Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="2edd9-109">The IID of the interface to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="2edd9-110">*PPV* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2edd9-110">*ppv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2edd9-111">Typ: \**LPVOID \** _</span><span class="sxs-lookup"><span data-stu-id="2edd9-111">Type: \**LPVOID\** _</span></span>

<span data-ttu-id="2edd9-112">Wenn diese Methode erfolgreich zurückgegeben wird, enthält Sie den im _riid \*-Parameter angeforderten Schnittstellen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="2edd9-112">When this method returns successfully, contains the interface pointer requested in _riid\* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2edd9-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2edd9-113">Return value</span></span>

<span data-ttu-id="2edd9-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2edd9-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2edd9-115">Gibt \_ beim erfolgreichen Abschluss S OK zurück.</span><span class="sxs-lookup"><span data-stu-id="2edd9-115">Returns S\_OK on successful completion.</span></span> <span data-ttu-id="2edd9-116">Gibt E \_ nointerface zurück, wenn die angeforderte Schnittstelle nicht gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="2edd9-116">Returns E\_NOINTERFACE if the requested interface can't be found.</span></span>

## <a name="see-also"></a><span data-ttu-id="2edd9-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2edd9-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2edd9-118">**Iaudioframenative**</span><span class="sxs-lookup"><span data-stu-id="2edd9-118">**IAudioFrameNative**</span></span>](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenative)
</dt> </dl>

 

 



