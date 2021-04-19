---
description: Benutzerdefinierte Aktionen können einem ProgressBar-Steuerelement Zeit-und Fortschrittsinformationen hinzufügen. Weitere Informationen zum Erstellen eines Aktions Anzeige Dialogfelds mit einer ProgressBar finden Sie unter Erstellen eines ProgressBar-Steuer Elements.
ms.assetid: 101e6b59-3791-450c-9dc6-8930bd665a93
title: Hinzufügen von benutzerdefinierten Aktionen zur ProgressBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ff2b6da9e72a37329b26cfce7590bab5f9792db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347964"
---
# <a name="adding-custom-actions-to-the-progressbar"></a><span data-ttu-id="b4420-104">Hinzufügen von benutzerdefinierten Aktionen zur ProgressBar</span><span class="sxs-lookup"><span data-stu-id="b4420-104">Adding Custom Actions to the ProgressBar</span></span>

<span data-ttu-id="b4420-105">[Benutzerdefinierte Aktionen](custom-actions.md) können einem [ProgressBar](progressbar-control.md) -Steuerelement Zeit-und Fortschrittsinformationen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b4420-105">[Custom Actions](custom-actions.md) can add time and progress information to a [ProgressBar](progressbar-control.md) control.</span></span> <span data-ttu-id="b4420-106">Weitere Informationen zum Erstellen eines Aktions Anzeige Dialogfelds mit einer ProgressBar finden Sie unter [Erstellen eines ProgressBar-Steuer](authoring-a-progressbar-control.md)Elements.</span><span class="sxs-lookup"><span data-stu-id="b4420-106">For more information about creating an action display dialog box having a ProgressBar, see [Authoring a ProgressBar Control](authoring-a-progressbar-control.md).</span></span>

<span data-ttu-id="b4420-107">Beachten Sie, dass dem Windows Installer Paket zwei benutzerdefinierte Aktionen hinzugefügt werden müssen, um Zeit-und Fortschrittsinformationen genau an die ProgressBar zu melden.</span><span class="sxs-lookup"><span data-stu-id="b4420-107">Note that two custom actions must be added to the Windows Installer package to accurately report time and progress information to the ProgressBar.</span></span> <span data-ttu-id="b4420-108">Eine benutzerdefinierte Aktion muss eine verzögerte benutzerdefinierte Aktion sein.</span><span class="sxs-lookup"><span data-stu-id="b4420-108">One custom action must be a deferred custom action.</span></span> <span data-ttu-id="b4420-109">Diese benutzerdefinierte Aktion sollte die benutzerdefinierte Installation vervollständigen und die Beträge einzelner Inkremente an das [ProgressBar](progressbar-control.md) -Steuerelement senden, wenn das Installationsskript vom Installationsprogramm ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b4420-109">This custom action should complete your custom installation and send the amounts of individual increments to the [ProgressBar](progressbar-control.md) control when the installer runs the installation script.</span></span> <span data-ttu-id="b4420-110">Die zweite benutzerdefinierte Aktion muss eine benutzerdefinierte Aktion der unmittelbaren Ausführung sein, die der ProgressBar mitteilt, wie viele Ticks bei der Erfassungs-und Skript Generierungs Phase der Installation der Gesamtanzahl hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b4420-110">The second custom action must be an immediate execution custom action that informs the ProgressBar how many ticks to add to the total count during the acquisition and script generation phase of the installation.</span></span>

<span data-ttu-id="b4420-111">**So fügen Sie der ProgressBar eine benutzerdefinierte Aktion hinzu**</span><span class="sxs-lookup"><span data-stu-id="b4420-111">**To add a custom action to the ProgressBar**</span></span>

