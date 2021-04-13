---
title: Inapcomponentconfig GetConfig-Methode (napcommon. h)
description: Ruft die Konfiguration der System Integritätsprüfung (SHV) ab.
ms.assetid: 57a1d3a7-05c0-4e0f-91b8-b3cf8982d04f
keywords:
- GetConfig-Methode NAP
- GetConfig-Methode NAP, inapcomponentconfig-Schnittstelle
- Inapcomponentconfig-Schnittstelle NAP, GetConfig-Methode
topic_type:
- apiref
api_name:
- INapComponentConfig.GetConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3e07465d768c8902166150e53d4200e775e2597
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478444"
---
# <a name="inapcomponentconfiggetconfig-method"></a><span data-ttu-id="6777a-106">Inapcomponentconfig:: GetConfig-Methode</span><span class="sxs-lookup"><span data-stu-id="6777a-106">INapComponentConfig::GetConfig method</span></span>

> [!Note]  
> <span data-ttu-id="6777a-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6777a-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="6777a-108">Die **GetConfig** -Methode ruft die Konfiguration der Systemintegritätsprüfungs-Komponente (SHV) ab.</span><span class="sxs-lookup"><span data-stu-id="6777a-108">The **GetConfig** method retrieves the system health validator (SHV) component configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="6777a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6777a-109">Syntax</span></span>


```C++
HRESULT GetConfig(
  [out] UINT16 *bCount,
  [out] BYTE   **data
) const;
```



## <a name="parameters"></a><span data-ttu-id="6777a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6777a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6777a-111">*BCOUNT* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6777a-111">*bCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6777a-112">Die Größe des *Daten* konfigurationsblobs in Byte.</span><span class="sxs-lookup"><span data-stu-id="6777a-112">The size, in bytes, of the *data* configuration blob.</span></span>

</dd> <dt>

<span data-ttu-id="6777a-113">*Daten* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6777a-113">*data* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6777a-114">Ein Zeiger auf die Adresse der Konfigurationsdaten der SHV-Komponente.</span><span class="sxs-lookup"><span data-stu-id="6777a-114">A pointer to the address of the SHV component configuration data.</span></span>

> [!Note]  
> <span data-ttu-id="6777a-115">Konfigurationsdaten, die mithilfe der **GetConfig** -Methode von einem x86-Computer exportiert werden, können mithilfe der [**setconfig**](inapcomponentconfig-setconfig.md) -Methode auf einen x64-Computer importiert werden und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="6777a-115">Configuration data exported from an x86 machine using the **GetConfig** method may be imported onto an x64 machine using the [**SetConfig**](inapcomponentconfig-setconfig.md) method, and vice versa.</span></span> <span data-ttu-id="6777a-116">Daher müssen Konfigurationsdaten in einem Architektur agnostischen Format wie XML vorliegen.</span><span class="sxs-lookup"><span data-stu-id="6777a-116">Therefore, configuration data must be in an architecture-agnostic format such as XML.</span></span> <span data-ttu-id="6777a-117">Durch die Verwendung von XML anstelle eines Bytestreams wird die Verwendung von Konfigurationsdaten auf verschiedenen Architekturen vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="6777a-117">Using XML instead of a byte stream makes it easier to use configuration data on different architectures.</span></span> <span data-ttu-id="6777a-118">Die XML-Elemente, die in den Konfigurationsdaten verwendet werden, werden durch den Implementierer bestimmt.</span><span class="sxs-lookup"><span data-stu-id="6777a-118">The XML elements used in the configuration data are determined by the implementer.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6777a-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6777a-119">Return value</span></span>

<span data-ttu-id="6777a-120">Gibt basierend auf dem Ergebnis dieses Vorgangs einen der folgenden Fehlercodes zurück.</span><span class="sxs-lookup"><span data-stu-id="6777a-120">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="6777a-121">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6777a-121">Return code</span></span>                                                                                     | <span data-ttu-id="6777a-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6777a-122">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="6777a-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6777a-123"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="6777a-124">Der Vorgang ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="6777a-124">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="6777a-125"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="6777a-125"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="6777a-126">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="6777a-126">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="6777a-127"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="6777a-127"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="6777a-128">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6777a-128">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6777a-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6777a-129">Remarks</span></span>

<span data-ttu-id="6777a-130">Der Data-Parameter muss vom aufgerufenen (komponentenimplementierer) mithilfe von **cotaskmemzuzugeordneten** zugewiesen und durch den Aufrufer mithilfe von " **CoTaskMemFree**" freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6777a-130">The data parameter must be allocated by the callee (component implementor) using **CoTaskMemAlloc** and freed by the caller using **CoTaskMemFree**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6777a-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6777a-131">Requirements</span></span>



| <span data-ttu-id="6777a-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6777a-132">Requirement</span></span> | <span data-ttu-id="6777a-133">Wert</span><span class="sxs-lookup"><span data-stu-id="6777a-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6777a-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6777a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6777a-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6777a-135">None supported</span></span><br/>                                                                |
| <span data-ttu-id="6777a-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6777a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6777a-137">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6777a-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6777a-138">Header</span><span class="sxs-lookup"><span data-stu-id="6777a-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="6777a-139"><dt>Napcommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6777a-139"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="6777a-140">IDL</span><span class="sxs-lookup"><span data-stu-id="6777a-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6777a-141"><dt>Napcommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6777a-141"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6777a-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6777a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6777a-143">**Inapcomponentconfig**</span><span class="sxs-lookup"><span data-stu-id="6777a-143">**INapComponentConfig**</span></span>](inapcomponentconfig.md)
</dt> <dt>

[<span data-ttu-id="6777a-144">**Inapcomponentconfig:: setconfig**</span><span class="sxs-lookup"><span data-stu-id="6777a-144">**INapComponentConfig::SetConfig**</span></span>](inapcomponentconfig-setconfig.md)
</dt> </dl>

 

 





