---
description: Ruft die nächste angegebene Anzahl von Anbieter Typen in der enumerationssequenz ab.
ms.assetid: 9a1d0db0-1e9b-48f8-b373-2a82a48e4f63
title: 'Isumpstoretypes:: Next-Methode (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes.Next
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 18981053de897b75d1febdc75e138e6561e65bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366868"
---
# <a name="ienumpstoretypesnext-method"></a><span data-ttu-id="706cc-103">Isumpstoretypes:: Next-Methode</span><span class="sxs-lookup"><span data-stu-id="706cc-103">IEnumPStoreTypes::Next method</span></span>

<span data-ttu-id="706cc-104">\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="706cc-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="706cc-105">Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="706cc-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="706cc-106">Pstore verwendet eine ältere Implementierung des Schutzes von Daten.</span><span class="sxs-lookup"><span data-stu-id="706cc-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="706cc-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="706cc-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="706cc-108">Ruft die nächste angegebene Anzahl von Anbieter Typen in der enumerationssequenz ab.</span><span class="sxs-lookup"><span data-stu-id="706cc-108">Gets the next specified number of provider types in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="706cc-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="706cc-109">Syntax</span></span>


```C++
HRESULT Next(
  [in]      DWORD  celt,
  [out]     LPWSTR *rgelt,
  [in, out] DWORD  *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="706cc-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="706cc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="706cc-111">*celt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="706cc-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="706cc-112">Die Anzahl der angeforderten Anbieter Typen.</span><span class="sxs-lookup"><span data-stu-id="706cc-112">The number of provider types requested.</span></span>

</dd> <dt>

<span data-ttu-id="706cc-113">*rgelt* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="706cc-113">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="706cc-114">Ein Zeiger auf eine Zeichenfolge, in die der Anbietertyp Name zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="706cc-114">A pointer to a string in which to return the provider type name.</span></span>

</dd> <dt>

<span data-ttu-id="706cc-115">*pceltfetch* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="706cc-115">*pceltFetched* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="706cc-116">Ein Zeiger auf die Anzahl der tatsächlich bereitgestellten Anbieter Typen.</span><span class="sxs-lookup"><span data-stu-id="706cc-116">A pointer to the number of provider types actually supplied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="706cc-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="706cc-117">Return value</span></span>

<span data-ttu-id="706cc-118">Der Rückgabewert ist ein **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="706cc-118">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="706cc-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="706cc-119">Requirements</span></span>



| <span data-ttu-id="706cc-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="706cc-120">Requirement</span></span> | <span data-ttu-id="706cc-121">Wert</span><span class="sxs-lookup"><span data-stu-id="706cc-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="706cc-122">Header</span><span class="sxs-lookup"><span data-stu-id="706cc-122">Header</span></span><br/> | <dl> <span data-ttu-id="706cc-123"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="706cc-123"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="706cc-124">DLL</span><span class="sxs-lookup"><span data-stu-id="706cc-124">DLL</span></span><br/>    | <dl> <span data-ttu-id="706cc-125"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="706cc-125"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="706cc-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="706cc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="706cc-127">**Iumumpstoretypes**</span><span class="sxs-lookup"><span data-stu-id="706cc-127">**IEnumPStoreTypes**</span></span>](ienumpstoretypes.md)
</dt> </dl>

 

 
