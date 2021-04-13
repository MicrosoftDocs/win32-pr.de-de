---
title: Befehls Blockierung
description: Um die Integrität von Vorgängen aufrechtzuerhalten, dürfen bestimmte TPM-Befehle von Software auf der Plattform nicht ausgeführt werden.
ms.assetid: 47402a4a-5f8d-4648-b3ea-06c95b2a1fc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8b9a302f12e7838240ee8bfeac1ea78a3884a1
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2020
ms.locfileid: "104390101"
---
# <a name="command-blocking"></a><span data-ttu-id="ec48d-103">Befehls Blockierung</span><span class="sxs-lookup"><span data-stu-id="ec48d-103">Command Blocking</span></span>

<span data-ttu-id="ec48d-104">Um die Integrität von Vorgängen aufrechtzuerhalten, dürfen bestimmte TPM-Befehle von Software auf der Plattform nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ec48d-104">To preserve integrity of operations, certain TPM commands are not allowed to be executed by software on the platform.</span></span> <span data-ttu-id="ec48d-105">Beispielsweise werden einige Befehle nur von der Systemsoftware ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ec48d-105">For example, some commands are only executed by system software.</span></span> <span data-ttu-id="ec48d-106">Wenn die TSB einen Befehl blockiert, wird nach Bedarf ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ec48d-106">When the TBS blocks a command, an error is returned as appropriate.</span></span> <span data-ttu-id="ec48d-107">Standardmäßig blockiert TSB Befehle, die Auswirkungen auf den System Datenschutz, die Sicherheit und die Stabilität haben können.</span><span class="sxs-lookup"><span data-stu-id="ec48d-107">By default, the TBS blocks commands that could impact system privacy, security, and stability.</span></span> <span data-ttu-id="ec48d-108">Der TSB geht auch davon aus, dass andere Teile des Software Stapels den Zugriff auf bestimmte Befehle auf autorisierte Entitäten einschränken können.</span><span class="sxs-lookup"><span data-stu-id="ec48d-108">The TBS also assumes that other parts of the software stack may restrict access to certain commands to authorized entities.</span></span>

<span data-ttu-id="ec48d-109">Für TPM-Befehle der Version 1,2 gibt es drei Listen mit blockierten Befehlen: eine Liste, die von der Gruppenrichtlinie gesteuert wird, eine Liste, die von lokalen Administratoren gesteuert wird, und eine Standardliste.</span><span class="sxs-lookup"><span data-stu-id="ec48d-109">For TPM version 1.2 commands, there are three lists of blocked commands: a list controlled by group policy, a list controlled by local administrators, and a default list.</span></span> <span data-ttu-id="ec48d-110">Ein TPM-Befehl wird blockiert, wenn er in einer der Listen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ec48d-110">A TPM command is blocked if it is on any of the lists.</span></span> <span data-ttu-id="ec48d-111">Es gibt jedoch Gruppenrichtlinien Flags, mit denen die TSB die lokale Liste und die Standardliste ignorieren kann.</span><span class="sxs-lookup"><span data-stu-id="ec48d-111">However, there are group policy flags to allow the TBS to ignore the local list and the default list.</span></span> <span data-ttu-id="ec48d-112">Die Gruppen Richtlinienflags können direkt bearbeitet oder über den Gruppenrichtlinienobjekt-Editor auf Sie zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="ec48d-112">The group policy flags can be edited directly or accessed through the Group Policy Object Editor.</span></span>

> [!Note]  
> <span data-ttu-id="ec48d-113">Die Liste der lokal blockierten Befehle wird nach einem Upgrade auf das Betriebssystem nicht beibehalten.</span><span class="sxs-lookup"><span data-stu-id="ec48d-113">The list of locally blocked commands is not preserved after an upgrade to the operating system.</span></span> <span data-ttu-id="ec48d-114">Befehle, die in der Gruppenrichtlinie Liste blockiert werden, werden beibehalten.</span><span class="sxs-lookup"><span data-stu-id="ec48d-114">Commands that are blocked on the Group Policy list are preserved.</span></span>

 

