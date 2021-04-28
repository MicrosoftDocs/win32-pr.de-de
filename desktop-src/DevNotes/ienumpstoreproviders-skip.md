---
description: 'IEnumPStoreProviders::Skip-Methode: Überspringt die nächste angegebene Anzahl von Elementen in der Enumerationssequenz.'
ms.assetid: bf9ea700-3f44-48a7-8ea0-ee66dea61836
title: IEnumPStoreProviders::Skip-Methode (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Skip
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 2f74c44de172d9235d9768b8f484405b5e8fb7fe
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096748"
---
# <a name="ienumpstoreprovidersskip-method"></a><span data-ttu-id="13079-103">IEnumPStoreProviders::Skip-Methode</span><span class="sxs-lookup"><span data-stu-id="13079-103">IEnumPStoreProviders::Skip method</span></span>

<span data-ttu-id="13079-104">\[Geschützter Speicher (Pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="13079-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="13079-105">Sie ist nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista verfügbar, ist in nachfolgenden Versionen jedoch möglicherweise nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="13079-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="13079-106">Pstore verwendet eine ältere Implementierung des Datenschutzes.</span><span class="sxs-lookup"><span data-stu-id="13079-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="13079-107">Entwicklern wird dringend empfohlen, den verstärkten Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="13079-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="13079-108">Überspringt die nächste angegebene Anzahl von Elementen in der Enumerationssequenz.</span><span class="sxs-lookup"><span data-stu-id="13079-108">Skips over the next specified number of items in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="13079-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="13079-109">Syntax</span></span>


```C++
HRESULT Skip(
  [in] DWORD celt
);
```



## <a name="parameters"></a><span data-ttu-id="13079-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="13079-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13079-111">*celt* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="13079-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13079-112">Die Anzahl der anbietertypen, die übersprungen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="13079-112">The number of provider types to be skipped.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13079-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="13079-113">Return value</span></span>

<span data-ttu-id="13079-114">Der Rückgabewert ist ein **HRESULT-Wert.**</span><span class="sxs-lookup"><span data-stu-id="13079-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="13079-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13079-115">Requirements</span></span>



| <span data-ttu-id="13079-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13079-116">Requirement</span></span> | <span data-ttu-id="13079-117">Wert</span><span class="sxs-lookup"><span data-stu-id="13079-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="13079-118">Header</span><span class="sxs-lookup"><span data-stu-id="13079-118">Header</span></span><br/> | <dl> <span data-ttu-id="13079-119"><dt>Pstore.h</dt></span><span class="sxs-lookup"><span data-stu-id="13079-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="13079-120">DLL</span><span class="sxs-lookup"><span data-stu-id="13079-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="13079-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13079-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13079-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="13079-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13079-123">**IEnumPStoreProviders**</span><span class="sxs-lookup"><span data-stu-id="13079-123">**IEnumPStoreProviders**</span></span>](ienumpstoreproviders.md)
</dt> </dl>

 

 
