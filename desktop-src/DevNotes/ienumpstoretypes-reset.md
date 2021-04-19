---
description: Setzt auf den Anfang der enumerationssequenz zurück.
ms.assetid: 35f14aa5-92cb-4ad8-b80c-2550dedb7a7f
title: 'Iumumpstoretypes:: Reset-Methode (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes.Reset
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 60aeb1f68bcbf18e903472fa736b5714076dfbfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360290"
---
# <a name="ienumpstoretypesreset-method"></a><span data-ttu-id="304b3-103">Iumumpstoretypes:: Reset-Methode</span><span class="sxs-lookup"><span data-stu-id="304b3-103">IEnumPStoreTypes::Reset method</span></span>

<span data-ttu-id="304b3-104">\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="304b3-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="304b3-105">Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="304b3-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="304b3-106">Pstore verwendet eine ältere Implementierung des Schutzes von Daten.</span><span class="sxs-lookup"><span data-stu-id="304b3-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="304b3-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="304b3-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="304b3-108">Setzt auf den Anfang der enumerationssequenz zurück.</span><span class="sxs-lookup"><span data-stu-id="304b3-108">Resets to the beginning of the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="304b3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="304b3-109">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="304b3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="304b3-110">Parameters</span></span>

<span data-ttu-id="304b3-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="304b3-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="304b3-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="304b3-112">Return value</span></span>

<span data-ttu-id="304b3-113">Der Rückgabewert ist ein **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="304b3-113">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="304b3-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="304b3-114">Requirements</span></span>



| <span data-ttu-id="304b3-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="304b3-115">Requirement</span></span> | <span data-ttu-id="304b3-116">Wert</span><span class="sxs-lookup"><span data-stu-id="304b3-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="304b3-117">Header</span><span class="sxs-lookup"><span data-stu-id="304b3-117">Header</span></span><br/> | <dl> <span data-ttu-id="304b3-118"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="304b3-118"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="304b3-119">DLL</span><span class="sxs-lookup"><span data-stu-id="304b3-119">DLL</span></span><br/>    | <dl> <span data-ttu-id="304b3-120"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="304b3-120"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="304b3-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="304b3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="304b3-122">**Iumumpstoretypes**</span><span class="sxs-lookup"><span data-stu-id="304b3-122">**IEnumPStoreTypes**</span></span>](ienumpstoretypes.md)
</dt> </dl>

 

 
