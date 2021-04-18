---
description: Initiiert das hashdown eines Datenstroms.
ms.assetid: 0EA7C98E-777C-4B2A-AF35-04F90BA3D024
title: A_SHAInit-Funktion (SHA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAInit
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 831c86b02c946896014fa9eec02270f2e963e484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364431"
---
# <a name="a_shainit-function"></a><span data-ttu-id="4805d-103">Eine \_ shainit-Funktion</span><span class="sxs-lookup"><span data-stu-id="4805d-103">A\_SHAInit function</span></span>

<span data-ttu-id="4805d-104">Initiiert das hashdown eines Datenstroms.</span><span class="sxs-lookup"><span data-stu-id="4805d-104">Initiates the hashing of a stream of data.</span></span>

## <a name="syntax"></a><span data-ttu-id="4805d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4805d-105">Syntax</span></span>


```C++
void RSA32API A_SHAInit(
  _Inout_ A_SHA_CTX *Context
);
```



## <a name="parameters"></a><span data-ttu-id="4805d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4805d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4805d-107">*Kontext* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4805d-107">*Context* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4805d-108">Der SHA-Kontext.</span><span class="sxs-lookup"><span data-stu-id="4805d-108">The SHA context.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4805d-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4805d-109">Return value</span></span>

<span data-ttu-id="4805d-110">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4805d-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4805d-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4805d-111">Remarks</span></span>

<span data-ttu-id="4805d-112">Diese Funktion ähnelt shainit stark, wird aber direkt aus der Bibliothek aufgerufen, anstatt über die kryptografieinfrastruktur weitergeleitet zu werden.</span><span class="sxs-lookup"><span data-stu-id="4805d-112">This function is very similar to SHAInit, but is called directly from the library, rather than being routed through the cryptography infrastructure.</span></span> <span data-ttu-id="4805d-113">Weitere Informationen finden Sie unter [Windows-ntkryptografieanbieter](/previous-versions/tn-archive/cc723484(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="4805d-113">For more information, see [Windows NTCryptographic Providers](/previous-versions/tn-archive/cc723484(v=technet.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="4805d-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4805d-114">Requirements</span></span>



| <span data-ttu-id="4805d-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4805d-115">Requirement</span></span> | <span data-ttu-id="4805d-116">Wert</span><span class="sxs-lookup"><span data-stu-id="4805d-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4805d-117">Header</span><span class="sxs-lookup"><span data-stu-id="4805d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="4805d-118"><dt>SHA. h</dt></span><span class="sxs-lookup"><span data-stu-id="4805d-118"><dt>Sha.h</dt></span></span> </dl>     |
| <span data-ttu-id="4805d-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4805d-119">Library</span></span><br/> | <dl> <span data-ttu-id="4805d-120"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4805d-120"><dt>Ntdll.dll</dt></span></span> </dl> |
| <span data-ttu-id="4805d-121">DLL</span><span class="sxs-lookup"><span data-stu-id="4805d-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="4805d-122"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4805d-122"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
