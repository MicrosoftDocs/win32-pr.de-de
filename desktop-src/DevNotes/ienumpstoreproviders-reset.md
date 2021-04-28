---
description: 'IEnumPStoreProviders::Reset-Methode: Setzt auf den Anfang der Enumerationssequenz zurück.'
ms.assetid: 9c5044b5-25a3-4d10-829b-ef4d8b5ac095
title: IEnumPStoreProviders::Reset-Methode (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Reset
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 3e37e131b6f67f94bb787051123be8eb430eb39e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096758"
---
# <a name="ienumpstoreprovidersreset-method"></a><span data-ttu-id="53c9d-103">IEnumPStoreProviders::Reset-Methode</span><span class="sxs-lookup"><span data-stu-id="53c9d-103">IEnumPStoreProviders::Reset method</span></span>

<span data-ttu-id="53c9d-104">\[Geschützter Speicher (Pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="53c9d-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="53c9d-105">Sie ist nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista verfügbar, ist in nachfolgenden Versionen jedoch möglicherweise nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="53c9d-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="53c9d-106">Pstore verwendet eine ältere Implementierung des Datenschutzes.</span><span class="sxs-lookup"><span data-stu-id="53c9d-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="53c9d-107">Entwicklern wird dringend empfohlen, den verstärkten Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="53c9d-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="53c9d-108">Setzt auf den Anfang der Enumerationssequenz zurück.</span><span class="sxs-lookup"><span data-stu-id="53c9d-108">Resets to the beginning of the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="53c9d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="53c9d-109">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="53c9d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="53c9d-110">Parameters</span></span>

<span data-ttu-id="53c9d-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="53c9d-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="53c9d-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="53c9d-112">Return value</span></span>

<span data-ttu-id="53c9d-113">Der Rückgabewert ist ein **HRESULT-Wert.**</span><span class="sxs-lookup"><span data-stu-id="53c9d-113">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="53c9d-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53c9d-114">Requirements</span></span>



| <span data-ttu-id="53c9d-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53c9d-115">Requirement</span></span> | <span data-ttu-id="53c9d-116">Wert</span><span class="sxs-lookup"><span data-stu-id="53c9d-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="53c9d-117">Header</span><span class="sxs-lookup"><span data-stu-id="53c9d-117">Header</span></span><br/> | <dl> <span data-ttu-id="53c9d-118"><dt>Pstore.h</dt></span><span class="sxs-lookup"><span data-stu-id="53c9d-118"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="53c9d-119">DLL</span><span class="sxs-lookup"><span data-stu-id="53c9d-119">DLL</span></span><br/>    | <dl> <span data-ttu-id="53c9d-120"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53c9d-120"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53c9d-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="53c9d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53c9d-122">**IEnumPStoreProviders**</span><span class="sxs-lookup"><span data-stu-id="53c9d-122">**IEnumPStoreProviders**</span></span>](ienumpstoreproviders.md)
</dt> </dl>

 

 
