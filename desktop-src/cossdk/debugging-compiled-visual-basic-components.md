---
description: Wenn Sie in vielen Fällen nur einen Teil der Komponenten Funktionen in der Microsoft Visual Basic Umgebung debuggen können, gibt es Situationen, in denen Sie Komponenten debuggen müssen, die mit Visual Basic erstellt wurden, nachdem Sie kompiliert wurden. Da dies in der Visual Basic Umgebung nicht möglich ist, müssen Sie stattdessen die Microsoft Visual C++ Umgebung verwenden.
ms.assetid: a58c5884-3c2d-4699-8b19-277003912dfd
title: Debuggen kompilierter Visual Basic Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b32a39f0f1c50e1da4c9534b40658838361225
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126710"
---
# <a name="debugging-compiled-visual-basic-components"></a><span data-ttu-id="06fc9-104">Debuggen kompilierter Visual Basic Komponenten</span><span class="sxs-lookup"><span data-stu-id="06fc9-104">Debugging Compiled Visual Basic Components</span></span>

<span data-ttu-id="06fc9-105">Wenn Sie in vielen Fällen nur einen Teil der Funktionalität Ihrer Komponente innerhalb der Microsoft Visual Basic Umgebung debuggen können, gibt es Situationen, in denen Sie Komponenten debuggen müssen, die mit Visual Basic erstellt wurden, nachdem Sie kompiliert wurden.</span><span class="sxs-lookup"><span data-stu-id="06fc9-105">Given that in many cases you will be able to debug only a portion of your component's functionality within the Microsoft Visual Basic environment, there will be situations in which you will need to debug components built with Visual Basic after they have been compiled.</span></span> <span data-ttu-id="06fc9-106">Da dies in der Visual Basic Umgebung nicht möglich ist, müssen Sie stattdessen die Microsoft Visual C++ Umgebung verwenden.</span><span class="sxs-lookup"><span data-stu-id="06fc9-106">Since the Visual Basic environment doesn't enable this, you must instead use the Microsoft Visual C++ environment.</span></span>

<span data-ttu-id="06fc9-107">**So debuggen Sie eine Visual Basic Komponente in der Visual C++-Umgebung**</span><span class="sxs-lookup"><span data-stu-id="06fc9-107">**To debug a Visual Basic component in the Visual C++ environment**</span></span>

1.  <span data-ttu-id="06fc9-108">Öffnen Sie in Visual Basic 6,0 das Visual Basic Projekt, das Sie debuggen möchten.</span><span class="sxs-lookup"><span data-stu-id="06fc9-108">In Visual Basic 6.0, open the Visual Basic project that you want to debug.</span></span>

2.  <span data-ttu-id="06fc9-109">Klicken Sie im Menü **Datei** auf **YourProject.dllerstellen**.</span><span class="sxs-lookup"><span data-stu-id="06fc9-109">On the **File** menu, click **Make YourProject.dll**.</span></span>

3.  <span data-ttu-id="06fc9-110">Klicken Sie im Dialogfeld **Projekt erstellen** auf **Optionen**.</span><span class="sxs-lookup"><span data-stu-id="06fc9-110">In the **Make Project** dialog box, click **Options**.</span></span>

4.  <span data-ttu-id="06fc9-111">Klicken Sie im Dialogfeld **Projekteigenschaften** auf der Registerkarte **Kompilieren** auf **in systemeigenen Code kompilieren** und dann auf **keine Optimierung** , und aktivieren Sie das Kontrollkästchen **symbolische Debuginformationen erstellen** .</span><span class="sxs-lookup"><span data-stu-id="06fc9-111">In the **Project Properties** dialog box, on the **Compile** tab, click **Compile to Native Code** and **No Optimization** and select the **Create Symbolic Debug Info** check box.</span></span>

5.  <span data-ttu-id="06fc9-112">Klicken Sie auf **OK**, und klicken Sie dann erneut auf **OK** , um das Projekt zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="06fc9-112">Click **OK**, and then click **OK** again to compile your project.</span></span>

