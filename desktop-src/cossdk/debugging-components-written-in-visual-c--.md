---
description: Wenn Sie bereit sind, die com+-Funktionalität in den Microsoft Visual C++ Komponenten zu debuggen, können Sie Visual C++ Projekt oder das Verwaltungs Programmkomponenten Dienste konfigurieren, um den Debugger zu starten.
ms.assetid: 206467ac-108a-49de-a884-66959dc77650
title: In Visual C++ geschriebene debuggingkomponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14e4b6324cc69531f09612c2af37fa03a036fd4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106338896"
---
# <a name="debugging-components-written-in-visual-c"></a><span data-ttu-id="e4576-103">In Visual C++ geschriebene debuggingkomponenten</span><span class="sxs-lookup"><span data-stu-id="e4576-103">Debugging Components Written in Visual C++</span></span>

<span data-ttu-id="e4576-104">Wenn Sie bereit sind, die com+-Funktionalität in den Microsoft Visual C++ Komponenten zu debuggen, können Sie Visual C++ Projekt oder das Verwaltungs Programmkomponenten Dienste konfigurieren, um den Debugger zu starten.</span><span class="sxs-lookup"><span data-stu-id="e4576-104">When you are ready to debug the COM+ functionality in your Microsoft Visual C++ components, you can configure Visual C++ project or the Component Services administrative tool to launch the debugger.</span></span> <span data-ttu-id="e4576-105">Wenn Sie Visual C++ verwenden, können Sie mit einem Remote Client debuggen, indem Sie das OLE-RPC-und JIT-Debugging (Just-in-Time) verwenden.</span><span class="sxs-lookup"><span data-stu-id="e4576-105">If you are using Visual C++, you can debug with a remote client using OLE RPC and just-in-time (JIT) debugging.</span></span> <span data-ttu-id="e4576-106">Wenn Sie den Client nicht im Debugger ausführen können oder wenn der Client auf einem anderen Computer ausgeführt wird, können Sie die com+-Einstellung **in Debugger** verwenden.</span><span class="sxs-lookup"><span data-stu-id="e4576-106">If you are unable to run your client under the debugger or if the client is running on another machine, you can use the COM+ **Launch in debugger** setting.</span></span> <span data-ttu-id="e4576-107">Diese finden Sie im Verwaltungs Programmkomponenten Dienste als Kontrollkästchen auf der Registerkarte **erweitert** im Dialogfeld COM+-Anwendungs **Eigenschaften** .</span><span class="sxs-lookup"><span data-stu-id="e4576-107">You will find this in the Component Services administrative tool as a check box on the **Advanced** tab of the COM+ application **Properties** dialog box.</span></span>

<span data-ttu-id="e4576-108">Wenn Sie das Debuggen abgeschlossen haben, sollten Sie die com+-Anwendungen Herunterfahren, die Sie Debuggen.</span><span class="sxs-lookup"><span data-stu-id="e4576-108">When you are finished debugging, you should shut down the COM+ applications you are debugging.</span></span> <span data-ttu-id="e4576-109">Wenn ein Server Prozess weiterhin ausgeführt wird, erhalten Sie möglicherweise eine Fehlermeldung, wenn Sie das nächste Mal versuchen, eine DLL zu erstellen, wenn die vorhandene DLL noch in den Arbeitsspeicher geladen ist.</span><span class="sxs-lookup"><span data-stu-id="e4576-109">If a server process is left running, you might get an error message the next time you try to build a DLL when the existing DLL is still loaded in memory.</span></span> <span data-ttu-id="e4576-110">Zum Herunterfahren einer COM+-Anwendung klicken Sie in der Konsolen Struktur mit der rechten Maustaste auf die Anwendung, und klicken Sie dann auf **herunter** fahren.</span><span class="sxs-lookup"><span data-stu-id="e4576-110">To shut down a COM+ application, right-click the application in the console tree and then click **Shut down**.</span></span>