1.  <span data-ttu-id="b4420-112">Entscheiden Sie, wie der Fortschritt von der benutzerdefinierten Aktion beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="b4420-112">Decide how the custom action will describe its progress.</span></span> <span data-ttu-id="b4420-113">Beispielsweise könnte eine benutzerdefinierte Aktion, die Registrierungsschlüssel installiert, eine Fortschrittsmeldung anzeigen und die [ProgressBar](progressbar-control.md) jedes Mal aktualisieren, wenn der Installer einen Registrierungsschlüssel schreibt.</span><span class="sxs-lookup"><span data-stu-id="b4420-113">For example, a custom action that installs registry keys could display a progress message and update the [ProgressBar](progressbar-control.md) each time the installer writes one registry key.</span></span>
2.  <span data-ttu-id="b4420-114">Jedes Update durch die benutzerdefinierte Aktion ändert die Länge der [ProgressBar](progressbar-control.md) durch ein konstantes Inkrement.</span><span class="sxs-lookup"><span data-stu-id="b4420-114">Each update by the custom action changes the length of the [ProgressBar](progressbar-control.md) by a constant increment.</span></span> <span data-ttu-id="b4420-115">Geben Sie die Anzahl der Ticks in jedem Inkrement an, oder berechnen Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="b4420-115">Specify or calculate the number of ticks in each increment.</span></span> <span data-ttu-id="b4420-116">In der Regel entspricht eine Änderung der ProgressBar-Länge eines Tick der Installation von einem Byte.</span><span class="sxs-lookup"><span data-stu-id="b4420-116">Typically a change in ProgressBar length of one tick corresponds to the installation of one byte.</span></span> <span data-ttu-id="b4420-117">Wenn das Installationsprogramm z. b. ungefähr 10000 Byte beim Schreiben eines Registrierungsschlüssels installiert, können Sie angeben, dass in einem Inkrement 10000 Ticks vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="b4420-117">For example, if the installer installs approximately 10000 bytes when it writes one registry key, you can specify that there are 10000 ticks in an increment.</span></span>
3.  <span data-ttu-id="b4420-118">Geben Sie die Gesamtzahl der Ticks an, die die benutzerdefinierte Aktion der Länge der [ProgressBar](progressbar-control.md)hinzufügt, oder berechnen Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="b4420-118">Specify or calculate the total number of ticks the custom action adds to the length of the [ProgressBar](progressbar-control.md).</span></span> <span data-ttu-id="b4420-119">Die Anzahl der von der benutzerdefinierten Aktion hinzugefügten Ticks wird in der Regel wie folgt berechnet: (Tick Increment) x (Anzahl der Elemente).</span><span class="sxs-lookup"><span data-stu-id="b4420-119">The number of ticks added by the custom action is usually calculated as: (tick increment) x (number of items).</span></span> <span data-ttu-id="b4420-120">Wenn die benutzerdefinierte Aktion z. b. 10 Registrierungsschlüssel schreibt, installiert der Installer ungefähr 100000 bytes, und das Installationsprogramm muss daher die Schätzung der endgültigen Gesamtlänge der ProgressBar um 100000 Ticks erhöhen.</span><span class="sxs-lookup"><span data-stu-id="b4420-120">For example, if the custom action writes 10 registry keys, the installer installs approximately 100000 bytes and the installer therefore must increase the estimate of the final total length of the ProgressBar by 100000 ticks.</span></span>
    > [!Note]  
    > <span data-ttu-id="b4420-121">Um dies dynamisch zu berechnen, muss die benutzerdefinierte Aktion einen Abschnitt enthalten, der sofort während der Skript Generierung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b4420-121">To calculate this dynamically, the custom action must contain a section that is immediately executed during script generation.</span></span> <span data-ttu-id="b4420-122">Die Menge der Ticks, die von der benutzerdefinierten Aktion der verzögerten Ausführung gemeldet wird, muss mit der Anzahl der Ticks übereinstimmen, die durch die sofortige Ausführungs Aktion der Gesamtzahl der Ticks hinzugefügt wird</span><span class="sxs-lookup"><span data-stu-id="b4420-122">The amount of ticks reported by your deferred execution custom action must be equal to the number of ticks added to the total tick count by the immediate execution action.</span></span> <span data-ttu-id="b4420-123">Wenn dies nicht der Fall ist, ist die vom timeremainung-Text Steuerelement gemeldete Zeit ungenau.</span><span class="sxs-lookup"><span data-stu-id="b4420-123">If this is not the case, the time remaining as reported by the TimeRemaining text control will be inaccurate.</span></span>

     

