---
title: Inapsohprocessor GetAttribute-Methode (napprotocol. h)
description: Ruft den Attributtyp und-Wert ab, wenn der Attribut Speicherort angegeben ist.
ms.assetid: 0d7bc655-428b-4a31-b03f-445e80a6d194
keywords:
- GetAttribute-Methode NAP
- GetAttribute-Methode NAP, inapsohprocessor-Schnittstelle
- Inapsohprocessor-Schnittstelle NAP, GetAttribute-Methode
topic_type:
- apiref
api_name:
- INapSoHProcessor.GetAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed2d7d9cbafa5a44e0f6c24f4c42959c456722a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340765"
---
# <a name="inapsohprocessorgetattribute-method"></a><span data-ttu-id="dfa32-106">Inapsohprocessor:: GetAttribute-Methode</span><span class="sxs-lookup"><span data-stu-id="dfa32-106">INapSoHProcessor::GetAttribute method</span></span>

> [!Note]  
> <span data-ttu-id="dfa32-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dfa32-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="dfa32-108">Die **inapsohprocessor:: GetAttribute** -Methode ruft den Attributtyp und-Wert ab, wenn der Speicherort des Attributs angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="dfa32-108">The **INapSoHProcessor::GetAttribute** method retrieves the attribute type and value, given the attribute location.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfa32-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="dfa32-109">Syntax</span></span>


```C++
HRESULT GetAttribute(
  [in]  UINT16            attributeLocation,
  [out] SoHAttributeType  *type,
  [out] SoHAttributeValue **value
);
```



## <a name="parameters"></a><span data-ttu-id="dfa32-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="dfa32-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfa32-111">*attributelokation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfa32-111">*attributeLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa32-112">Der Speicherort (Index) des Attributs, dessen Typ und Wert abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dfa32-112">The location (index) of the attribute whose type and value are to be retrieved.</span></span> <span data-ttu-id="dfa32-113">Der Wert von *attributelokation* wird von einem vorherigen [**inapsohprocessor:: findnextattribute**](inapsohprocessor-findnextattribute-method.md)-Rückruf zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dfa32-113">The value of *attributeLocation* is returned from a prior call to [**INapSoHProcessor::FindNextAttribute**](inapsohprocessor-findnextattribute-method.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfa32-114">*Typ* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dfa32-114">*type* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa32-115">Ein Zeiger auf eine [**sohattributetype**](sohattributetype-enum.md) -Struktur, die den Typ des Attributs im *Wert* angibt.</span><span class="sxs-lookup"><span data-stu-id="dfa32-115">A pointer to an [**SoHAttributeType**](sohattributetype-enum.md) structure that specifies the attribute's type in *value*.</span></span>

</dd> <dt>

<span data-ttu-id="dfa32-116">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dfa32-116">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa32-117">Ein Zeiger auf einen Zeiger auf eine [**sohattributevalue**](sohattributevalue-union.md) -Struktur, die den Wert des Attributs gemäß der Definition durch den *Typ* enthält.</span><span class="sxs-lookup"><span data-stu-id="dfa32-117">A pointer to a pointer to a [**SoHAttributeValue**](sohattributevalue-union.md) structure that contains the attribute's value as defined by *type*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfa32-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dfa32-118">Return value</span></span>

<span data-ttu-id="dfa32-119">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="dfa32-119">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="dfa32-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="dfa32-120">Return code</span></span>                                                                                     | <span data-ttu-id="dfa32-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dfa32-121">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="dfa32-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dfa32-122"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="dfa32-123">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="dfa32-123">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="dfa32-124"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="dfa32-124"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="dfa32-125">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="dfa32-125">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="dfa32-126"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="dfa32-126"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="dfa32-127">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="dfa32-127">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="dfa32-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dfa32-128">Requirements</span></span>



| <span data-ttu-id="dfa32-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dfa32-129">Requirement</span></span> | <span data-ttu-id="dfa32-130">Wert</span><span class="sxs-lookup"><span data-stu-id="dfa32-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfa32-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dfa32-131">Minimum supported client</span></span><br/> | <span data-ttu-id="dfa32-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dfa32-132">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="dfa32-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dfa32-133">Minimum supported server</span></span><br/> | <span data-ttu-id="dfa32-134">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dfa32-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="dfa32-135">Header</span><span class="sxs-lookup"><span data-stu-id="dfa32-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfa32-136"><dt>Napprotocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfa32-136"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="dfa32-137">IDL</span><span class="sxs-lookup"><span data-stu-id="dfa32-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dfa32-138"><dt>Napprotocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dfa32-138"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="dfa32-139">DLL</span><span class="sxs-lookup"><span data-stu-id="dfa32-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfa32-140"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfa32-140"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="dfa32-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dfa32-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfa32-142">**Inapsohprocessor**</span><span class="sxs-lookup"><span data-stu-id="dfa32-142">**INapSoHProcessor**</span></span>](inapsohprocessor.md)
</dt> </dl>

 

 





