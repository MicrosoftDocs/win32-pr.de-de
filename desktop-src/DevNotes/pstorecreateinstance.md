---
description: Ruft einen Schnittstellen Zeiger auf einen Speicher Anbieter ab.
ms.assetid: 22b5b003-82fa-48f1-96db-a8d6dd70d6d1
title: Pstorecreateinstance-Funktion (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PStoreCreateInstance
api_type:
- DllExport
api_location:
- Pstorec.dll
ms.openlocfilehash: ce61a0d320b34ad09f4801d4ee5b53625e61501b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358132"
---
# <a name="pstorecreateinstance-function"></a><span data-ttu-id="f0b89-103">Pstorecreatanstance-Funktion</span><span class="sxs-lookup"><span data-stu-id="f0b89-103">PStoreCreateInstance function</span></span>

<span data-ttu-id="f0b89-104">\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f0b89-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="f0b89-105">Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f0b89-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="f0b89-106">Pstore verwendet eine ältere Implementierung des Schutzes von Daten.</span><span class="sxs-lookup"><span data-stu-id="f0b89-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="f0b89-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="f0b89-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="f0b89-108">\[Diese Funktion kann in zukünftigen Versionen von Windows geändert werden oder nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="f0b89-108">\[This function may be altered or unavailable in future versions of Windows.</span></span> <span data-ttu-id="f0b89-109">Verwenden Sie anstelle dieser Funktion die Funktionen " **CryptProtectData** " und " **CryptUnprotectData** ".\]</span><span class="sxs-lookup"><span data-stu-id="f0b89-109">Use the **CryptProtectData** and **CryptUnprotectData** functions instead of this function.\]</span></span>

<span data-ttu-id="f0b89-110">Ruft einen Schnittstellen Zeiger auf einen Speicher Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="f0b89-110">Retrieves an interface pointer to a storage provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0b89-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0b89-111">Syntax</span></span>


```C++
HRESULT __stdcall PStoreCreateInstance(
  _Out_ IPStore        **ppProvider,
  _In_  PST_PROVIDERID *pProviderID,
  _In_  void           *pReserved,
  _In_  DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="f0b89-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0b89-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0b89-113">*ppprovider* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f0b89-113">*ppProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0b89-114">Ein Zeiger auf den abgerufenen Schnittstellen Zeiger für den Speicher Anbieter.</span><span class="sxs-lookup"><span data-stu-id="f0b89-114">A pointer to the retrieved interface pointer for the storage provider.</span></span> <span data-ttu-id="f0b89-115">Wenn Sie die-Schnittstelle verwenden, verringern Sie den Verweis Zähler, indem Sie die [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f0b89-115">When you finish using the interface, decrement its reference count by calling its [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method.</span></span> <span data-ttu-id="f0b89-116">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="f0b89-116">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f0b89-117">*pproviderid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0b89-117">*pProviderID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0b89-118">Ein Zeiger auf die **GUID** , die den Speicher Anbieter identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f0b89-118">A pointer to the **GUID** that identifies the storage provider.</span></span> <span data-ttu-id="f0b89-119">Wenn dieser Parameter **null** ist, wird der Basis Speicher Anbieter verwendet.</span><span class="sxs-lookup"><span data-stu-id="f0b89-119">If this parameter is **NULL**, then the base storage provider is used.</span></span>

</dd> <dt>

<span data-ttu-id="f0b89-120">*beibehalten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0b89-120">*pReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0b89-121">Bleiben muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="f0b89-121">Reserved; must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f0b89-122">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0b89-122">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0b89-123">Bleiben muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="f0b89-123">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0b89-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f0b89-124">Return value</span></span>

<span data-ttu-id="f0b89-125">Der Rückgabewert ist ein **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f0b89-125">The return value is an **HRESULT**.</span></span> <span data-ttu-id="f0b89-126">Der Wert **S \_ OK** gibt an, dass die Funktion erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="f0b89-126">A value of **S\_OK** indicates the function was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0b89-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f0b89-127">Remarks</span></span>

<span data-ttu-id="f0b89-128">Diese Funktion verfügt über keine zugeordnete Import Bibliothek. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f0b89-128">This function has no associated import library; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0b89-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0b89-129">Requirements</span></span>



| <span data-ttu-id="f0b89-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0b89-130">Requirement</span></span> | <span data-ttu-id="f0b89-131">Wert</span><span class="sxs-lookup"><span data-stu-id="f0b89-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0b89-132">Header</span><span class="sxs-lookup"><span data-stu-id="f0b89-132">Header</span></span><br/> | <dl> <span data-ttu-id="f0b89-133"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0b89-133"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="f0b89-134">DLL</span><span class="sxs-lookup"><span data-stu-id="f0b89-134">DLL</span></span><br/>    | <dl> <span data-ttu-id="f0b89-135"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0b89-135"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0b89-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0b89-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0b89-137">**CryptProtectData**</span><span class="sxs-lookup"><span data-stu-id="f0b89-137">**CryptProtectData**</span></span>](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata)
</dt> <dt>

[<span data-ttu-id="f0b89-138">**CryptUnprotectData**</span><span class="sxs-lookup"><span data-stu-id="f0b89-138">**CryptUnprotectData**</span></span>](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)
</dt> </dl>

 

 
