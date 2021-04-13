---
title: Inapsohprocessor getnumofattributes-Methode (napprotocol. h)
description: Ruft die Gesamtanzahl der Attribute im SoH ab.
ms.assetid: ee0b1857-65a7-47bb-ae91-c939344a24d0
keywords:
- Getnumofattributes-Methode NAP
- Getnumofattributes-Methode NAP, inapsohprocessor-Schnittstelle
- Inapsohprocessor-Schnittstelle NAP, getnumofattributes-Methode
topic_type:
- apiref
api_name:
- INapSoHProcessor.GetNumberOfAttributes
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f1336362b44d49c71ce81b197f9f95b1a1b8fc9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517771"
---
# <a name="inapsohprocessorgetnumberofattributes-method"></a><span data-ttu-id="871d7-106">Inapsohprocessor:: getzahlofattributes-Methode</span><span class="sxs-lookup"><span data-stu-id="871d7-106">INapSoHProcessor::GetNumberOfAttributes method</span></span>

> [!Note]  
> <span data-ttu-id="871d7-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="871d7-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="871d7-108">Die **inapsohprocessor:: getzahlofattributes** -Methode ruft die Gesamtanzahl der Attribute im SoH ab.</span><span class="sxs-lookup"><span data-stu-id="871d7-108">The **INapSoHProcessor::GetNumberOfAttributes** method retrieves the total number of attributes in the SoH.</span></span>

## <a name="syntax"></a><span data-ttu-id="871d7-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="871d7-109">Syntax</span></span>


```C++
HRESULT GetNumberOfAttributes(
  [out] UINT16 *attributeCount
);
```



## <a name="parameters"></a><span data-ttu-id="871d7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="871d7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="871d7-111">*AttributeCount* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="871d7-111">*attributeCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="871d7-112">Ein Zeiger auf die zurückgegebene Attribut Anzahl.</span><span class="sxs-lookup"><span data-stu-id="871d7-112">A pointer to the returned attribute count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="871d7-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="871d7-113">Return value</span></span>

<span data-ttu-id="871d7-114">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="871d7-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="871d7-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="871d7-115">Return code</span></span>                                                                                     | <span data-ttu-id="871d7-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="871d7-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="871d7-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="871d7-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="871d7-118">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="871d7-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="871d7-119"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="871d7-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="871d7-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="871d7-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="871d7-121"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="871d7-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="871d7-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="871d7-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="871d7-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="871d7-123">Requirements</span></span>



| <span data-ttu-id="871d7-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="871d7-124">Requirement</span></span> | <span data-ttu-id="871d7-125">Wert</span><span class="sxs-lookup"><span data-stu-id="871d7-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="871d7-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="871d7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="871d7-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="871d7-127">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="871d7-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="871d7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="871d7-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="871d7-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="871d7-130">Header</span><span class="sxs-lookup"><span data-stu-id="871d7-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="871d7-131"><dt>Napprotocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="871d7-131"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="871d7-132">IDL</span><span class="sxs-lookup"><span data-stu-id="871d7-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="871d7-133"><dt>Napprotocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="871d7-133"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="871d7-134">DLL</span><span class="sxs-lookup"><span data-stu-id="871d7-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="871d7-135"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="871d7-135"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="871d7-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="871d7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="871d7-137">**Inapsohprocessor**</span><span class="sxs-lookup"><span data-stu-id="871d7-137">**INapSoHProcessor**</span></span>](inapsohprocessor.md)
</dt> </dl>

 

 





