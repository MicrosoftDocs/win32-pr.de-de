---
description: Weitere Informationen zu finden Sie unter dem Beispiel für ein umfassendes Dienst
ms.assetid: a3aeea9b-09c0-4834-892a-c378b67402f4
title: Das Complete Service-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb87ebfef3f964eacee66be94a4b5291c335d0d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350384"
---
# <a name="the-complete-service-sample"></a><span data-ttu-id="ebb2c-103">Das Complete Service-Beispiel</span><span class="sxs-lookup"><span data-stu-id="ebb2c-103">The Complete Service Sample</span></span>

<span data-ttu-id="ebb2c-104">Die Themen in diesem Abschnitt bilden eine umfassende Dienst Stichprobe:</span><span class="sxs-lookup"><span data-stu-id="ebb2c-104">The topics in this section form a complete service sample:</span></span>

-   <span data-ttu-id="ebb2c-105">[Sample.MC](sample-mc.md) (enthält Fehlermeldungen)</span><span class="sxs-lookup"><span data-stu-id="ebb2c-105">[Sample.mc](sample-mc.md) (contains error messages)</span></span>
-   <span data-ttu-id="ebb2c-106">[Svc. cpp](svc-cpp.md) (enthält den Dienst Code)</span><span class="sxs-lookup"><span data-stu-id="ebb2c-106">[Svc.cpp](svc-cpp.md) (contains the service code)</span></span>
-   <span data-ttu-id="ebb2c-107">[Svcconfig. cpp](svcconfig-cpp.md) (enthält Dienst Konfigurations Code)</span><span class="sxs-lookup"><span data-stu-id="ebb2c-107">[SvcConfig.cpp](svcconfig-cpp.md) (contains service configuration code)</span></span>
-   <span data-ttu-id="ebb2c-108">[Svccontrol. cpp](svccontrol-cpp.md) (enthält Dienst Steuerungs Code)</span><span class="sxs-lookup"><span data-stu-id="ebb2c-108">[SvcControl.cpp](svccontrol-cpp.md) (contains service control code)</span></span>

## <a name="building-the-service"></a><span data-ttu-id="ebb2c-109">Erstellen des Dienstes</span><span class="sxs-lookup"><span data-stu-id="ebb2c-109">Building the Service</span></span>

<span data-ttu-id="ebb2c-110">Im folgenden Verfahren wird beschrieben, wie der Dienst erstellt und die Ereignis Nachrichten-DLL registriert wird.</span><span class="sxs-lookup"><span data-stu-id="ebb2c-110">The following procedure describes how to build the service and register the event message DLL.</span></span>

<span data-ttu-id="ebb2c-111">**So erstellen Sie den Dienst und registrieren die Ereignis Nachrichten-dll**</span><span class="sxs-lookup"><span data-stu-id="ebb2c-111">**To build the service and register the event message DLL**</span></span>

1.  <span data-ttu-id="ebb2c-112">Erstellen Sie die Nachrichten-dll aus Sample.MC, indem Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="ebb2c-112">Build the message DLL from Sample.mc using the following steps:</span></span>
    1.  <span data-ttu-id="ebb2c-113">**MC-U Sample.MC**</span><span class="sxs-lookup"><span data-stu-id="ebb2c-113">**mc -U sample.mc**</span></span>
    2.  <span data-ttu-id="ebb2c-114">**RC-r-Beispiel. RC**</span><span class="sxs-lookup"><span data-stu-id="ebb2c-114">**rc -r sample.rc**</span></span>
    3.  <span data-ttu-id="ebb2c-115">**Link-dll-NOENTRY -out:sample.dll Sample. res**</span><span class="sxs-lookup"><span data-stu-id="ebb2c-115">**link -dll -noentry -out:sample.dll sample.res**</span></span>
