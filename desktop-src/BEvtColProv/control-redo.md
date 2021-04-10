---
description: Setzt die aktive Konfiguration des Sammlers aus der späteren Sicherungsdatei zurück (festgelegt durch Weiterleiten vom aktuellen ursprünglichen Zeitstempel). Wenn die Konfiguration rückgängig gemacht wurde, bedeutet dies, dass die rückgängig gemachte Änderung rückgängig gemacht wird.
ms.assetid: bd153ea3-9148-4e65-a44e-3f9fa1855f2f
ms.tgt_platform: multiple
title: Redo-Methode der Steuerelement Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Redo
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 5ed77aac62dca0bf81ed13474e8acebb0235ea71
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125834"
---
# <a name="redo-method-of-the-control-class"></a><span data-ttu-id="a43a2-104">Redo-Methode der Steuerelement Klasse</span><span class="sxs-lookup"><span data-stu-id="a43a2-104">Redo method of the Control class</span></span>

<span data-ttu-id="a43a2-105">Setzt die aktive Konfiguration des Sammlers aus der späteren Sicherungsdatei zurück (festgelegt durch Weiterleiten vom aktuellen ursprünglichen Zeitstempel).</span><span class="sxs-lookup"><span data-stu-id="a43a2-105">Reset the active configuration of the collector from the later backup file (determined by going forward from the current original timestamp).</span></span> <span data-ttu-id="a43a2-106">Wenn die Konfiguration rückgängig gemacht wurde, bedeutet dies, dass die rückgängig gemachte Änderung rückgängig gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="a43a2-106">If the configuration has been undone, this means redoing the undone change.</span></span>

## <a name="syntax"></a><span data-ttu-id="a43a2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a43a2-107">Syntax</span></span>


