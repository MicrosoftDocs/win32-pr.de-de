---
description: 'IEnumPStoreTypes::Reset-Methode: Setzt auf den Anfang der Enumerationssequenz zurück.'
ms.assetid: 35f14aa5-92cb-4ad8-b80c-2550dedb7a7f
title: IEnumPStoreTypes::Reset-Methode (Pstore.h)
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
ms.openlocfilehash: 55953a67d19ac94f792769974d860bae9b57f1ea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089318"
---
# <a name="ienumpstoretypesreset-method"></a><span data-ttu-id="804de-103">IEnumPStoreTypes::Reset-Methode</span><span class="sxs-lookup"><span data-stu-id="804de-103">IEnumPStoreTypes::Reset method</span></span>

<span data-ttu-id="804de-104">\[Geschützter Speicher (Pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="804de-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="804de-105">Sie ist nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista verfügbar, ist in nachfolgenden Versionen jedoch möglicherweise nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="804de-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="804de-106">Pstore verwendet eine ältere Implementierung des Datenschutzes.</span><span class="sxs-lookup"><span data-stu-id="804de-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="804de-107">Entwicklern wird dringend empfohlen, den verstärkten Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="804de-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="804de-108">Setzt auf den Anfang der Enumerationssequenz zurück.</span><span class="sxs-lookup"><span data-stu-id="804de-108">Resets to the beginning of the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="804de-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="804de-109">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="804de-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="804de-110">Parameters</span></span>

<span data-ttu-id="804de-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="804de-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="804de-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="804de-112">Return value</span></span>

<span data-ttu-id="804de-113">Der Rückgabewert ist ein **HRESULT-Wert.**</span><span class="sxs-lookup"><span data-stu-id="804de-113">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="804de-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="804de-114">Requirements</span></span>



| <span data-ttu-id="804de-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="804de-115">Requirement</span></span> | <span data-ttu-id="804de-116">Wert</span><span class="sxs-lookup"><span data-stu-id="804de-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="804de-117">Header</span><span class="sxs-lookup"><span data-stu-id="804de-117">Header</span></span><br/> | <dl> <span data-ttu-id="804de-118"><dt>Pstore.h</dt></span><span class="sxs-lookup"><span data-stu-id="804de-118"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="804de-119">DLL</span><span class="sxs-lookup"><span data-stu-id="804de-119">DLL</span></span><br/>    | <dl> <span data-ttu-id="804de-120"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="804de-120"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="804de-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="804de-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="804de-122">**IEnumPStoreTypes**</span><span class="sxs-lookup"><span data-stu-id="804de-122">**IEnumPStoreTypes**</span></span>](ienumpstoretypes.md)
</dt> </dl>

 

 