> [!Note]  
> <span data-ttu-id="e4576-111">Wenn Sie Transaktionen verwenden, möchten Sie möglicherweise auch den Transaktions Timeout erhöhen, der standardmäßig 60 Sekunden beträgt.</span><span class="sxs-lookup"><span data-stu-id="e4576-111">If you are using transactions, you might also want to increase the transaction time-out, which defaults to 60 seconds.</span></span> <span data-ttu-id="e4576-112">Sie können auch den Wert 0 angeben und einen unbegrenzten Transaktions Timeout Zeitraum angeben.</span><span class="sxs-lookup"><span data-stu-id="e4576-112">You can also specify a value of 0, effectively specifying an infinite transaction time-out period.</span></span> <span data-ttu-id="e4576-113">Ändern Sie mithilfe des Verwaltungs Programms Komponenten Dienste die Einstellung Transaktions Timeout auf der Registerkarte **Optionen** des Fensters **Eigenschaften von Arbeitsplatz** .</span><span class="sxs-lookup"><span data-stu-id="e4576-113">Using the Component Services administrative tool, change the transaction time-out setting on the **Options** tab of the **My Computer Properties** window.</span></span>

 

## <a name="debugging-server-application-components-with-visual-c"></a><span data-ttu-id="e4576-114">Debuggen von Server Anwendungskomponenten mit Visual C++</span><span class="sxs-lookup"><span data-stu-id="e4576-114">Debugging Server Application Components with Visual C++</span></span>

<span data-ttu-id="e4576-115">Wenn Sie com+-Server Anwendungen debuggen, können Sie Remote Aufrufe Debuggen, indem Sie sowohl die Client-als auch die Serveranwendung in den Debugger laden.</span><span class="sxs-lookup"><span data-stu-id="e4576-115">When debugging COM+ server applications, you may want to debug remote calls by loading both the client and the server application into the debugger.</span></span> <span data-ttu-id="e4576-116">Mit Visual C++ können Sie Remote Aufrufe ihrer Komponenten über die Just-in-time (JIT)-und OLE-RPC-Einstellungen Debuggen.</span><span class="sxs-lookup"><span data-stu-id="e4576-116">With Visual C++, you can debug remote calls to your components through the just-in-time (JIT) and OLE RPC settings.</span></span> <span data-ttu-id="e4576-117">Die JIT-Einstellung bewirkt, dass die kompilierte Komponente den Visual C++ Debugger startet, wenn ein Fehler auftritt. mit der OLE-RPC-Einstellung kann der Debugger beim Durchlaufen des Codes von Client zu Komponente wechseln.</span><span class="sxs-lookup"><span data-stu-id="e4576-117">The JIT setting causes the compiled component to start the Visual C++ debugger when an error occurs; the OLE RPC setting enables the debugger to step from client to component as you step through your code.</span></span>

<span data-ttu-id="e4576-118">Wenn diese Funktionen aktiviert sind, können Sie den Client unter dem Debugger starten.</span><span class="sxs-lookup"><span data-stu-id="e4576-118">When these features are enabled, you can start your client under the debugger.</span></span> <span data-ttu-id="e4576-119">Wenn der Client die Komponente aufruft, führt der Debugger einen Einzelschritt in den Code der Komponente im Server Prozess aus, auch wenn sich der Server auf einem anderen Computer im Netzwerk befindet.</span><span class="sxs-lookup"><span data-stu-id="e4576-119">When the client makes a call to your component, the debugger will step into the component's code in the server process, even if the server is on a different computer on the network.</span></span> <span data-ttu-id="e4576-120">Eine Debugsitzung wird ggf. automatisch auf dem Server Computer gestartet.</span><span class="sxs-lookup"><span data-stu-id="e4576-120">A debugging session is automatically started on the server computer if necessary.</span></span> <span data-ttu-id="e4576-121">Ebenso wird beim einmaligen durch springen der Return-Anweisung im Code der Komponente das Debuggen zur nächsten Anweisung im Client Code zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e4576-121">Similarly, single stepping past the return statement in the component's code will return debugging to the next statement in the client's code.</span></span>

