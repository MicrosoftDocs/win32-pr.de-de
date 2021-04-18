---
description: Stellen Sie die aktive Konfiguration des Sammlers aus der vorherigen Sicherungsdatei wieder her (festgelegt durch zurückkehren vom aktuellen ursprünglichen Zeitstempel).
ms.assetid: 150fa554-9efd-483e-a177-5fc7766a6a6c
ms.tgt_platform: multiple
title: Rückgängig-Methode der Steuerelement Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Undo
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 285f1ec39ea52f6c388e324f72745d72f65207e6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344806"
---
# <a name="undo-method-of-the-control-class"></a><span data-ttu-id="3268a-103">Rückgängig-Methode der Steuerelement Klasse</span><span class="sxs-lookup"><span data-stu-id="3268a-103">Undo method of the Control class</span></span>

<span data-ttu-id="3268a-104">Stellen Sie die aktive Konfiguration des Sammlers aus der vorherigen Sicherungsdatei wieder her (festgelegt durch zurückkehren vom aktuellen ursprünglichen Zeitstempel).</span><span class="sxs-lookup"><span data-stu-id="3268a-104">Restore the active configuration of the collector from the previous backup file (determined by going back from the current original timestamp).</span></span> <span data-ttu-id="3268a-105">Wenn die Konfiguration gerade festgelegt wurde, bedeutet dies, dass diese Änderung nicht mehr durchgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="3268a-105">If the configuration has been just set, this means undoing that change.</span></span> <span data-ttu-id="3268a-106">Die aufeinander folgenden Aufrufe werden in früheren und früheren Konfigurationen rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="3268a-106">The consecutive calls will undo to the earlier and earlier configurations.</span></span> <span data-ttu-id="3268a-107">Gibt bei Erfolg den Wert 1 zurück, 0 bei Fehler.</span><span class="sxs-lookup"><span data-stu-id="3268a-107">Returns 1 on success, 0 on error.</span></span>

## <a name="syntax"></a><span data-ttu-id="3268a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3268a-108">Syntax</span></span>


