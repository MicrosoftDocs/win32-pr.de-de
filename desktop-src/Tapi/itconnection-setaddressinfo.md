---
description: Die setaddressinfo-Methode legt die Adressinformationen fest.
ms.assetid: 100b96af-e6ba-4496-9978-4df133e1c2b5
title: 'Itconnection:: setaddressinfo-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae181911527c22639c8c2da3038c0377734fd1da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364886"
---
# <a name="itconnectionsetaddressinfo-method"></a><span data-ttu-id="cfb8d-103">Itconnection:: setaddressinfo-Methode</span><span class="sxs-lookup"><span data-stu-id="cfb8d-103">ITConnection::SetAddressInfo method</span></span>

<span data-ttu-id="cfb8d-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cfb8d-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cfb8d-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="cfb8d-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="cfb8d-106">Die **setaddressinfo** -Methode legt die Adressinformationen fest.</span><span class="sxs-lookup"><span data-stu-id="cfb8d-106">The **SetAddressInfo** method sets the address information.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfb8d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cfb8d-107">Syntax</span></span>


```C++
HRESULT SetAddressInfo(
  [in] BSTR          pStartAddress,
  [in] LONG          NumAddresses,
  [in] unsigned char Ttl
);
```



## <a name="parameters"></a><span data-ttu-id="cfb8d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cfb8d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfb8d-109">*pStartAddress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cfb8d-109">*pStartAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfb8d-110">Zeiger auf einen **BSTR** -Wert, der die Startadresse enthält.</span><span class="sxs-lookup"><span data-stu-id="cfb8d-110">Pointer to a **BSTR** containing the start address.</span></span>

</dd> <dt>

<span data-ttu-id="cfb8d-111">*Numadkleider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cfb8d-111">*NumAddresses* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfb8d-112">Anzahl der Adressen, die für die Sitzung verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cfb8d-112">Number of addresses to be used for the session.</span></span>

</dd> <dt>

<span data-ttu-id="cfb8d-113">Gültigkeitsdauer  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cfb8d-113">*Ttl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfb8d-114">Gültigkeitsbereich der Gültigkeits [*Dauer*](t-tapgloss.md) (TTL) für Übertragungen der Adressen.</span><span class="sxs-lookup"><span data-stu-id="cfb8d-114">[*time to live*](t-tapgloss.md) (TTL) scope for transmissions on the addresses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfb8d-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cfb8d-115">Return value</span></span>

<span data-ttu-id="cfb8d-116">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="cfb8d-116">This method can return one of these values.</span></span>



| <span data-ttu-id="cfb8d-117">Wert</span><span class="sxs-lookup"><span data-stu-id="cfb8d-117">Value</span></span>                                                                                         | <span data-ttu-id="cfb8d-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cfb8d-118">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cfb8d-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cfb8d-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="cfb8d-120">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="cfb8d-120">Method succeeded.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="cfb8d-121"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="cfb8d-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="cfb8d-122">Der Parameter " *pStartAddress*", " *numadkleidungs*" oder " *TTL* " ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="cfb8d-122">The *pStartAddress*, *NumAddresses*, or *Ttl* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="cfb8d-123"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="cfb8d-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="cfb8d-124">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="cfb8d-124">Insufficient memory exists to perform the operation.</span></span><br/>                  |
| <dl> <span data-ttu-id="cfb8d-125"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="cfb8d-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="cfb8d-126">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="cfb8d-126">Unspecified error.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="cfb8d-127"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="cfb8d-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="cfb8d-128">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="cfb8d-128">This method is not yet implemented.</span></span><br/>                                   |



 

## <a name="remarks"></a><span data-ttu-id="cfb8d-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cfb8d-129">Remarks</span></span>

<span data-ttu-id="cfb8d-130">Die Anwendung muss " [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) " verwenden, um Speicher für den *pStartAddress* -Parameter zuzuweisen, und " [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) " verwenden, um den Arbeitsspeicher freizugeben, wenn die Variable nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="cfb8d-130">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pStartAddress* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfb8d-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cfb8d-131">Requirements</span></span>



| <span data-ttu-id="cfb8d-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cfb8d-132">Requirement</span></span> | <span data-ttu-id="cfb8d-133">Wert</span><span class="sxs-lookup"><span data-stu-id="cfb8d-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cfb8d-134">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="cfb8d-134">TAPI version</span></span><br/> | <span data-ttu-id="cfb8d-135">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="cfb8d-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="cfb8d-136">Header</span><span class="sxs-lookup"><span data-stu-id="cfb8d-136">Header</span></span><br/>       | <dl> <span data-ttu-id="cfb8d-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfb8d-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="cfb8d-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cfb8d-138">Library</span></span><br/>      | <dl> <span data-ttu-id="cfb8d-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cfb8d-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="cfb8d-140">DLL</span><span class="sxs-lookup"><span data-stu-id="cfb8d-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="cfb8d-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfb8d-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfb8d-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cfb8d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfb8d-143">**Itconnection**</span><span class="sxs-lookup"><span data-stu-id="cfb8d-143">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