2.  <span data-ttu-id="ebb2c-116">Erstellen Sie Svc.exe, SvcConfig.exe und SvcControl.exe aus "svc. cpp", "svcconfig. cpp" und "svccontrol. cpp".</span><span class="sxs-lookup"><span data-stu-id="ebb2c-116">Build Svc.exe, SvcConfig.exe, and SvcControl.exe from Svc.cpp, SvcConfig.cpp, and SvcControl.cpp, respectively.</span></span>
3.  <span data-ttu-id="ebb2c-117">Erstellen Sie den Registrierungsschlüssel **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services \\ EventLog \\ Application \\ SvcName** , und fügen Sie diesem Schlüssel die folgenden Registrierungs Werte hinzu.</span><span class="sxs-lookup"><span data-stu-id="ebb2c-117">Create the registry key **HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\EventLog\\Application\\SvcName** and add the following registry values to this key.</span></span>

    | <span data-ttu-id="ebb2c-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ebb2c-118">Value</span></span>                              | <span data-ttu-id="ebb2c-119">type</span><span class="sxs-lookup"><span data-stu-id="ebb2c-119">Type</span></span>       | <span data-ttu-id="ebb2c-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ebb2c-120">Description</span></span>                                                                                                        |
    |------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="ebb2c-121">**EventMessageFile**  =  *dll- \_ Pfad*</span><span class="sxs-lookup"><span data-stu-id="ebb2c-121">**EventMessageFile** = *dll\_path*</span></span> | <span data-ttu-id="ebb2c-122">REG- \_ SZ</span><span class="sxs-lookup"><span data-stu-id="ebb2c-122">REG\_SZ</span></span>    | <span data-ttu-id="ebb2c-123">Der Pfad zur reinen Ressourcen-DLL, die Zeichen folgen enthält, die der Dienst in das Ereignisprotokoll schreiben kann.</span><span class="sxs-lookup"><span data-stu-id="ebb2c-123">The path to the resource-only DLL that contains strings that the service can write to the event log.</span></span>               |
    | <span data-ttu-id="ebb2c-124">**Typessupported** = 0x00000007</span><span class="sxs-lookup"><span data-stu-id="ebb2c-124">**TypesSupported** = 0x00000007</span></span>    | <span data-ttu-id="ebb2c-125">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="ebb2c-125">REG\_DWORD</span></span> | <span data-ttu-id="ebb2c-126">Eine Bitmaske, die die unterstützten Ereignis Typen angibt.</span><span class="sxs-lookup"><span data-stu-id="ebb2c-126">A bit mask that specifies the supported event types.</span></span> <span data-ttu-id="ebb2c-127">Der Wert 0x000000007 gibt an, dass alle Typen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="ebb2c-127">The value 0x000000007 indicates that all types are supported.</span></span> |

    

     

## <a name="testing-the-service"></a><span data-ttu-id="ebb2c-128">Testen des Diensts</span><span class="sxs-lookup"><span data-stu-id="ebb2c-128">Testing the Service</span></span>

<span data-ttu-id="ebb2c-129">Im folgenden Verfahren wird beschrieben, wie der-Dienst getestet wird.</span><span class="sxs-lookup"><span data-stu-id="ebb2c-129">The following procedure describes how to test the service.</span></span>

<span data-ttu-id="ebb2c-130">**So testen Sie den Dienst**</span><span class="sxs-lookup"><span data-stu-id="ebb2c-130">**To test the service**</span></span>

