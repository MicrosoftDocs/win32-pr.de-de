---
description: Gibt Informationen zum Speicher Anbieter zurück.
ms.assetid: bdacb5bb-a37a-4970-add7-57625bec1ce0
title: 'Ipstore:: GetInfo-Methode (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetInfo
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 7747c3acf15a60f5556a8855ef4825715ef5050b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106363218"
---
# <a name="ipstoregetinfo-method"></a><span data-ttu-id="a1c8f-103">Ipstore:: GetInfo-Methode</span><span class="sxs-lookup"><span data-stu-id="a1c8f-103">IPStore::GetInfo method</span></span>

<span data-ttu-id="a1c8f-104">\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a1c8f-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="a1c8f-105">Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a1c8f-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="a1c8f-106">Pstore verwendet eine ältere Implementierung des Schutzes von Daten.</span><span class="sxs-lookup"><span data-stu-id="a1c8f-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="a1c8f-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="a1c8f-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="a1c8f-108">Gibt Informationen zum Speicher Anbieter zurück.</span><span class="sxs-lookup"><span data-stu-id="a1c8f-108">Returns information on the storage provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1c8f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1c8f-109">Syntax</span></span>


```C++
HRESULT GetInfo(
  [out] PPST_PROVIDERINFO *ppProperties
);
```



## <a name="parameters"></a><span data-ttu-id="a1c8f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1c8f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1c8f-111">*ppproperties* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a1c8f-111">*ppProperties* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1c8f-112">Ein Zeiger auf eine **ppst \_ ProviderInfo** -Struktur, die Informationen über den Speicher Anbieter enthält.</span><span class="sxs-lookup"><span data-stu-id="a1c8f-112">A pointer to a **PPST\_PROVIDERINFO** structure that contains information about the storage provider.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1c8f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a1c8f-113">Return value</span></span>

<span data-ttu-id="a1c8f-114">Der Rückgabewert ist ein **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="a1c8f-114">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="a1c8f-115">Der Wert **PST \_ E \_ OK** gibt an, dass die Funktion erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="a1c8f-115">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1c8f-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a1c8f-116">Requirements</span></span>



| <span data-ttu-id="a1c8f-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1c8f-117">Requirement</span></span> | <span data-ttu-id="a1c8f-118">Wert</span><span class="sxs-lookup"><span data-stu-id="a1c8f-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1c8f-119">Header</span><span class="sxs-lookup"><span data-stu-id="a1c8f-119">Header</span></span><br/> | <dl> <span data-ttu-id="a1c8f-120"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1c8f-120"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="a1c8f-121">DLL</span><span class="sxs-lookup"><span data-stu-id="a1c8f-121">DLL</span></span><br/>    | <dl> <span data-ttu-id="a1c8f-122"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1c8f-122"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1c8f-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1c8f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1c8f-124">**Ipstore**</span><span class="sxs-lookup"><span data-stu-id="a1c8f-124">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