> [!Note]  
> <span data-ttu-id="e4576-122">Mithilfe der com+-Einstellung **in der Debugger** -Einstellung können Sie möglicherweise einige Schritte speichern.</span><span class="sxs-lookup"><span data-stu-id="e4576-122">You may be able to save a few steps by using the COM+ **Launch in debugger** setting.</span></span> <span data-ttu-id="e4576-123">Dies ermöglicht es Ihnen, den Visual C++ (oder einen anderen) Debugger anzugeben, ohne spezielle Debugeinstellungen in der Visual C++ Umgebung vornehmen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="e4576-123">This allows you to specify the Visual C++ (or other) debugger without having to make special debug settings in the Visual C++ environment.</span></span> <span data-ttu-id="e4576-124">Diese finden Sie im Verwaltungs Programmkomponenten Dienste als Kontrollkästchen auf der Registerkarte **erweitert** im Dialogfeld COM+-Anwendungs **Eigenschaften** .</span><span class="sxs-lookup"><span data-stu-id="e4576-124">You will find this in the Component Services administrative tool as a check box on the **Advanced** tab of the COM+ application **Properties** dialog box.</span></span> <span data-ttu-id="e4576-125">Weitere Informationen finden Sie unter "Debuggen ohne Visual C++" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="e4576-125">For more information, see "Debugging Without Visual C++" in this topic.</span></span>

 

<span data-ttu-id="e4576-126">Wenn die COM+-Anwendung, die die Komponente enthält, eine Serveranwendung ist, müssen Sie zunächst die Anwendung mithilfe des Verwaltungs Programms Komponenten Dienste Herunterfahren.</span><span class="sxs-lookup"><span data-stu-id="e4576-126">When the COM+ application containing your component is a server application, you must begin by shutting down the application using the Component Services administrative tool.</span></span> <span data-ttu-id="e4576-127">Klicken Sie hierzu in der Konsolen Struktur mit der rechten Maustaste auf die COM+-Anwendung, und klicken Sie dann auf **herunter** fahren.</span><span class="sxs-lookup"><span data-stu-id="e4576-127">To do this, right-click the COM+ application in the console tree and then click **Shut down**.</span></span>

<span data-ttu-id="e4576-128">**So aktivieren Sie das RPC-Debugging in Visual C++**</span><span class="sxs-lookup"><span data-stu-id="e4576-128">**To enable RPC debugging in Visual C++**</span></span>

1.  <span data-ttu-id="e4576-129">Klicken Sie in Visual C++ im **Menü Extras** auf **Optionen**.</span><span class="sxs-lookup"><span data-stu-id="e4576-129">In Visual C++, on the **Tools** menu, click **Options**.</span></span>

2.  <span data-ttu-id="e4576-130">Aktivieren Sie im Dialogfeld **Optionen** auf der Registerkarte **Debuggen** die Kontrollkästchen **OLE-RPC-Debuggen** und **Just-in-Time-Debuggen** .</span><span class="sxs-lookup"><span data-stu-id="e4576-130">In the **Options** dialog box, on the **Debug** tab, select the **OLE RPC debugging** and **Just-in time debugging** check boxes.</span></span>

3.  <span data-ttu-id="e4576-131">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="e4576-131">Click **OK**.</span></span>

<span data-ttu-id="e4576-132">Starten Sie das-Client Projekt im Debugger, um mit dem Debuggen zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="e4576-132">To begin debugging, start your client project in the debugger.</span></span>

<span data-ttu-id="e4576-133">Sie können die Komponente auch Debuggen, ohne den Client im Debugger zu starten.</span><span class="sxs-lookup"><span data-stu-id="e4576-133">You can also debug your component without launching your client in the debugger.</span></span> <span data-ttu-id="e4576-134">In diesem Fall muss die Komponente den Debugger eigenständig starten.</span><span class="sxs-lookup"><span data-stu-id="e4576-134">In this case, your component must launch the debugger on its own.</span></span> <span data-ttu-id="e4576-135">Zu diesem Zweck muss das Komponenten Projekt eine ausführbare Datei für die Debugsitzung sowie die com+-Anwendungs-ID angeben.</span><span class="sxs-lookup"><span data-stu-id="e4576-135">To do this, your component project must specify an executable for the debug session, along with the COM+ application ID.</span></span>

<span data-ttu-id="e4576-136">**So aktivieren Sie eine Server Anwendungs Komponente, um den Visual C++ Debugger zu starten**</span><span class="sxs-lookup"><span data-stu-id="e4576-136">**To enable a server application component to launch the Visual C++ debugger**</span></span>