1.  <span data-ttu-id="ebb2c-131">Starten Sie in der Systemsteuerung die **Dienst** Anwendung.</span><span class="sxs-lookup"><span data-stu-id="ebb2c-131">In Control Panel, start the **Services** application.</span></span> <span data-ttu-id="ebb2c-132">(Verwenden Sie in den folgenden Schritten die Taste F5, um die Anzeige zu aktualisieren, nachdem Sie einen Befehl ausgeführt haben, der die Informationen in der **Dienste** -Anwendung ändert.)</span><span class="sxs-lookup"><span data-stu-id="ebb2c-132">(In the following steps, use the F5 key to refresh the display after executing a command that modifies the information in the **Services** application.)</span></span>
2.  <span data-ttu-id="ebb2c-133">Führen Sie den folgenden Befehl aus, um den Dienst zu installieren:</span><span class="sxs-lookup"><span data-stu-id="ebb2c-133">Run the following command to install the service:</span></span>

    <span data-ttu-id="ebb2c-134">**SVC-Installation**</span><span class="sxs-lookup"><span data-stu-id="ebb2c-134">**svc install**</span></span>

    <span data-ttu-id="ebb2c-135">Der Dienst schreibt "der Dienst wurde erfolgreich installiert" in die Konsole, wenn der Vorgang erfolgreich ist, oder andernfalls eine Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="ebb2c-135">The service writes "Service installed successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

    <span data-ttu-id="ebb2c-136">Wenn die Dienst Installation erfolgreich ist, wird der Dienst in der **Dienst** Anwendung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ebb2c-136">If the service installation succeeds, the service is displayed in the **Services** application.</span></span> <span data-ttu-id="ebb2c-137">Beachten Sie, dass **Name** auf "SvcName" festgelegt ist, **Beschreibung** und **Status** leer sind und **Starttyp** auf "manuell" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ebb2c-137">Note that **Name** is set to "SvcName", **Description** and **Status** are blank, and **Startup Type** is set to "Manual".</span></span>

3.  <span data-ttu-id="ebb2c-138">Führen Sie den folgenden Befehl aus, um den Dienst zu starten:</span><span class="sxs-lookup"><span data-stu-id="ebb2c-138">Run the following command to start the service:</span></span>

    <span data-ttu-id="ebb2c-139">**svccontrol-Start SvcName**</span><span class="sxs-lookup"><span data-stu-id="ebb2c-139">**svccontrol start SvcName**</span></span>

    <span data-ttu-id="ebb2c-140">Wenn der Vorgang erfolgreich ist, schreibt das Dienst Steuerungsprogramm "Dienst Start steht aus...". und dann "der Dienst wurde erfolgreich gestartet" in der Konsole.</span><span class="sxs-lookup"><span data-stu-id="ebb2c-140">If the operation succeeds, the service control program writes "Service start pending..." and then "Service started successfully" to the console.</span></span> <span data-ttu-id="ebb2c-141">Andernfalls schreibt das Programm eine Fehlermeldung in die Konsole.</span><span class="sxs-lookup"><span data-stu-id="ebb2c-141">Otherwise, the program writes an error message to the console.</span></span>

    <span data-ttu-id="ebb2c-142">Wenn der Dienst erfolgreich gestartet wird, wird der **Status** auf "gestartet" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ebb2c-142">If the service starts successfully, **Status** is set to "Started".</span></span> <span data-ttu-id="ebb2c-143">Der Code in der [*ServiceMain*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) -Funktion wird vom SCM ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ebb2c-143">The code in the [*ServiceMain*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) function is executed by the SCM.</span></span> <span data-ttu-id="ebb2c-144">Wenn ein Fehler auftritt, schreibt der Dienst eine Fehlermeldung in das Ereignisprotokoll.</span><span class="sxs-lookup"><span data-stu-id="ebb2c-144">If an error occurs, the service will write an error message to the event log.</span></span> <span data-ttu-id="ebb2c-145">Diese Meldung enthält den Namen der Funktion, die fehlgeschlagen ist, und den Fehlercode, der bei einem Fehler zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="ebb2c-145">This message includes the name of the function that failed and the error code that was returned on failure.</span></span>

4.  <span data-ttu-id="ebb2c-146">Führen Sie den folgenden Befehl aus, um die Dienst Beschreibung zu aktualisieren:</span><span class="sxs-lookup"><span data-stu-id="ebb2c-146">Run the following command to update the service description:</span></span>

    <span data-ttu-id="ebb2c-147">**svcconfig beschreiben SvcName**</span><span class="sxs-lookup"><span data-stu-id="ebb2c-147">**svcconfig describe SvcName**</span></span>

    <span data-ttu-id="ebb2c-148">Das Dienst Konfigurationsprogramm schreibt die "Dienst Beschreibung wurde erfolgreich aktualisiert" in die Konsole, wenn der Vorgang erfolgreich ist, oder andernfalls eine Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="ebb2c-148">The service configuration program writes "Service description updated successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

    <span data-ttu-id="ebb2c-149">Wenn das Update erfolgreich ist, wird die **Beschreibung** auf "This is a Test Description" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ebb2c-149">If the update succeeds, **Description** is set to "This is a test description".</span></span>

