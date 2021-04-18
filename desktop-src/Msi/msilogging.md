---
description: Die MsiLogging-Eigenschaft legt den Standard Protokollierungs Modus für das Windows Installer Paket fest.
ms.assetid: f5ae389e-bc27-465d-886b-4f4f41d49118
title: MsiLogging-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97e53df57723157f7184a904e512aac9035a9f53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358757"
---
# <a name="msilogging-property"></a><span data-ttu-id="85911-103">MsiLogging-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="85911-103">MsiLogging property</span></span>

<span data-ttu-id="85911-104">Die **MsiLogging** -Eigenschaft legt den Standard Protokollierungs Modus für das Windows Installer Paket fest.</span><span class="sxs-lookup"><span data-stu-id="85911-104">The **MsiLogging** property sets the default logging mode for the Windows Installer package.</span></span> <span data-ttu-id="85911-105">Wenn diese optionale Eigenschaft in der [Eigenschaften Tabelle](property-table.md)vorhanden ist, generiert das Installationsprogramm eine Protokolldatei mit dem Namen MSI \* . Angezeigt.</span><span class="sxs-lookup"><span data-stu-id="85911-105">If this optional property is present in the [Property table](property-table.md), the installer generates a log file named MSI\*.LOG.</span></span> <span data-ttu-id="85911-106">Der vollständige Pfad zur Protokolldatei wird durch den Wert der [**msilogfileloation**](msilogfilelocation.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="85911-106">The full path to the log file is given by the value of the [**MsiLogFileLocation**](msilogfilelocation.md) property.</span></span>

## <a name="value"></a><span data-ttu-id="85911-107">Wert</span><span class="sxs-lookup"><span data-stu-id="85911-107">Value</span></span>

<span data-ttu-id="85911-108">Der Wert dieser Eigenschaft muss eine Zeichenfolge mit den folgenden Zeichen sein, die den Standard Protokollierungs Modus angeben.</span><span class="sxs-lookup"><span data-stu-id="85911-108">The value of this property should be a string of the following characters that specify the default logging mode.</span></span>



| <span data-ttu-id="85911-109">Wert</span><span class="sxs-lookup"><span data-stu-id="85911-109">Value</span></span>                                                                        | <span data-ttu-id="85911-110">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="85911-110">Meaning</span></span>                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="85911-111"><dt>I</dt></span><span class="sxs-lookup"><span data-stu-id="85911-111"><dt>I</dt></span></span> </dl> | <span data-ttu-id="85911-112">Status Meldungen.</span><span class="sxs-lookup"><span data-stu-id="85911-112">Status messages.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="85911-113"><dt>w</dt></span><span class="sxs-lookup"><span data-stu-id="85911-113"><dt>w</dt></span></span> </dl> | <span data-ttu-id="85911-114">Nicht schwerwiegende Warnungen.</span><span class="sxs-lookup"><span data-stu-id="85911-114">Nonfatal warnings.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="85911-115"><dt>e</dt></span><span class="sxs-lookup"><span data-stu-id="85911-115"><dt>e</dt></span></span> </dl> | <span data-ttu-id="85911-116">Alle Fehlermeldungen.</span><span class="sxs-lookup"><span data-stu-id="85911-116">All error messages.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="85911-117"><dt>ein</dt></span><span class="sxs-lookup"><span data-stu-id="85911-117"><dt>a</dt></span></span> </dl> | <span data-ttu-id="85911-118">Starten von Aktionen.</span><span class="sxs-lookup"><span data-stu-id="85911-118">Start up of actions.</span></span><br/>                                                |
| <dl> <span data-ttu-id="85911-119"><dt>r</dt></span><span class="sxs-lookup"><span data-stu-id="85911-119"><dt>r</dt></span></span> </dl> | <span data-ttu-id="85911-120">Aktions spezifische Datensätze.</span><span class="sxs-lookup"><span data-stu-id="85911-120">Action-specific records.</span></span><br/>                                            |
| <dl> <span data-ttu-id="85911-121"><dt>n</dt></span><span class="sxs-lookup"><span data-stu-id="85911-121"><dt>u</dt></span></span> </dl> | <span data-ttu-id="85911-122">Benutzer Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="85911-122">User requests.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="85911-123"><dt>c</dt></span><span class="sxs-lookup"><span data-stu-id="85911-123"><dt>c</dt></span></span> </dl> | <span data-ttu-id="85911-124">Anfängliche Parameter für die Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="85911-124">Initial UI parameters.</span></span><br/>                                              |
| <dl> <span data-ttu-id="85911-125"><dt>m</dt></span><span class="sxs-lookup"><span data-stu-id="85911-125"><dt>m</dt></span></span> </dl> | <span data-ttu-id="85911-126">Nicht genügend Arbeitsspeicher oder schwerwiegende Exit-Informationen.</span><span class="sxs-lookup"><span data-stu-id="85911-126">Out-of-memory or fatal exit information.</span></span><br/>                            |
| <dl> <span data-ttu-id="85911-127"><dt>o</dt></span><span class="sxs-lookup"><span data-stu-id="85911-127"><dt>o</dt></span></span> </dl> | <span data-ttu-id="85911-128">Nicht genügend Speicherplatz Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="85911-128">Out-of-disk-space messages.</span></span><br/>                                         |
| <dl> <span data-ttu-id="85911-129"><dt>cker</dt></span><span class="sxs-lookup"><span data-stu-id="85911-129"><dt>p</dt></span></span> </dl> | <span data-ttu-id="85911-130">Terminal Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="85911-130">Terminal properties.</span></span><br/>                                                |
| <dl> <span data-ttu-id="85911-131"><dt>Ramelow</dt></span><span class="sxs-lookup"><span data-stu-id="85911-131"><dt>v</dt></span></span> </dl> | <span data-ttu-id="85911-132">Ausführliche Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="85911-132">Verbose output.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="85911-133"><dt>x</dt></span><span class="sxs-lookup"><span data-stu-id="85911-133"><dt>x</dt></span></span> </dl> | <span data-ttu-id="85911-134">Zusätzliche Debuginformationen.</span><span class="sxs-lookup"><span data-stu-id="85911-134">Extra debugging information.</span></span> <span data-ttu-id="85911-135">Nur verfügbar auf Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="85911-135">Only available on Windows Server 2003.</span></span><br/> |
| <dl> <span data-ttu-id="85911-136"><dt>!</dt></span><span class="sxs-lookup"><span data-stu-id="85911-136"><dt>!</dt></span></span> </dl> | <span data-ttu-id="85911-137">Leeren Sie jede Zeile in das Protokoll.</span><span class="sxs-lookup"><span data-stu-id="85911-137">Flush each line to the log.</span></span><br/>                                         |



 

## <a name="remarks"></a><span data-ttu-id="85911-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85911-138">Remarks</span></span>

<span data-ttu-id="85911-139">Diese Eigenschaft ist ab Windows Installer 4,0 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="85911-139">This property is available starting with Windows Installer 4.0.</span></span>

<span data-ttu-id="85911-140">Sie können die Werte "+" und " \* " der/L-Option nicht im Wert der **MsiLogging** -Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="85911-140">You cannot use the "+" and "\*" values of the /L option in the value of the **MsiLogging** property.</span></span>

<span data-ttu-id="85911-141">Der Protokollierungs Modus kann mithilfe von Richtlinie, einer Befehlszeilenoption oder Programm gesteuert festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="85911-141">The logging mode can be set using policy, a command-line option, or programmatically.</span></span> <span data-ttu-id="85911-142">Dies überschreibt den Standard Protokollierungs Modus.</span><span class="sxs-lookup"><span data-stu-id="85911-142">This overrides the default logging mode.</span></span> <span data-ttu-id="85911-143">Weitere Informationen zu allen Methoden, die zum Festlegen des Protokollierungs Modus verfügbar sind, finden Sie unter [normale Protokollierung](normal-logging.md) im Abschnitt [Windows Installer Protokollierung](windows-installer-logging.md) .</span><span class="sxs-lookup"><span data-stu-id="85911-143">For more information about all the methods that are available for setting the logging mode, see [Normal Logging](normal-logging.md) in the [Windows Installer Logging](windows-installer-logging.md) section.</span></span>

<span data-ttu-id="85911-144">Wenn die **MsiLogging** -Eigenschaft in der [Eigenschaften Tabelle](property-table.md)vorhanden ist, kann der Standard Protokollierungs Modus des Pakets durch Ändern des Werts dieser Eigenschaft mithilfe einer [Daten Bank Transformation](database-transforms.md)geändert werden.</span><span class="sxs-lookup"><span data-stu-id="85911-144">If the **MsiLogging** property is present in the [Property table](property-table.md), the default logging mode of the package can be modified by changing the value of this property using a [database transform](database-transforms.md).</span></span> <span data-ttu-id="85911-145">Der Standard Protokollierungs Modus kann nicht mithilfe eines [Patchpakets](patch-packages.md) (MSP-Datei) geändert werden.</span><span class="sxs-lookup"><span data-stu-id="85911-145">The default logging mode cannot be changed using a [Patch Package](patch-packages.md) (a .msp file.)</span></span>

<span data-ttu-id="85911-146">Wenn die **MsiLogging** -Eigenschaft in der [Eigenschaften Tabelle](property-table.md)festgelegt wurde, kann der Standard Protokollierungs Modus für alle Benutzer des Computers durch Festlegen der Richtlinie " [disableloggingfrompackage](disableloggingfrompackage.md) " und der [Protokollierungs](logging.md) Richtlinie angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="85911-146">If the **MsiLogging** property has been set in the [Property table](property-table.md), the default logging mode for all users of the computer can be specified by setting both the [DisableLoggingFromPackage](disableloggingfrompackage.md) policy and [Logging](logging.md) policy.</span></span> <span data-ttu-id="85911-147">Durch das Festlegen der disableloggingfrompackage-Richtlinie und der Protokollierungs Richtlinie wird die **MsiLogging** -Eigenschaft für alle Pakete überschrieben.</span><span class="sxs-lookup"><span data-stu-id="85911-147">Setting both the DisableLoggingFromPackage policy and Logging policy will override the **MsiLogging** property for all packages.</span></span>

## <a name="requirements"></a><span data-ttu-id="85911-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85911-148">Requirements</span></span>



| <span data-ttu-id="85911-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85911-149">Requirement</span></span> | <span data-ttu-id="85911-150">Wert</span><span class="sxs-lookup"><span data-stu-id="85911-150">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85911-151">Version</span><span class="sxs-lookup"><span data-stu-id="85911-151">Version</span></span><br/> | <span data-ttu-id="85911-152">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="85911-152">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="85911-153">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="85911-153">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="85911-154">Windows Installer 4,5 unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="85911-154">Windows Installer 4.5 on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="85911-155">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="85911-155">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="85911-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85911-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85911-157">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="85911-157">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="85911-158">Wird in Windows Installer 3,1 und früheren Versionen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="85911-158">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