<span data-ttu-id="ec48d-115">Bei TPM-Befehlen der Version 2,0 wird die Logik für die Blockierung invertiert. Es wird eine Liste zulässiger Befehle verwendet.</span><span class="sxs-lookup"><span data-stu-id="ec48d-115">For TPM version 2.0 commands, the logic for blocking is inverted; it uses a list of allowed commands.</span></span> <span data-ttu-id="ec48d-116">Diese Logik blockiert automatisch Befehle, die nicht bekannt waren, als die Liste erstmalig erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ec48d-116">This logic will automatically block commands that were not known when the list was first made.</span></span> <span data-ttu-id="ec48d-117">Wenn der TPM-Spezifikation Befehle hinzugefügt werden, nachdem eine Version von Windows ausgeliefert wurde, werden diese neuen Befehle automatisch blockiert.</span><span class="sxs-lookup"><span data-stu-id="ec48d-117">When commands are added to the TPM specification after a version of Windows has shipped, these new commands are automatically blocked.</span></span> <span data-ttu-id="ec48d-118">Nur ein Update der Registrierung fügt diese neuen Befehle der Liste der zulässigen Befehle hinzu.</span><span class="sxs-lookup"><span data-stu-id="ec48d-118">Only an update of the registry will add these new commands to the list of allowed commands.</span></span>

<span data-ttu-id="ec48d-119">Ab Windows 10 1809 (Windows Server 2019) können zulässige TPM 2,0-Befehle nicht mehr über Registrierungs Einstellungen manipuliert werden.</span><span class="sxs-lookup"><span data-stu-id="ec48d-119">Starting with Windows 10 1809 (Windows Server 2019), allowed TPM 2.0 commands can no longer be manipulated through registry settings.</span></span> <span data-ttu-id="ec48d-120">Für diese Windows 10-Versionen werden die zulässigen TPM 2,0-Befehle im TPM-Treiber korrigiert.</span><span class="sxs-lookup"><span data-stu-id="ec48d-120">For these Windows 10 versions, the allowed TPM 2.0 commands are fixed in the TPM driver.</span></span> <span data-ttu-id="ec48d-121">TPM 1,2-Befehle können weiterhin blockiert und durch Registrierungs Änderungen aufgehoben werden.</span><span class="sxs-lookup"><span data-stu-id="ec48d-121">TPM 1.2 commands can still be blocked and unblocked through registry changes.</span></span> 

## <a name="direct-registry-access"></a><span data-ttu-id="ec48d-122">Direkter Registrierungs Zugriff</span><span class="sxs-lookup"><span data-stu-id="ec48d-122">Direct Registry Access</span></span>

<span data-ttu-id="ec48d-123">Die Gruppenrichtlinie-Flags befinden sich unter dem Registrierungsschlüssel **HKEY \_ local \_ Machine** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **TPM** \\ **blockedcommands**.</span><span class="sxs-lookup"><span data-stu-id="ec48d-123">The Group Policy flags are under registry key **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Tpm**\\**BlockedCommands**.</span></span>

<span data-ttu-id="ec48d-124">Um zu ermitteln, welche Listen zum Blockieren von TPM-Befehlen verwendet werden sollen, gibt es zwei **DWORD** -Werte, die als boolesche Flags verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="ec48d-124">To determine which lists should be used to block TPM commands, there are two **DWORD** values that are used as Boolean flags:</span></span>

-   <span data-ttu-id="ec48d-125">"Ignoredefaultlist"</span><span class="sxs-lookup"><span data-stu-id="ec48d-125">"IgnoreDefaultList"</span></span>

    <span data-ttu-id="ec48d-126">Wenn festgelegt ist (der Wert ist vorhanden und ungleich null), ignoriert TSB die Liste der blockierten Standard Befehle.</span><span class="sxs-lookup"><span data-stu-id="ec48d-126">If set (value exists and is nonzero), the TBS ignores the default blocked-commands list.</span></span>

-   <span data-ttu-id="ec48d-127">"Ignorelocallist"</span><span class="sxs-lookup"><span data-stu-id="ec48d-127">"IgnoreLocalList"</span></span>

    <span data-ttu-id="ec48d-128">Wenn festgelegt ist (der Wert ist vorhanden und nicht null), ignoriert TSB die Liste der lokalen blockierten Befehle.</span><span class="sxs-lookup"><span data-stu-id="ec48d-128">If set (value exists and is nonzero), the TBS ignores the local blocked-commands list.</span></span>

