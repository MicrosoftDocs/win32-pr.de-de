---
description: Liest die Zugriffsregeln für einen angegebenen Typ.
ms.assetid: fd569e7f-ca5c-4571-bbaa-c669e8780a97
title: 'Ipstore:: Read accessruleset-Methode (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.ReadAccessRuleSet
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: f69c206bde67c2ddf9ed87ba0c50633ab9c15bc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371226"
---
# <a name="ipstorereadaccessruleset-method"></a><span data-ttu-id="ad90e-103">Ipstore:: Read accessruleset-Methode</span><span class="sxs-lookup"><span data-stu-id="ad90e-103">IPStore::ReadAccessRuleSet method</span></span>

<span data-ttu-id="ad90e-104">\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ad90e-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="ad90e-105">Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ad90e-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="ad90e-106">Pstore verwendet eine ältere Implementierung des Schutzes von Daten.</span><span class="sxs-lookup"><span data-stu-id="ad90e-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="ad90e-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="ad90e-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="ad90e-108">\[Diese Methode ist nicht implementiert.\]</span><span class="sxs-lookup"><span data-stu-id="ad90e-108">\[This method is not implemented.\]</span></span>

<span data-ttu-id="ad90e-109">Liest die Zugriffsregeln für einen angegebenen Typ.</span><span class="sxs-lookup"><span data-stu-id="ad90e-109">Reads the access rules for a given type.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad90e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad90e-110">Syntax</span></span>


```C++
HRESULT ReadAccessRuleSet(
  [in]       PST_KEY            Key,
  [in] const GUID               *pType,
  [in] const GUID               *pSubtype,
  [in]       PPST_TYPEINFO      pInfo,
  [in]       PPST_ACCESSRULESET **ppRules,
  [in]       DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="ad90e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad90e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad90e-112">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad90e-112">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad90e-113">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="ad90e-113">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="ad90e-114">*pType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad90e-114">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad90e-115">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="ad90e-115">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="ad90e-116">*psubtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad90e-116">*pSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad90e-117">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="ad90e-117">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="ad90e-118">*pinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad90e-118">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad90e-119">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="ad90e-119">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="ad90e-120">*pprules* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad90e-120">*ppRules* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad90e-121">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="ad90e-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="ad90e-122">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad90e-122">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad90e-123">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="ad90e-123">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad90e-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ad90e-124">Return value</span></span>

<span data-ttu-id="ad90e-125">Bei Aufrufen dieser Methode tritt immer ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="ad90e-125">Calls to this method will always fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad90e-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad90e-126">Requirements</span></span>



| <span data-ttu-id="ad90e-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ad90e-127">Requirement</span></span> | <span data-ttu-id="ad90e-128">Wert</span><span class="sxs-lookup"><span data-stu-id="ad90e-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad90e-129">Header</span><span class="sxs-lookup"><span data-stu-id="ad90e-129">Header</span></span><br/> | <dl> <span data-ttu-id="ad90e-130"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad90e-130"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="ad90e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="ad90e-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="ad90e-132"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad90e-132"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad90e-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad90e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad90e-134">**Ipstore**</span><span class="sxs-lookup"><span data-stu-id="ad90e-134">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