5.  <span data-ttu-id="ebb2c-150">Führen Sie den folgenden Befehl aus, um die Dienst Konfiguration abzufragen:</span><span class="sxs-lookup"><span data-stu-id="ebb2c-150">Run the following command to query the service configuration:</span></span>

    <span data-ttu-id="ebb2c-151">**svcconfig-Abfrage SvcName**</span><span class="sxs-lookup"><span data-stu-id="ebb2c-151">**svcconfig query SvcName**</span></span>

    <span data-ttu-id="ebb2c-152">Das Dienst Konfigurationsprogramm schreibt die Dienst Konfigurationsinformationen in die Konsole, wenn der Vorgang erfolgreich ist, oder andernfalls eine Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="ebb2c-152">The service configuration program writes the service configuration information to the console if the operation succeeds or an error message otherwise.</span></span>

6.  <span data-ttu-id="ebb2c-153">Führen Sie den folgenden Befehl aus, um die Dienst-DACL zu ändern:</span><span class="sxs-lookup"><span data-stu-id="ebb2c-153">Run the following command to change the service DACL:</span></span>

    <span data-ttu-id="ebb2c-154">**svccontrol DACL SvcName**</span><span class="sxs-lookup"><span data-stu-id="ebb2c-154">**svccontrol dacl SvcName**</span></span>

    <span data-ttu-id="ebb2c-155">Das Dienst Konfigurationsprogramm schreibt die "Dienst-DACL wurde erfolgreich aktualisiert" in die Konsole, wenn der Vorgang erfolgreich ist, oder andernfalls eine Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="ebb2c-155">The service configuration program writes "Service DACL updated successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

7.  <span data-ttu-id="ebb2c-156">Führen Sie den folgenden Befehl aus, um den Dienst zu deaktivieren:</span><span class="sxs-lookup"><span data-stu-id="ebb2c-156">Run the following command to disable the service:</span></span>

    <span data-ttu-id="ebb2c-157">**svcconfig "SvcName deaktivieren"**</span><span class="sxs-lookup"><span data-stu-id="ebb2c-157">**svcconfig disable SvcName**</span></span>

    <span data-ttu-id="ebb2c-158">Das Dienst Konfigurationsprogramm schreibt "der Dienst wurde erfolgreich deaktiviert" in die Konsole, wenn der Vorgang erfolgreich ist, oder andernfalls eine Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="ebb2c-158">The service configuration program writes "Service disabled successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

    <span data-ttu-id="ebb2c-159">Wenn der Dienst erfolgreich deaktiviert wurde, wird der **Starttyp** auf "deaktiviert" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ebb2c-159">If the service is disabled successfully, **Startup Type** is set to "Disabled".</span></span>

8.  <span data-ttu-id="ebb2c-160">Führen Sie den folgenden Befehl aus, um den Dienst zu aktivieren:</span><span class="sxs-lookup"><span data-stu-id="ebb2c-160">Run the following command to enable the service:</span></span>

    <span data-ttu-id="ebb2c-161">**svcconfig SvcName aktivieren**</span><span class="sxs-lookup"><span data-stu-id="ebb2c-161">**svcconfig enable SvcName**</span></span>

    <span data-ttu-id="ebb2c-162">Das Dienst Konfigurationsprogramm schreibt "der Dienst wurde erfolgreich aktiviert" in die Konsole, wenn der Vorgang erfolgreich ist, oder andernfalls eine Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="ebb2c-162">The service configuration program writes "Service enabled successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

    <span data-ttu-id="ebb2c-163">Wenn der Dienst erfolgreich aktiviert wurde, wird der **Starttyp** auf "manuell" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ebb2c-163">If the service is enabled successfully, **Startup Type** is set to "Manual".</span></span>

