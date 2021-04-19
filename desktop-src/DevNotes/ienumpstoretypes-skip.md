---
description: Überspringt die nächste angegebene Anzahl von Elementen in der enumerationssequenz.
ms.assetid: 4c02aac8-0496-4ad9-9863-2074b2c71902
title: 'Isumpstoretypes:: Skip-Methode (pstore. h)'
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
ms.openlocfilehash: 511595dd55f66e91ae0f5606f9e047918e7ff0fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361675"
---
# <a name="ienumpstoretypesskip-method"></a><span data-ttu-id="57af1-103">Iumumpstoretypes:: Skip-Methode</span><span class="sxs-lookup"><span data-stu-id="57af1-103">IEnumPStoreTypes::Skip method</span></span>

<span data-ttu-id="57af1-104">\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="57af1-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="57af1-105">Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="57af1-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="57af1-106">Pstore verwendet eine ältere Implementierung des Schutzes von Daten.</span><span class="sxs-lookup"><span data-stu-id="57af1-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="57af1-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="57af1-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="57af1-108">Überspringt die nächste angegebene Anzahl von Elementen in der enumerationssequenz.</span><span class="sxs-lookup"><span data-stu-id="57af1-108">Skips over the next specified number of items in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="57af1-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="57af1-109">Syntax</span></span>


```C++
HRESULT Skip(
  [in] DWORD celt
);
```



## <a name="parameters"></a><span data-ttu-id="57af1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="57af1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57af1-111">*celt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57af1-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57af1-112">Die Anzahl der Anbieter Typen, die übersprungen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="57af1-112">The number of provider types to be skipped.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57af1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="57af1-113">Return value</span></span>

<span data-ttu-id="57af1-114">Der Rückgabewert ist ein **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="57af1-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="57af1-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="57af1-115">Requirements</span></span>



| <span data-ttu-id="57af1-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="57af1-116">Requirement</span></span> | <span data-ttu-id="57af1-117">Wert</span><span class="sxs-lookup"><span data-stu-id="57af1-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="57af1-118">Header</span><span class="sxs-lookup"><span data-stu-id="57af1-118">Header</span></span><br/> | <dl> <span data-ttu-id="57af1-119"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="57af1-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="57af1-120">DLL</span><span class="sxs-lookup"><span data-stu-id="57af1-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="57af1-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57af1-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57af1-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57af1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57af1-123">**Iumumpstoretypes**</span><span class="sxs-lookup"><span data-stu-id="57af1-123">**IEnumPStoreTypes**</span></span>](ienumpstoretypes.md)
</dt> </dl>

 

 
