---
description: Berechnet den abschließenden Hash der Daten, die von der MD5Update-Funktion eingegeben werden.
ms.assetid: A0457D26-F4E3-4ED4-B374-0AFCB6F661FB
title: A_SHAFinal-Funktion (SHA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAFinal
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 2a206005a686d02891a593243bc0ef3a4ad7db23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369937"
---
# <a name="a_shafinal-function"></a><span data-ttu-id="5c692-103">Eine " \_ shafinal"-Funktion</span><span class="sxs-lookup"><span data-stu-id="5c692-103">A\_SHAFinal function</span></span>

<span data-ttu-id="5c692-104">Berechnet den abschließenden Hash der Daten, die von der MD5Update-Funktion eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5c692-104">Computes the final hash of the data entered by the MD5Update function.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c692-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c692-105">Syntax</span></span>


```C++
VOID RSA32API A_SHAFinal(
  _Inout_ A_SHA_CTX     *Context,
  _Out_   UNSIGNED CHAR Result
);
```



## <a name="parameters"></a><span data-ttu-id="5c692-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c692-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c692-107">*Kontext* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5c692-107">*Context* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c692-108">Der SHA-Kontext.</span><span class="sxs-lookup"><span data-stu-id="5c692-108">The SHA context.</span></span>

</dd> <dt>

<span data-ttu-id="5c692-109">*Ergebnis* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5c692-109">*Result* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c692-110">Die resultierende Hash Tabelle.</span><span class="sxs-lookup"><span data-stu-id="5c692-110">The resulting hash table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c692-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5c692-111">Return value</span></span>

<span data-ttu-id="5c692-112">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5c692-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c692-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c692-113">Remarks</span></span>

<span data-ttu-id="5c692-114">Diese Funktion ähnelt der Verwendung von "shafinal", wird aber direkt aus der Bibliothek aufgerufen, anstatt durch die kryptografieinfrastruktur weitergeleitet zu werden.</span><span class="sxs-lookup"><span data-stu-id="5c692-114">This function is very similar to SHAFinal, but is called directly from the library, rather than being routed through the cryptography infrastructure.</span></span> <span data-ttu-id="5c692-115">Weitere Informationen finden Sie unter [Windows-ntkryptografieanbieter](/previous-versions/tn-archive/cc723484(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="5c692-115">For more information, see [Windows NTCryptographic Providers](/previous-versions/tn-archive/cc723484(v=technet.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c692-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c692-116">Requirements</span></span>



| <span data-ttu-id="5c692-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5c692-117">Requirement</span></span> | <span data-ttu-id="5c692-118">Wert</span><span class="sxs-lookup"><span data-stu-id="5c692-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5c692-119">Header</span><span class="sxs-lookup"><span data-stu-id="5c692-119">Header</span></span><br/>  | <dl> <span data-ttu-id="5c692-120"><dt>SHA. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c692-120"><dt>Sha.h</dt></span></span> </dl>     |
| <span data-ttu-id="5c692-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5c692-121">Library</span></span><br/> | <dl> <span data-ttu-id="5c692-122"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c692-122"><dt>Ntdll.dll</dt></span></span> </dl> |
| <span data-ttu-id="5c692-123">DLL</span><span class="sxs-lookup"><span data-stu-id="5c692-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="5c692-124"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c692-124"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
