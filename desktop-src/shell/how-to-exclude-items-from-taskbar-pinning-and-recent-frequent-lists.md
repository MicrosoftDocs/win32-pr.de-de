---
description: Anwendungen, Prozesse und Windows können sich dazu entscheiden, sich selbst nicht für das Anheften an die Taskleiste oder für die Aufnahme in die Liste der am häufigsten verwendeten (MFU-) Startmenüs zu entscheiden.
title: Ausschließen von Elementen aus der Taskleiste anheften und zuletzt auftretenden Listen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7f32ad641832703804f94b8cc28f47ea9cabb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979561"
---
# <a name="how-to-exclude-items-from-taskbar-pinning-and-recentfrequent-lists"></a><span data-ttu-id="ec0b1-103">Ausschließen von Elementen aus der Taskleiste anheften und zuletzt auftretenden Listen</span><span class="sxs-lookup"><span data-stu-id="ec0b1-103">How to Exclude Items from Taskbar Pinning and Recent/Frequent Lists</span></span>

<span data-ttu-id="ec0b1-104">Anwendungen, Prozesse und Windows können sich dazu entscheiden, sich selbst nicht für das Anheften an die Taskleiste oder für die Aufnahme in die Liste der am häufigsten verwendeten (MFU-) **Startmenüs** zu entscheiden.</span><span class="sxs-lookup"><span data-stu-id="ec0b1-104">Applications, processes, and windows can opt to make themselves unavailable for pinning to the taskbar or for inclusion in the **Start** menu's Most Frequently Used (MFU) list.</span></span>

## <a name="instructions"></a><span data-ttu-id="ec0b1-105">Instructions</span><span class="sxs-lookup"><span data-stu-id="ec0b1-105">Instructions</span></span>


<span data-ttu-id="ec0b1-106">Es gibt drei Mechanismen, um den Ausschluss von Elementen aus dem anheften der Taskleiste und der aktuellen bzw. häufigen Listen zu erreichen:</span><span class="sxs-lookup"><span data-stu-id="ec0b1-106">There are three mechanisms to accomplish the exclusion of items from taskbar pinning and recent/frequent lists:</span></span>

-   <span data-ttu-id="ec0b1-107">Fügen Sie den NoStartPage-Eintrag zur Registrierung der Anwendung hinzu, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="ec0b1-107">Add the NoStartPage entry to the application's registration as shown in this example:</span></span>

    ```
    HKEY_CLASSES_ROOT
       Applications
          Example.exe
             NoStartPage
    ```

    <span data-ttu-id="ec0b1-108">Die dem NoStartPage-Eintrag zugeordneten Daten werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="ec0b1-108">The data associated with the NoStartPage entry is ignored.</span></span> <span data-ttu-id="ec0b1-109">Nur das vorhanden sein des Eintrags ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ec0b1-109">Only the presence of the entry is required.</span></span> <span data-ttu-id="ec0b1-110">Daher ist der ideale Typ für NoStartPage " **reg \_ None**".</span><span class="sxs-lookup"><span data-stu-id="ec0b1-110">Therefore, the ideal type for NoStartPage is **REG\_NONE**.</span></span>

    <span data-ttu-id="ec0b1-111">Beachten Sie, dass jede Verwendung einer expliziten App-Benutzer Modell-ID (appusermodelid) den NoStartPage-Eintrag überschreibt.</span><span class="sxs-lookup"><span data-stu-id="ec0b1-111">Note that any use of an explicit Application User Model ID (AppUserModelID) overrides the NoStartPage entry.</span></span> <span data-ttu-id="ec0b1-112">Wenn eine explizite appusermodelid auf eine Verknüpfung, einen Prozess oder ein Fenster angewendet wird, wird Sie gepinckbar und ist für die MFU-Liste des **Start** Menüs geeignet.</span><span class="sxs-lookup"><span data-stu-id="ec0b1-112">If an explicit AppUserModelID is applied to a shortcut, process, or window, it becomes pinnable and eligible for the **Start** menu MFU list.</span></span>

