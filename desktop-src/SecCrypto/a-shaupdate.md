---
description: Fügt einem angegebenen Hash Objektdaten hinzu.
ms.assetid: 8E32BBC4-C2DD-4174-9FF1-9001E4A7D87B
title: A_SHAUpdate-Funktion (SHA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAUpdate
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: a0f8ac49d8221538a168ade536e55766e209d3d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358225"
---
# <a name="a_shaupdate-function"></a><span data-ttu-id="6532b-103">Eine \_ shaupdate-Funktion</span><span class="sxs-lookup"><span data-stu-id="6532b-103">A\_SHAUpdate function</span></span>

<span data-ttu-id="6532b-104">Fügt einem angegebenen Hash Objektdaten hinzu.</span><span class="sxs-lookup"><span data-stu-id="6532b-104">Adds data to a specified hash object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6532b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6532b-105">Syntax</span></span>


```C++
void RSA32API A_SHAUpdate(
  _Inout_ A_SHA_CTX     *Context,
  _Out_   UNSIGNED CHAR *Buffer,
          UNSIGNED INT  BufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="6532b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6532b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6532b-107">*Kontext* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6532b-107">*Context* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6532b-108">Der SHA-Kontext.</span><span class="sxs-lookup"><span data-stu-id="6532b-108">The SHA context.</span></span>

</dd> <dt>

<span data-ttu-id="6532b-109">*Puffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6532b-109">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6532b-110">Die Hash Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6532b-110">The hash table.</span></span>

</dd> <dt>

<span data-ttu-id="6532b-111">*BufferSize*</span><span class="sxs-lookup"><span data-stu-id="6532b-111">*BufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="6532b-112">Die Größe des Puffers.</span><span class="sxs-lookup"><span data-stu-id="6532b-112">The size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6532b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6532b-113">Return value</span></span>

<span data-ttu-id="6532b-114">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6532b-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6532b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6532b-115">Remarks</span></span>

<span data-ttu-id="6532b-116">Diese Funktion kann mehrmals aufgerufen werden, um den Hash für lange Datenströme oder diskontinuierliche Datenströme zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="6532b-116">This function can be called multiple times to compute the hash on long data streams or discontinuous data streams.</span></span> <span data-ttu-id="6532b-117">Vor dem Abrufen des Hashwerts muss vor dem Abrufen des Hashwerts die Funktion "- [**\_ Wellen**](a-shafinal.md) " aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="6532b-117">The [**A\_SHAFinal**](a-shafinal.md) function must be called before retrieving the hash value.</span></span>

<span data-ttu-id="6532b-118">Diese Funktion ähnelt von "shaupdate", wird aber direkt aus der Bibliothek aufgerufen, anstatt durch die kryptografieinfrastruktur weitergeleitet zu werden.</span><span class="sxs-lookup"><span data-stu-id="6532b-118">This function is very similar to SHAUpdate, but is called directly from the library, rather than being routed through the cryptography infrastructure.</span></span> <span data-ttu-id="6532b-119">Weitere Informationen finden Sie unter [Windows-ntkryptografieanbieter](/previous-versions/tn-archive/cc723484(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="6532b-119">For more information, see [Windows NTCryptographic Providers](/previous-versions/tn-archive/cc723484(v=technet.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="6532b-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6532b-120">Requirements</span></span>



| <span data-ttu-id="6532b-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6532b-121">Requirement</span></span> | <span data-ttu-id="6532b-122">Wert</span><span class="sxs-lookup"><span data-stu-id="6532b-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6532b-123">Header</span><span class="sxs-lookup"><span data-stu-id="6532b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="6532b-124"><dt>SHA. h</dt></span><span class="sxs-lookup"><span data-stu-id="6532b-124"><dt>Sha.h</dt></span></span> </dl>     |
| <span data-ttu-id="6532b-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6532b-125">Library</span></span><br/> | <dl> <span data-ttu-id="6532b-126"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6532b-126"><dt>Ntdll.dll</dt></span></span> </dl> |
| <span data-ttu-id="6532b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="6532b-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="6532b-128"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6532b-128"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
