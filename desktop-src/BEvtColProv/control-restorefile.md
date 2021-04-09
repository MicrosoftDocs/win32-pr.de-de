---
description: Stellen Sie die aktive Konfiguration des Sammlers aus einer Sicherungsdatei wieder her.
ms.assetid: b59b04a5-d2b3-4299-8347-5026b982dc02
ms.tgt_platform: multiple
title: Restorefile-Methode der Steuerelement Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.RestoreFile
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 330486da86c9cac5c5f700d2aea91e0844fdca09
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958159"
---
# <a name="restorefile-method-of-the-control-class"></a><span data-ttu-id="7ff98-103">Restorefile-Methode der Steuerelement Klasse</span><span class="sxs-lookup"><span data-stu-id="7ff98-103">RestoreFile method of the Control class</span></span>

<span data-ttu-id="7ff98-104">Stellen Sie die aktive Konfiguration des Sammlers aus einer Sicherungsdatei wieder her.</span><span class="sxs-lookup"><span data-stu-id="7ff98-104">Restore the active configuration of the collector from a backup file.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ff98-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ff98-105">Syntax</span></span>


```mof
Uint32 RestoreFile(
  [in]  string File,
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



## <a name="parameters"></a><span data-ttu-id="7ff98-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ff98-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ff98-107">*Datei* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ff98-107">*File* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ff98-108">Der Name der wiederherzustellenden Sicherungsdatei aus der Liste, die von listbackups () zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="7ff98-108">Name of the backup file to restore, from the list returned by ListBackups().</span></span>

</dd> <dt>

<span data-ttu-id="7ff98-109">*Oldtimestamplow* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ff98-109">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ff98-110">Der Zeitstempel, zu dem die vorherige Konfiguration festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="7ff98-110">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="7ff98-111">Wenn nicht 0, aktiviert die atomizitäts Überprüfung: die neue Konfiguration wird nur angewendet, wenn der Zeitstempel der alten Konfiguration übereinstimmt (d. h., die Konfiguration wurde nicht in between geändert).</span><span class="sxs-lookup"><span data-stu-id="7ff98-111">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="7ff98-112">Dies ist der niedrige Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="7ff98-112">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="7ff98-113">*Oldtimestamphigh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ff98-113">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ff98-114">Der Zeitstempel, zu dem die vorherige Konfiguration festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="7ff98-114">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="7ff98-115">Wenn nicht 0, aktiviert die atomizitäts Überprüfung: die neue Konfiguration wird nur angewendet, wenn der Zeitstempel der alten Konfiguration übereinstimmt (d. h., die Konfiguration wurde nicht in between geändert).</span><span class="sxs-lookup"><span data-stu-id="7ff98-115">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="7ff98-116">Dies ist der große Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="7ff98-116">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="7ff98-117">*Newtimestamplow* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7ff98-117">*NewTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ff98-118">Der Zeitstempel, zu dem die neue Konfiguration festgelegt wurde,, wenn der-Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="7ff98-118">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="7ff98-119">Dies ist der niedrige Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="7ff98-119">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="7ff98-120">*Newtimestamphigh* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7ff98-120">*NewTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ff98-121">Der Zeitstempel, zu dem die neue Konfiguration festgelegt wurde,, wenn der-Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="7ff98-121">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="7ff98-122">Dies ist der große Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="7ff98-122">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="7ff98-123">*Originaltimestamplow* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7ff98-123">*OriginalTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ff98-124">Der ursprüngliche Zeitstempel, zu dem die wiederhergestellte Konfiguration zum ersten Mal festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="7ff98-124">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="7ff98-125">Dies ist der niedrige Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="7ff98-125">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="7ff98-126">*Originaltimestamphigh* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7ff98-126">*OriginalTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ff98-127">Der ursprüngliche Zeitstempel, zu dem die wiederhergestellte Konfiguration zum ersten Mal festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="7ff98-127">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="7ff98-128">Dies ist der große Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="7ff98-128">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="7ff98-129">*ErrorString* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7ff98-129">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ff98-130">Die Text Zeichenfolge mit einer Erläuterung des Fehlers.</span><span class="sxs-lookup"><span data-stu-id="7ff98-130">The text string with explanation of the error.</span></span>

</dd> <dt>

<span data-ttu-id="7ff98-131">*Warningstring* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7ff98-131">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ff98-132">Die Text Zeichenfolge mit Warnungen.</span><span class="sxs-lookup"><span data-stu-id="7ff98-132">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="7ff98-133">*InfoString* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7ff98-133">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ff98-134">Die Text Zeichenfolge mit Informationen zur Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="7ff98-134">The text string with information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="7ff98-135">*ErrorType* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7ff98-135">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ff98-136">Der Typ des Fehlers: Beachten Sie, dass 0 oder nicht vorhanden den Erfolg angibt.</span><span class="sxs-lookup"><span data-stu-id="7ff98-136">The type of the error: note that 0 or absent indicates success.</span></span>

<dt>

<span data-ttu-id="7ff98-137">0</span><span class="sxs-lookup"><span data-stu-id="7ff98-137">0</span></span>
</dt> <dd>

<span data-ttu-id="7ff98-138">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="7ff98-138">Success.</span></span>

</dd> <dt>

<span data-ttu-id="7ff98-139">1</span><span class="sxs-lookup"><span data-stu-id="7ff98-139">1</span></span>
</dt> <dd>

<span data-ttu-id="7ff98-140">Ungültiges Argument Format</span><span class="sxs-lookup"><span data-stu-id="7ff98-140">bad argument format</span></span>

</dd> <dt>

<span data-ttu-id="7ff98-141">2</span><span class="sxs-lookup"><span data-stu-id="7ff98-141">2</span></span>
</dt> <dd>

<span data-ttu-id="7ff98-142">Ungültiger Argument Wert</span><span class="sxs-lookup"><span data-stu-id="7ff98-142">bad argument value</span></span>

</dd> <dt>

<span data-ttu-id="7ff98-143">3</span><span class="sxs-lookup"><span data-stu-id="7ff98-143">3</span></span>
</dt> <dd>

<span data-ttu-id="7ff98-144">Fehler beim Öffnen der Ressource (Socket).</span><span class="sxs-lookup"><span data-stu-id="7ff98-144">resource (socket) open error</span></span>

</dd> <dt>

<span data-ttu-id="7ff98-145">4</span><span class="sxs-lookup"><span data-stu-id="7ff98-145">4</span></span>
</dt> <dd>

<span data-ttu-id="7ff98-146">Persistenz (Datei Schreibfehler)</span><span class="sxs-lookup"><span data-stu-id="7ff98-146">persistence (file write) error</span></span>

</dd> <dt>

<span data-ttu-id="7ff98-147">5</span><span class="sxs-lookup"><span data-stu-id="7ff98-147">5</span></span>
</dt> <dd>

<span data-ttu-id="7ff98-148">Unteilbarkeit-Fehler (der alte Zeitstempel entsprach nicht.)</span><span class="sxs-lookup"><span data-stu-id="7ff98-148">atomicity error (the old timestamp didn't match)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ff98-149">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7ff98-149">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="7ff98-150">0</span><span class="sxs-lookup"><span data-stu-id="7ff98-150">0</span></span>

<span data-ttu-id="7ff98-151">Fehler</span><span class="sxs-lookup"><span data-stu-id="7ff98-151">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="7ff98-152">1</span><span class="sxs-lookup"><span data-stu-id="7ff98-152">1</span></span>

<span data-ttu-id="7ff98-153">Erfolg</span><span class="sxs-lookup"><span data-stu-id="7ff98-153">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7ff98-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7ff98-154">Requirements</span></span>



| <span data-ttu-id="7ff98-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7ff98-155">Requirement</span></span> | <span data-ttu-id="7ff98-156">Wert</span><span class="sxs-lookup"><span data-stu-id="7ff98-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ff98-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7ff98-157">Minimum supported client</span></span><br/> | <span data-ttu-id="7ff98-158">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7ff98-158">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7ff98-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7ff98-159">Minimum supported server</span></span><br/> | <span data-ttu-id="7ff98-160">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7ff98-160">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="7ff98-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="7ff98-161">Namespace</span></span><br/>                | <span data-ttu-id="7ff98-162">Stammverzeichnis von \\ Microsoft \\ Windows \\ booteventcollector</span><span class="sxs-lookup"><span data-stu-id="7ff98-162">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="7ff98-163">MOF</span><span class="sxs-lookup"><span data-stu-id="7ff98-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7ff98-164"><dt>Booteventcollector WMI. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7ff98-164"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="7ff98-165">DLL</span><span class="sxs-lookup"><span data-stu-id="7ff98-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ff98-166"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7ff98-166"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="7ff98-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ff98-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ff98-168">**Control**</span><span class="sxs-lookup"><span data-stu-id="7ff98-168">**Control**</span></span>](control.md)
</dt> </dl>

 

