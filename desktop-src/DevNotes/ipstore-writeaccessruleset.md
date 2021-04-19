---
description: Schreibt die Zugriffsregeln für den angegebenen Typ.
ms.assetid: d5cfd782-8d87-45ae-a574-0a294a30ca71
title: 'Ipstore:: schreiteaccessruleset-Methode (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.WriteAccessRuleset
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 7399ff800087720d65cb45e80ccab080a7df9baf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372455"
---
# <a name="ipstorewriteaccessruleset-method"></a><span data-ttu-id="38c6d-103">Ipstore:: schreiteaccessruleset-Methode</span><span class="sxs-lookup"><span data-stu-id="38c6d-103">IPStore::WriteAccessRuleset method</span></span>

<span data-ttu-id="38c6d-104">\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="38c6d-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="38c6d-105">Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="38c6d-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="38c6d-106">Pstore verwendet eine ältere Implementierung des Schutzes von Daten.</span><span class="sxs-lookup"><span data-stu-id="38c6d-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="38c6d-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="38c6d-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="38c6d-108">\[Diese Methode ist nicht implementiert.\]</span><span class="sxs-lookup"><span data-stu-id="38c6d-108">\[This method is not implemented.\]</span></span>

<span data-ttu-id="38c6d-109">Schreibt die Zugriffsregeln für den angegebenen Typ.</span><span class="sxs-lookup"><span data-stu-id="38c6d-109">Writes the access rules for the given type.</span></span>

## <a name="syntax"></a><span data-ttu-id="38c6d-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="38c6d-110">Syntax</span></span>


```C++
HRESULT WriteAccessRuleset(
  [in]       PST_KEY            Key,
  [in] const GUID               *pType,
  [in] const GUID               *pSubtype,
  [in]       PPST_TYPEINFO      pInfo,
  [in]       PPST_ACCESSRULESET pRules,
  [in]       DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="38c6d-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="38c6d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38c6d-112">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38c6d-112">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38c6d-113">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="38c6d-113">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="38c6d-114">*pType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38c6d-114">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38c6d-115">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="38c6d-115">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="38c6d-116">*psubtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38c6d-116">*pSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38c6d-117">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="38c6d-117">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="38c6d-118">*pinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38c6d-118">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38c6d-119">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="38c6d-119">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="38c6d-120">*prules* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38c6d-120">*pRules* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38c6d-121">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="38c6d-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="38c6d-122">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38c6d-122">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38c6d-123">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="38c6d-123">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38c6d-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="38c6d-124">Return value</span></span>

<span data-ttu-id="38c6d-125">Bei Aufrufen dieser Methode tritt immer ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="38c6d-125">Calls to this method will always fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="38c6d-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="38c6d-126">Requirements</span></span>



| <span data-ttu-id="38c6d-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="38c6d-127">Requirement</span></span> | <span data-ttu-id="38c6d-128">Wert</span><span class="sxs-lookup"><span data-stu-id="38c6d-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="38c6d-129">Header</span><span class="sxs-lookup"><span data-stu-id="38c6d-129">Header</span></span><br/> | <dl> <span data-ttu-id="38c6d-130"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="38c6d-130"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="38c6d-131">DLL</span><span class="sxs-lookup"><span data-stu-id="38c6d-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="38c6d-132"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38c6d-132"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38c6d-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38c6d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38c6d-134">**Ipstore**</span><span class="sxs-lookup"><span data-stu-id="38c6d-134">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