4.  <span data-ttu-id="b4420-124">Trennen Sie Ihre benutzerdefinierte Aktion in zwei Code Abschnitte: einen Abschnitt, der während der Skript Generierungs Phase ausgeführt wird, und einen Abschnitt, der während der Ausführungsphase der Installation ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b4420-124">Separate your custom action into two sections of code: a section that runs during the script generation phase and a section that runs during the execution phase of the installation.</span></span> <span data-ttu-id="b4420-125">Hierfür können Sie zwei Dateien verwenden, oder Sie können eine Datei verwenden, indem Sie im Ausführ Modus des Installers eine Anlage ausführen.</span><span class="sxs-lookup"><span data-stu-id="b4420-125">You can do this using two files or you can use one file by conditioning on the run mode of the installer.</span></span> <span data-ttu-id="b4420-126">Im folgenden Beispiel wird eine Datei verwendet, und der Installationsstatus wird überprüft.</span><span class="sxs-lookup"><span data-stu-id="b4420-126">The following sample uses one file and checks the installation state.</span></span> <span data-ttu-id="b4420-127">Die Abschnitte des Beispiels sind abhängig davon, ob sich das Installationsprogramm in der Ausführungs-oder Skript Generierungs Phase der Installation befindet, abhängig davon, ob es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b4420-127">Sections of the sample are conditioned to run depending on whether the installer is in the execution or script generation phase of the installation.</span></span>
5.  <span data-ttu-id="b4420-128">Der Abschnitt, der während der Erstellung des Skripts ausgeführt wird, sollte die Schätzung der endgültigen Gesamtlänge der [ProgressBar](progressbar-control.md) durch die Gesamtzahl der Ticks in der benutzerdefinierten Aktion erhöhen.</span><span class="sxs-lookup"><span data-stu-id="b4420-128">The section that runs during script generation should increase the estimate of the final total length of the [ProgressBar](progressbar-control.md) by the total number of ticks in the custom action.</span></span> <span data-ttu-id="b4420-129">Dies erfolgt durch Senden einer Statusmeldung " **progressaddition** ".</span><span class="sxs-lookup"><span data-stu-id="b4420-129">This is done by sending a **ProgressAddition** progress message.</span></span>
6.  <span data-ttu-id="b4420-130">Der Abschnitt, der in der Ausführungsphase der Installation ausgeführt wird, sollte Meldungs Text und Vorlagen einrichten, um den Benutzer darüber zu informieren, was die benutzerdefinierte Aktion ausführt, und den Installer beim Aktualisieren des [ProgressBar](progressbar-control.md) -Steuer Elements weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="b4420-130">The section that runs during the execution phase of installation should set up message text and templates to inform the user about what the custom action is doing and to direct the installer on updating the [ProgressBar](progressbar-control.md) control.</span></span> <span data-ttu-id="b4420-131">Informieren Sie den Installer beispielsweise darüber, dass die ProgressBar ein Inkrement vorwärts bewegt wird, und senden Sie mit jedem Update eine explizite Statusmeldung.</span><span class="sxs-lookup"><span data-stu-id="b4420-131">For example, inform the installer to move the ProgressBar forward one increment and send an explicit progress message with each update.</span></span> <span data-ttu-id="b4420-132">In diesem Abschnitt gibt es in der Regel eine Schleife, wenn die benutzerdefinierte Aktion etwas installiert.</span><span class="sxs-lookup"><span data-stu-id="b4420-132">There is usually a loop in this section if the custom action is installing something.</span></span> <span data-ttu-id="b4420-133">Bei jedem Durchlauf dieser Schleife kann das Installationsprogramm ein Verweis Element, z. b. einen Registrierungsschlüssel, installieren und das ProgressBar-Steuerelement aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="b4420-133">With each pass through this loop, the installer can install one reference item such as a registry key and update the ProgressBar control</span></span>
7.  <span data-ttu-id="b4420-134">Fügen Sie Ihrem Windows Installer Paket eine benutzerdefinierte Aktion für die sofortige Ausführung hinzu.</span><span class="sxs-lookup"><span data-stu-id="b4420-134">Add an immediate execution custom action to your Windows Installer package.</span></span> <span data-ttu-id="b4420-135">Durch diese benutzerdefinierte Aktion wird der [ProgressBar](progressbar-control.md) mitgeteilt, wie viel im Rahmen der Erfassungs-und Skript Generierungs Phasen der Installation fortzufahren ist.</span><span class="sxs-lookup"><span data-stu-id="b4420-135">This custom action informs the [ProgressBar](progressbar-control.md) how much to advance during the aquisition and script generation phases of the installation.</span></span> <span data-ttu-id="b4420-136">Im folgenden Beispiel ist die Quelle die dll, die durch Kompilieren des Beispielcodes erstellt wird, und das Ziel ist der Einstiegspunkt, caprogress.</span><span class="sxs-lookup"><span data-stu-id="b4420-136">For the following sample, the source is the DLL created by compiling the sample code and the target is the entry point, CAProgress.</span></span>
8.  <span data-ttu-id="b4420-137">Fügen Sie Ihrem Windows Installer Paket eine benutzerdefinierte Aktion für die verzögerte Ausführung hinzu.</span><span class="sxs-lookup"><span data-stu-id="b4420-137">Add a deferred execution custom action to your Windows Installer package.</span></span> <span data-ttu-id="b4420-138">Durch diese benutzerdefinierte Aktion werden die Schritte der eigentlichen Installation abgeschlossen und der [ProgressBar](progressbar-control.md) mitgeteilt, wie viel Zeit für die Ausführung des Installations Skripts durch das Installationsprogramm erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="b4420-138">This custom action completes the steps of the actual installation and informs the [ProgressBar](progressbar-control.md) how much to advance the bar at the time when the installer runs the installation script.</span></span> <span data-ttu-id="b4420-139">Im folgenden Beispiel ist die Quelle die dll, die durch Kompilieren des Beispielcodes erstellt wird, und das Ziel ist der Einstiegspunkt, caprogress.</span><span class="sxs-lookup"><span data-stu-id="b4420-139">For the following sample, the source is the DLL created by compiling the sample code and the target is the entry point, CAProgress.</span></span>
9.  <span data-ttu-id="b4420-140">Planen Sie sowohl benutzerdefinierte Aktionen zwischen [InstallInitialize](installinitialize-action.md) und [InstallFinalize](installfinalize-action.md) in der [InstallExecuteSequence](installexecutesequence-table.md) -Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b4420-140">Schedule both custom actions between [InstallInitialize](installinitialize-action.md) and [InstallFinalize](installfinalize-action.md) in the [InstallExecuteSequence](installexecutesequence-table.md) table.</span></span> <span data-ttu-id="b4420-141">Die verzögerte benutzerdefinierte Aktion sollte unmittelbar nach der benutzerdefinierten Aktion "sofortige Ausführung" geplant werden.</span><span class="sxs-lookup"><span data-stu-id="b4420-141">The deferred custom action should be scheduled immediately after the immediate execution custom action.</span></span> <span data-ttu-id="b4420-142">Der Installer führt die verzögerte benutzerdefinierte Aktion erst aus, nachdem das Skript ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="b4420-142">The installer will not run the deferred custom action until the script is executed.</span></span>

