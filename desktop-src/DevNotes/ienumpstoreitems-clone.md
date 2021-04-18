---
description: Erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle Enumerator enthält.
ms.assetid: ab9eaf63-54e4-4322-9bb5-227982b15c73
title: 'Iumumpstoreitems:: Clone-Methode (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems.Clone
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 919c0359f5c7f6d3ab547f53a105246c43e20fb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372695"
---
# <a name="ienumpstoreitemsclone-method"></a><span data-ttu-id="9a45f-103">Iumumpstoreitems:: Clone-Methode</span><span class="sxs-lookup"><span data-stu-id="9a45f-103">IEnumPStoreItems::Clone method</span></span>

<span data-ttu-id="9a45f-104">\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9a45f-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="9a45f-105">Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9a45f-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="9a45f-106">Pstore verwendet eine ältere Implementierung des Schutzes von Daten.</span><span class="sxs-lookup"><span data-stu-id="9a45f-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="9a45f-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="9a45f-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="9a45f-108">Erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle Enumerator enthält.</span><span class="sxs-lookup"><span data-stu-id="9a45f-108">Creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a45f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a45f-109">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumPStoreItems **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="9a45f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a45f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a45f-111">*ppum* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9a45f-111">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a45f-112">Ein Zeiger auf einen [**iumumpstoreitems**](ienumpstoreitems.md) -Zeiger.</span><span class="sxs-lookup"><span data-stu-id="9a45f-112">A pointer to an [**IEnumPStoreItems**](ienumpstoreitems.md) pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a45f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9a45f-113">Return value</span></span>

<span data-ttu-id="9a45f-114">Der Rückgabewert ist ein **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="9a45f-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a45f-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a45f-115">Requirements</span></span>



| <span data-ttu-id="9a45f-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9a45f-116">Requirement</span></span> | <span data-ttu-id="9a45f-117">Wert</span><span class="sxs-lookup"><span data-stu-id="9a45f-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a45f-118">Header</span><span class="sxs-lookup"><span data-stu-id="9a45f-118">Header</span></span><br/> | <dl> <span data-ttu-id="9a45f-119"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a45f-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="9a45f-120">DLL</span><span class="sxs-lookup"><span data-stu-id="9a45f-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="9a45f-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a45f-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a45f-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a45f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a45f-123">**Iumumpstoreitems**</span><span class="sxs-lookup"><span data-stu-id="9a45f-123">**IEnumPStoreItems**</span></span>](ienumpstoreitems.md)
</dt> </dl>

 

 
