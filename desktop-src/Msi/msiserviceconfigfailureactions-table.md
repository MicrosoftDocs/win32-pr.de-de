---
description: In der msiserviceconfigfailureactions-Tabelle sind die Vorgänge aufgeführt, die ausgeführt werden, nachdem ein Dienst fehlgeschlagen ist. Die in dieser Tabelle angegebenen Vorgänge werden beim nächsten Start des Systems ausgeführt.
ms.assetid: 7c450b74-1f91-4a1c-beee-646a407eb8a8
title: Msiserviceconfigfailureactions-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae55d095e227611271de35d673289fc9eb5b174e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353868"
---
# <a name="msiserviceconfigfailureactions-table"></a><span data-ttu-id="42e58-104">Msiserviceconfigfailureactions-Tabelle</span><span class="sxs-lookup"><span data-stu-id="42e58-104">MsiServiceConfigFailureActions Table</span></span>

<span data-ttu-id="42e58-105">In der msiserviceconfigfailureactions-Tabelle sind die Vorgänge aufgeführt, die ausgeführt werden, nachdem ein Dienst fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="42e58-105">The MsiServiceConfigFailureActions table lists operations to be run after a service fails.</span></span> <span data-ttu-id="42e58-106">Die in dieser Tabelle angegebenen Vorgänge werden beim nächsten Start des Systems ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="42e58-106">The operations specified in this table run the next time the system is started.</span></span>