6.  <span data-ttu-id="06fc9-113">Verschieben Sie die kompilierte DLL an den Speicherort, an dem com+-Anwendungen normalerweise installiert sind.</span><span class="sxs-lookup"><span data-stu-id="06fc9-113">Move the compiled DLL to the location where COM+ applications are normally installed.</span></span>

    > [!Note]  
    > <span data-ttu-id="06fc9-114">Wenn Sie die dll nicht verschieben, erhalten Sie möglicherweise eine Fehlermeldung, die Sie darüber informiert, dass keine symbolischen Debuginformationen für die dll gefunden werden konnten.</span><span class="sxs-lookup"><span data-stu-id="06fc9-114">If you don't move the DLL, you may get an error message informing you that symbolic debugging information for the DLL could not be located.</span></span> <span data-ttu-id="06fc9-115">Wenn Sie Probleme haben, den Debugger an Haltepunkten in der Komponente anzuhalten, vergewissern Sie sich, dass sich die dll im Standardpaket Verzeichnis befindet, löschen Sie die Komponente aus dem zugehörigen Paket, und fügen Sie die Komponente erneut hinzu.</span><span class="sxs-lookup"><span data-stu-id="06fc9-115">If you have trouble getting the debugger to stop at breakpoints in your component, confirm that the DLL is in the standard packages directory, delete the component from its package, and re-add the component.</span></span>

     

7.  <span data-ttu-id="06fc9-116">Starten Sie Visual C++.</span><span class="sxs-lookup"><span data-stu-id="06fc9-116">Start Visual C++.</span></span>

8.  <span data-ttu-id="06fc9-117">Klicken Sie im Menü **Datei** auf **Arbeitsbereich öffnen**.</span><span class="sxs-lookup"><span data-stu-id="06fc9-117">On the **File** menu, click **Open Workspace**.</span></span>

9.  <span data-ttu-id="06fc9-118">Legen Sie im Dialogfeld **Arbeitsbereich öffnen** den **Dateityp** auf **alle Dateien ( \* . \* )** fest, wählen Sie die kompilierte Komponente aus, und klicken Sie auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="06fc9-118">In the **Open Workspace** dialog box, set **Files of Type** to **All files(\*.\*)**, select your compiled component, and click **Open**.</span></span>

10. <span data-ttu-id="06fc9-119">Klicken Sie im Menü **Datei** auf **Öffnen** (nicht **Arbeitsbereich öffnen**), und öffnen Sie das Visual Basic Modul (Bas), das Formular (. frm) oder die Klasse (. CLS), das Sie debuggen möchten.</span><span class="sxs-lookup"><span data-stu-id="06fc9-119">From the **File** menu, click **Open** (not **Open Workspace**) and open the Visual Basic module (.bas), form (.frm), or class (.cls) that you want to debug.</span></span>

11. <span data-ttu-id="06fc9-120">Klicken Sie im Menü **Projekt** auf **Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="06fc9-120">On the **Project** menu, click **Settings**.</span></span>

12. <span data-ttu-id="06fc9-121">Wählen Sie im Dialogfeld **Projekteinstellungen** auf der Registerkarte **Debuggen** die Option **Allgemein** im Feld **Kategorie** aus.</span><span class="sxs-lookup"><span data-stu-id="06fc9-121">In the **Project Settings** dialog box, on the **Debug** tab, select **General** in the **Category** box.</span></span>

13. <span data-ttu-id="06fc9-122">Geben Sie im Feld **ausführbare Datei für Debugsitzung** den voll qualifizierten Pfad für Dllhost.exe ein, gefolgt von einem Argument, das die Prozess-ID der com+-Anwendung angibt, die die Komponente enthält.</span><span class="sxs-lookup"><span data-stu-id="06fc9-122">In the **Executable for debug session** box, enter the fully qualified path for Dllhost.exe, followed by an argument specifying the process ID of the COM+ application containing the component.</span></span> <span data-ttu-id="06fc9-123">Die Prozess-ID finden Sie auf der Registerkarte **Allgemein** im Dialogfeld **Eigenschaften** der com+-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="06fc9-123">You will find the process ID on the **General** tab of the COM+ application's **Properties** dialog box.</span></span> <span data-ttu-id="06fc9-124">Im folgenden finden Sie ein Beispiel: C: \\ Winnt \\ system32 \\Dllhost.exe/ProcessID: { <processID> }.</span><span class="sxs-lookup"><span data-stu-id="06fc9-124">Following is an example: C:\\Winnt\\System32\\Dllhost.exe /ProcessID:{<processID>}.</span></span>

14. <span data-ttu-id="06fc9-125">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="06fc9-125">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06fc9-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="06fc9-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06fc9-127">Com+-Visual Basic Debugunterstützung im Vergleich zu MTS</span><span class="sxs-lookup"><span data-stu-id="06fc9-127">COM+ Visual Basic Debugging Support Contrasted with MTS</span></span>](com--visual-basic-debugging-support-contrasted-with-mts.md)
</dt> <dt>

[<span data-ttu-id="06fc9-128">Debuggen in der Visual Basic IDE</span><span class="sxs-lookup"><span data-stu-id="06fc9-128">Debugging in the Visual Basic IDE</span></span>](debugging-in-the-visual-basic-ide.md)
</dt> </dl>

 

 



