---
description: Um dem Ordner Komponenten einer COM+-Anwendung Komponenten hinzuzufügen, können Sie entweder den com+-Komponenteninstallations-Assistenten verwenden oder DLL-Dateien ziehen, die die Komponenten aus dem Windows-Explorer enthalten, und Sie in der Anwendung ablegen.
ms.assetid: 3cb0c24d-cd52-42ac-8b07-d8774698b90c
title: Installieren neuer Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 434bdb59c0a0e9c786bb3460a0cb1cbb6a1f50dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041468"
---
# <a name="installing-new-components"></a><span data-ttu-id="22207-103">Installieren neuer Komponenten</span><span class="sxs-lookup"><span data-stu-id="22207-103">Installing New Components</span></span>

<span data-ttu-id="22207-104">Um dem Ordner **Komponenten** einer COM+-Anwendung Komponenten hinzuzufügen, können Sie entweder den com+-Komponenteninstallations-Assistenten verwenden oder DLL-Dateien ziehen, die die Komponenten aus dem Windows-Explorer enthalten, und Sie in der Anwendung ablegen.</span><span class="sxs-lookup"><span data-stu-id="22207-104">To add components to the **Components** folder of a COM+ application, you can either use the COM+ Component Install Wizard or drag .dll files that contain the components from the Windows Explorer and drop them in the application.</span></span>

<span data-ttu-id="22207-105">Wenn Sie den com+-Komponenteninstallations-Assistenten verwenden, können Sie entweder eine neue-Komponente installieren, die die Komponente auf dem Computer registriert, oder bereits registrierte Komponenten importieren.</span><span class="sxs-lookup"><span data-stu-id="22207-105">If you use the COM+ Component Install Wizard, you can either install a new component, which registers the component on the computer, or import components that have already been registered.</span></span> <span data-ttu-id="22207-106">Komponenten können leeren Anwendungen oder vorhandenen Anwendungen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="22207-106">Components can be added to empty applications or existing applications.</span></span>

<span data-ttu-id="22207-107">**So fügen Sie einer COM+-Anwendung eine Komponente hinzu**</span><span class="sxs-lookup"><span data-stu-id="22207-107">**To add a component to a COM+ application**</span></span>

1.  <span data-ttu-id="22207-108">Wählen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste den Computer aus, auf dem die COM+-Anwendung gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="22207-108">In the console tree of the Component Services administrative tool, select the computer hosting the COM+ application.</span></span>

2.  <span data-ttu-id="22207-109">Öffnen Sie den Ordner **com+-Anwendungen** für diesen Computer, und wählen Sie die Anwendung aus, in der Sie die Komponenten installieren möchten.</span><span class="sxs-lookup"><span data-stu-id="22207-109">Open the **COM+ Applications** folder for that computer, and select the application in which you want to install the component(s).</span></span>

3.  <span data-ttu-id="22207-110">Öffnen Sie den Anwendungsordner, und wählen Sie **Komponenten** aus.</span><span class="sxs-lookup"><span data-stu-id="22207-110">Open the application folder and select **Components**.</span></span>

4.  <span data-ttu-id="22207-111">Zeigen Sie im Menü **Aktion** auf **neu**, und klicken Sie dann auf **Komponente**.</span><span class="sxs-lookup"><span data-stu-id="22207-111">On the **Action** menu, point to **New**, and then click **Component**.</span></span> <span data-ttu-id="22207-112">Sie können auch mit der rechten Maustaste auf den Ordner **Komponenten** , zeigen Sie auf **neu**, und klicken Sie dann auf **Komponente**.</span><span class="sxs-lookup"><span data-stu-id="22207-112">You can also right-click the **Components** folder, point to **New**, and then click **Component**.</span></span>

5.  <span data-ttu-id="22207-113">Klicken Sie auf der **Willkommens** Seite des COM+-Anwendungsinstallations-Assistenten auf **weiter**, und klicken Sie dann im Dialogfeld **Komponente importieren oder installieren** auf **neue Komponenten installieren** .</span><span class="sxs-lookup"><span data-stu-id="22207-113">On the **Welcome** page of the COM+ Application Install Wizard, click **Next**, and then in the **Import or Install a Component** dialog box, click **Install new components** .</span></span>

