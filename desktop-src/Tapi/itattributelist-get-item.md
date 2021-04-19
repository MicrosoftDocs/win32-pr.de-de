---
description: Die get \_ Item-Methode gibt das vom Index angegebene Attribut zurück.
ms.assetid: 67e36587-0bf5-4586-ace9-ef107f0b6548
title: 'Itattributelist:: get_Item-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33745c10bf95fe8a1e9c6d9edc73cad54855a8c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367805"
---
# <a name="itattributelistget_item-method"></a><span data-ttu-id="d258a-103">Itattributelist:: get \_ Item-Methode</span><span class="sxs-lookup"><span data-stu-id="d258a-103">ITAttributeList::get\_Item method</span></span>

<span data-ttu-id="d258a-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d258a-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d258a-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="d258a-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="d258a-106">Die **get \_ Item** -Methode gibt das vom Index angegebene Attribut zurück.</span><span class="sxs-lookup"><span data-stu-id="d258a-106">The **get\_Item** method returns the attribute specified by the index.</span></span>

## <a name="syntax"></a><span data-ttu-id="d258a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d258a-107">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]  LONG Index,
  [out] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="d258a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d258a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d258a-109">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d258a-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d258a-110">Der Index des zu entzurufenden Elements.</span><span class="sxs-lookup"><span data-stu-id="d258a-110">Index of the item to get.</span></span>

</dd> <dt>

<span data-ttu-id="d258a-111">*PVal* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d258a-111">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d258a-112">Zeiger auf einen **BSTR** -Wert, der die Werte des Elements enthält.</span><span class="sxs-lookup"><span data-stu-id="d258a-112">Pointer to a **BSTR** containing the values of the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d258a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d258a-113">Return value</span></span>

<span data-ttu-id="d258a-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="d258a-114">This method can return one of these values.</span></span>



| <span data-ttu-id="d258a-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d258a-115">Return code</span></span>                                                                                   | <span data-ttu-id="d258a-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d258a-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="d258a-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d258a-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d258a-118">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="d258a-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="d258a-119"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="d258a-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d258a-120">Der *PVal* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="d258a-120">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="d258a-121"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="d258a-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d258a-122">Der *Index* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="d258a-122">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="d258a-123"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="d258a-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d258a-124">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d258a-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="d258a-125"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="d258a-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="d258a-126">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="d258a-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="d258a-127"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="d258a-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="d258a-128">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="d258a-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="d258a-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d258a-129">Remarks</span></span>

<span data-ttu-id="d258a-130">Die Anwendung muss [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den für den *PVal* -Parameter zugeordneten Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="d258a-130">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *pVal* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="d258a-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d258a-131">Requirements</span></span>



| <span data-ttu-id="d258a-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d258a-132">Requirement</span></span> | <span data-ttu-id="d258a-133">Wert</span><span class="sxs-lookup"><span data-stu-id="d258a-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d258a-134">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="d258a-134">TAPI version</span></span><br/> | <span data-ttu-id="d258a-135">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="d258a-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="d258a-136">Header</span><span class="sxs-lookup"><span data-stu-id="d258a-136">Header</span></span><br/>       | <dl> <span data-ttu-id="d258a-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="d258a-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="d258a-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d258a-138">Library</span></span><br/>      | <dl> <span data-ttu-id="d258a-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d258a-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="d258a-140">DLL</span><span class="sxs-lookup"><span data-stu-id="d258a-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="d258a-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d258a-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d258a-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d258a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d258a-143">**Itattributelist**</span><span class="sxs-lookup"><span data-stu-id="d258a-143">**ITAttributeList**</span></span>](itattributelist.md)
</dt> </dl>

 