## <a name="group-policy-object-editor"></a><span data-ttu-id="ec48d-129">Gruppenrichtlinienobjekt-Editor</span><span class="sxs-lookup"><span data-stu-id="ec48d-129">Group Policy Object Editor</span></span>

<span data-ttu-id="ec48d-130">**So greifen Sie auf den Gruppenrichtlinie Objekt-Editor zu**</span><span class="sxs-lookup"><span data-stu-id="ec48d-130">**To access the Group Policy object editor**</span></span>

1.  <span data-ttu-id="ec48d-131">Klicken Sie auf **Start**.</span><span class="sxs-lookup"><span data-stu-id="ec48d-131">Click **Start**.</span></span>
2.  <span data-ttu-id="ec48d-132">Klicken Sie auf **Ausführen**.</span><span class="sxs-lookup"><span data-stu-id="ec48d-132">Click **Run**.</span></span>
3.  <span data-ttu-id="ec48d-133">Geben Sie **gpedit.msc** im Feld **Öffnen** ein.</span><span class="sxs-lookup"><span data-stu-id="ec48d-133">In the **Open** box, type **gpedit.msc**.</span></span> <span data-ttu-id="ec48d-134">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="ec48d-134">Click **OK**.</span></span> <span data-ttu-id="ec48d-135">Der Gruppenrichtlinie Objekt-Editor wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="ec48d-135">The Group Policy object editor opens.</span></span>
4.  <span data-ttu-id="ec48d-136">Erweitern Sie **Computer Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="ec48d-136">Expand **Computer Configuration**.</span></span>
5.  <span data-ttu-id="ec48d-137">Erweitern Sie **Administrative Vorlagen**.</span><span class="sxs-lookup"><span data-stu-id="ec48d-137">Expand **Administrative Templates**.</span></span>
6.  <span data-ttu-id="ec48d-138">Erweitern Sie **System**.</span><span class="sxs-lookup"><span data-stu-id="ec48d-138">Expand **System**.</span></span>
7.  <span data-ttu-id="ec48d-139">Erweitern Sie **Trusted Platform Module Dienste**.</span><span class="sxs-lookup"><span data-stu-id="ec48d-139">Expand **Trusted Platform Module Services**.</span></span>

<span data-ttu-id="ec48d-140">Die Listen bestimmter Blockierter TPM 1.2-Befehle können direkt an den folgenden Speicherorten bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="ec48d-140">The lists of specific blocked TPM1.2 commands can be edited directly in the following locations.</span></span>

-   <span data-ttu-id="ec48d-141">Gruppenrichtlinien Liste:</span><span class="sxs-lookup"><span data-stu-id="ec48d-141">Group policy list:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Policies
             Microsoft
                Tpm
                   BlockedCommands
                      List
    ```

-   <span data-ttu-id="ec48d-142">Lokale Liste:</span><span class="sxs-lookup"><span data-stu-id="ec48d-142">Local list:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Services
                SharedAccess
                   Parameters
                      Tpm
                         BlockedCommands
                            List
    ```