<span data-ttu-id="b4420-143">Im folgenden Beispiel wird gezeigt, wie der [ProgressBar](progressbar-control.md)eine benutzerdefinierte Aktion hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b4420-143">The following sample shows how a custom action can be added to the [ProgressBar](progressbar-control.md).</span></span> <span data-ttu-id="b4420-144">Die Quelle der beiden benutzerdefinierten Aktionen ist die dll, die durch Kompilieren des Beispielcodes erstellt wird, und das Ziel der beiden benutzerdefinierten Aktionen ist der Einstiegspunkt, caprogress.</span><span class="sxs-lookup"><span data-stu-id="b4420-144">The source of both custom actions is the DLL created by compiling the sample code and the target of both custom actions is the entry point, CAProgress.</span></span> <span data-ttu-id="b4420-145">In diesem Beispiel werden keine tatsächlichen Änderungen am System vorgenommen, sondern die ProgressBar so betrieben, als ob 10 Verweis Elemente mit einer Größe von ungefähr 10.000 Byte installiert werden.</span><span class="sxs-lookup"><span data-stu-id="b4420-145">This sample does not make any actual changes to the system, but operates the ProgressBar as if installing 10 reference items that are each approximately 10,000 bytes in size.</span></span> <span data-ttu-id="b4420-146">Das Installationsprogramm aktualisiert die Meldung und die ProgressBar bei jeder Installation eines Verweis Elements.</span><span class="sxs-lookup"><span data-stu-id="b4420-146">The installer updates the message and ProgressBar each time it installs a reference item.</span></span>


