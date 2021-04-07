---
description: Legen Sie die neue aktive Konfiguration des Sammlers fest.
ms.assetid: 1979e657-a8f3-4eab-991c-a884bde10724
ms.tgt_platform: multiple
title: SetConfiguration-Methode der Steuerelement Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.SetConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 4f482de9c4cd8f410371da51e605762a1f92e104
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747784"
---
# <a name="setconfiguration-method-of-the-control-class"></a><span data-ttu-id="fe458-103">SetConfiguration-Methode der Steuerelement Klasse</span><span class="sxs-lookup"><span data-stu-id="fe458-103">SetConfiguration method of the Control class</span></span>

<span data-ttu-id="fe458-104">Legen Sie die neue aktive Konfiguration des Sammlers fest.</span><span class="sxs-lookup"><span data-stu-id="fe458-104">Set the new active configuration of the collector.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe458-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe458-105">Syntax</span></span>


```mof
Uint32 SetConfiguration(
  [in]  string Config,
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] Uint32 NewTimestampLow,
  [out] Uint32 NewTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a><span data-ttu-id="fe458-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe458-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe458-107">*Config* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe458-107">*Config* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe458-108">Die zu Aktivier-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="fe458-108">The configuration to activate.</span></span>

</dd> <dt>

<span data-ttu-id="fe458-109">*Oldtimestamplow* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe458-109">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe458-110">Die nieder wertigen Bits eines Zeitstempels, der angibt, wann die aktuelle aktive Konfiguration festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="fe458-110">The low-order bits of a timestamp that indicates when the current active configuration was set.</span></span> <span data-ttu-id="fe458-111">Die atomizitäts Prüfung ist aktiviert, wenn diese Eigenschaft nicht auf 0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="fe458-111">Atomicity checking is enabled if this property is not set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="fe458-112">*Oldtimestamphigh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe458-112">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe458-113">Die höherwertigen Bits eines Zeitstempels, der angibt, wann die aktuelle aktive Konfiguration festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="fe458-113">The high-order bits of a timestamp that indicates when the current active configuration was set.</span></span> <span data-ttu-id="fe458-114">Die atomizitäts Prüfung ist aktiviert, wenn diese Eigenschaft nicht auf 0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="fe458-114">Atomicity checking is enabled if this property is not set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="fe458-115">*Newtimestamplow* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fe458-115">*NewTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe458-116">Wenn diese Methode zurückgegeben wird, enthält dieser Parameter die nieder wertigen Bits eines Zeitstempels, der angibt, wann die neue Konfiguration festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="fe458-116">When this method returns, this parameter contains the low-order bits of a timestamp that indicates when the new configuration was set.</span></span> <span data-ttu-id="fe458-117">Die atomizitäts Prüfung ist aktiviert, wenn diese Eigenschaft nicht auf 0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="fe458-117">Atomicity checking is enabled if this property is not set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="fe458-118">*Newtimestamphigh* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fe458-118">*NewTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe458-119">Wenn diese Methode zurückgegeben wird, enthält dieser Parameter die höherwertigen Bits des Zeitstempels, der angibt, wann die neue Konfiguration festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="fe458-119">When this method returns, this parameter contains the high-order bits of the timestamp that indicates when the new configuration was set.</span></span> <span data-ttu-id="fe458-120">Die atomizitäts Prüfung ist aktiviert, wenn diese Eigenschaft nicht auf 0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="fe458-120">Atomicity checking is enabled if this property is not set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="fe458-121">*ErrorString* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fe458-121">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe458-122">Wenn diese Methode zurückgegeben wird, enthält dieser Parameter die Fehlerbeschreibung, wenn ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="fe458-122">When this method returns, if there was an error, this parameter contains the error description.</span></span>

</dd> <dt>

<span data-ttu-id="fe458-123">*Warningstring* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fe458-123">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe458-124">Wenn diese Methode zurückgegeben wird, enthält dieser Parameter alle Warnmeldungen für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="fe458-124">When this method returns, this parameter contains any warnings messages for the operation.</span></span>

</dd> <dt>

<span data-ttu-id="fe458-125">*InfoString* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fe458-125">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe458-126">Wenn diese Methode zurückgegeben wird, enthält dieser Parameterinformationen für die neue aktive Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="fe458-126">When this method returns, this parameter contains information for the new active configuration.</span></span>

</dd> <dt>

<span data-ttu-id="fe458-127">*ErrorType* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fe458-127">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe458-128">Wenn diese Methode zurückgegeben wird, gibt dieser Parameter den Fehlertyp an, wenn ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="fe458-128">When this method returns, if there was an error, this parameter indicates the error type.</span></span>

<dt>

<span data-ttu-id="fe458-129">0</span><span class="sxs-lookup"><span data-stu-id="fe458-129">0</span></span>
</dt> <dd>

<span data-ttu-id="fe458-130">Die neue Konfiguration fehlt.</span><span class="sxs-lookup"><span data-stu-id="fe458-130">The new configuration is missing.</span></span>

</dd> <dt>

<span data-ttu-id="fe458-131">1</span><span class="sxs-lookup"><span data-stu-id="fe458-131">1</span></span>
</dt> <dd>

<span data-ttu-id="fe458-132">Das Format der neuen Konfiguration ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="fe458-132">The format of the new configuration is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="fe458-133">2</span><span class="sxs-lookup"><span data-stu-id="fe458-133">2</span></span>
</dt> <dd>

<span data-ttu-id="fe458-134">Die neue Konfiguration ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="fe458-134">The new configuration is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="fe458-135">3</span><span class="sxs-lookup"><span data-stu-id="fe458-135">3</span></span>
</dt> <dd>

<span data-ttu-id="fe458-136">Es ist ein Fehler aufgetreten, der durch einen geöffneten Socket verursacht wurde.</span><span class="sxs-lookup"><span data-stu-id="fe458-136">There was an error caused by an open socket.</span></span>

</dd> <dt>

<span data-ttu-id="fe458-137">4</span><span class="sxs-lookup"><span data-stu-id="fe458-137">4</span></span>
</dt> <dd>

<span data-ttu-id="fe458-138">Fehler beim Schreiben von Dateien.</span><span class="sxs-lookup"><span data-stu-id="fe458-138">There was a file write error.</span></span>

</dd> <dt>

<span data-ttu-id="fe458-139">5</span><span class="sxs-lookup"><span data-stu-id="fe458-139">5</span></span>
</dt> <dd>

<span data-ttu-id="fe458-140">Unteilbarkeit-Fehler.</span><span class="sxs-lookup"><span data-stu-id="fe458-140">There was an atomicity error.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe458-141">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fe458-141">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="fe458-142">0</span><span class="sxs-lookup"><span data-stu-id="fe458-142">0</span></span>

<span data-ttu-id="fe458-143">Fehler</span><span class="sxs-lookup"><span data-stu-id="fe458-143">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="fe458-144">1</span><span class="sxs-lookup"><span data-stu-id="fe458-144">1</span></span>

<span data-ttu-id="fe458-145">Erfolg</span><span class="sxs-lookup"><span data-stu-id="fe458-145">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fe458-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe458-146">Requirements</span></span>



| <span data-ttu-id="fe458-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe458-147">Requirement</span></span> | <span data-ttu-id="fe458-148">Wert</span><span class="sxs-lookup"><span data-stu-id="fe458-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe458-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fe458-149">Minimum supported client</span></span><br/> | <span data-ttu-id="fe458-150">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe458-150">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fe458-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fe458-151">Minimum supported server</span></span><br/> | <span data-ttu-id="fe458-152">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="fe458-152">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="fe458-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="fe458-153">Namespace</span></span><br/>                | <span data-ttu-id="fe458-154">Stammverzeichnis von \\ Microsoft \\ Windows \\ booteventcollector</span><span class="sxs-lookup"><span data-stu-id="fe458-154">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="fe458-155">MOF</span><span class="sxs-lookup"><span data-stu-id="fe458-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fe458-156"><dt>Booteventcollector WMI. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fe458-156"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="fe458-157">DLL</span><span class="sxs-lookup"><span data-stu-id="fe458-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe458-158"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fe458-158"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="fe458-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe458-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe458-160">**Control**</span><span class="sxs-lookup"><span data-stu-id="fe458-160">**Control**</span></span>](control.md)
</dt> </dl>

 

 




