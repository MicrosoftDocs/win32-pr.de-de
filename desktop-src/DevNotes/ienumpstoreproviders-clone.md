---
description: Erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle Enumerator enthält.
ms.assetid: c9a53005-4bb2-4a07-8f58-28d51f22c9e8
title: 'Ienumpstoreproviders:: Clone-Methode (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Clone
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: fdd7825a44dcea672eff24a15126921f0426a986
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361304"
---
# <a name="ienumpstoreprovidersclone-method"></a><span data-ttu-id="12f7a-103">Ienumpstoreproviders:: Clone-Methode</span><span class="sxs-lookup"><span data-stu-id="12f7a-103">IEnumPStoreProviders::Clone method</span></span>

<span data-ttu-id="12f7a-104">\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="12f7a-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="12f7a-105">Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="12f7a-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="12f7a-106">Pstore verwendet eine ältere Implementierung des Schutzes von Daten.</span><span class="sxs-lookup"><span data-stu-id="12f7a-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="12f7a-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="12f7a-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="12f7a-108">Erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle Enumerator enthält.</span><span class="sxs-lookup"><span data-stu-id="12f7a-108">Creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="12f7a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="12f7a-109">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumPStoreProviders **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="12f7a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="12f7a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12f7a-111">*ppum* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="12f7a-111">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12f7a-112">Ein Zeiger auf einen [**ienumpstoreproviders**](ienumpstoreproviders.md) -Zeiger.</span><span class="sxs-lookup"><span data-stu-id="12f7a-112">A pointer to an [**IEnumPStoreProviders**](ienumpstoreproviders.md) pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12f7a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="12f7a-113">Return value</span></span>

<span data-ttu-id="12f7a-114">Der Rückgabewert ist ein **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="12f7a-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="12f7a-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="12f7a-115">Requirements</span></span>



| <span data-ttu-id="12f7a-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="12f7a-116">Requirement</span></span> | <span data-ttu-id="12f7a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="12f7a-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="12f7a-118">Header</span><span class="sxs-lookup"><span data-stu-id="12f7a-118">Header</span></span><br/> | <dl> <span data-ttu-id="12f7a-119"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="12f7a-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="12f7a-120">DLL</span><span class="sxs-lookup"><span data-stu-id="12f7a-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="12f7a-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12f7a-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12f7a-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12f7a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12f7a-123">**Ienumpstoreproviders**</span><span class="sxs-lookup"><span data-stu-id="12f7a-123">**IEnumPStoreProviders**</span></span>](ienumpstoreproviders.md)
</dt> </dl>

 

 
