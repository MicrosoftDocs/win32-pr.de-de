---
description: Stellen Sie die aktive Konfiguration des Sammlers aus einer Sicherungsdatei wieder her, die durch einen Zeitstempel ausgewählt wird.
ms.assetid: 3ee4156b-c68f-4c44-b9be-dd86e8f4b340
ms.tgt_platform: multiple
title: Restorefromtime-Methode der Control-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.RestoreFromTime
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 79b89c0c89e4954d8a641d037e08757f83cad618
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339711"
---
# <a name="restorefromtime-method-of-the-control-class"></a><span data-ttu-id="5fe1d-103">Restorefromtime-Methode der Control-Klasse</span><span class="sxs-lookup"><span data-stu-id="5fe1d-103">RestoreFromTime method of the Control class</span></span>

<span data-ttu-id="5fe1d-104">Stellen Sie die aktive Konfiguration des Sammlers aus einer Sicherungsdatei wieder her, die durch einen Zeitstempel ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="5fe1d-104">Restore the active configuration of the collector from a backup file, selected by a timestamp.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fe1d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5fe1d-105">Syntax</span></span>


```mof
Uint32 RestoreFromTime(
  [in]  Uint32 TargetTimestampLow,
  [in]  Uint32 TargetTimestampHigh,
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] Uint32 NewTimestampLow,
  [out] Uint32 NewTimestampHigh,
  [out] Uint32 OriginalTimestampLow,
  [out] Uint32 OriginalTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a><span data-ttu-id="5fe1d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5fe1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fe1d-107">*Targettimestamplow* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5fe1d-107">*TargetTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fe1d-108">Stellen Sie die Sicherungsdatei mit diesem Zeitstempel wieder her.</span><span class="sxs-lookup"><span data-stu-id="5fe1d-108">Restore to the backup file at this timestamp.</span></span> <span data-ttu-id="5fe1d-109">Dies ist der niedrige Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="5fe1d-109">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="5fe1d-110">*Targettimestamphigh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5fe1d-110">*TargetTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fe1d-111">Stellen Sie die Sicherungsdatei mit diesem Zeitstempel wieder her.</span><span class="sxs-lookup"><span data-stu-id="5fe1d-111">Restore to the backup file at this timestamp.</span></span> <span data-ttu-id="5fe1d-112">Dies ist der große Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="5fe1d-112">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="5fe1d-113">*Oldtimestamplow* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5fe1d-113">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fe1d-114">Der Zeitstempel, zu dem die vorherige Konfiguration festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="5fe1d-114">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="5fe1d-115">Wenn nicht 0, aktiviert die atomizitäts Überprüfung: die neue Konfiguration wird nur angewendet, wenn der Zeitstempel der alten Konfiguration übereinstimmt (d. h., die Konfiguration wurde nicht in between geändert).</span><span class="sxs-lookup"><span data-stu-id="5fe1d-115">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="5fe1d-116">Dies ist der niedrige Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="5fe1d-116">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="5fe1d-117">*Oldtimestamphigh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5fe1d-117">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fe1d-118">Der Zeitstempel, zu dem die vorherige Konfiguration festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="5fe1d-118">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="5fe1d-119">Wenn nicht 0, aktiviert die atomizitäts Überprüfung: die neue Konfiguration wird nur angewendet, wenn der Zeitstempel der alten Konfiguration übereinstimmt (d. h., die Konfiguration wurde nicht in between geändert).</span><span class="sxs-lookup"><span data-stu-id="5fe1d-119">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="5fe1d-120">Dies ist der große Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="5fe1d-120">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="5fe1d-121">*Newtimestamplow* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5fe1d-121">*NewTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5fe1d-122">Der Zeitstempel, zu dem die neue Konfiguration festgelegt wurde,, wenn der-Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="5fe1d-122">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="5fe1d-123">Dies ist der niedrige Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="5fe1d-123">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="5fe1d-124">*Newtimestamphigh* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5fe1d-124">*NewTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5fe1d-125">Der Zeitstempel, zu dem die neue Konfiguration festgelegt wurde,, wenn der-Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="5fe1d-125">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="5fe1d-126">Dies ist der große Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="5fe1d-126">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="5fe1d-127">*Originaltimestamplow* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5fe1d-127">*OriginalTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5fe1d-128">Der ursprüngliche Zeitstempel, zu dem die wiederhergestellte Konfiguration zum ersten Mal festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="5fe1d-128">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="5fe1d-129">Dies ist der niedrige Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="5fe1d-129">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="5fe1d-130">*Originaltimestamphigh* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5fe1d-130">*OriginalTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5fe1d-131">Der ursprüngliche Zeitstempel, zu dem die wiederhergestellte Konfiguration zum ersten Mal festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="5fe1d-131">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="5fe1d-132">Dies ist der große Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="5fe1d-132">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="5fe1d-133">*ErrorString* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5fe1d-133">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5fe1d-134">Die Text Zeichenfolge mit einer Erläuterung des Fehlers.</span><span class="sxs-lookup"><span data-stu-id="5fe1d-134">The text string with explanation of the error.</span></span>

</dd> <dt>

<span data-ttu-id="5fe1d-135">*Warningstring* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5fe1d-135">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5fe1d-136">Die Text Zeichenfolge mit Warnungen.</span><span class="sxs-lookup"><span data-stu-id="5fe1d-136">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="5fe1d-137">*InfoString* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5fe1d-137">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5fe1d-138">Die Text Zeichenfolge mit Informationen zur Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="5fe1d-138">The text string with information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="5fe1d-139">*ErrorType* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5fe1d-139">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5fe1d-140">Der Typ des Fehlers: Beachten Sie, dass 0 oder nicht vorhanden den Erfolg angibt.</span><span class="sxs-lookup"><span data-stu-id="5fe1d-140">The type of the error: note that 0 or absent indicates success.</span></span>

<dt>

<span data-ttu-id="5fe1d-141">0</span><span class="sxs-lookup"><span data-stu-id="5fe1d-141">0</span></span>
</dt> <dd>

<span data-ttu-id="5fe1d-142">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="5fe1d-142">Success.</span></span>

</dd> <dt>

<span data-ttu-id="5fe1d-143">1</span><span class="sxs-lookup"><span data-stu-id="5fe1d-143">1</span></span>
</dt> <dd>

<span data-ttu-id="5fe1d-144">Ungültiges Argument Format</span><span class="sxs-lookup"><span data-stu-id="5fe1d-144">bad argument format</span></span>

</dd> <dt>

<span data-ttu-id="5fe1d-145">2</span><span class="sxs-lookup"><span data-stu-id="5fe1d-145">2</span></span>
</dt> <dd>

<span data-ttu-id="5fe1d-146">Ungültiger Argument Wert</span><span class="sxs-lookup"><span data-stu-id="5fe1d-146">bad argument value</span></span>

</dd> <dt>

<span data-ttu-id="5fe1d-147">3</span><span class="sxs-lookup"><span data-stu-id="5fe1d-147">3</span></span>
</dt> <dd>

<span data-ttu-id="5fe1d-148">Fehler beim Öffnen der Ressource (Socket).</span><span class="sxs-lookup"><span data-stu-id="5fe1d-148">resource (socket) open error</span></span>

</dd> <dt>

<span data-ttu-id="5fe1d-149">4</span><span class="sxs-lookup"><span data-stu-id="5fe1d-149">4</span></span>
</dt> <dd>

<span data-ttu-id="5fe1d-150">Persistenz (Datei Schreibfehler)</span><span class="sxs-lookup"><span data-stu-id="5fe1d-150">persistence (file write) error</span></span>

</dd> <dt>

<span data-ttu-id="5fe1d-151">5</span><span class="sxs-lookup"><span data-stu-id="5fe1d-151">5</span></span>
</dt> <dd>

<span data-ttu-id="5fe1d-152">Unteilbarkeit-Fehler (der alte Zeitstempel entsprach nicht.)</span><span class="sxs-lookup"><span data-stu-id="5fe1d-152">atomicity error (the old timestamp didn't match)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fe1d-153">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5fe1d-153">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="5fe1d-154">0</span><span class="sxs-lookup"><span data-stu-id="5fe1d-154">0</span></span>

<span data-ttu-id="5fe1d-155">Fehler</span><span class="sxs-lookup"><span data-stu-id="5fe1d-155">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="5fe1d-156">1</span><span class="sxs-lookup"><span data-stu-id="5fe1d-156">1</span></span>

<span data-ttu-id="5fe1d-157">Erfolg</span><span class="sxs-lookup"><span data-stu-id="5fe1d-157">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5fe1d-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5fe1d-158">Requirements</span></span>



| <span data-ttu-id="5fe1d-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5fe1d-159">Requirement</span></span> | <span data-ttu-id="5fe1d-160">Wert</span><span class="sxs-lookup"><span data-stu-id="5fe1d-160">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fe1d-161">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5fe1d-161">Minimum supported client</span></span><br/> | <span data-ttu-id="5fe1d-162">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5fe1d-162">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="5fe1d-163">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5fe1d-163">Minimum supported server</span></span><br/> | <span data-ttu-id="5fe1d-164">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="5fe1d-164">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="5fe1d-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="5fe1d-165">Namespace</span></span><br/>                | <span data-ttu-id="5fe1d-166">Stammverzeichnis von \\ Microsoft \\ Windows \\ booteventcollector</span><span class="sxs-lookup"><span data-stu-id="5fe1d-166">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="5fe1d-167">MOF</span><span class="sxs-lookup"><span data-stu-id="5fe1d-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5fe1d-168"><dt>Booteventcollector WMI. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5fe1d-168"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="5fe1d-169">DLL</span><span class="sxs-lookup"><span data-stu-id="5fe1d-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5fe1d-170"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5fe1d-170"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="5fe1d-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5fe1d-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fe1d-172">**Control**</span><span class="sxs-lookup"><span data-stu-id="5fe1d-172">**Control**</span></span>](control.md)
</dt> </dl>

 

