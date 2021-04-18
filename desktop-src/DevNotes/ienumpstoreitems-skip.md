---
description: Überspringt die nächste angegebene Anzahl von Elementen in der angegebenen enumerationssequenz.
ms.assetid: 1459c18a-ccff-451f-8904-32858cc72b78
title: 'Iumumpstoreitems:: Skip-Methode (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems.Skip
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 912dea836ec5ac04ddaf54de9f7f7b609e4e23ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371516"
---
# <a name="ienumpstoreitemsskip-method"></a><span data-ttu-id="6e362-103">Iumumpstoreitems:: Skip-Methode</span><span class="sxs-lookup"><span data-stu-id="6e362-103">IEnumPStoreItems::Skip method</span></span>

<span data-ttu-id="6e362-104">\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6e362-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="6e362-105">Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6e362-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="6e362-106">Pstore verwendet eine ältere Implementierung des Schutzes von Daten.</span><span class="sxs-lookup"><span data-stu-id="6e362-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="6e362-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="6e362-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="6e362-108">Überspringt die nächste angegebene Anzahl von Elementen in der angegebenen enumerationssequenz.</span><span class="sxs-lookup"><span data-stu-id="6e362-108">Skips over the next specified number of items in the given enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e362-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e362-109">Syntax</span></span>


```C++
HRESULT Skip(
  [in] DWORD celt
);
```



## <a name="parameters"></a><span data-ttu-id="6e362-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e362-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e362-111">*celt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6e362-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e362-112">Die Anzahl der Datenelemente, die übersprungen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6e362-112">The number of data items to be skipped.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e362-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6e362-113">Return value</span></span>

<span data-ttu-id="6e362-114">Der Rückgabewert ist ein **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="6e362-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e362-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6e362-115">Requirements</span></span>



| <span data-ttu-id="6e362-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6e362-116">Requirement</span></span> | <span data-ttu-id="6e362-117">Wert</span><span class="sxs-lookup"><span data-stu-id="6e362-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e362-118">Header</span><span class="sxs-lookup"><span data-stu-id="6e362-118">Header</span></span><br/> | <dl> <span data-ttu-id="6e362-119"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e362-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="6e362-120">DLL</span><span class="sxs-lookup"><span data-stu-id="6e362-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="6e362-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e362-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e362-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e362-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e362-123">**Iumumpstoreitems**</span><span class="sxs-lookup"><span data-stu-id="6e362-123">**IEnumPStoreItems**</span></span>](ienumpstoreitems.md)
</dt> </dl>

 

 