```C++
#include <windows.h>
#include <msiquery.h>
#pragma comment(lib, "msi.lib")

// Specify or calculate the number of ticks in an increment
// to the ProgressBar
const UINT iTickIncrement = 10000;
 
// Specify or calculate the total number of ticks the custom 
// action adds to the length of the ProgressBar
const UINT iNumberItems = 10;
const UINT iTotalTicks = iTickIncrement * iNumberItems;
 
UINT __stdcall CAProgress(MSIHANDLE hInstall)
{
    // Tell the installer to check the installation state and execute
    // the code needed during the rollback, acquisition, or
    // execution phases of the installation.
  
    if (MsiGetMode(hInstall,MSIRUNMODE_SCHEDULED) == TRUE)
    {
        PMSIHANDLE hActionRec = MsiCreateRecord(3);
        PMSIHANDLE hProgressRec = MsiCreateRecord(3);

        // Installer is executing the installation script. Set up a
        // record specifying appropriate templates and text for
        // messages that will inform the user about what the custom
        // action is doing. Tell the installer to use this template and 
        // text in progress messages.
 
        MsiRecordSetString(hActionRec, 1, TEXT("MyCustomAction"));
        MsiRecordSetString(hActionRec, 2, TEXT("Incrementing the Progress Bar..."));
        MsiRecordSetString(hActionRec, 3, TEXT("Incrementing tick [1] of [2]"));
        UINT iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_ACTIONSTART, hActionRec);
        if ((iResult == IDCANCEL))
            return ERROR_INSTALL_USEREXIT;
              
        // Tell the installer to use explicit progress messages.
        MsiRecordSetInteger(hProgressRec, 1, 1);
        MsiRecordSetInteger(hProgressRec, 2, 1);
        MsiRecordSetInteger(hProgressRec, 3, 0);
        iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_PROGRESS, hProgressRec);
        if ((iResult == IDCANCEL))
            return ERROR_INSTALL_USEREXIT;
              
        //Specify that an update of the progress bar's position in
        //this case means to move it forward by one increment.
        MsiRecordSetInteger(hProgressRec, 1, 2);
        MsiRecordSetInteger(hProgressRec, 2, iTickIncrement);
        MsiRecordSetInteger(hProgressRec, 3, 0);
 
        // The following loop sets up the record needed by the action
        // messages and tells the installer to send a message to update
        // the progress bar.

        MsiRecordSetInteger(hActionRec, 2, iTotalTicks);
       
        for( int i = 0; i < iTotalTicks; i+=iTickIncrement)
        {
            MsiRecordSetInteger(hActionRec, 1, i);

            iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_ACTIONDATA, hActionRec);
            if ((iResult == IDCANCEL))
                return ERROR_INSTALL_USEREXIT;
          
            iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_PROGRESS, hProgressRec);
            if ((iResult == IDCANCEL))
                return ERROR_INSTALL_USEREXIT;
   
            //A real custom action would have code here that does a part
            //of the installation. For this sample, code that installs
            //10 registry keys.
            Sleep(1000);
                    
        }
        return ERROR_SUCCESS;
    }
    else
    {
        // Installer is generating the installation script of the
        // custom action.
  
        // Tell the installer to increase the value of the final total
        // length of the progress bar by the total number of ticks in
        // the custom action.
        PMSIHANDLE hProgressRec = MsiCreateRecord(2);

         MsiRecordSetInteger(hProgressRec, 1, 3);
            MsiRecordSetInteger(hProgressRec, 2, iTotalTicks);
        UINT iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_PROGRESS, hProgressRec);
           if ((iResult == IDCANCEL))
            return ERROR_INSTALL_USEREXIT;     
        return ERROR_SUCCESS;
     }
}
```



 

 



