---
description: Überprüfen Sie einen Konfigurations Text auf Richtigkeit, ohne ihn als aktiv festzulegen. Gibt bei Erfolg den Wert 1 zurück, 0 bei Fehler.
ms.assetid: baeabed0-7717-498a-9886-e49e4a101711
ms.tgt_platform: multiple
title: Validateconfiguration-Methode der Control-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.ValidateConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: d4e1d0061b779a54973aeea1a487d8838781cf6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958157"
---
# <a name="validateconfiguration-method-of-the-control-class"></a><span data-ttu-id="e448d-104">Validateconfiguration-Methode der Control-Klasse</span><span class="sxs-lookup"><span data-stu-id="e448d-104">ValidateConfiguration method of the Control class</span></span>

<span data-ttu-id="e448d-105">Überprüfen Sie einen Konfigurations Text auf Richtigkeit, ohne ihn als aktiv festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e448d-105">Validate a configuration text for correctness without setting it active.</span></span> <span data-ttu-id="e448d-106">Gibt bei Erfolg den Wert 1 zurück, 0 bei Fehler.</span><span class="sxs-lookup"><span data-stu-id="e448d-106">Returns 1 on success, 0 on error.</span></span>

## <a name="syntax"></a><span data-ttu-id="e448d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e448d-107">Syntax</span></span>


```mof
Uint32 ValidateConfiguration(
  [in]  string Config,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a><span data-ttu-id="e448d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e448d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e448d-109">*Config* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e448d-109">*Config* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e448d-110">Die Konfiguration, die überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="e448d-110">The configuration to check.</span></span>

</dd> <dt>

<span data-ttu-id="e448d-111">*ErrorString* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e448d-111">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e448d-112">Wenn diese Methode zurückgegeben wird, enthält dieser Parameter eine Beschreibung des Validierungs Fehlers für den Vorgang, wenn ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="e448d-112">When this method returns, if there was a error, this parameter contains a description of the validation error for the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e448d-113">*Warningstring* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e448d-113">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e448d-114">Wenn diese Methode zurückgegeben wird, enthält dieser Parameter eine Beschreibung aller Validierungs Warnungen für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="e448d-114">When this method returns, this parameter contains a description of any validation warnings for the operation.</span></span>

<span data-ttu-id="e448d-115">Die Text Zeichenfolge mit Warnungen.</span><span class="sxs-lookup"><span data-stu-id="e448d-115">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="e448d-116">*InfoString* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e448d-116">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e448d-117">Wenn diese Methode zurückgegeben wird, enthält dieser Parameter einen Satz von Informationen zur Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e448d-117">When this method returns, this parameter contains a set of information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="e448d-118">*ErrorType* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e448d-118">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e448d-119">Wenn diese Methode zurückgegeben wird, gibt dieser Parameter den Fehlertyp an, wenn ein Validierungs Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="e448d-119">When this method returns, if there was a validation error, this parameter indicates the error type.</span></span>

<span data-ttu-id="e448d-120">Mögliche Werte sind:</span><span class="sxs-lookup"><span data-stu-id="e448d-120">The possible values are:</span></span>

<dt>

<span data-ttu-id="e448d-121">0</span><span class="sxs-lookup"><span data-stu-id="e448d-121">0</span></span>
</dt> <dd>

<span data-ttu-id="e448d-122">Das Argument fehlt.</span><span class="sxs-lookup"><span data-stu-id="e448d-122">The argument is missing.</span></span>

</dd> <dt>

<span data-ttu-id="e448d-123">1</span><span class="sxs-lookup"><span data-stu-id="e448d-123">1</span></span>
</dt> <dd>

<span data-ttu-id="e448d-124">Das Argument Format ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="e448d-124">The argument format is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="e448d-125">2</span><span class="sxs-lookup"><span data-stu-id="e448d-125">2</span></span>
</dt> <dd>

<span data-ttu-id="e448d-126">Ein Konfigurations Argument ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="e448d-126">A configuration argument is invalid.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e448d-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e448d-127">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="e448d-128">0</span><span class="sxs-lookup"><span data-stu-id="e448d-128">0</span></span>

<span data-ttu-id="e448d-129">Fehler</span><span class="sxs-lookup"><span data-stu-id="e448d-129">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="e448d-130">1</span><span class="sxs-lookup"><span data-stu-id="e448d-130">1</span></span>

<span data-ttu-id="e448d-131">Erfolg</span><span class="sxs-lookup"><span data-stu-id="e448d-131">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e448d-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e448d-132">Requirements</span></span>



| <span data-ttu-id="e448d-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e448d-133">Requirement</span></span> | <span data-ttu-id="e448d-134">Wert</span><span class="sxs-lookup"><span data-stu-id="e448d-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e448d-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e448d-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e448d-136">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e448d-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="e448d-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e448d-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e448d-138">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e448d-138">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="e448d-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="e448d-139">Namespace</span></span><br/>                | <span data-ttu-id="e448d-140">Stammverzeichnis von \\ Microsoft \\ Windows \\ booteventcollector</span><span class="sxs-lookup"><span data-stu-id="e448d-140">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="e448d-141">MOF</span><span class="sxs-lookup"><span data-stu-id="e448d-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e448d-142"><dt>Booteventcollector WMI. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e448d-142"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="e448d-143">DLL</span><span class="sxs-lookup"><span data-stu-id="e448d-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e448d-144"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e448d-144"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="e448d-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e448d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e448d-146">**Control**</span><span class="sxs-lookup"><span data-stu-id="e448d-146">**Control**</span></span>](control.md)
</dt> </dl>

 

 




