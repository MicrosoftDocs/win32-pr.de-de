---
description: Wenn vorhandene Anwendungen veraltet sind oder nicht mehr verwendet werden, müssen Sie Sie möglicherweise entfernen.
ms.assetid: 5cce94c9-8eff-40b9-946d-a57749da073d
title: Eine COM+-Anwendung wird gelöscht.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da685e5a7ae7590fcc247caa765d49dc34d076e9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393130"
---
# <a name="deleting-a-com-application"></a><span data-ttu-id="4cf28-103">Eine COM+-Anwendung wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="4cf28-103">Deleting a COM+ Application</span></span>

<span data-ttu-id="4cf28-104">Wenn vorhandene Anwendungen veraltet sind oder nicht mehr verwendet werden, müssen Sie Sie möglicherweise entfernen.</span><span class="sxs-lookup"><span data-stu-id="4cf28-104">As existing applications become dated or are no longer being used, you may need to remove them.</span></span>

<span data-ttu-id="4cf28-105">**So löschen Sie eine COM+-Anwendung**</span><span class="sxs-lookup"><span data-stu-id="4cf28-105">**To delete a COM+ application**</span></span>

1.  <span data-ttu-id="4cf28-106">Wählen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste den Computer aus, für den Sie eine Anwendung löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="4cf28-106">In the console tree of the Component Services administrative tool, select the computer for which you want to delete an application.</span></span>

2.  <span data-ttu-id="4cf28-107">Öffnen Sie den **com+-Anwendungs** Ordner für den angegebenen Computer, um alle Anwendungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4cf28-107">Open the **COM+ Applications** folder for the specified computer to display all the applications.</span></span>

3.  <span data-ttu-id="4cf28-108">Wählen Sie die Anwendung aus, die Sie entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="4cf28-108">Select the application you want to remove.</span></span>

4.  <span data-ttu-id="4cf28-109">Wenn Sie eine Serveranwendung ausgewählt haben, fahren Sie die Anwendung herunter.</span><span class="sxs-lookup"><span data-stu-id="4cf28-109">If you selected a server application, shut down the application.</span></span> <span data-ttu-id="4cf28-110">Sie können eine Anwendung Herunterfahren, indem Sie Sie im Verwaltungs Programmkomponenten Dienste auswählen, mit der rechten Maustaste klicken und dann auf **herunter** fahren klicken.</span><span class="sxs-lookup"><span data-stu-id="4cf28-110">You can shut down an application by selecting it in the Component Services administrative tool, right-clicking, and then clicking **Shut down**.</span></span> <span data-ttu-id="4cf28-111">Wenn Sie eine Bibliotheks Anwendung ausgewählt haben, stellen Sie sicher, dass alle derzeit diese Bibliotheks Anwendung verwendeten Prozesse heruntergefahren werden.</span><span class="sxs-lookup"><span data-stu-id="4cf28-111">If you selected a library application, make sure that all processes currently using this library application are shut down.</span></span>

5.  <span data-ttu-id="4cf28-112">Klicken Sie im Menü **Aktion** auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="4cf28-112">On the **Action** menu, click **Delete**.</span></span> <span data-ttu-id="4cf28-113">Sie können auch mit der rechten Maustaste auf den Anwendungsnamen klicken und dann auf **Löschen** klicken.</span><span class="sxs-lookup"><span data-stu-id="4cf28-113">You can also right-click the application name and then click **Delete**.</span></span> <span data-ttu-id="4cf28-114">Sie können eine Anwendung auch löschen, indem Sie Sie im Verwaltungs Programmkomponenten Dienste auswählen und die ENTF-Taste drücken, oder Sie können die Anwendung auswählen, **mit der rechten** Maustaste klicken und dann auf **Löschen** klicken.</span><span class="sxs-lookup"><span data-stu-id="4cf28-114">You can also delete an application by selecting it in the Component Services administrative tool and pressing the **Delete** key, or you can select the application, right-click, and then click **Delete**.</span></span>

