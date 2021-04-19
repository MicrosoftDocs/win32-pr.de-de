---
description: Ruft die nächste angegebene Anzahl von Anbietern in der enumerationssequenz ab.
ms.assetid: 9ef8d330-6f78-4063-825c-9cf5b4f283cf
title: 'Ienumpstoreproviders:: Next-Methode (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Next
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: f468d29682c4e3767d4d8fe7d59e60976f103484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354090"
---
# <a name="ienumpstoreprovidersnext-method"></a><span data-ttu-id="9fcc2-103">Ienumpstoreproviders:: Next-Methode</span><span class="sxs-lookup"><span data-stu-id="9fcc2-103">IEnumPStoreProviders::Next method</span></span>

<span data-ttu-id="9fcc2-104">\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9fcc2-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="9fcc2-105">Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9fcc2-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="9fcc2-106">Pstore verwendet eine ältere Implementierung des Schutzes von Daten.</span><span class="sxs-lookup"><span data-stu-id="9fcc2-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="9fcc2-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="9fcc2-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="9fcc2-108">Ruft die nächste angegebene Anzahl von Anbietern in der enumerationssequenz ab.</span><span class="sxs-lookup"><span data-stu-id="9fcc2-108">Gets the next specified number of providers in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fcc2-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="9fcc2-109">Syntax</span></span>


```C++
HRESULT Next(
  [in]      DWORD  celt,
  [out]     LPWSTR *rgelt,
  [in, out] DWORD  *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="9fcc2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9fcc2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fcc2-111">*celt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fcc2-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fcc2-112">Die Anzahl der angeforderten Anbieter Typen.</span><span class="sxs-lookup"><span data-stu-id="9fcc2-112">The number of provider types requested.</span></span>

</dd> <dt>

<span data-ttu-id="9fcc2-113">*rgelt* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9fcc2-113">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9fcc2-114">Ein Zeiger auf eine Zeichenfolge, in die der Anbietertyp Name zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="9fcc2-114">A pointer to a string in which to return the provider type name.</span></span>

</dd> <dt>

<span data-ttu-id="9fcc2-115">*pceltfetch* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="9fcc2-115">*pceltFetched* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9fcc2-116">Ein Zeiger auf die Anzahl der tatsächlich bereitgestellten Anbieter Typen.</span><span class="sxs-lookup"><span data-stu-id="9fcc2-116">A pointer to the number of provider types that was actually supplied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fcc2-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9fcc2-117">Return value</span></span>

<span data-ttu-id="9fcc2-118">Der Rückgabewert ist ein **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="9fcc2-118">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fcc2-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9fcc2-119">Requirements</span></span>



| <span data-ttu-id="9fcc2-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9fcc2-120">Requirement</span></span> | <span data-ttu-id="9fcc2-121">Wert</span><span class="sxs-lookup"><span data-stu-id="9fcc2-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9fcc2-122">Header</span><span class="sxs-lookup"><span data-stu-id="9fcc2-122">Header</span></span><br/> | <dl> <span data-ttu-id="9fcc2-123"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fcc2-123"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="9fcc2-124">DLL</span><span class="sxs-lookup"><span data-stu-id="9fcc2-124">DLL</span></span><br/>    | <dl> <span data-ttu-id="9fcc2-125"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fcc2-125"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fcc2-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9fcc2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fcc2-127">**Ienumpstoreproviders**</span><span class="sxs-lookup"><span data-stu-id="9fcc2-127">**IEnumPStoreProviders**</span></span>](ienumpstoreproviders.md)
</dt> </dl>

 

 