```mof
Uint32 Redo(
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



## <a name="parameters"></a><span data-ttu-id="a43a2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a43a2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a43a2-109">*Oldtimestamplow* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a43a2-109">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a43a2-110">Der Zeitstempel, zu dem die vorherige Konfiguration festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="a43a2-110">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="a43a2-111">Wenn nicht 0, aktiviert die atomizitäts Überprüfung: die neue Konfiguration wird nur angewendet, wenn der Zeitstempel der alten Konfiguration übereinstimmt (d. h., die Konfiguration wurde nicht in between geändert).</span><span class="sxs-lookup"><span data-stu-id="a43a2-111">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="a43a2-112">Dies ist der niedrige Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="a43a2-112">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="a43a2-113">*Oldtimestamphigh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a43a2-113">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a43a2-114">Der Zeitstempel, zu dem die vorherige Konfiguration festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="a43a2-114">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="a43a2-115">Wenn nicht 0, aktiviert die atomizitäts Überprüfung: die neue Konfiguration wird nur angewendet, wenn der Zeitstempel der alten Konfiguration übereinstimmt (d. h., die Konfiguration wurde nicht in between geändert).</span><span class="sxs-lookup"><span data-stu-id="a43a2-115">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="a43a2-116">Dies ist der große Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="a43a2-116">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="a43a2-117">*Newtimestamplow* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a43a2-117">*NewTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a43a2-118">Der Zeitstempel, zu dem die neue Konfiguration festgelegt wurde,, wenn der-Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="a43a2-118">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="a43a2-119">Dies ist der niedrige Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="a43a2-119">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="a43a2-120">*Newtimestamphigh* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a43a2-120">*NewTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a43a2-121">Der Zeitstempel, zu dem die neue Konfiguration festgelegt wurde,, wenn der-Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="a43a2-121">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="a43a2-122">Dies ist der große Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="a43a2-122">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="a43a2-123">*Originaltimestamplow* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a43a2-123">*OriginalTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a43a2-124">Der ursprüngliche Zeitstempel, zu dem die wiederhergestellte Konfiguration zum ersten Mal festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="a43a2-124">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="a43a2-125">Dies ist der niedrige Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="a43a2-125">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="a43a2-126">*Originaltimestamphigh* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a43a2-126">*OriginalTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a43a2-127">Der ursprüngliche Zeitstempel, zu dem die wiederhergestellte Konfiguration zum ersten Mal festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="a43a2-127">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="a43a2-128">Dies ist der große Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="a43a2-128">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="a43a2-129">*ErrorString* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a43a2-129">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a43a2-130">Die Text Zeichenfolge mit einer Erläuterung des Fehlers.</span><span class="sxs-lookup"><span data-stu-id="a43a2-130">The text string with explanation of the error.</span></span>

</dd> <dt>

<span data-ttu-id="a43a2-131">*Warningstring* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a43a2-131">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a43a2-132">Die Text Zeichenfolge mit Warnungen.</span><span class="sxs-lookup"><span data-stu-id="a43a2-132">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="a43a2-133">*InfoString* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a43a2-133">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a43a2-134">Die Text Zeichenfolge mit Informationen zur Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a43a2-134">The text string with information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="a43a2-135">*ErrorType* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a43a2-135">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a43a2-136">Der Typ des Fehlers.</span><span class="sxs-lookup"><span data-stu-id="a43a2-136">The type of the error.</span></span> <span data-ttu-id="a43a2-137">Beachten Sie, dass 0 oder nicht vorhanden den Erfolg angibt.</span><span class="sxs-lookup"><span data-stu-id="a43a2-137">Note that 0 or absent indicates success.</span></span>

<dt>

<span data-ttu-id="a43a2-138">0</span><span class="sxs-lookup"><span data-stu-id="a43a2-138">0</span></span>
</dt> <dd>

<span data-ttu-id="a43a2-139">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="a43a2-139">Success.</span></span>

</dd> <dt>

<span data-ttu-id="a43a2-140">1</span><span class="sxs-lookup"><span data-stu-id="a43a2-140">1</span></span>
</dt> <dd>

<span data-ttu-id="a43a2-141">Ungültiges Argument Format</span><span class="sxs-lookup"><span data-stu-id="a43a2-141">bad argument format</span></span>

</dd> <dt>

<span data-ttu-id="a43a2-142">2</span><span class="sxs-lookup"><span data-stu-id="a43a2-142">2</span></span>
</dt> <dd>

<span data-ttu-id="a43a2-143">Ungültiger Argument Wert</span><span class="sxs-lookup"><span data-stu-id="a43a2-143">bad argument value</span></span>

</dd> <dt>

<span data-ttu-id="a43a2-144">3</span><span class="sxs-lookup"><span data-stu-id="a43a2-144">3</span></span>
</dt> <dd>

<span data-ttu-id="a43a2-145">Fehler beim Öffnen der Ressource (Socket).</span><span class="sxs-lookup"><span data-stu-id="a43a2-145">resource (socket) open error</span></span>

</dd> <dt>

<span data-ttu-id="a43a2-146">4</span><span class="sxs-lookup"><span data-stu-id="a43a2-146">4</span></span>
</dt> <dd>

<span data-ttu-id="a43a2-147">Persistenz (Datei Schreibfehler)</span><span class="sxs-lookup"><span data-stu-id="a43a2-147">persistence (file write) error</span></span>

</dd> <dt>

<span data-ttu-id="a43a2-148">5</span><span class="sxs-lookup"><span data-stu-id="a43a2-148">5</span></span>
</dt> <dd>

<span data-ttu-id="a43a2-149">Unteilbarkeit-Fehler (der alte Zeitstempel entsprach nicht.)</span><span class="sxs-lookup"><span data-stu-id="a43a2-149">atomicity error (the old timestamp didn't match)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a43a2-150">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a43a2-150">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="a43a2-151">0</span><span class="sxs-lookup"><span data-stu-id="a43a2-151">0</span></span>

<span data-ttu-id="a43a2-152">Fehler</span><span class="sxs-lookup"><span data-stu-id="a43a2-152">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a43a2-153">1</span><span class="sxs-lookup"><span data-stu-id="a43a2-153">1</span></span>

<span data-ttu-id="a43a2-154">Erfolg</span><span class="sxs-lookup"><span data-stu-id="a43a2-154">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a43a2-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a43a2-155">Requirements</span></span>



| <span data-ttu-id="a43a2-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a43a2-156">Requirement</span></span> | <span data-ttu-id="a43a2-157">Wert</span><span class="sxs-lookup"><span data-stu-id="a43a2-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a43a2-158">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a43a2-158">Minimum supported client</span></span><br/> | <span data-ttu-id="a43a2-159">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a43a2-159">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a43a2-160">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a43a2-160">Minimum supported server</span></span><br/> | <span data-ttu-id="a43a2-161">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a43a2-161">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="a43a2-162">Namespace</span><span class="sxs-lookup"><span data-stu-id="a43a2-162">Namespace</span></span><br/>                | <span data-ttu-id="a43a2-163">Stammverzeichnis von \\ Microsoft \\ Windows \\ booteventcollector</span><span class="sxs-lookup"><span data-stu-id="a43a2-163">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="a43a2-164">MOF</span><span class="sxs-lookup"><span data-stu-id="a43a2-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a43a2-165"><dt>Booteventcollector WMI. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a43a2-165"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="a43a2-166">DLL</span><span class="sxs-lookup"><span data-stu-id="a43a2-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a43a2-167"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a43a2-167"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="a43a2-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a43a2-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a43a2-169">**Control**</span><span class="sxs-lookup"><span data-stu-id="a43a2-169">**Control**</span></span>](control.md)
</dt> </dl>

 