6.  <span data-ttu-id="4cf28-115">Klicken Sie auf **Ja** , wenn Sie zur Bestätigung Ihrer Aktion aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="4cf28-115">Click **Yes** when prompted to confirm your action.</span></span>

<span data-ttu-id="4cf28-116">Außerdem können Sie, wenn eine Serveranwendung oder ein Anwendungs Proxy mithilfe von Windows Installer auf einem Computer installiert wurde (wie unter "Installieren von com+-Anwendungen" beschrieben), das Hilfsprogramm "Software" in der Microsoft Windows-Systemsteuerung löschen.</span><span class="sxs-lookup"><span data-stu-id="4cf28-116">In addition, if a server application or application proxy has been installed on a computer using Windows Installer (as described in "Installing COM+ Applications" in the Component Services Administration Guide), you can delete it through the Add/Remove Programs utility in the Microsoft Windows Control Panel.</span></span> <span data-ttu-id="4cf28-117">Oder Sie können eine installierte Serveranwendung oder einen Anwendungs Proxy mithilfe der Windows Installer Befehlszeilen Syntax löschen:</span><span class="sxs-lookup"><span data-stu-id="4cf28-117">Or you can delete an installed server application or application proxy by using the Windows Installer command line syntax:</span></span>

<span data-ttu-id="4cf28-118">**msiexec-x** *Anwendungs \_ Name \* \* *. msi**</span><span class="sxs-lookup"><span data-stu-id="4cf28-118">**msiexec -x** *application\_name\*\*\*.msi*\*</span></span>

<span data-ttu-id="4cf28-119">Diese Methoden sind besonders nützlich zum Löschen von com+-Anwendungen auf Client Computern, auf denen das Verwaltungs Programmkomponenten Dienste nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4cf28-119">These methods are especially useful for deleting COM+ applications on client machines that are not running the Component Services administrative tool.</span></span>

<span data-ttu-id="4cf28-120">Wenn Sie die Anwendung löschen, werden auch alle in der Anwendung enthaltenen Komponenten gelöscht.</span><span class="sxs-lookup"><span data-stu-id="4cf28-120">Deleting the application also deletes any components contained in the application.</span></span> <span data-ttu-id="4cf28-121">Wenn diese Komponenten von zusätzlichen Ressourcen (Datenbankverbindungen, Daten-oder Textdateien, IIS Virtual root Configuration usw.) abhängen, müssen diese Ressourcen über andere Mechanismen als das Verwaltungs Programmkomponenten Dienste entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="4cf28-121">If these components depend on additional resources (database connections, data or text files, IIS virtual root configuration, and so on), these resources must be removed through mechanisms other than the Component Services administrative tool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4cf28-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4cf28-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4cf28-123">Kopieren von Komponenten</span><span class="sxs-lookup"><span data-stu-id="4cf28-123">Copying Components</span></span>](copying-components.md)
</dt> <dt>

[<span data-ttu-id="4cf28-124">Eine neue COM+-Anwendung wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="4cf28-124">Creating a New COM+ Application</span></span>](creating-a-new-com--application.md)
</dt> <dt>

[<span data-ttu-id="4cf28-125">Importieren von Komponenten</span><span class="sxs-lookup"><span data-stu-id="4cf28-125">Importing Components</span></span>](importing-components.md)
</dt> <dt>

[<span data-ttu-id="4cf28-126">Installieren neuer Komponenten</span><span class="sxs-lookup"><span data-stu-id="4cf28-126">Installing New Components</span></span>](installing-new-components.md)
</dt> <dt>

[<span data-ttu-id="4cf28-127">Verschieben von Komponenten</span><span class="sxs-lookup"><span data-stu-id="4cf28-127">Moving Components</span></span>](moving-components.md)
</dt> <dt>

[<span data-ttu-id="4cf28-128">Entfernen einer Komponente aus einer COM+-Anwendung</span><span class="sxs-lookup"><span data-stu-id="4cf28-128">Removing a Component from a COM+ Application</span></span>](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



