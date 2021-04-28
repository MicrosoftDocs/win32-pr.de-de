---
description: 'IEnumPStoreTypes::Skip-Methode: Überspringt die nächste angegebene Anzahl von Elementen in der Enumerationssequenz.'
ms.assetid: 4c02aac8-0496-4ad9-9863-2074b2c71902
title: IEnumPStoreTypes::Skip-Methode (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes.Skip
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: fdc656af2a8f50d02d2f88545d189d9c9285a7f9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096738"
---
# <a name="ienumpstoretypesskip-method"></a><span data-ttu-id="3a0fe-103">IEnumPStoreTypes::Skip-Methode</span><span class="sxs-lookup"><span data-stu-id="3a0fe-103">IEnumPStoreTypes::Skip method</span></span>

<span data-ttu-id="3a0fe-104">\[Protected Storage (Pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3a0fe-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="3a0fe-105">Es ist nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista verfügbar, aber in nachfolgenden Versionen möglicherweise nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3a0fe-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="3a0fe-106">Pstore verwendet eine ältere Implementierung des Datenschutzes.</span><span class="sxs-lookup"><span data-stu-id="3a0fe-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="3a0fe-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den [**Funktionen CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData bereitgestellt**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) wird.\]</span><span class="sxs-lookup"><span data-stu-id="3a0fe-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="3a0fe-108">Überspringt die nächste angegebene Anzahl von Elementen in der Enumerationssequenz.</span><span class="sxs-lookup"><span data-stu-id="3a0fe-108">Skips over the next specified number of items in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a0fe-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a0fe-109">Syntax</span></span>


```C++
HRESULT Skip(
  [in] DWORD celt
);
```



## <a name="parameters"></a><span data-ttu-id="3a0fe-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a0fe-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a0fe-111">*celt* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="3a0fe-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a0fe-112">Die Anzahl der anbietertypen, die übersprungen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3a0fe-112">The number of provider types to be skipped.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a0fe-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3a0fe-113">Return value</span></span>

<span data-ttu-id="3a0fe-114">Der Rückgabewert ist ein **HRESULT-Wert.**</span><span class="sxs-lookup"><span data-stu-id="3a0fe-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a0fe-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a0fe-115">Requirements</span></span>



| <span data-ttu-id="3a0fe-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a0fe-116">Requirement</span></span> | <span data-ttu-id="3a0fe-117">Wert</span><span class="sxs-lookup"><span data-stu-id="3a0fe-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a0fe-118">Header</span><span class="sxs-lookup"><span data-stu-id="3a0fe-118">Header</span></span><br/> | <dl> <span data-ttu-id="3a0fe-119"><dt>Pstore.h</dt></span><span class="sxs-lookup"><span data-stu-id="3a0fe-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="3a0fe-120">DLL</span><span class="sxs-lookup"><span data-stu-id="3a0fe-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="3a0fe-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a0fe-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a0fe-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3a0fe-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a0fe-123">**IEnumPStoreTypes**</span><span class="sxs-lookup"><span data-stu-id="3a0fe-123">**IEnumPStoreTypes**</span></span>](ienumpstoretypes.md)
</dt> </dl>

 

 
