---
description: Die Add-Methode fügt das Attribut am angegebenen Index hinzu.
ms.assetid: 5b74c177-bf5c-4547-bebb-034a9a10be13
title: 'Itattributelist:: Add-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5504a216549231aca82eac3b3311ae7208eb8432
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367843"
---
# <a name="itattributelistadd-method"></a><span data-ttu-id="b4bb6-103">Itattributelist:: Add-Methode</span><span class="sxs-lookup"><span data-stu-id="b4bb6-103">ITAttributeList::Add method</span></span>

<span data-ttu-id="b4bb6-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b4bb6-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="b4bb6-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b4bb6-106">Die **Add** -Methode fügt das Attribut am angegebenen Index hinzu.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-106">The **Add** method adds the attribute at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4bb6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4bb6-107">Syntax</span></span>


```C++
HRESULT Add(
  [in] LONG Index,
  [in] BSTR pAttribute
);
```



## <a name="parameters"></a><span data-ttu-id="b4bb6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4bb6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4bb6-109">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b4bb6-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4bb6-110">Der Index des hinzu zufügenden Attributs.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-110">Index of the attribute to add.</span></span>

</dd> <dt>

<span data-ttu-id="b4bb6-111">*pattribute* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b4bb6-111">*pAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4bb6-112">Zeiger auf einen **BSTR** -Wert, der den Wert des hinzu zufügenden Attributs enthält.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-112">Pointer to a **BSTR** containing the value of the attribute to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4bb6-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b4bb6-113">Return value</span></span>

<span data-ttu-id="b4bb6-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-114">This method can return one of these values.</span></span>



| <span data-ttu-id="b4bb6-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b4bb6-115">Return code</span></span>                                                                                   | <span data-ttu-id="b4bb6-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b4bb6-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="b4bb6-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b4bb6-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b4bb6-118">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b4bb6-119"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="b4bb6-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b4bb6-120">Der *Index* -oder der *pattribute* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-120">The *Index* or *pAttribute* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="b4bb6-121"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="b4bb6-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b4bb6-122">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="b4bb6-123"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="b4bb6-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="b4bb6-124">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="b4bb6-125"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="b4bb6-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="b4bb6-126">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="b4bb6-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4bb6-127">Remarks</span></span>

<span data-ttu-id="b4bb6-128">Die Anwendung muss " [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) " verwenden, um Speicher für den *pattribute* -Parameter zuzuweisen, und " [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) " verwenden, um den Arbeitsspeicher freizugeben, wenn die Variable nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="b4bb6-128">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pAttribute* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4bb6-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4bb6-129">Requirements</span></span>



| <span data-ttu-id="b4bb6-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b4bb6-130">Requirement</span></span> | <span data-ttu-id="b4bb6-131">Wert</span><span class="sxs-lookup"><span data-stu-id="b4bb6-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b4bb6-132">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="b4bb6-132">TAPI version</span></span><br/> | <span data-ttu-id="b4bb6-133">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="b4bb6-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="b4bb6-134">Header</span><span class="sxs-lookup"><span data-stu-id="b4bb6-134">Header</span></span><br/>       | <dl> <span data-ttu-id="b4bb6-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4bb6-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="b4bb6-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b4bb6-136">Library</span></span><br/>      | <dl> <span data-ttu-id="b4bb6-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4bb6-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="b4bb6-138">DLL</span><span class="sxs-lookup"><span data-stu-id="b4bb6-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="b4bb6-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4bb6-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4bb6-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4bb6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4bb6-141">**Itattributelist**</span><span class="sxs-lookup"><span data-stu-id="b4bb6-141">**ITAttributeList**</span></span>](itattributelist.md)
</dt> </dl>

 