```mof
Uint32 Undo(
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



## <a name="parameters"></a><span data-ttu-id="3268a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3268a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3268a-110">*Oldtimestamplow* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3268a-110">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3268a-111">Der Zeitstempel, zu dem die vorherige Konfiguration festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="3268a-111">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="3268a-112">Wenn nicht 0, aktiviert die atomizitäts Überprüfung: die neue Konfiguration wird nur angewendet, wenn der Zeitstempel der alten Konfiguration übereinstimmt (d. h., die Konfiguration wurde nicht in between geändert).</span><span class="sxs-lookup"><span data-stu-id="3268a-112">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="3268a-113">Dies ist der niedrige Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="3268a-113">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="3268a-114">*Oldtimestamphigh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3268a-114">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3268a-115">Der Zeitstempel, zu dem die vorherige Konfiguration festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="3268a-115">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="3268a-116">Wenn nicht 0, aktiviert die atomizitäts Überprüfung: die neue Konfiguration wird nur angewendet, wenn der Zeitstempel der alten Konfiguration übereinstimmt (d. h., die Konfiguration wurde nicht in between geändert).</span><span class="sxs-lookup"><span data-stu-id="3268a-116">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="3268a-117">Dies ist der große Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="3268a-117">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="3268a-118">*Newtimestamplow* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3268a-118">*NewTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3268a-119">Der Zeitstempel, zu dem die neue Konfiguration festgelegt wurde,, wenn der-Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="3268a-119">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="3268a-120">Dies ist der niedrige Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="3268a-120">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="3268a-121">*Newtimestamphigh* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3268a-121">*NewTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3268a-122">Der Zeitstempel, zu dem die neue Konfiguration festgelegt wurde,, wenn der-Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="3268a-122">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="3268a-123">Dies ist der große Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="3268a-123">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="3268a-124">*Originaltimestamplow* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3268a-124">*OriginalTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3268a-125">Der ursprüngliche Zeitstempel, zu dem die wiederhergestellte Konfiguration zum ersten Mal festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="3268a-125">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="3268a-126">Dies ist der niedrige Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="3268a-126">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="3268a-127">*Originaltimestamphigh* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3268a-127">*OriginalTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3268a-128">Der ursprüngliche Zeitstempel, zu dem die wiederhergestellte Konfiguration zum ersten Mal festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="3268a-128">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="3268a-129">Dies ist der große Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="3268a-129">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="3268a-130">*ErrorString* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3268a-130">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3268a-131">Die Text Zeichenfolge mit einer Erläuterung des Fehlers.</span><span class="sxs-lookup"><span data-stu-id="3268a-131">The text string with explanation of the error.</span></span>

</dd> <dt>

<span data-ttu-id="3268a-132">*Warningstring* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3268a-132">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3268a-133">Die Text Zeichenfolge mit Warnungen.</span><span class="sxs-lookup"><span data-stu-id="3268a-133">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="3268a-134">*InfoString* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3268a-134">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3268a-135">Die Text Zeichenfolge mit Informationen zur Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="3268a-135">The text string with information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="3268a-136">*ErrorType* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3268a-136">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3268a-137">Der Typ des Fehlers: Beachten Sie, dass 0 oder nicht vorhanden den Erfolg angibt.</span><span class="sxs-lookup"><span data-stu-id="3268a-137">The type of the error: note that 0 or absent indicates success.</span></span>

<dt>

<span data-ttu-id="3268a-138">0</span><span class="sxs-lookup"><span data-stu-id="3268a-138">0</span></span>
</dt> <dd>

<span data-ttu-id="3268a-139">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="3268a-139">Success.</span></span>

</dd> <dt>

<span data-ttu-id="3268a-140">1</span><span class="sxs-lookup"><span data-stu-id="3268a-140">1</span></span>
</dt> <dd>

<span data-ttu-id="3268a-141">Ungültiges Argument Format</span><span class="sxs-lookup"><span data-stu-id="3268a-141">bad argument format</span></span>

</dd> <dt>

<span data-ttu-id="3268a-142">2</span><span class="sxs-lookup"><span data-stu-id="3268a-142">2</span></span>
</dt> <dd>

<span data-ttu-id="3268a-143">Ungültiger Argument Wert</span><span class="sxs-lookup"><span data-stu-id="3268a-143">bad argument value</span></span>

</dd> <dt>

<span data-ttu-id="3268a-144">3</span><span class="sxs-lookup"><span data-stu-id="3268a-144">3</span></span>
</dt> <dd>

<span data-ttu-id="3268a-145">Fehler beim Öffnen der Ressource (Socket).</span><span class="sxs-lookup"><span data-stu-id="3268a-145">resource (socket) open error</span></span>

</dd> <dt>

<span data-ttu-id="3268a-146">4</span><span class="sxs-lookup"><span data-stu-id="3268a-146">4</span></span>
</dt> <dd>

<span data-ttu-id="3268a-147">Persistenz (Datei Schreibfehler)</span><span class="sxs-lookup"><span data-stu-id="3268a-147">persistence (file write) error</span></span>

</dd> <dt>

<span data-ttu-id="3268a-148">5</span><span class="sxs-lookup"><span data-stu-id="3268a-148">5</span></span>
</dt> <dd>

<span data-ttu-id="3268a-149">Unteilbarkeit-Fehler (der alte Zeitstempel entsprach nicht.)</span><span class="sxs-lookup"><span data-stu-id="3268a-149">atomicity error (the old timestamp didn't match)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3268a-150">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3268a-150">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="3268a-151">0</span><span class="sxs-lookup"><span data-stu-id="3268a-151">0</span></span>

<span data-ttu-id="3268a-152">Fehler</span><span class="sxs-lookup"><span data-stu-id="3268a-152">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3268a-153">1</span><span class="sxs-lookup"><span data-stu-id="3268a-153">1</span></span>

<span data-ttu-id="3268a-154">Erfolg</span><span class="sxs-lookup"><span data-stu-id="3268a-154">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3268a-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3268a-155">Requirements</span></span>



| <span data-ttu-id="3268a-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3268a-156">Requirement</span></span> | <span data-ttu-id="3268a-157">Wert</span><span class="sxs-lookup"><span data-stu-id="3268a-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3268a-158">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3268a-158">Minimum supported client</span></span><br/> | <span data-ttu-id="3268a-159">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3268a-159">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3268a-160">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3268a-160">Minimum supported server</span></span><br/> | <span data-ttu-id="3268a-161">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3268a-161">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="3268a-162">Namespace</span><span class="sxs-lookup"><span data-stu-id="3268a-162">Namespace</span></span><br/>                | <span data-ttu-id="3268a-163">Stammverzeichnis von \\ Microsoft \\ Windows \\ booteventcollector</span><span class="sxs-lookup"><span data-stu-id="3268a-163">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="3268a-164">MOF</span><span class="sxs-lookup"><span data-stu-id="3268a-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3268a-165"><dt>Booteventcollector WMI. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3268a-165"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="3268a-166">DLL</span><span class="sxs-lookup"><span data-stu-id="3268a-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3268a-167"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3268a-167"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="3268a-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3268a-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3268a-169">**Control**</span><span class="sxs-lookup"><span data-stu-id="3268a-169">**Control**</span></span>](control.md)
</dt> </dl>

 

