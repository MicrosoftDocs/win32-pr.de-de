---
description: Wenn die aktuelle Konfiguration das Ergebnis der rückgängig/Wiederherstellung/Wiederherstellung ist, kennzeichnet Sie diese als explizit festgelegt, sodass der Verlauf den Zeitpunkt der Festlegung beibehält und bei der nächsten Konfigurationsänderung eine Sicherungsdatei erstellt wird.
ms.assetid: 1b3d398a-c7f9-4e21-9e43-1245a13fe564
ms.tgt_platform: multiple
title: Checkpoint-Methode der Steuerelement Klasse (srrestoreptapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Checkpoint
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 44453f647d55f29a9a6cfc5622e29dcc88ad2446
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125845"
---
# <a name="checkpoint-method-of-the-control-class"></a><span data-ttu-id="78e92-103">Checkpoint-Methode der Steuerelement Klasse</span><span class="sxs-lookup"><span data-stu-id="78e92-103">Checkpoint method of the Control class</span></span>

<span data-ttu-id="78e92-104">Wenn die aktuelle Konfiguration das Ergebnis der rückgängig/Wiederherstellung/Wiederherstellung ist, kennzeichnet Sie diese als explizit festgelegt, sodass der Verlauf den Zeitpunkt der Festlegung beibehält und bei der nächsten Konfigurationsänderung eine Sicherungsdatei erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="78e92-104">If the current configuration is a result of the Undo/Redo/Restore, marks it as if it has been set explicitly, so that the history will preserve the time when it was set, and a backup file will be created for it on the next configuration change.</span></span> <span data-ttu-id="78e92-105">Wenn die aktuelle Konfiguration bereits explizit festgelegt wurde, hat keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="78e92-105">If the current configuration was already set explicitly, has no effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="78e92-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="78e92-106">Syntax</span></span>


```mof
Uint32 Checkpoint(
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a><span data-ttu-id="78e92-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="78e92-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78e92-108">*Oldtimestamplow* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78e92-108">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78e92-109">Der Zeitstempel, zu dem die aktuelle Konfiguration festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="78e92-109">The timestamp of when the current configuration was set.</span></span> <span data-ttu-id="78e92-110">Wenn nicht 0, aktiviert die atomizitäts Überprüfung: die Aktion wird nur angewendet, wenn der Zeitstempel der alten Konfiguration übereinstimmt (d. h., die Konfiguration wurde nicht in between geändert).</span><span class="sxs-lookup"><span data-stu-id="78e92-110">If not 0, enables the atomicity check: the action will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="78e92-111">Dies ist der niedrige Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="78e92-111">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="78e92-112">*Oldtimestamphigh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78e92-112">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78e92-113">Der Zeitstempel, zu dem die aktuelle Konfiguration festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="78e92-113">The timestamp of when the current configuration was set.</span></span> <span data-ttu-id="78e92-114">Wenn nicht 0, aktiviert die atomizitäts Überprüfung: die Aktion wird nur angewendet, wenn der Zeitstempel der alten Konfiguration übereinstimmt (d. h., die Konfiguration wurde nicht in between geändert).</span><span class="sxs-lookup"><span data-stu-id="78e92-114">If not 0, enables the atomicity check: the action will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="78e92-115">Dies ist der große Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="78e92-115">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="78e92-116">*ErrorString* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="78e92-116">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78e92-117">Die Text Zeichenfolge mit einer Erläuterung des Fehlers.</span><span class="sxs-lookup"><span data-stu-id="78e92-117">The text string with explanation of the error.</span></span>

</dd> <dt>

<span data-ttu-id="78e92-118">*Warningstring* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="78e92-118">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78e92-119">Die Text Zeichenfolge mit Warnungen.</span><span class="sxs-lookup"><span data-stu-id="78e92-119">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="78e92-120">*InfoString* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="78e92-120">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78e92-121">Die Text Zeichenfolge mit Informationen zur Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="78e92-121">The text string with information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="78e92-122">*ErrorType* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="78e92-122">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78e92-123">Der Typ des Fehlers.</span><span class="sxs-lookup"><span data-stu-id="78e92-123">The type of the error.</span></span> <span data-ttu-id="78e92-124">Beachten Sie, dass 0 oder nicht vorhanden den Erfolg angibt.</span><span class="sxs-lookup"><span data-stu-id="78e92-124">Note that 0 or absent indicates success.</span></span>

<dt>

<span data-ttu-id="78e92-125">0</span><span class="sxs-lookup"><span data-stu-id="78e92-125">0</span></span>
</dt> <dd>

<span data-ttu-id="78e92-126">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="78e92-126">Success.</span></span>

</dd> <dt>

<span data-ttu-id="78e92-127">1</span><span class="sxs-lookup"><span data-stu-id="78e92-127">1</span></span>
</dt> <dd>

<span data-ttu-id="78e92-128">Ungültiges Argument Format</span><span class="sxs-lookup"><span data-stu-id="78e92-128">bad argument format</span></span>

</dd> <dt>

<span data-ttu-id="78e92-129">2</span><span class="sxs-lookup"><span data-stu-id="78e92-129">2</span></span>
</dt> <dd>

<span data-ttu-id="78e92-130">Ungültiger Argument Wert</span><span class="sxs-lookup"><span data-stu-id="78e92-130">bad argument value</span></span>

</dd> <dt>

<span data-ttu-id="78e92-131">3</span><span class="sxs-lookup"><span data-stu-id="78e92-131">3</span></span>
</dt> <dd>

<span data-ttu-id="78e92-132">Fehler beim Öffnen der Ressource (Socket).</span><span class="sxs-lookup"><span data-stu-id="78e92-132">resource (socket) open error</span></span>

</dd> <dt>

<span data-ttu-id="78e92-133">4</span><span class="sxs-lookup"><span data-stu-id="78e92-133">4</span></span>
</dt> <dd>

<span data-ttu-id="78e92-134">Persistenz (Datei Schreibfehler)</span><span class="sxs-lookup"><span data-stu-id="78e92-134">persistence (file write) error</span></span>

</dd> <dt>

<span data-ttu-id="78e92-135">5</span><span class="sxs-lookup"><span data-stu-id="78e92-135">5</span></span>
</dt> <dd>

<span data-ttu-id="78e92-136">Unteilbarkeit-Fehler (der alte Zeitstempel entsprach nicht.)</span><span class="sxs-lookup"><span data-stu-id="78e92-136">atomicity error (the old timestamp didn't match)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78e92-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="78e92-137">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="78e92-138">0</span><span class="sxs-lookup"><span data-stu-id="78e92-138">0</span></span>

<span data-ttu-id="78e92-139">Fehler</span><span class="sxs-lookup"><span data-stu-id="78e92-139">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="78e92-140">1</span><span class="sxs-lookup"><span data-stu-id="78e92-140">1</span></span>

<span data-ttu-id="78e92-141">Erfolg</span><span class="sxs-lookup"><span data-stu-id="78e92-141">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="78e92-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78e92-142">Requirements</span></span>



| <span data-ttu-id="78e92-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78e92-143">Requirement</span></span> | <span data-ttu-id="78e92-144">Wert</span><span class="sxs-lookup"><span data-stu-id="78e92-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78e92-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="78e92-145">Minimum supported client</span></span><br/> | <span data-ttu-id="78e92-146">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="78e92-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="78e92-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="78e92-147">Minimum supported server</span></span><br/> | <span data-ttu-id="78e92-148">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="78e92-148">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="78e92-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="78e92-149">Namespace</span></span><br/>                | <span data-ttu-id="78e92-150">Stammverzeichnis von \\ Microsoft \\ Windows \\ booteventcollector</span><span class="sxs-lookup"><span data-stu-id="78e92-150">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="78e92-151">Header</span><span class="sxs-lookup"><span data-stu-id="78e92-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="78e92-152"><dt>Srrestoreptapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="78e92-152"><dt>Srrestoreptapi.h</dt></span></span> </dl>          |
| <span data-ttu-id="78e92-153">MOF</span><span class="sxs-lookup"><span data-stu-id="78e92-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78e92-154"><dt>Booteventcollector WMI. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="78e92-154"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="78e92-155">DLL</span><span class="sxs-lookup"><span data-stu-id="78e92-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78e92-156"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="78e92-156"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="78e92-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78e92-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78e92-158">**Control**</span><span class="sxs-lookup"><span data-stu-id="78e92-158">**Control**</span></span>](control.md)
</dt> </dl>

 