<span data-ttu-id="42e58-107">**[Windows Installer 4,5 oder früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="42e58-107">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="42e58-108">Diese Tabelle ist ab Windows Installer 5,0 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="42e58-108">This table is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="42e58-109">Die msiserviceconfigfailureactions-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="42e58-109">The MsiServiceConfigFailureActions table has the following columns.</span></span>



| <span data-ttu-id="42e58-110">Spalte</span><span class="sxs-lookup"><span data-stu-id="42e58-110">Column</span></span>                         | <span data-ttu-id="42e58-111">Typ</span><span class="sxs-lookup"><span data-stu-id="42e58-111">Type</span></span>                         | <span data-ttu-id="42e58-112">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="42e58-112">Key</span></span> | <span data-ttu-id="42e58-113">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="42e58-113">Nullable</span></span> |
|--------------------------------|------------------------------|-----|----------|
| <span data-ttu-id="42e58-114">Msiserviceconfigfailureactions</span><span class="sxs-lookup"><span data-stu-id="42e58-114">MsiServiceConfigFailureActions</span></span> | [<span data-ttu-id="42e58-115">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="42e58-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="42e58-116">J</span><span class="sxs-lookup"><span data-stu-id="42e58-116">Y</span></span>   | <span data-ttu-id="42e58-117">N</span><span class="sxs-lookup"><span data-stu-id="42e58-117">N</span></span>        |
| <span data-ttu-id="42e58-118">Name</span><span class="sxs-lookup"><span data-stu-id="42e58-118">Name</span></span>                           | [<span data-ttu-id="42e58-119">Großformatige</span><span class="sxs-lookup"><span data-stu-id="42e58-119">Formatted</span></span>](formatted.md)   | <span data-ttu-id="42e58-120">N</span><span class="sxs-lookup"><span data-stu-id="42e58-120">N</span></span>   | <span data-ttu-id="42e58-121">N</span><span class="sxs-lookup"><span data-stu-id="42e58-121">N</span></span>        |
| <span data-ttu-id="42e58-122">Ereignis</span><span class="sxs-lookup"><span data-stu-id="42e58-122">Event</span></span>                          | [<span data-ttu-id="42e58-123">Integer</span><span class="sxs-lookup"><span data-stu-id="42e58-123">Integer</span></span>](integer.md)       | <span data-ttu-id="42e58-124">N</span><span class="sxs-lookup"><span data-stu-id="42e58-124">N</span></span>   | <span data-ttu-id="42e58-125">N</span><span class="sxs-lookup"><span data-stu-id="42e58-125">N</span></span>        |
| <span data-ttu-id="42e58-126">Resetperiod</span><span class="sxs-lookup"><span data-stu-id="42e58-126">ResetPeriod</span></span>                    | [<span data-ttu-id="42e58-127">Integer</span><span class="sxs-lookup"><span data-stu-id="42e58-127">Integer</span></span>](integer.md)       | <span data-ttu-id="42e58-128">N</span><span class="sxs-lookup"><span data-stu-id="42e58-128">N</span></span>   | <span data-ttu-id="42e58-129">J</span><span class="sxs-lookup"><span data-stu-id="42e58-129">Y</span></span>        |
| <span data-ttu-id="42e58-130">Rebootmessage</span><span class="sxs-lookup"><span data-stu-id="42e58-130">RebootMessage</span></span>                  | [<span data-ttu-id="42e58-131">Großformatige</span><span class="sxs-lookup"><span data-stu-id="42e58-131">Formatted</span></span>](formatted.md)   | <span data-ttu-id="42e58-132">N</span><span class="sxs-lookup"><span data-stu-id="42e58-132">N</span></span>   | <span data-ttu-id="42e58-133">J</span><span class="sxs-lookup"><span data-stu-id="42e58-133">Y</span></span>        |
| <span data-ttu-id="42e58-134">Get-Help</span><span class="sxs-lookup"><span data-stu-id="42e58-134">Command</span></span>                        | [<span data-ttu-id="42e58-135">Großformatige</span><span class="sxs-lookup"><span data-stu-id="42e58-135">Formatted</span></span>](formatted.md)   | <span data-ttu-id="42e58-136">N</span><span class="sxs-lookup"><span data-stu-id="42e58-136">N</span></span>   | <span data-ttu-id="42e58-137">J</span><span class="sxs-lookup"><span data-stu-id="42e58-137">Y</span></span>        |
| <span data-ttu-id="42e58-138">Aktionen</span><span class="sxs-lookup"><span data-stu-id="42e58-138">Actions</span></span>                        | [<span data-ttu-id="42e58-139">Text</span><span class="sxs-lookup"><span data-stu-id="42e58-139">Text</span></span>](text.md)             | <span data-ttu-id="42e58-140">N</span><span class="sxs-lookup"><span data-stu-id="42e58-140">N</span></span>   | <span data-ttu-id="42e58-141">J</span><span class="sxs-lookup"><span data-stu-id="42e58-141">Y</span></span>        |
| <span data-ttu-id="42e58-142">Delta Actions</span><span class="sxs-lookup"><span data-stu-id="42e58-142">DelayActions</span></span>                   | [<span data-ttu-id="42e58-143">Text</span><span class="sxs-lookup"><span data-stu-id="42e58-143">Text</span></span>](text.md)             | <span data-ttu-id="42e58-144">N</span><span class="sxs-lookup"><span data-stu-id="42e58-144">N</span></span>   | <span data-ttu-id="42e58-145">J</span><span class="sxs-lookup"><span data-stu-id="42e58-145">Y</span></span>        |
| <span data-ttu-id="42e58-146">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="42e58-146">Component\_</span></span>                    | [<span data-ttu-id="42e58-147">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="42e58-147">Identifier</span></span>](identifier.md) | <span data-ttu-id="42e58-148">N</span><span class="sxs-lookup"><span data-stu-id="42e58-148">N</span></span>   | <span data-ttu-id="42e58-149">N</span><span class="sxs-lookup"><span data-stu-id="42e58-149">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="42e58-150">Spalten</span><span class="sxs-lookup"><span data-stu-id="42e58-150">Columns</span></span>

<dl> <dt>

<span data-ttu-id="42e58-151"><span id="MsiServiceConfigFailureActions"></span><span id="msiserviceconfigfailureactions"></span><span id="MSISERVICECONFIGFAILUREACTIONS"></span>Msiserviceconfigfailureactions</span><span class="sxs-lookup"><span data-stu-id="42e58-151"><span id="MsiServiceConfigFailureActions"></span><span id="msiserviceconfigfailureactions"></span><span id="MSISERVICECONFIGFAILUREACTIONS"></span>MsiServiceConfigFailureActions</span></span>
</dt> <dd>

<span data-ttu-id="42e58-152">Dies ist der Primärschlüssel dieser Tabelle, der eine Fehler Aktion identifiziert.</span><span class="sxs-lookup"><span data-stu-id="42e58-152">This is the primary key of this table that identifies a failure action.</span></span>

</dd> <dt>

<span data-ttu-id="42e58-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Benennen</span><span class="sxs-lookup"><span data-stu-id="42e58-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="42e58-154">Diese Spalte enthält den Namen eines dienstanteils, der Teil dieses Pakets ist oder bereits installiert ist.</span><span class="sxs-lookup"><span data-stu-id="42e58-154">This column contains the name of a service that is a part of this package or that is already is installed.</span></span>

</dd> <dt>

<span data-ttu-id="42e58-155"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Veranstalter</span><span class="sxs-lookup"><span data-stu-id="42e58-155"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Event</span></span>
</dt> <dd>

<span data-ttu-id="42e58-156">Diese Spalte gibt an, wann die Konfiguration des Dienstanbieter geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="42e58-156">This column specifies when to change the service's configuration.</span></span> <span data-ttu-id="42e58-157">Die folgenden Werte sind Bitfelder, die kombiniert werden können, um mehrere Vorgänge darzustellen.</span><span class="sxs-lookup"><span data-stu-id="42e58-157">The following values are bit fields that can be combined to represent multiple operations.</span></span> <span data-ttu-id="42e58-158">Alle anderen Bitfeldwerte werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="42e58-158">Any other bit field values are ignored.</span></span>



| <span data-ttu-id="42e58-159">Konstante</span><span class="sxs-lookup"><span data-stu-id="42e58-159">Constant</span></span>                                         | <span data-ttu-id="42e58-160">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="42e58-160">Description</span></span>                                     |
|--------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="42e58-161">**msidbserviceconfgeventinstall** 1</span><span class="sxs-lookup"><span data-stu-id="42e58-161">**msidbServiceConfigEventInstall** 1</span></span><br/>   | <span data-ttu-id="42e58-162">Änderung während der Installation der Komponente.</span><span class="sxs-lookup"><span data-stu-id="42e58-162">Change during installation of the component.</span></span>    |
| <span data-ttu-id="42e58-163">**msidbserviceconfgeventuninstall** 2</span><span class="sxs-lookup"><span data-stu-id="42e58-163">**msidbServiceConfigEventUninstall** 2</span></span><br/> | <span data-ttu-id="42e58-164">Änderung während der deinstalstallation der Komponente.</span><span class="sxs-lookup"><span data-stu-id="42e58-164">Change during uninstallation of the component.</span></span>  |
| <span data-ttu-id="42e58-165">**msidbserviceconfgeventreinstall** 4</span><span class="sxs-lookup"><span data-stu-id="42e58-165">**msidbServiceConfigEventReinstall** 4</span></span><br/> | <span data-ttu-id="42e58-166">Änderung während der erneuten Installation der Komponente.</span><span class="sxs-lookup"><span data-stu-id="42e58-166">Change during re-installation of the component.</span></span> |



 

</dd> <dt>

<span data-ttu-id="42e58-167"><span id="ResetPeriod"></span><span id="resetperiod"></span><span id="RESETPERIOD"></span>Resetperiod</span><span class="sxs-lookup"><span data-stu-id="42e58-167"><span id="ResetPeriod"></span><span id="resetperiod"></span><span id="RESETPERIOD"></span>ResetPeriod</span></span>
</dt> <dd>

<span data-ttu-id="42e58-168">Der Zurücksetzungs Zeitraum (in Sekunden) der Fehler Anzahl für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="42e58-168">The reset period in seconds of service's failure count.</span></span> <span data-ttu-id="42e58-169">Der [Dienststeuerungs-Manager (Service Control Manager](../services/service-control-manager.md) , SCM) zählt, wie oft der Dienst seit dem letzten Neustart des Systems fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="42e58-169">The [Service Control Manager](../services/service-control-manager.md) (SCM) counts the number of times each service has failed since the system was last restarted.</span></span> <span data-ttu-id="42e58-170">Die Anzahl wird auf 0 (null) zurückgesetzt, wenn der Dienst für den Zurücksetzungs Zeitraum nicht ausfällt.</span><span class="sxs-lookup"><span data-stu-id="42e58-170">The count is reset to zero if the service does not fail for the reset period.</span></span> <span data-ttu-id="42e58-171">Wenn der Dienst für die n-te Zeit fehlschlägt, führt das System die Aktion aus, die im \[ -Element N-1 des Arrays angegeben ist, das \] im Aktionsfeld angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="42e58-171">When the service fails for the Nth time, the system performs the action specified in the element \[N-1\] of the array specified in the Actions field.</span></span>

<span data-ttu-id="42e58-172">Lassen Sie das Feld resetperiod leer, um anzugeben, dass die Fehler Anzahl nie zurückgesetzt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="42e58-172">Leave ResetPeriod field empty to indicate that failure count should never be reset.</span></span>

</dd> <dt>

<span data-ttu-id="42e58-173"><span id="RebootMessage"></span><span id="rebootmessage"></span><span id="REBOOTMESSAGE"></span>Rebootmessage</span><span class="sxs-lookup"><span data-stu-id="42e58-173"><span id="RebootMessage"></span><span id="rebootmessage"></span><span id="REBOOTMESSAGE"></span>RebootMessage</span></span>
</dt> <dd>

<span data-ttu-id="42e58-174">Die Nachricht, die vor dem Neustart des Computers als Reaktion auf eine Aktion **zum \_ \_ Neustart der SC-Aktion** gesendet wurde, die in der Spalte Aktionen angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="42e58-174">The message sent to users before restarting the computer in response to a **SC\_ACTION\_REBOOT** action specified in the Actions column.</span></span> <span data-ttu-id="42e58-175">Sie können eine leere Zeichenfolge ("") verwenden, um die aktuelle Nachricht unverändert zu senden.</span><span class="sxs-lookup"><span data-stu-id="42e58-175">You can use an empty string, "", to send the current message unchanged.</span></span> <span data-ttu-id="42e58-176">Sie können \[ ~ \] die Syntax des [formatierten](formatted.md) Datentyps verwenden, um die aktuelle Nachricht zu löschen und keine Nachricht zu senden.</span><span class="sxs-lookup"><span data-stu-id="42e58-176">You can use \[~\] syntax of the [Formatted](formatted.md) data type to delete the current message and send no message.</span></span>

</dd> <dt>

<span data-ttu-id="42e58-177"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>S</span><span class="sxs-lookup"><span data-stu-id="42e58-177"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>Command</span></span>
</dt> <dd>

<span data-ttu-id="42e58-178">Die Befehlszeile, die von dem Prozess ausgeführt wird [**, der von der Funktion "**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) up" als Antwort auf eine Aktion zum **Ausführen eines SC- \_ Aktions \_ \_ Befehls** erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="42e58-178">The command line run by the process created by the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function in response to a **SC\_ACTION\_RUN\_COMMAND** action specified in the Actions column.</span></span> <span data-ttu-id="42e58-179">Der neue Prozess wird unter dem gleichen Konto ausgeführt wie der Dienst und nur dann, wenn das Aktionsfeld den **\_ \_ \_ Befehl SC Action Run** hat.</span><span class="sxs-lookup"><span data-stu-id="42e58-179">The new process runs under the same account as the service and only if the Action field is **SC\_ACTION\_RUN\_COMMAND**.</span></span> <span data-ttu-id="42e58-180">Sie können eine leere Zeichenfolge ("") verwenden, um die aktuelle Befehlszeile unverändert zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="42e58-180">You can use an empty string, "", to use the current command line unchanged.</span></span> <span data-ttu-id="42e58-181">Sie können \[ ~ \] die Syntax des [formatierten](formatted.md) Datentyps verwenden, um die aktuelle Befehlszeile zu löschen und keinen Vorgang auszuführen, wenn der Dienst fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="42e58-181">You can use \[~\] syntax of the [Formatted](formatted.md) data type to delete the current command line and run no operation when the service fails.</span></span>

</dd> <dt>

<span data-ttu-id="42e58-182"><span id="Actions"></span><span id="actions"></span><span id="ACTIONS"></span>Handlungs</span><span class="sxs-lookup"><span data-stu-id="42e58-182"><span id="Actions"></span><span id="actions"></span><span id="ACTIONS"></span>Actions</span></span>
</dt> <dd>

<span data-ttu-id="42e58-183">Dieses Feld enthält ein Array von ganzzahligen Werten, die die Aktionen angeben, die vom SCM durchgeführt werden, wenn der Dienst fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="42e58-183">This field contains an array of integer values that specify the actions taken by the SCM if the service fails.</span></span> <span data-ttu-id="42e58-184">Trennen Sie die Werte im Array durch \[ ~ \] .</span><span class="sxs-lookup"><span data-stu-id="42e58-184">Separate the values in the array by \[~\].</span></span> <span data-ttu-id="42e58-185">Der ganzzahlige Wert im Nth-Element des Arrays gibt die Aktion an, die ausgeführt wird, wenn der Dienst für die n-te Zeit fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="42e58-185">The integer value in the Nth element of the array specifies the action performed when the service fails for the Nth time.</span></span> <span data-ttu-id="42e58-186">Jeder Member des Arrays ist einer der folgenden ganzzahligen Werte.</span><span class="sxs-lookup"><span data-stu-id="42e58-186">Each member of the array is one of following integer values.</span></span>



| <span data-ttu-id="42e58-187">Konstante</span><span class="sxs-lookup"><span data-stu-id="42e58-187">Constant</span></span>                                 | <span data-ttu-id="42e58-188">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="42e58-188">Description</span></span>           |
|------------------------------------------|-----------------------|
| <span data-ttu-id="42e58-189">**SC \_ Aktion " \_ None** 0"</span><span class="sxs-lookup"><span data-stu-id="42e58-189">**SC\_ACTION\_NONE** 0</span></span><br/>         | <span data-ttu-id="42e58-190">Keine Aktion.</span><span class="sxs-lookup"><span data-stu-id="42e58-190">No action.</span></span>            |
| <span data-ttu-id="42e58-191">**SC \_ Aktions \_ Neustart** 2</span><span class="sxs-lookup"><span data-stu-id="42e58-191">**SC\_ACTION\_REBOOT** 2</span></span><br/>       | <span data-ttu-id="42e58-192">Starten Sie den Computer neu.</span><span class="sxs-lookup"><span data-stu-id="42e58-192">Restart the computer.</span></span> |
| <span data-ttu-id="42e58-193">**SC \_ Aktion \_ neu starten** 1</span><span class="sxs-lookup"><span data-stu-id="42e58-193">**SC\_ACTION\_RESTART** 1</span></span><br/>      | <span data-ttu-id="42e58-194">Starten Sie den Dienst neu.</span><span class="sxs-lookup"><span data-stu-id="42e58-194">Restart the service.</span></span>  |
| <span data-ttu-id="42e58-195">**SC \_ \_ \_ Befehl zum Ausführen von Aktionen** 3</span><span class="sxs-lookup"><span data-stu-id="42e58-195">**SC\_ACTION\_RUN\_COMMAND** 3</span></span><br/> | <span data-ttu-id="42e58-196">Führen Sie einen Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="42e58-196">Run a command.</span></span>        |



 

</dd> <dt>

<span data-ttu-id="42e58-197"><span id="DelayActions"></span><span id="delayactions"></span><span id="DELAYACTIONS"></span>Delta Actions</span><span class="sxs-lookup"><span data-stu-id="42e58-197"><span id="DelayActions"></span><span id="delayactions"></span><span id="DELAYACTIONS"></span>DelayActions</span></span>
</dt> <dd>

<span data-ttu-id="42e58-198">Dieses Feld enthält ein Array von ganzzahligen Werten, die die Zeit in Millisekunden angeben, die gewartet werden soll, bevor die in der Aktionsspalte angegebene Aktion durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="42e58-198">This field contains an array of integer values that specify the time in milliseconds to wait before performing the action specified in the Action column.</span></span> <span data-ttu-id="42e58-199">Trennen Sie die Werte im Array durch \[ ~ \] .</span><span class="sxs-lookup"><span data-stu-id="42e58-199">Separate the values in the array by \[~\].</span></span> <span data-ttu-id="42e58-200">Die Anzahl der Elemente im delayactions-Array muss gleich der Anzahl der Elemente im Aktions Array sein.</span><span class="sxs-lookup"><span data-stu-id="42e58-200">The number of elements in the DelayActions array must be equal to the number of elements in the Actions array.</span></span> <span data-ttu-id="42e58-201">Das n-te Element des delayactions-Arrays gibt die Zeitverzögerung für das n-te Element des Aktions Arrays an.</span><span class="sxs-lookup"><span data-stu-id="42e58-201">The Nth element of the DelayActions array specifies the time delay for the nth element of the Actions array.</span></span>

</dd> <dt>

<span data-ttu-id="42e58-202"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_</span><span class="sxs-lookup"><span data-stu-id="42e58-202"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="42e58-203">Externer Schlüssel für Spalte einer der [Komponenten Tabellen](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="42e58-203">External key to column one of the [Component Table](component-table.md).</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="42e58-204">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="42e58-204">Validation</span></span>

<dl>

[<span data-ttu-id="42e58-205">ICE102</span><span class="sxs-lookup"><span data-stu-id="42e58-205">ICE102</span></span>](ice-102.md)  
[<span data-ttu-id="42e58-206">ICE03</span><span class="sxs-lookup"><span data-stu-id="42e58-206">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="42e58-207">ICE06</span><span class="sxs-lookup"><span data-stu-id="42e58-207">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="42e58-208">ICE32</span><span class="sxs-lookup"><span data-stu-id="42e58-208">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="42e58-209">ICE45</span><span class="sxs-lookup"><span data-stu-id="42e58-209">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="42e58-210">ICE46</span><span class="sxs-lookup"><span data-stu-id="42e58-210">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="42e58-211">ICE69</span><span class="sxs-lookup"><span data-stu-id="42e58-211">ICE69</span></span>](ice69.md)  
</dl>

 

 
