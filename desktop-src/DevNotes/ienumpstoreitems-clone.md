---
description: 'IEnumPStoreItems::Clone-Methode: Erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle enthält.'
ms.assetid: ab9eaf63-54e4-4322-9bb5-227982b15c73
title: IEnumPStoreItems::Clone-Methode (Pstore.h)
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
ms.openlocfilehash: 29b618881305296a560dc9102f7571c08236d1bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089328"
---
# <a name="ienumpstoreitemsclone-method"></a><span data-ttu-id="57690-103">IEnumPStoreItems::Clone-Methode</span><span class="sxs-lookup"><span data-stu-id="57690-103">IEnumPStoreItems::Clone method</span></span>

<span data-ttu-id="57690-104">\[Geschützter Speicher (Pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="57690-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="57690-105">Sie ist nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista verfügbar, ist in nachfolgenden Versionen jedoch möglicherweise nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="57690-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="57690-106">Pstore verwendet eine ältere Implementierung des Datenschutzes.</span><span class="sxs-lookup"><span data-stu-id="57690-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="57690-107">Entwicklern wird dringend empfohlen, den verstärkten Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="57690-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="57690-108">Erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle Enumerator enthält.</span><span class="sxs-lookup"><span data-stu-id="57690-108">Creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="57690-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="57690-109">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumPStoreItems **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="57690-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="57690-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57690-111">*ppenum* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="57690-111">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57690-112">Ein Zeiger auf einen [**IEnumPStoreItems-Zeiger.**](ienumpstoreitems.md)</span><span class="sxs-lookup"><span data-stu-id="57690-112">A pointer to an [**IEnumPStoreItems**](ienumpstoreitems.md) pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57690-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="57690-113">Return value</span></span>

<span data-ttu-id="57690-114">Der Rückgabewert ist ein **HRESULT-Wert.**</span><span class="sxs-lookup"><span data-stu-id="57690-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="57690-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="57690-115">Requirements</span></span>



| <span data-ttu-id="57690-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="57690-116">Requirement</span></span> | <span data-ttu-id="57690-117">Wert</span><span class="sxs-lookup"><span data-stu-id="57690-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="57690-118">Header</span><span class="sxs-lookup"><span data-stu-id="57690-118">Header</span></span><br/> | <dl> <span data-ttu-id="57690-119"><dt>Pstore.h</dt></span><span class="sxs-lookup"><span data-stu-id="57690-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="57690-120">DLL</span><span class="sxs-lookup"><span data-stu-id="57690-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="57690-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57690-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57690-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="57690-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57690-123">**IEnumPStoreItems**</span><span class="sxs-lookup"><span data-stu-id="57690-123">**IEnumPStoreItems**</span></span>](ienumpstoreitems.md)
</dt> </dl>

 

 