-   <span data-ttu-id="ec48d-143">Standardliste:</span><span class="sxs-lookup"><span data-stu-id="ec48d-143">Default list:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Tpm
                BlockedCommands
                   List
    ```

<span data-ttu-id="ec48d-144">Unter jedem dieser Registrierungsschlüssel gibt es eine Liste von Registrierungs Werten des REG SZ- \_ Typs.</span><span class="sxs-lookup"><span data-stu-id="ec48d-144">Under each of these registry keys, there is a list of registry values of REG\_SZ type.</span></span> <span data-ttu-id="ec48d-145">Jeder Wert stellt einen gesperrten TPM-Befehl dar.</span><span class="sxs-lookup"><span data-stu-id="ec48d-145">Each value represents a blocked TPM command.</span></span> <span data-ttu-id="ec48d-146">Jeder Registrierungsschlüssel weist das Feld "Wertname" und das Feld "Wertdaten" auf.</span><span class="sxs-lookup"><span data-stu-id="ec48d-146">Each registry key has a "Value name" field and a "Value data" field.</span></span> <span data-ttu-id="ec48d-147">Beide Felder ("Wertname" und "Wertdaten") sollten genau mit dem Dezimalwert der zu blockierenden TPM-Befehls Ordinalzahl übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="ec48d-147">Both fields ("Value Name" and "Value data"), should exactly match the decimal value of the TPM command ordinal to be blocked.</span></span>

<span data-ttu-id="ec48d-148">Die Liste der spezifischen zulässigen TPM 2,0-Befehle kann direkt an folgendem Speicherort bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="ec48d-148">The list of specific allowed TPM 2.0 commands can be edited directly in the following location.</span></span> <span data-ttu-id="ec48d-149">Unter dem Registrierungsschlüssel befindet sich eine Liste mit Registrierungs Werten des reg \_ DWORD-Typs.</span><span class="sxs-lookup"><span data-stu-id="ec48d-149">Under the registry key, there is a list of registry values of REG\_DWORD type.</span></span> <span data-ttu-id="ec48d-150">Jeder Wert stellt einen zulässigen TPM 2,0-Befehl dar.</span><span class="sxs-lookup"><span data-stu-id="ec48d-150">Each value represents an allowed TPM 2.0 command.</span></span> <span data-ttu-id="ec48d-151">Jeder Registrierungs Wert verfügt über einen **Namen** und ein **Wertfeld** .</span><span class="sxs-lookup"><span data-stu-id="ec48d-151">Each registry value has a **name** and a **value** field.</span></span> <span data-ttu-id="ec48d-152">Der **Name** entspricht der hexadezimalen TPM 2,0-Befehls Ordinalzahl, die zulässig sein soll.</span><span class="sxs-lookup"><span data-stu-id="ec48d-152">The **name** matches the hexadecimal TPM 2.0 command ordinal that should be allowed.</span></span> <span data-ttu-id="ec48d-153">Der **Wert** hat den Wert 1, wenn der Befehl zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="ec48d-153">The **value** has a value of 1 if the command is allowed.</span></span> <span data-ttu-id="ec48d-154">Wenn eine Befehls Ordinalzahl nicht vorhanden ist oder den Wert 0 hat, wird der Befehl blockiert.</span><span class="sxs-lookup"><span data-stu-id="ec48d-154">If a command ordinal is not present or has a value of 0, the command will be blocked.</span></span>

-   <span data-ttu-id="ec48d-155">Standardliste:</span><span class="sxs-lookup"><span data-stu-id="ec48d-155">Default list:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Tpm
                AllowedW8Commands
                   List
    ```

<span data-ttu-id="ec48d-156">Für Windows 8, Windows Server 2012 und höher, bestimmen die Registrierungsschlüssel **blockedcommands** und **AllowedW8Commands** die gesperrten oder zulässigen TPM-Befehle für Administrator Konten.</span><span class="sxs-lookup"><span data-stu-id="ec48d-156">For Windows 8, Windows Server 2012 and later, the **BlockedCommands** and **AllowedW8Commands** registry keys respectively determine the blocked or allowed TPM commands for administrator accounts.</span></span> <span data-ttu-id="ec48d-157">Benutzerkonten enthalten eine Liste der blockierten oder zulässigen TPM-Befehle in den Registrierungs Schlüsseln **blockedusercommands** bzw. **AllowedW8UserCommands** .</span><span class="sxs-lookup"><span data-stu-id="ec48d-157">User accounts have a list of blocked or allowed TPM commands in the **BlockedUserCommands** and **AllowedW8UserCommands** registry keys respectively.</span></span> <span data-ttu-id="ec48d-158">In Windows 10, Version 1607, wurden neue Registrierungsschlüssel für appcontainer-Anwendungen eingeführt: **blockedappcontainercommands** und **AllowedW8AppContainerCommands**.</span><span class="sxs-lookup"><span data-stu-id="ec48d-158">In Windows 10, version 1607, new registry keys have been introduces for AppContainer applications: **BlockedAppContainerCommands** and **AllowedW8AppContainerCommands**.</span></span>

 

 