6.  <span data-ttu-id="22207-114">Klicken Sie im Dialogfeld **neue Komponenten installieren** auf **Hinzufügen** , um die Komponente zu suchen, die Sie hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="22207-114">In the **Install new components** dialog box, click **Add** to browse for the component you want to add.</span></span>

7.  <span data-ttu-id="22207-115">Geben Sie im Dialogfeld **zu installierenden Dateien auswählen** den Dateinamen der zu installierenden Komponente ein, oder wählen Sie einen Dateinamen aus der angezeigten Liste aus.</span><span class="sxs-lookup"><span data-stu-id="22207-115">In the **Select files to install** dialog box, type the filename of the component to install or select a filename from the displayed list.</span></span> <span data-ttu-id="22207-116">Klicken Sie auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="22207-116">Click **Open**.</span></span>

    <span data-ttu-id="22207-117">Nachdem Sie die Dateien hinzugefügt haben, werden im Dialogfeld **neue Komponenten installieren** die Dateien angezeigt, die Sie hinzugefügt haben, und die zugehörigen Komponenten.</span><span class="sxs-lookup"><span data-stu-id="22207-117">After you add the files, the **Install new components** dialog box displays the files you have added and their associated components.</span></span> <span data-ttu-id="22207-118">Wenn Sie das Kontrollkästchen **Details** aktivieren, werden weitere Informationen zum Inhalt der Datei und zu den gefundenen Komponenten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="22207-118">If you select the **Details** check box, you will see more information about file contents and the components that were found.</span></span>

    > [!Note]  
    > <span data-ttu-id="22207-119">Nicht konfigurierte COM-Komponenten müssen eine Typbibliothek aufweisen.</span><span class="sxs-lookup"><span data-stu-id="22207-119">Unconfigured COM components must have a type library.</span></span> <span data-ttu-id="22207-120">Wenn com+ die Typbibliothek der Komponente nicht finden kann, wird die Komponente nicht in der Liste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="22207-120">If COM+ cannot find your component's type library, your component will not appear in the list.</span></span> <span data-ttu-id="22207-121">Sie können eine Datei auch aus der Liste **zu installierendes Dateien entfernen,** indem Sie Sie auswählen und auf **Entfernen** klicken.</span><span class="sxs-lookup"><span data-stu-id="22207-121">You can also remove a file from the **Files to install** list by selecting it and clicking **Remove**.</span></span>

     

8.  <span data-ttu-id="22207-122">Klicken Sie auf **weiter** und dann auf **Fertig** stellen, um die Komponente zu installieren.</span><span class="sxs-lookup"><span data-stu-id="22207-122">Click **Next**, and then click **Finish** to install the component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22207-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="22207-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22207-124">Kopieren von Komponenten</span><span class="sxs-lookup"><span data-stu-id="22207-124">Copying Components</span></span>](copying-components.md)
</dt> <dt>

[<span data-ttu-id="22207-125">Eine neue COM+-Anwendung wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="22207-125">Creating a New COM+ Application</span></span>](creating-a-new-com--application.md)
</dt> <dt>

[<span data-ttu-id="22207-126">Eine COM+-Anwendung wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="22207-126">Deleting a COM+ Application</span></span>](deleting-a-com--application.md)
</dt> <dt>

[<span data-ttu-id="22207-127">Importieren von Komponenten</span><span class="sxs-lookup"><span data-stu-id="22207-127">Importing Components</span></span>](importing-components.md)
</dt> <dt>

[<span data-ttu-id="22207-128">Verschieben von Komponenten</span><span class="sxs-lookup"><span data-stu-id="22207-128">Moving Components</span></span>](moving-components.md)
</dt> <dt>

[<span data-ttu-id="22207-129">Entfernen einer Komponente aus einer COM+-Anwendung</span><span class="sxs-lookup"><span data-stu-id="22207-129">Removing a Component from a COM+ Application</span></span>](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



