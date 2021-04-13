---
title: Inapcomponentconfig-setconfig-Methode (napcommon. h)
description: Legt die Konfiguration der Systemintegritätsprüfungs-Komponente (SHV) fest.
ms.assetid: ec27e30b-4205-40bc-a24b-61072a746e53
keywords:
- Setconfig-Methode NAP
- Setconfig-Methode NAP, inapcomponentconfig-Schnittstelle
- Inapcomponentconfig-Schnittstelle NAP, setconfig-Methode
topic_type:
- apiref
api_name:
- INapComponentConfig.SetConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1f3d557517ec27f9537a7cbcd46be9e2cd107e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519284"
---
# <a name="inapcomponentconfigsetconfig-method"></a><span data-ttu-id="466f8-106">Inapcomponentconfig:: setconfig-Methode</span><span class="sxs-lookup"><span data-stu-id="466f8-106">INapComponentConfig::SetConfig method</span></span>

> [!Note]  
> <span data-ttu-id="466f8-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="466f8-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="466f8-108">Die **setconfig** -Methode legt die Konfiguration der Systemintegritätsprüfungs-Komponente (SHV) fest.</span><span class="sxs-lookup"><span data-stu-id="466f8-108">The **SetConfig** method sets the system health validator (SHV) component configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="466f8-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="466f8-109">Syntax</span></span>


```C++
HRESULT SetConfig(
  [in] UINT16 bCount,
  [in] BYTE   *data
);
```



## <a name="parameters"></a><span data-ttu-id="466f8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="466f8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="466f8-111">*BCOUNT* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="466f8-111">*bCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="466f8-112">Die Größe des *Daten* konfigurationsblobs in Byte.</span><span class="sxs-lookup"><span data-stu-id="466f8-112">The size, in bytes, of the *data* configuration blob.</span></span>

</dd> <dt>

<span data-ttu-id="466f8-113">*Daten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="466f8-113">*data* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="466f8-114">Ein Zeiger auf die Konfigurationsdaten der SHV-Komponente.</span><span class="sxs-lookup"><span data-stu-id="466f8-114">A pointer to the SHV component configuration data.</span></span>

> [!Note]  
> <span data-ttu-id="466f8-115">Konfigurationsdaten, die mithilfe der [**GetConfig**](inapcomponentconfig-getconfig.md) -Methode von einem x86-Computer exportiert werden, können mithilfe der **setconfig** -Methode auf einen x64-Computer importiert werden und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="466f8-115">Configuration data exported from an x86 machine using the [**GetConfig**](inapcomponentconfig-getconfig.md) method may be imported onto an x64 machine using the **SetConfig** method, and vice versa.</span></span> <span data-ttu-id="466f8-116">Daher müssen Konfigurationsdaten in einem Architektur agnostischen Format wie XML vorliegen.</span><span class="sxs-lookup"><span data-stu-id="466f8-116">Therefore, configuration data must be in an architecture-agnostic format such as XML.</span></span> <span data-ttu-id="466f8-117">Durch die Verwendung von XML anstelle eines Bytestreams wird die Verwendung von Konfigurationsdaten auf verschiedenen Architekturen vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="466f8-117">Using XML instead of a byte stream makes it easier to use configuration data on different architectures.</span></span> <span data-ttu-id="466f8-118">Die XML-Elemente, die in den Konfigurationsdaten verwendet werden, werden durch den Implementierer bestimmt.</span><span class="sxs-lookup"><span data-stu-id="466f8-118">The XML elements used in the configuration data are determined by the implementer.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="466f8-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="466f8-119">Return value</span></span>

<span data-ttu-id="466f8-120">Gibt basierend auf dem Ergebnis dieses Vorgangs einen der folgenden Fehlercodes zurück.</span><span class="sxs-lookup"><span data-stu-id="466f8-120">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="466f8-121">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="466f8-121">Return code</span></span>                                                                                     | <span data-ttu-id="466f8-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="466f8-122">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="466f8-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="466f8-123"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="466f8-124">Der Vorgang ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="466f8-124">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="466f8-125"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="466f8-125"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="466f8-126">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="466f8-126">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="466f8-127"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="466f8-127"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="466f8-128">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="466f8-128">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="466f8-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="466f8-129">Remarks</span></span>

<span data-ttu-id="466f8-130">Informationen zur Versionsverwaltung von Komponenten sollten im datenkonfigurationsblob enthalten sein. </span><span class="sxs-lookup"><span data-stu-id="466f8-130">Component versioning information should be included in the *data* configuration blob.</span></span> <span data-ttu-id="466f8-131">Die Versionsinformationen können verwendet werden, wenn von einer SHV-Version zu einer anderen migriert wird.</span><span class="sxs-lookup"><span data-stu-id="466f8-131">The versioning information may be used when migrating from one SHV version to another.</span></span>

## <a name="requirements"></a><span data-ttu-id="466f8-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="466f8-132">Requirements</span></span>



| <span data-ttu-id="466f8-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="466f8-133">Requirement</span></span> | <span data-ttu-id="466f8-134">Wert</span><span class="sxs-lookup"><span data-stu-id="466f8-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="466f8-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="466f8-135">Minimum supported client</span></span><br/> | <span data-ttu-id="466f8-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="466f8-136">None supported</span></span><br/>                                                                |
| <span data-ttu-id="466f8-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="466f8-137">Minimum supported server</span></span><br/> | <span data-ttu-id="466f8-138">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="466f8-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="466f8-139">Header</span><span class="sxs-lookup"><span data-stu-id="466f8-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="466f8-140"><dt>Napcommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="466f8-140"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="466f8-141">IDL</span><span class="sxs-lookup"><span data-stu-id="466f8-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="466f8-142"><dt>Napcommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="466f8-142"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="466f8-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="466f8-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="466f8-144">**Inapcomponentconfig**</span><span class="sxs-lookup"><span data-stu-id="466f8-144">**INapComponentConfig**</span></span>](inapcomponentconfig.md)
</dt> <dt>

[<span data-ttu-id="466f8-145">**Inapconponentconfig:: GetConfig**</span><span class="sxs-lookup"><span data-stu-id="466f8-145">**INapConponentConfig::GetConfig**</span></span>](inapcomponentconfig-getconfig.md)
</dt> </dl>

 

 