1.  <span data-ttu-id="e4576-137">Klicken Sie im Menü **Projekt** auf **Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="e4576-137">On the **Project** menu, click **Settings**.</span></span>

2.  <span data-ttu-id="e4576-138">Wählen Sie im Dialogfeld **Projekteinstellungen** im Feld **Einstellungen für** die Option **Win32 Debug** aus.</span><span class="sxs-lookup"><span data-stu-id="e4576-138">In the **Project Settings** dialog box, in the **Settings For** box, select **Win32 Debug**.</span></span>

3.  <span data-ttu-id="e4576-139">Wählen Sie auf der Registerkarte **Debuggen** im Feld **Kategorie** die Option **Allgemein** aus.</span><span class="sxs-lookup"><span data-stu-id="e4576-139">On the **Debug** tab, in the **Category** box, select **General**.</span></span>

4.  <span data-ttu-id="e4576-140">Geben Sie im Feld **ausführbare Datei für Debugsitzung** den voll qualifizierten Pfad für Dllhost.exe ein, gefolgt von einem Argument, das die Anwendungs-ID der com+-Anwendung angibt, die die Komponente enthält.</span><span class="sxs-lookup"><span data-stu-id="e4576-140">In the **Executable for debug session** box, enter the fully qualified path for Dllhost.exe, followed by an argument specifying the application ID of the COM+ application containing the component.</span></span>

    > [!Note]  
    > <span data-ttu-id="e4576-141">Mithilfe des Verwaltungs Tools Komponenten Dienste finden Sie die Anwendungs-ID auf der Registerkarte **Allgemein** im Dialogfeld **Eigenschaften** der com+-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="e4576-141">Using the Component Services administrative tool, you will find the application ID on the **General** tab of the COM+ application's **Properties** dialog box.</span></span> <span data-ttu-id="e4576-142">Dies ist ein Beispiel:</span><span class="sxs-lookup"><span data-stu-id="e4576-142">Following is an example:</span></span>

     

    > [!Note]  
    > <span data-ttu-id="e4576-143">C: \\ Winnt \\ system32 \\Dllhost.exe/ProcessID: {ApplicationId}</span><span class="sxs-lookup"><span data-stu-id="e4576-143">C:\\Winnt\\System32\\Dllhost.exe /ProcessID:{applicationID}</span></span>

     

5.  <span data-ttu-id="e4576-144">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="e4576-144">Click **OK**.</span></span>

<span data-ttu-id="e4576-145">Sie können jetzt Breakpoints festlegen, den Debugger starten und mit dem Ausführen von Aufrufen an die Komponente beginnen.</span><span class="sxs-lookup"><span data-stu-id="e4576-145">You can now set breakpoints, start the debugger, and begin making calls to your component.</span></span>

## <a name="debugging-library-application-components-with-visual-c"></a><span data-ttu-id="e4576-146">Debuggen von Bibliotheks Anwendungskomponenten mit Visual C++</span><span class="sxs-lookup"><span data-stu-id="e4576-146">Debugging Library Application Components with Visual C++</span></span>

<span data-ttu-id="e4576-147">Wenn Sie Komponenten in einer Bibliotheks Anwendung debuggen möchten, müssen Sie das Projekt des Clients konfigurieren, da der Client Prozess die Bibliotheks Anwendung hostet.</span><span class="sxs-lookup"><span data-stu-id="e4576-147">To debug components in a library application, you must configure the client's project because the client's process will host the library application.</span></span>

<span data-ttu-id="e4576-148">**So aktivieren Sie das Debuggen von Bibliotheksanwendungen mit Visual C++**</span><span class="sxs-lookup"><span data-stu-id="e4576-148">**To enable library application debugging with Visual C++**</span></span>

1.  <span data-ttu-id="e4576-149">Klicken Sie in Visual C++ im Menü **Projekt** auf **Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="e4576-149">In Visual C++, on the **Project** menu, click **Settings**.</span></span>

2.  <span data-ttu-id="e4576-150">Klicken Sie im Dialogfeld **Projekteinstellungen** im Feld **Einstellungen für** auf **Win32 Debuggen**.</span><span class="sxs-lookup"><span data-stu-id="e4576-150">In the **Project Settings** dialog box, in the **Settings For** box, click **Win32 Debug**.</span></span>

