---
description: Setzt auf den Anfang der angegebenen enumerationssequenz zurück.
ms.assetid: add91f5d-3f84-4069-93c0-9380a3935b85
title: 'Iumumpstoreitems:: Reset-Methode (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems.Reset
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: d5b05c23ba40ab647b2c4b3bb552f92ee34e12c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359754"
---
# <a name="ienumpstoreitemsreset-method"></a><span data-ttu-id="d4c1d-103">Iumumpstoreitems:: Reset-Methode</span><span class="sxs-lookup"><span data-stu-id="d4c1d-103">IEnumPStoreItems::Reset method</span></span>

<span data-ttu-id="d4c1d-104">\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d4c1d-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="d4c1d-105">Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d4c1d-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="d4c1d-106">Pstore verwendet eine ältere Implementierung des Schutzes von Daten.</span><span class="sxs-lookup"><span data-stu-id="d4c1d-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="d4c1d-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="d4c1d-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="d4c1d-108">Setzt auf den Anfang der angegebenen enumerationssequenz zurück.</span><span class="sxs-lookup"><span data-stu-id="d4c1d-108">Resets to the beginning of the given enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4c1d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4c1d-109">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="d4c1d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4c1d-110">Parameters</span></span>

<span data-ttu-id="d4c1d-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="d4c1d-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d4c1d-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d4c1d-112">Return value</span></span>

<span data-ttu-id="d4c1d-113">Der Rückgabewert ist ein **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="d4c1d-113">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4c1d-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4c1d-114">Requirements</span></span>



| <span data-ttu-id="d4c1d-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4c1d-115">Requirement</span></span> | <span data-ttu-id="d4c1d-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d4c1d-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4c1d-117">Header</span><span class="sxs-lookup"><span data-stu-id="d4c1d-117">Header</span></span><br/> | <dl> <span data-ttu-id="d4c1d-118"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4c1d-118"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="d4c1d-119">DLL</span><span class="sxs-lookup"><span data-stu-id="d4c1d-119">DLL</span></span><br/>    | <dl> <span data-ttu-id="d4c1d-120"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4c1d-120"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4c1d-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4c1d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4c1d-122">**Iumumpstoreitems**</span><span class="sxs-lookup"><span data-stu-id="d4c1d-122">**IEnumPStoreItems**</span></span>](ienumpstoreitems.md)
</dt> </dl>

 

 
