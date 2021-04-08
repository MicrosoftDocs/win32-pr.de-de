---
title: Inapsohprocessor findnextattribute-Methode (napprotocol. h)
description: Sucht den Speicherort (Index) des nächsten Attributs des Typs, der von sohattributetype angegeben wird.
ms.assetid: 0ff94a32-ece8-4a89-9ee9-93c5e14dfb6c
keywords:
- Findnextattribute-Methode NAP
- Findnextattribute-Methode NAP, inapsohprocessor-Schnittstelle
- Inapsohprocessor-Schnittstelle NAP, findnextattribute-Methode
topic_type:
- apiref
api_name:
- INapSoHProcessor.FindNextAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1a270e36f8254ed5dbfcd9776cf013f9d10d4a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740224"
---
# <a name="inapsohprocessorfindnextattribute-method"></a><span data-ttu-id="f3f35-106">Inapsohprocessor:: findnextattribute-Methode</span><span class="sxs-lookup"><span data-stu-id="f3f35-106">INapSoHProcessor::FindNextAttribute method</span></span>

> [!Note]  
> <span data-ttu-id="f3f35-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f3f35-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f3f35-108">Die **inapsohprocessor:: findnextattribute** -Methode sucht den Speicherort (Index) des nächsten Attributs des Typs, der von *sohattributetype* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f3f35-108">The **INapSoHProcessor::FindNextAttribute** method finds the location (index) of the next attribute of the type indicated by *SoHAttributeType*.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3f35-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3f35-109">Syntax</span></span>


```C++
HRESULT FindNextAttribute(
  [in]  UINT16           fromLocation,
  [in]  SoHAttributeType type,
  [out] UINT16           *attributeLocation
);
```



## <a name="parameters"></a><span data-ttu-id="f3f35-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3f35-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3f35-111">*fromlocation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3f35-111">*fromLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3f35-112">Der Start Speicherort (Index) im SoH-Paket (Statement of Health) zum Starten der Attribut Suche.</span><span class="sxs-lookup"><span data-stu-id="f3f35-112">The starting location (index) in the Statement of Health (SoH) packet to begin the attribute search.</span></span> <span data-ttu-id="f3f35-113">Dieser Wert muss zwischen 0 und (**numatdreib** -1) liegen, wobei **numatdreib** mit [**inapsohprocessor:: getnumofattributes**](inapsohprocessor-getnumberofattributes-method.md)abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f3f35-113">This value must be in the range of 0 to (**numAttrib** - 1) where **numAttrib** is retrieved using [**INapSoHProcessor::GetNumberOfAttributes**](inapsohprocessor-getnumberofattributes-method.md).</span></span>

> [!Note]  
> <span data-ttu-id="f3f35-114">Das SoH-Paket verwendet 0-basierte Attribut Indizes.</span><span class="sxs-lookup"><span data-stu-id="f3f35-114">The SoH packet uses 0-based attribute indices.</span></span>

 

</dd> <dt>

<span data-ttu-id="f3f35-115">*Typ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3f35-115">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3f35-116">Eine [**sohattributetype**](sohattributetype-enum.md) -Struktur, die den zu suchenden Attributtyp enthält.</span><span class="sxs-lookup"><span data-stu-id="f3f35-116">An [**SoHAttributeType**](sohattributetype-enum.md) structure that contains the attribute type to locate.</span></span>

</dd> <dt>

<span data-ttu-id="f3f35-117">*attributelokation* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f3f35-117">*attributeLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3f35-118">Ein Zeiger, der den Speicherort (Index) im SoH-Paket des ersten Attributs vom Typ *sohattributetype* aus dem Index *fromlocation* enthält.</span><span class="sxs-lookup"><span data-stu-id="f3f35-118">A pointer that contains the location (index) in the SoH packet of the first attribute of type *SoHAttributeType* from the index *fromLocation*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3f35-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f3f35-119">Return value</span></span>

<span data-ttu-id="f3f35-120">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f3f35-120">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="f3f35-121">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f3f35-121">Return code</span></span>                                                                                            | <span data-ttu-id="f3f35-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3f35-122">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="f3f35-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f3f35-123"><dt>**S\_OK** </dt></span></span> </dl>                  | <span data-ttu-id="f3f35-124">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f3f35-124">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f3f35-125"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="f3f35-125"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>        | <span data-ttu-id="f3f35-126">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="f3f35-126">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="f3f35-127"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="f3f35-127"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>         | <span data-ttu-id="f3f35-128">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f3f35-128">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="f3f35-129"><dt>**Fehler \_ Datei \_ nicht \_ gefunden.**</dt></span><span class="sxs-lookup"><span data-stu-id="f3f35-129"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="f3f35-130">Das Attribut wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="f3f35-130">Attribute not found.</span></span><br/>                                    |



 

## <a name="remarks"></a><span data-ttu-id="f3f35-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f3f35-131">Remarks</span></span>

<span data-ttu-id="f3f35-132">Die **findnextattribute** -Methode sucht nach Attributen vom Typ *sohattributetype* aus dem von *fromlocation* angegebenen Index und höher, bis eine Entsprechung gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="f3f35-132">The **FindNextAttribute** method searches for attributes of type *SoHAttributeType* from the index specified by *fromLocation* and higher until a match is found.</span></span> <span data-ttu-id="f3f35-133">Wenn keine Entsprechung gefunden wird, wird die **Fehler \_ Datei \_ nicht \_ gefunden** .</span><span class="sxs-lookup"><span data-stu-id="f3f35-133">If no match is found, **ERROR\_FILE\_NOT\_FOUND** is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3f35-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f3f35-134">Requirements</span></span>



| <span data-ttu-id="f3f35-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f3f35-135">Requirement</span></span> | <span data-ttu-id="f3f35-136">Wert</span><span class="sxs-lookup"><span data-stu-id="f3f35-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3f35-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f3f35-137">Minimum supported client</span></span><br/> | <span data-ttu-id="f3f35-138">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f3f35-138">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f3f35-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f3f35-139">Minimum supported server</span></span><br/> | <span data-ttu-id="f3f35-140">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f3f35-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="f3f35-141">Header</span><span class="sxs-lookup"><span data-stu-id="f3f35-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3f35-142"><dt>Napprotocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3f35-142"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="f3f35-143">IDL</span><span class="sxs-lookup"><span data-stu-id="f3f35-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f3f35-144"><dt>Napprotocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f3f35-144"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="f3f35-145">DLL</span><span class="sxs-lookup"><span data-stu-id="f3f35-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3f35-146"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3f35-146"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="f3f35-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3f35-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3f35-148">**Inapsohprocessor**</span><span class="sxs-lookup"><span data-stu-id="f3f35-148">**INapSoHProcessor**</span></span>](inapsohprocessor.md)
</dt> </dl>

 

 