3.  <span data-ttu-id="e4576-151">Klicken Sie auf der Registerkarte **Debuggen** im Feld **Kategorie** auf **zusätzliche DLLs**.</span><span class="sxs-lookup"><span data-stu-id="e4576-151">On the **Debug** tab, in the **Category** box, click **Additional DLLs**.</span></span>

4.  <span data-ttu-id="e4576-152">Fügen Sie in der Liste **Module** die Komponenten-DLLs in der Bibliotheks Anwendung hinzu.</span><span class="sxs-lookup"><span data-stu-id="e4576-152">In the **Modules** list, add the component DLLs in your library application.</span></span> <span data-ttu-id="e4576-153">Dies ermöglicht es Ihnen, Breakpoints festzulegen, bevor die dll tatsächlich geladen wird.</span><span class="sxs-lookup"><span data-stu-id="e4576-153">This allows you to set breakpoints before your DLL is actually loaded.</span></span>

5.  <span data-ttu-id="e4576-154">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="e4576-154">Click **OK**.</span></span>

## <a name="debugging-without-visual-c"></a><span data-ttu-id="e4576-155">Debuggen ohne Visual C++</span><span class="sxs-lookup"><span data-stu-id="e4576-155">Debugging Without Visual C++</span></span>

<span data-ttu-id="e4576-156">Unabhängig davon, ob Sie Visual C++ für das Debuggen verwenden, können Sie die Einstellung **in Debugger starten** verwenden, um den Debugger anzugeben, in dem die Komponenten ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e4576-156">Whether or not you are using Visual C++ for debugging, you can use the **Launch in debugger** setting to specify the debugger in which your components should run.</span></span>

<span data-ttu-id="e4576-157">**So geben Sie einen Debugger über das Verwaltungs Programm "Komponenten Dienste" an**</span><span class="sxs-lookup"><span data-stu-id="e4576-157">**To specify a debugger from the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="e4576-158">Wählen Sie in der Konsolen Struktur die COM+-Bibliotheks Anwendung aus, die die Komponenten enthält, die Sie debuggen möchten.</span><span class="sxs-lookup"><span data-stu-id="e4576-158">In the console tree, select the COM+ library application containing the components you wish to debug.</span></span>

2.  <span data-ttu-id="e4576-159">Klicken Sie mit der rechten Maustaste auf die Anwendung, und klicken Sie auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="e4576-159">Right-click the application, and then click **Properties**.</span></span>

3.  <span data-ttu-id="e4576-160">Klicken Sie im Dialogfeld **Eigenschaften** der Anwendung auf die Registerkarte **erweitert** .</span><span class="sxs-lookup"><span data-stu-id="e4576-160">In the application's **Properties** dialog box, click the **Advanced** tab.</span></span>

4.  <span data-ttu-id="e4576-161">Aktivieren Sie unter **Debuggen** das Kontrollkästchen **in Debugger starten** .</span><span class="sxs-lookup"><span data-stu-id="e4576-161">Under **Debugging**, select the **Launch in debugger** check box.</span></span>

5.  <span data-ttu-id="e4576-162">Geben Sie im Feld **Debuggerpfad** den Pfad zu dem Debugger ein, den Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="e4576-162">In the **Debugger path** box, enter path to the debugger you want to use.</span></span> <span data-ttu-id="e4576-163">Sie können auch auf **Durchsuchen** klicken, um den Debugger zu suchen.</span><span class="sxs-lookup"><span data-stu-id="e4576-163">You can also click **Browse** to locate the debugger.</span></span> <span data-ttu-id="e4576-164">Im folgenden finden Sie ein Beispiel: C: \\ Winnt \\ system32 \\Ntsd.exe.</span><span class="sxs-lookup"><span data-stu-id="e4576-164">Following is an example: C:\\Winnt\\System32\\Ntsd.exe.</span></span>

6.  <span data-ttu-id="e4576-165">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="e4576-165">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4576-166">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e4576-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4576-167">In Visual Basic geschriebene debuggingkomponenten</span><span class="sxs-lookup"><span data-stu-id="e4576-167">Debugging Components Written in Visual Basic</span></span>](debugging-components-written-in-visual-basic.md)
</dt> </dl>

 

 



