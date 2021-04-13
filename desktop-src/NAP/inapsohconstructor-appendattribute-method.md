---
title: Inapsohconstructor appendattribute-Methode (napprotocol. h)
description: Fügt ein TLV am Ende des SoH-Puffers hinzu.
ms.assetid: 5706ceaa-757f-49d2-90e0-011415853875
keywords:
- Appendattribute-Methode NAP
- Appendattribute-Methode NAP, inapsohconstructor-Schnittstelle
- Inapsohconstructor Interface NAP, appendattribute-Methode
topic_type:
- apiref
api_name:
- INapSoHConstructor.AppendAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc10fad9c775d324822700b77afed4e65a798db6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517708"
---
# <a name="inapsohconstructorappendattribute-method"></a><span data-ttu-id="42e06-106">Inapsohconstructor:: appendattribute-Methode</span><span class="sxs-lookup"><span data-stu-id="42e06-106">INapSoHConstructor::AppendAttribute method</span></span>

> [!Note]  
> <span data-ttu-id="42e06-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="42e06-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="42e06-108">Die **inapsohconstructor:: appendattribute** -Methode fügt ein TLV am Ende des SoH-Puffers hinzu.</span><span class="sxs-lookup"><span data-stu-id="42e06-108">The **INapSoHConstructor::AppendAttribute** method adds a TLV to the end of the SoH buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="42e06-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="42e06-109">Syntax</span></span>


```C++
HRESULT AppendAttribute(
  [in]       SoHAttributeType  type,
  [in] const SoHAttributeValue *value
);
```



## <a name="parameters"></a><span data-ttu-id="42e06-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="42e06-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42e06-111">*Typ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42e06-111">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42e06-112">Eine [**sohattributetype**](sohattributetype-enum.md) -Enumeration, die den Attributtyp des neuen TLV angibt.</span><span class="sxs-lookup"><span data-stu-id="42e06-112">A [**SoHAttributeType**](sohattributetype-enum.md) enumeration that indicates the attribute type of the new TLV.</span></span>

</dd> <dt>

<span data-ttu-id="42e06-113">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42e06-113">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42e06-114">Ein Zeiger auf eine [**sohattributevalue**](sohattributevalue-union.md) -Struktur, die den Wert für das neue TLV enthält.</span><span class="sxs-lookup"><span data-stu-id="42e06-114">A pointer to an [**SoHAttributeValue**](sohattributevalue-union.md) structure that contains the value for the new TLV.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42e06-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="42e06-115">Return value</span></span>

<span data-ttu-id="42e06-116">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="42e06-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="42e06-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="42e06-117">Return code</span></span>                                                                                     | <span data-ttu-id="42e06-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42e06-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="42e06-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="42e06-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="42e06-120">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="42e06-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="42e06-121"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="42e06-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="42e06-122">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="42e06-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="42e06-123"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="42e06-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="42e06-124">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="42e06-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="42e06-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42e06-125">Remarks</span></span>

<span data-ttu-id="42e06-126">Der TLV " [**sohattributetypesystemhealthid**](sohattributetype-enum.md) " darf nicht mit dieser Funktion hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="42e06-126">The [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md) TLV must not be added using this function.</span></span> <span data-ttu-id="42e06-127">Es wird als erstes TLV von [**inapsohconstructor:: Initialize**](inapsohconstructor-initialize-method.md) zu neu erstellten SoH-Paketen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="42e06-127">It is added as the first TLV by [**INapSoHConstructor::Initialize**](inapsohconstructor-initialize-method.md) to newly constructed SOH packets.</span></span>

<span data-ttu-id="42e06-128">Wenn ein Attribut angehängt wird, das vom NAP-System genutzt wird, sollte es nicht verschlüsselt oder geändert werden.</span><span class="sxs-lookup"><span data-stu-id="42e06-128">When appending an attribute which will be consumed by the Nap System, it should not be encrypted or modified in any manner.</span></span> <span data-ttu-id="42e06-129">Wenn die Integritäts Entität eine Verschlüsselung/Integritäts Überprüfung (Macs) privater Informationen erfordert, sollte Sie nur in das [**sohattributetypevendorspecific**](sohattributetype-enum.md) -Attribut eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="42e06-129">If the HealthEntity requires encryption/integrity checking (MACs) of private information, it should be included only in the [**sohAttributeTypeVendorSpecific**](sohattributetype-enum.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="42e06-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42e06-130">Requirements</span></span>



| <span data-ttu-id="42e06-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="42e06-131">Requirement</span></span> | <span data-ttu-id="42e06-132">Wert</span><span class="sxs-lookup"><span data-stu-id="42e06-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="42e06-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="42e06-133">Minimum supported client</span></span><br/> | <span data-ttu-id="42e06-134">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42e06-134">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="42e06-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="42e06-135">Minimum supported server</span></span><br/> | <span data-ttu-id="42e06-136">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42e06-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="42e06-137">Header</span><span class="sxs-lookup"><span data-stu-id="42e06-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="42e06-138"><dt>Napprotocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="42e06-138"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="42e06-139">IDL</span><span class="sxs-lookup"><span data-stu-id="42e06-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="42e06-140"><dt>Napprotocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="42e06-140"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="42e06-141">DLL</span><span class="sxs-lookup"><span data-stu-id="42e06-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42e06-142"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42e06-142"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="42e06-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42e06-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42e06-144">**Inapsohconstructor**</span><span class="sxs-lookup"><span data-stu-id="42e06-144">**INapSoHConstructor**</span></span>](inapsohconstructor.md)
</dt> </dl>

 

 