-   <span data-ttu-id="ec0b1-113">Legen Sie die [System. appusermodel. preventpinning](../properties/props-system-appusermodel-preventpinning.md) -Eigenschaft unter Windows und Verknüpfungen fest.</span><span class="sxs-lookup"><span data-stu-id="ec0b1-113">Set the [System.AppUserModel.PreventPinning](../properties/props-system-appusermodel-preventpinning.md) property on windows and shortcuts.</span></span> <span data-ttu-id="ec0b1-114">Diese Eigenschaft muss für ein Fenster festgelegt werden, bevor die [pkey- \_ appusermodel- \_ ID](../properties/props-system-appusermodel-id.md) -Eigenschaft festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="ec0b1-114">This property must be set on a window before the [PKEY\_AppUserModel\_ID](../properties/props-system-appusermodel-id.md) property is set.</span></span>
-   <span data-ttu-id="ec0b1-115">Fügen Sie eine explizite appusermodelid als Wert unter dem folgenden Registrierungs Unterschlüssel hinzu, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="ec0b1-115">Add an explicit AppUserModelID as a value under the following registry subkey as shown in this example:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      FileAssociation
                         NoStartPageAppUserModelIDs
                            AppUserModelID1
                            AppUserModelID2
                            AppUserModelID3
    ```

    <span data-ttu-id="ec0b1-116">Jeder Eintrag ist ein **reg- \_ null** -Wert mit dem Namen der appusermodelid.</span><span class="sxs-lookup"><span data-stu-id="ec0b1-116">Each entry is a **REG\_NULL** value with the name of the AppUserModelID.</span></span> <span data-ttu-id="ec0b1-117">Alle in dieser Liste gefundenen appusermodelid-Werte können nicht in die MFU-Liste des **Start** Menüs eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="ec0b1-117">Any AppUserModelID that is found in this list is not pinnable and not eligible for inclusion in the **Start** menu MFU list.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec0b1-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ec0b1-118">Remarks</span></span>

<span data-ttu-id="ec0b1-119">Beachten Sie, dass bestimmte ausführbare Dateien und Verknüpfungen, die bestimmte Zeichen folgen in ihren Namen enthalten, automatisch vom anhechern und einschließen in die MFU-Liste ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="ec0b1-119">Be aware that certain executable files, as well as shortcuts that contain certain strings in their names, are automatically excluded from pinning and inclusion in the MFU list.</span></span>

> [!Note]  
> <span data-ttu-id="ec0b1-120">Dieser automatische Ausschluss kann überschrieben werden, indem eine explizite appusermodelid angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="ec0b1-120">This automatic exclusion can be overridden by applying an explicit AppUserModelID.</span></span>

 

<span data-ttu-id="ec0b1-121">Wenn eine der folgenden Zeichen folgen, unabhängig von der Groß-/Kleinschreibung, im Verknüpfungs Namen enthalten ist, kann das Programm nicht festgelegt werden und wird nicht in der am häufigsten verwendeten Liste angezeigt (gilt nicht für Windows 10):</span><span class="sxs-lookup"><span data-stu-id="ec0b1-121">If any of the following strings, regardless of case, are included in the shortcut name, the program is not pinnable and is not displayed in the most frequently used list (not applicable to Windows 10):</span></span>

-   <span data-ttu-id="ec0b1-122">Dokumentation</span><span class="sxs-lookup"><span data-stu-id="ec0b1-122">Documentation</span></span>
-   <span data-ttu-id="ec0b1-123">Hilfe</span><span class="sxs-lookup"><span data-stu-id="ec0b1-123">Help</span></span>
-   <span data-ttu-id="ec0b1-124">Installieren</span><span class="sxs-lookup"><span data-stu-id="ec0b1-124">Install</span></span>
-   <span data-ttu-id="ec0b1-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ec0b1-125">More Info</span></span>
-   <span data-ttu-id="ec0b1-126">Lesezugriff</span><span class="sxs-lookup"><span data-stu-id="ec0b1-126">Read me</span></span>
-   <span data-ttu-id="ec0b1-127">Zuerst lesen</span><span class="sxs-lookup"><span data-stu-id="ec0b1-127">Read First</span></span>
-   <span data-ttu-id="ec0b1-128">Infodatei</span><span class="sxs-lookup"><span data-stu-id="ec0b1-128">Readme</span></span>
-   <span data-ttu-id="ec0b1-129">Remove (Entfernen)</span><span class="sxs-lookup"><span data-stu-id="ec0b1-129">Remove</span></span>
-   <span data-ttu-id="ec0b1-130">Einrichten</span><span class="sxs-lookup"><span data-stu-id="ec0b1-130">Setup</span></span>
-   <span data-ttu-id="ec0b1-131">Support</span><span class="sxs-lookup"><span data-stu-id="ec0b1-131">Support</span></span>
-   <span data-ttu-id="ec0b1-132">Neuerungen</span><span class="sxs-lookup"><span data-stu-id="ec0b1-132">What's New</span></span>

<span data-ttu-id="ec0b1-133">Die folgende Liste der Programme ist nicht pinckbar und wird aus der Liste der am häufigsten verwendeten Programme ausgeschlossen:</span><span class="sxs-lookup"><span data-stu-id="ec0b1-133">The following list of programs are not pinnable and are excluded from the most frequently used list:</span></span>

-   <span data-ttu-id="ec0b1-134">Applaunch.exe</span><span class="sxs-lookup"><span data-stu-id="ec0b1-134">Applaunch.exe</span></span>
-   <span data-ttu-id="ec0b1-135">Control.exe</span><span class="sxs-lookup"><span data-stu-id="ec0b1-135">Control.exe</span></span>
-   <span data-ttu-id="ec0b1-136">Dfsvc.exe</span><span class="sxs-lookup"><span data-stu-id="ec0b1-136">Dfsvc.exe</span></span>
-   <span data-ttu-id="ec0b1-137">Dllhost.exe</span><span class="sxs-lookup"><span data-stu-id="ec0b1-137">Dllhost.exe</span></span>
-   <span data-ttu-id="ec0b1-138">Guestmodemsg.exe</span><span class="sxs-lookup"><span data-stu-id="ec0b1-138">Guestmodemsg.exe</span></span>
-   <span data-ttu-id="ec0b1-139">Hh.exe</span><span class="sxs-lookup"><span data-stu-id="ec0b1-139">Hh.exe</span></span>
-   <span data-ttu-id="ec0b1-140">Install.exe</span><span class="sxs-lookup"><span data-stu-id="ec0b1-140">Install.exe</span></span>
-   <span data-ttu-id="ec0b1-141">Isuninst.exe</span><span class="sxs-lookup"><span data-stu-id="ec0b1-141">Isuninst.exe</span></span>
-   <span data-ttu-id="ec0b1-142">Lnkstub.exe</span><span class="sxs-lookup"><span data-stu-id="ec0b1-142">Lnkstub.exe</span></span>
-   <span data-ttu-id="ec0b1-143">Mmc.exe</span><span class="sxs-lookup"><span data-stu-id="ec0b1-143">Mmc.exe</span></span>
-   <span data-ttu-id="ec0b1-144">Mshta.exe</span><span class="sxs-lookup"><span data-stu-id="ec0b1-144">Mshta.exe</span></span>
-   <span data-ttu-id="ec0b1-145">Msiexec.exe</span><span class="sxs-lookup"><span data-stu-id="ec0b1-145">Msiexec.exe</span></span>
-   <span data-ttu-id="ec0b1-146">Msoobe.exe</span><span class="sxs-lookup"><span data-stu-id="ec0b1-146">Msoobe.exe</span></span>
-   <span data-ttu-id="ec0b1-147">Rundll32.exe</span><span class="sxs-lookup"><span data-stu-id="ec0b1-147">Rundll32.exe</span></span>
-   <span data-ttu-id="ec0b1-148">Setup.exe</span><span class="sxs-lookup"><span data-stu-id="ec0b1-148">Setup.exe</span></span>
-   <span data-ttu-id="ec0b1-149">St5unst.exe</span><span class="sxs-lookup"><span data-stu-id="ec0b1-149">St5unst.exe</span></span>
-   <span data-ttu-id="ec0b1-150">Unwise.exe</span><span class="sxs-lookup"><span data-stu-id="ec0b1-150">Unwise.exe</span></span>
-   <span data-ttu-id="ec0b1-151">Unwise32.exe</span><span class="sxs-lookup"><span data-stu-id="ec0b1-151">Unwise32.exe</span></span>
-   <span data-ttu-id="ec0b1-152">Werfault.exe</span><span class="sxs-lookup"><span data-stu-id="ec0b1-152">Werfault.exe</span></span>
-   <span data-ttu-id="ec0b1-153">Winhlp32.exe</span><span class="sxs-lookup"><span data-stu-id="ec0b1-153">Winhlp32.exe</span></span>
-   <span data-ttu-id="ec0b1-154">Wlrmdr.exe</span><span class="sxs-lookup"><span data-stu-id="ec0b1-154">Wlrmdr.exe</span></span>
-   <span data-ttu-id="ec0b1-155">Wuapp.exe</span><span class="sxs-lookup"><span data-stu-id="ec0b1-155">Wuapp.exe</span></span>

<span data-ttu-id="ec0b1-156">Die vorangehenden Listen werden in den folgenden Registrierungs Werten gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ec0b1-156">The preceding lists are stored in the following registry values.</span></span>

> [!Note]  
> <span data-ttu-id="ec0b1-157">Diese Listen sollten nicht von Anwendungen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="ec0b1-157">These lists should not be modified by applications.</span></span> <span data-ttu-id="ec0b1-158">Verwenden Sie eine der Methoden der Ausschlussliste, die weiter oben in diesem Thema beschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="ec0b1-158">Use one of the exclusion list methods described earlier in this topic for the same experience.</span></span>

 

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FileAssociation
                     AddRemoveApps
                     HostApps
```

## <a name="related-topics"></a><span data-ttu-id="ec0b1-159">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ec0b1-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec0b1-160">Die Taskleiste</span><span class="sxs-lookup"><span data-stu-id="ec0b1-160">The Taskbar</span></span>](taskbar.md)
</dt> <dt>

[<span data-ttu-id="ec0b1-161">Task leisten Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="ec0b1-161">Taskbar Extensions</span></span>](taskbar-extensions.md)
</dt> </dl>

 

 
