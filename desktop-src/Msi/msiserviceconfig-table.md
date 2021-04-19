---
description: Die msiserviceconfig-Tabelle konfiguriert einen Dienst, der vom aktuellen Paket installiert oder installiert wird.
ms.assetid: 0d9fd005-9326-4a18-8496-35b5d1927f47
title: Msiserviceconfig-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 357b6787e56d52a893dd1a118a3e2fcbc13379e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360736"
---
# <a name="msiserviceconfig-table"></a><span data-ttu-id="79856-103">Msiserviceconfig-Tabelle</span><span class="sxs-lookup"><span data-stu-id="79856-103">MsiServiceConfig Table</span></span>

<span data-ttu-id="79856-104">Die msiserviceconfig-Tabelle konfiguriert einen Dienst, der vom aktuellen Paket installiert oder installiert wird.</span><span class="sxs-lookup"><span data-stu-id="79856-104">The MsiServiceConfig table configures a service that is installed or being installed by the current package.</span></span>

<span data-ttu-id="79856-105">**[Windows Installer 4,5 oder früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="79856-105">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="79856-106">Diese Tabelle ist ab Windows Installer 5,0 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="79856-106">This table is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="79856-107">Die msiserviceconfig-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="79856-107">The MsiServiceConfig table has the following columns.</span></span>



| <span data-ttu-id="79856-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="79856-108">Column</span></span>           | <span data-ttu-id="79856-109">Typ</span><span class="sxs-lookup"><span data-stu-id="79856-109">Type</span></span>                         | <span data-ttu-id="79856-110">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="79856-110">Key</span></span> | <span data-ttu-id="79856-111">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="79856-111">Nullable</span></span> |
|------------------|------------------------------|-----|----------|
| <span data-ttu-id="79856-112">Msiserviceconfig</span><span class="sxs-lookup"><span data-stu-id="79856-112">MsiServiceConfig</span></span> | [<span data-ttu-id="79856-113">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="79856-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="79856-114">J</span><span class="sxs-lookup"><span data-stu-id="79856-114">Y</span></span>   | <span data-ttu-id="79856-115">N</span><span class="sxs-lookup"><span data-stu-id="79856-115">N</span></span>        |
| <span data-ttu-id="79856-116">Name</span><span class="sxs-lookup"><span data-stu-id="79856-116">Name</span></span>             | [<span data-ttu-id="79856-117">Großformatige</span><span class="sxs-lookup"><span data-stu-id="79856-117">Formatted</span></span>](formatted.md)   | <span data-ttu-id="79856-118">N</span><span class="sxs-lookup"><span data-stu-id="79856-118">N</span></span>   | <span data-ttu-id="79856-119">N</span><span class="sxs-lookup"><span data-stu-id="79856-119">N</span></span>        |
| <span data-ttu-id="79856-120">Ereignis</span><span class="sxs-lookup"><span data-stu-id="79856-120">Event</span></span>            | [<span data-ttu-id="79856-121">Integer</span><span class="sxs-lookup"><span data-stu-id="79856-121">Integer</span></span>](integer.md)       | <span data-ttu-id="79856-122">N</span><span class="sxs-lookup"><span data-stu-id="79856-122">N</span></span>   | <span data-ttu-id="79856-123">N</span><span class="sxs-lookup"><span data-stu-id="79856-123">N</span></span>        |
| <span data-ttu-id="79856-124">ConfigType</span><span class="sxs-lookup"><span data-stu-id="79856-124">ConfigType</span></span>       | [<span data-ttu-id="79856-125">Integer</span><span class="sxs-lookup"><span data-stu-id="79856-125">Integer</span></span>](integer.md)       | <span data-ttu-id="79856-126">N</span><span class="sxs-lookup"><span data-stu-id="79856-126">N</span></span>   | <span data-ttu-id="79856-127">N</span><span class="sxs-lookup"><span data-stu-id="79856-127">N</span></span>        |
| <span data-ttu-id="79856-128">Argument</span><span class="sxs-lookup"><span data-stu-id="79856-128">Argument</span></span>         | [<span data-ttu-id="79856-129">Großformatige</span><span class="sxs-lookup"><span data-stu-id="79856-129">Formatted</span></span>](formatted.md)   | <span data-ttu-id="79856-130">N</span><span class="sxs-lookup"><span data-stu-id="79856-130">N</span></span>   | <span data-ttu-id="79856-131">J</span><span class="sxs-lookup"><span data-stu-id="79856-131">Y</span></span>        |
| <span data-ttu-id="79856-132">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="79856-132">Component\_</span></span>      | [<span data-ttu-id="79856-133">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="79856-133">Identifier</span></span>](identifier.md) | <span data-ttu-id="79856-134">N</span><span class="sxs-lookup"><span data-stu-id="79856-134">N</span></span>   | <span data-ttu-id="79856-135">N</span><span class="sxs-lookup"><span data-stu-id="79856-135">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="79856-136">Spalten</span><span class="sxs-lookup"><span data-stu-id="79856-136">Columns</span></span>

<dl> <dt>

<span data-ttu-id="79856-137"><span id="MsiServiceConfig"></span><span id="msiserviceconfig"></span><span id="MSISERVICECONFIG"></span>Msiserviceconfig</span><span class="sxs-lookup"><span data-stu-id="79856-137"><span id="MsiServiceConfig"></span><span id="msiserviceconfig"></span><span id="MSISERVICECONFIG"></span>MsiServiceConfig</span></span>
</dt> <dd>

<span data-ttu-id="79856-138">Dies ist der Primärschlüssel dieser Tabelle.</span><span class="sxs-lookup"><span data-stu-id="79856-138">This is the primary key of this table.</span></span>

</dd> <dt>

<span data-ttu-id="79856-139"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Benennen</span><span class="sxs-lookup"><span data-stu-id="79856-139"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="79856-140">Diese Spalte enthält den Namen eines dienstanteils, der Teil dieses Pakets ist oder bereits installiert ist.</span><span class="sxs-lookup"><span data-stu-id="79856-140">This column contains the name of a service that is a part of this package or that is already is installed.</span></span>

</dd> <dt>

<span data-ttu-id="79856-141"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Veranstalter</span><span class="sxs-lookup"><span data-stu-id="79856-141"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Event</span></span>
</dt> <dd>

<span data-ttu-id="79856-142">Diese Spalte gibt an, wann die Dienst Konfiguration geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="79856-142">This column specifies when to change the service configuration.</span></span> <span data-ttu-id="79856-143">Die folgenden Werte können kombiniert werden, um mehrere Vorgänge darzustellen.</span><span class="sxs-lookup"><span data-stu-id="79856-143">The following values can be combined to represent multiple operations.</span></span> <span data-ttu-id="79856-144">Alle darin enthaltenen Werte werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="79856-144">Any values included other than these are ignored.</span></span>



| <span data-ttu-id="79856-145">Konstante</span><span class="sxs-lookup"><span data-stu-id="79856-145">Constant</span></span>                                         | <span data-ttu-id="79856-146">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79856-146">Description</span></span>                                              |
|--------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="79856-147">**msidbserviceconfgeventinstall** 1</span><span class="sxs-lookup"><span data-stu-id="79856-147">**msidbServiceConfigEventInstall** 1</span></span><br/>   | <span data-ttu-id="79856-148">Führt die Aktion während der Installation der Komponente aus.</span><span class="sxs-lookup"><span data-stu-id="79856-148">Takes the action during installation of the component.</span></span>   |
| <span data-ttu-id="79856-149">**msidbserviceconfgeventuninstall** 2</span><span class="sxs-lookup"><span data-stu-id="79856-149">**msidbServiceConfigEventUninstall** 2</span></span><br/> | <span data-ttu-id="79856-150">Führt die Aktion während der deinstalstallation der Komponente aus.</span><span class="sxs-lookup"><span data-stu-id="79856-150">Takes the action during uninstallation of the component.</span></span> |
| <span data-ttu-id="79856-151">**msidbserviceconfgeventreinstall** 4</span><span class="sxs-lookup"><span data-stu-id="79856-151">**msidbServiceConfigEventReinstall** 4</span></span><br/> | <span data-ttu-id="79856-152">Führt die Aktion während der erneuten Installation der Komponente aus.</span><span class="sxs-lookup"><span data-stu-id="79856-152">Takes the action during reinstallation of the component.</span></span> |



 

</dd> <dt>

<span data-ttu-id="79856-153"><span id="ConfigType"></span><span id="configtype"></span><span id="CONFIGTYPE"></span>ConfigType</span><span class="sxs-lookup"><span data-stu-id="79856-153"><span id="ConfigType"></span><span id="configtype"></span><span id="CONFIGTYPE"></span>ConfigType</span></span>
</dt> <dd>

<span data-ttu-id="79856-154">Der Wert in diesem Feld, in Kombination mit dem Wert im Feld Argumente, gibt an, welche Änderung an der Dienst Konfiguration vorgenommen werden soll.</span><span class="sxs-lookup"><span data-stu-id="79856-154">The value in this field, combined with the value in the Arguments field, specify what change to make to the service configuration.</span></span> <span data-ttu-id="79856-155">Die angegebene Änderung wird wirksam, wenn das System das nächste Mal gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="79856-155">The specified change takes effect the next time the system is started.</span></span>



| <span data-ttu-id="79856-156">Config</span><span class="sxs-lookup"><span data-stu-id="79856-156">Config</span></span>                                                      | <span data-ttu-id="79856-157">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79856-157">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79856-158">**Dienst \_ Konfigurations \_ Verzögertes \_ Automatisches \_ starten** 3</span><span class="sxs-lookup"><span data-stu-id="79856-158">**SERVICE\_CONFIG\_DELAYED\_AUTO\_START** 3</span></span><br/>       | <span data-ttu-id="79856-159">Konfigurieren Sie die Zeitverzögerung eines [automatischen Start Dienstanbieter](../services/automatically-starting-services.md).</span><span class="sxs-lookup"><span data-stu-id="79856-159">Configure the time delay of an [auto-start service](../services/automatically-starting-services.md).</span></span> <br/> <span data-ttu-id="79856-160">Geben Sie im Feld Argument den Wert 1 ein, um den Dienst nach anderen automatischen Start Diensten und einer Zeitverzögerung zu starten.</span><span class="sxs-lookup"><span data-stu-id="79856-160">Enter 1 in the Argument field to start the service after other auto-start services plus a time delay.</span></span> <br/> <span data-ttu-id="79856-161">Geben Sie im Feld Argument den Wert 0 ein, um die Verzögerung für den automatischen Start Dienst zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="79856-161">Enter 0 in the Argument field to turn off the auto-start service delay.</span></span><br/> <span data-ttu-id="79856-162">Gilt nur für installierte Auto Start Dienste oder Dienste, die von diesem Paket mit **dem \_ automatischen \_ Start des Diensts** im Feld StartType der [Tabelle ServiceInstall](serviceinstall-table.md)installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="79856-162">Applies only to installed auto-start services or services installed by this package with **SERVICE\_AUTO\_START** in the StartType field of the [ServiceInstall table](serviceinstall-table.md).</span></span><br/>                                                                         |
| <span data-ttu-id="79856-163">**Dienst \_ Konfigurations \_ erforderliche \_ Berechtigungen \_ Info** 6</span><span class="sxs-lookup"><span data-stu-id="79856-163">**SERVICE\_CONFIG\_REQUIRED\_PRIVILEGES\_INFO** 6</span></span><br/> | <span data-ttu-id="79856-164">Ändern Sie die Liste der Berechtigungen, die für den Dienst erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="79856-164">Change the list of privileges required by the service.</span></span><br/> <span data-ttu-id="79856-165">Geben Sie eine Liste der angeforderten Berechtigungen in das Argument Feld ein.</span><span class="sxs-lookup"><span data-stu-id="79856-165">Enter a list of requested privileges in the Argument field.</span></span> <span data-ttu-id="79856-166">Der [formatierte](formatted.md) Zeichen folgen Wert im Feld Argument listet die [**Berechtigungs Konstanten**](../secauthz/privilege-constants.md) für die angeforderten Berechtigungen auf.</span><span class="sxs-lookup"><span data-stu-id="79856-166">The [Formatted](formatted.md) string value in the Argument field lists the [**Privilege Constants**](../secauthz/privilege-constants.md) for the requested privileges.</span></span> <span data-ttu-id="79856-167">Sie können die \[ ~ \] Syntax der [formatierten](formatted.md) Zeichenfolge verwenden, um ein NULL-Zeichen einzufügen.</span><span class="sxs-lookup"><span data-stu-id="79856-167">You can use the \[~\] syntax of the [Formatted](formatted.md) string to insert a null character.</span></span> <span data-ttu-id="79856-168">Trennen Sie die Berechtigungs Konstanten in der Liste durch \[ ~ \] .</span><span class="sxs-lookup"><span data-stu-id="79856-168">Separate the privilege constants in the list by \[~\].</span></span><br/>                                                                                                                              |
| <span data-ttu-id="79856-169">**Dienst \_ Konfigurations \_ Dienst- \_ sid \_ Informationen** 5</span><span class="sxs-lookup"><span data-stu-id="79856-169">**SERVICE\_CONFIG\_SERVICE\_SID\_INFO** 5</span></span><br/>         | <span data-ttu-id="79856-170">Fügen Sie dem Prozess Token, das diesen Dienst enthält, einen Dienst-SID-Typ hinzu.</span><span class="sxs-lookup"><span data-stu-id="79856-170">Add a service SID type to the process token containing this service.</span></span><br/> <span data-ttu-id="79856-171">Geben Sie im Feld Argument einen gültigen Dienst-SID-Typ für die [**Dienst- \_ sid- \_ Informations**](/windows/win32/api/winsvc/ns-winsvc-service_sid_info) Struktur ein: **Dienst-SID- \_ \_ Typ \_ None** (0x00), **Dienst-SID- \_ \_ Typ \_ eingeschränkt** (0x03) oder **Dienst-SID- \_ \_ Typ \_ uneingeschränkt** (0x01).</span><span class="sxs-lookup"><span data-stu-id="79856-171">Enter in the Argument field a valid service SID type for the [**SERVICE\_SID\_INFO**](/windows/win32/api/winsvc/ns-winsvc-service_sid_info) structure: **SERVICE\_SID\_TYPE\_NONE** (0x00), **SERVICE\_SID\_TYPE\_RESTRICTED** (0x03), or **SERVICE\_SID\_TYPE\_UNRESTRICTED** (0x01).</span></span> <br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="79856-172">**Dienst \_ Configuration \_ Preshutdown \_ Info** 7</span><span class="sxs-lookup"><span data-stu-id="79856-172">**SERVICE\_CONFIG\_PRESHUTDOWN\_INFO** 7</span></span><br/>          | <span data-ttu-id="79856-173">Konfigurieren Sie die Zeitspanne, die der [Dienststeuerungs-Manager](../services/service-control-manager.md) (SCM) wartet, bevor Sie mit anderen Shutdown-Vorgängen fortfahren.</span><span class="sxs-lookup"><span data-stu-id="79856-173">Configure the length of the time the [Service Control Manager](../services/service-control-manager.md) (SCM) waits before proceeding with other shutdown operations.</span></span> <span data-ttu-id="79856-174">Der SCM wartet in diesem Zeitraum nach dem Senden der Dienst Steuerungs Benachrichtigung vor dem **\_ \_ herunter** fahren an den Dienst.</span><span class="sxs-lookup"><span data-stu-id="79856-174">The SCM waits for this period of time after sending the **SERVICE\_CONTROL\_PRESHUTDOWN** notification to the service.</span></span> <br/> <span data-ttu-id="79856-175">Geben Sie die Zeitverzögerungs Länge (in Millisekunden) in das Argument Feld ein.</span><span class="sxs-lookup"><span data-stu-id="79856-175">Enter the time delay length, in milliseconds, in the Argument field.</span></span> <span data-ttu-id="79856-176">Belassen Sie das Argument Feld leer, um die Zeitverzögerung auf den Standardwert von 3 Minuten zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="79856-176">Leave the Argument field empty to reset the time delay to the default of 3 minutes.</span></span> <br/>                                                                                                                               |
| <span data-ttu-id="79856-177">**Dienst \_ Flag für Konfigurations \_ Fehler \_ Aktionen \_** 4</span><span class="sxs-lookup"><span data-stu-id="79856-177">**SERVICE\_CONFIG\_FAILURE\_ACTIONS\_FLAG** 4</span></span><br/>     | <span data-ttu-id="79856-178">Konfigurieren Sie, wann die Fehler Aktionen für diesen Dienst ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="79856-178">Configure when to run the failure actions for this service.</span></span> <span data-ttu-id="79856-179">Diese Einstellung wird ignoriert, wenn für den Dienst keine Fehler Aktionen konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="79856-179">This setting is ignored if the service has no configured failure actions.</span></span><br/> <span data-ttu-id="79856-180">Geben Sie 0 ein, um die Aktionen nur dann auszuführen, wenn der Dienst beendet wird, ohne den Berichterstattungs **Dienst \_**</span><span class="sxs-lookup"><span data-stu-id="79856-180">Enter 0 to run the actions only if the service terminates without reporting **SERVICE\_STOPPED**.</span></span><br/> <span data-ttu-id="79856-181">Geben Sie 1 ein, um die Aktionen auszuführen, wenn der Dienst beendet wird, dass der Bericht Erstellungs Dienst beendet wird und der **dwWin32ExitCode** -Member der [**Dienst \_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) Struktur nicht **Fehler \_** **\_**</span><span class="sxs-lookup"><span data-stu-id="79856-181">Enter 1 to run the actions if the service terminates reporting **SERVICE\_STOPPED** and the **dwWin32ExitCode** member of [**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status) structure is not **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="79856-182">Konfigurierte Fehler Aktionen werden auch ausgeführt, wenn der Dienst beendet wird, ohne dass der Berichterstattungs **Dienst \_** beendet wird</span><span class="sxs-lookup"><span data-stu-id="79856-182">Configured failure actions are also run if the service terminates without reporting **SERVICE\_STOPPED**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="79856-183"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Gestritten</span><span class="sxs-lookup"><span data-stu-id="79856-183"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument</span></span>
</dt> <dd>

<span data-ttu-id="79856-184">Der Wert in diesem Feld, in Kombination mit dem Wert im Feld ConfigType, gibt an, welche Änderung an der Dienst Konfiguration vorgenommen werden soll.</span><span class="sxs-lookup"><span data-stu-id="79856-184">The value in this field, combined with the value in the ConfigType field, specify what change to make to the service configuration.</span></span> <span data-ttu-id="79856-185">Die angegebene Änderung wird wirksam, wenn das System das nächste Mal gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="79856-185">The specified change takes effect the next time the system is started.</span></span>

</dd> <dt>

<span data-ttu-id="79856-186"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_</span><span class="sxs-lookup"><span data-stu-id="79856-186"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="79856-187">Externer Schlüssel zur Komponenten Spalte der [Komponenten Tabelle](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="79856-187">External key to the Component column of the [Component Table](component-table.md).</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="79856-188">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="79856-188">Validation</span></span>

<dl>

[<span data-ttu-id="79856-189">ICE102</span><span class="sxs-lookup"><span data-stu-id="79856-189">ICE102</span></span>](ice-102.md)  
[<span data-ttu-id="79856-190">ICE03</span><span class="sxs-lookup"><span data-stu-id="79856-190">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="79856-191">ICE06</span><span class="sxs-lookup"><span data-stu-id="79856-191">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="79856-192">ICE32</span><span class="sxs-lookup"><span data-stu-id="79856-192">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="79856-193">ICE45</span><span class="sxs-lookup"><span data-stu-id="79856-193">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="79856-194">ICE46</span><span class="sxs-lookup"><span data-stu-id="79856-194">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="79856-195">ICE69</span><span class="sxs-lookup"><span data-stu-id="79856-195">ICE69</span></span>](ice69.md)  
</dl>

 

 
