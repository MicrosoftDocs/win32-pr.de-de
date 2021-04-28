---
description: 'IEnumPStoreProviders::Clone-Methode: Erstellt einen weiteren Enumerator, der denselben Enumerationszustand wie der aktuelle enthält.'
ms.assetid: c9a53005-4bb2-4a07-8f58-28d51f22c9e8
title: IEnumPStoreProviders::Clone-Methode (Pstore.h)
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
ms.openlocfilehash: 2eb5f5788c903c854d9cf1551d6cf5a1bd2b51f6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096798"
---
# <a name="ienumpstoreprovidersclone-method"></a><span data-ttu-id="d8ad0-103">IEnumPStoreProviders::Clone-Methode</span><span class="sxs-lookup"><span data-stu-id="d8ad0-103">IEnumPStoreProviders::Clone method</span></span>

<span data-ttu-id="d8ad0-104">\[Protected Storage (Pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d8ad0-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="d8ad0-105">Es ist nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista verfügbar, aber in nachfolgenden Versionen möglicherweise nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d8ad0-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="d8ad0-106">Pstore verwendet eine ältere Implementierung des Datenschutzes.</span><span class="sxs-lookup"><span data-stu-id="d8ad0-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="d8ad0-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den [**Funktionen CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData bereitgestellt**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) wird.\]</span><span class="sxs-lookup"><span data-stu-id="d8ad0-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="d8ad0-108">Erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle Enumerator enthält.</span><span class="sxs-lookup"><span data-stu-id="d8ad0-108">Creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8ad0-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8ad0-109">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumPStoreProviders **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="d8ad0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8ad0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8ad0-111">*ppenum* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d8ad0-111">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8ad0-112">Ein Zeiger auf einen [**IEnumPStoreProviders-Zeiger.**](ienumpstoreproviders.md)</span><span class="sxs-lookup"><span data-stu-id="d8ad0-112">A pointer to an [**IEnumPStoreProviders**](ienumpstoreproviders.md) pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8ad0-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d8ad0-113">Return value</span></span>

<span data-ttu-id="d8ad0-114">Der Rückgabewert ist ein **HRESULT-Wert.**</span><span class="sxs-lookup"><span data-stu-id="d8ad0-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8ad0-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d8ad0-115">Requirements</span></span>



| <span data-ttu-id="d8ad0-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d8ad0-116">Requirement</span></span> | <span data-ttu-id="d8ad0-117">Wert</span><span class="sxs-lookup"><span data-stu-id="d8ad0-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8ad0-118">Header</span><span class="sxs-lookup"><span data-stu-id="d8ad0-118">Header</span></span><br/> | <dl> <span data-ttu-id="d8ad0-119"><dt>Pstore.h</dt></span><span class="sxs-lookup"><span data-stu-id="d8ad0-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="d8ad0-120">DLL</span><span class="sxs-lookup"><span data-stu-id="d8ad0-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="d8ad0-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8ad0-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8ad0-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d8ad0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8ad0-123">**IEnumPStoreProviders**</span><span class="sxs-lookup"><span data-stu-id="d8ad0-123">**IEnumPStoreProviders**</span></span>](ienumpstoreproviders.md)
</dt> </dl>

 

 