9.  <span data-ttu-id="ebb2c-164">Führen Sie den folgenden Befehl aus, um den Dienst zu unterbinden:</span><span class="sxs-lookup"><span data-stu-id="ebb2c-164">Run the following command to stop the service:</span></span>

    <span data-ttu-id="ebb2c-165">**svccontrol stoppt SvcName.**</span><span class="sxs-lookup"><span data-stu-id="ebb2c-165">**svccontrol stop SvcName**</span></span>

    <span data-ttu-id="ebb2c-166">Wenn der Vorgang erfolgreich ausgeführt wird, schreibt das Dienst Steuerungsprogramm "Dienst Ende steht aus...". und dann "der Dienst wurde erfolgreich beendet" in der Konsole.</span><span class="sxs-lookup"><span data-stu-id="ebb2c-166">If the operation succeeds, the service control program writes "Service stop pending..." and then "Service stopped successfully" to the console.</span></span> <span data-ttu-id="ebb2c-167">Andernfalls schreibt das Programm eine Fehlermeldung in die Konsole.</span><span class="sxs-lookup"><span data-stu-id="ebb2c-167">Otherwise, the program writes an error message to the console.</span></span>

    <span data-ttu-id="ebb2c-168">Wenn der Dienst erfolgreich beendet wird, ist der **Status** leer.</span><span class="sxs-lookup"><span data-stu-id="ebb2c-168">If the service stops successfully, **Status** is blank.</span></span>

    <span data-ttu-id="ebb2c-169">Wenn der Dienst nicht beendet werden kann, schreibt das Dienst Steuerungsprogramm eine Fehlermeldung in das Ereignisprotokoll, das den Namen der fehlgeschlagenen Funktion und den Fehlercode enthält, der bei einem Fehler zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="ebb2c-169">If the service fails to stop, the service control program writes an error message to the event log that includes the name of the function that failed and the error code that was returned on failure.</span></span>

10. <span data-ttu-id="ebb2c-170">Führen Sie den folgenden Befehl aus, um den Dienst zu löschen:</span><span class="sxs-lookup"><span data-stu-id="ebb2c-170">Run the following command to delete the service:</span></span>

    <span data-ttu-id="ebb2c-171">**svcconfig DELETE SvcName**</span><span class="sxs-lookup"><span data-stu-id="ebb2c-171">**svcconfig delete SvcName**</span></span>

    <span data-ttu-id="ebb2c-172">Das Dienst Konfigurationsprogramm schreibt "der Dienst wurde erfolgreich gelöscht" in die Konsole, wenn der Vorgang erfolgreich abgeschlossen wurde, andernfalls wird eine Fehlermeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ebb2c-172">The service configuration program writes "Service deleted successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

    <span data-ttu-id="ebb2c-173">Wenn der Dienst erfolgreich gelöscht wurde, wird er nicht mehr in der **Dienst** Anwendung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ebb2c-173">If the service is deleted successfully, it is no longer displayed in the **Services** application.</span></span> <span data-ttu-id="ebb2c-174">(Beachten Sie Folgendes: Wenn Sie versuchen, einen Dienst zu löschen, der nicht beendet wurde, ist der Vorgang erfolgreich, aber der **Starttyp** ist auf "deaktiviert" festgelegt, und der Dienst Eintrag wird beim Neustart des Systems oder beim Beenden des Dienstanbieter mithilfe des Task-Managers gelöscht.)</span><span class="sxs-lookup"><span data-stu-id="ebb2c-174">(Note that if you attempt to delete a service that is not stopped, the operation succeeds but **Startup Type** is set to "Disabled" and the service entry will be deleted at system restart or when the service is terminated using Task Manager.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="ebb2c-175">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ebb2c-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebb2c-176">Verwenden von Diensten</span><span class="sxs-lookup"><span data-stu-id="ebb2c-176">Using Services</span></span>](using-services.md)
</dt> </dl>

 

 
