---
description: Mithilfe des Verwaltungs Programms Komponenten Dienste können Sie in anwendungsspezifische Komponenten importieren, die bereits als COM-Komponenten in der Windows-Registrierung auf Ihrem Computer registriert wurden.
ms.assetid: 5310e08a-5146-41f8-ae65-8467b921abd4
title: Importieren von Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1b67d944e9b8880b3edd0583569155fffecb23b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483035"
---
# <a name="importing-components"></a><span data-ttu-id="3501e-103">Importieren von Komponenten</span><span class="sxs-lookup"><span data-stu-id="3501e-103">Importing Components</span></span>

<span data-ttu-id="3501e-104">Mithilfe des Verwaltungs Programms Komponenten Dienste können Sie in anwendungsspezifische Komponenten importieren, die bereits als COM-Komponenten in der Windows-Registrierung auf Ihrem Computer registriert wurden.</span><span class="sxs-lookup"><span data-stu-id="3501e-104">You can use the Component Services administrative tool to import into applications specific components that have already been registered on your computer as COM components in the Windows registry.</span></span> <span data-ttu-id="3501e-105">Beim Importieren einer Komponente werden die Schnittstellen-oder Methoden Informationen, die zum Festlegen von Schnittstelleneigenschaften oder zum Konfigurieren des Zugriffs auf die Komponente von einem Remote Client benötigt werden, nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="3501e-105">Importing a component does not install the interface or method information required to set interface properties or to configure access to the component from a remote client.</span></span> <span data-ttu-id="3501e-106">Daher sollten Sie, wenn möglich, installieren, anstatt nicht konfigurierte Komponenten zu importieren.</span><span class="sxs-lookup"><span data-stu-id="3501e-106">Therefore, if possible, you should install rather than import unconfigured components.</span></span>

> [!Note]  
> <span data-ttu-id="3501e-107">Beim Importieren einer Komponente in eine COM+-Anwendung füllt com+ keine Schnittstellen-und Methoden Informationen für die Komponente auf.</span><span class="sxs-lookup"><span data-stu-id="3501e-107">When importing a component into a COM+ application, COM+ does not populate interface and method information for the component.</span></span> <span data-ttu-id="3501e-108">Beim Exportieren eines Anwendungs Proxys stellt com+ keine Marshallinginformationen (Typbibliotheken oder Proxy/stusb) für einige oder alle Schnittstellen bereit.</span><span class="sxs-lookup"><span data-stu-id="3501e-108">During the export of an application proxy, COM+ will not provide marshaling information (type libraries or proxy/stubs) for some or all of the interfaces.</span></span> <span data-ttu-id="3501e-109">Das Exportieren von Anwendungs Proxys, die importierte Komponenten enthalten, schlägt fehl oder bewirkt, dass eine Warnung ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3501e-109">Exporting application proxies that contain imported components will fail or cause a warning to be issued.</span></span>

 

<span data-ttu-id="3501e-110">**So importieren Sie eine Komponente in eine COM+-Anwendung**</span><span class="sxs-lookup"><span data-stu-id="3501e-110">**To import a component into a COM+ application**</span></span>

1.  <span data-ttu-id="3501e-111">Wählen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste den Computer aus, auf dem die COM+-Anwendung gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="3501e-111">In the console tree of the Component Services administrative tool, select the computer hosting the COM+ application.</span></span>

2.  <span data-ttu-id="3501e-112">Öffnen Sie den Ordner **com+-Anwendungen** für diesen Computer, und wählen Sie die Anwendung aus, in der die Komponente installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3501e-112">Open the **COM+ Applications** folder for that computer, and select the application in which you want to install the component.</span></span>

3.  <span data-ttu-id="3501e-113">Öffnen Sie den Anwendungsordner, und wählen Sie **Komponenten** aus.</span><span class="sxs-lookup"><span data-stu-id="3501e-113">Open the application folder and select **Components**.</span></span>

4.  <span data-ttu-id="3501e-114">Zeigen Sie im Menü **Aktion** auf **neu**, und klicken Sie dann auf **Komponente**.</span><span class="sxs-lookup"><span data-stu-id="3501e-114">On the **Action** menu, point to **New**, and then click **Component**.</span></span> <span data-ttu-id="3501e-115">Sie können auch mit der rechten Maustaste auf den Ordner **Komponenten** , zeigen Sie auf **neu**, und klicken Sie dann auf **Komponente**.</span><span class="sxs-lookup"><span data-stu-id="3501e-115">You can also right-click the **Components** folder, point to **New**, and then click **Component**.</span></span>

5.  <span data-ttu-id="3501e-116">Klicken Sie auf der **Willkommens** Seite des COM+-Anwendungsinstallations-Assistenten auf **weiter**, und klicken Sie dann im Dialogfeld **Komponente importieren oder installieren** auf die **Komponente (en) importieren, die bereits registriert sind**.</span><span class="sxs-lookup"><span data-stu-id="3501e-116">On the **Welcome** page of the COM+ Application Install Wizard, click **Next**, and then in the **Import or Install a Component** dialog box, click **Import component(s) that are already registered**.</span></span>

6.  <span data-ttu-id="3501e-117">Aktivieren Sie im Dialogfeld **zu importierende Komponenten auswählen** das Kontrollkästchen **Details** , um die gesamten Informationen zu den bereits registrierten Komponenten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3501e-117">In the **Choose Components to Import** dialog box, select the **Details** check box to see complete information about the components that are already registered.</span></span> <span data-ttu-id="3501e-118">Wählen Sie die zu importierenden Komponenten aus der angezeigten Liste aus, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="3501e-118">Select the component(s) you want to import from the displayed list, and click **Next**.</span></span>

7.  <span data-ttu-id="3501e-119">Klicken Sie auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="3501e-119">Click **Finish**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3501e-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3501e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3501e-121">Kopieren von Komponenten</span><span class="sxs-lookup"><span data-stu-id="3501e-121">Copying Components</span></span>](copying-components.md)
</dt> <dt>

[<span data-ttu-id="3501e-122">Eine neue COM+-Anwendung wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="3501e-122">Creating a New COM+ Application</span></span>](creating-a-new-com--application.md)
</dt> <dt>

[<span data-ttu-id="3501e-123">Eine COM+-Anwendung wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3501e-123">Deleting a COM+ Application</span></span>](deleting-a-com--application.md)
</dt> <dt>

[<span data-ttu-id="3501e-124">Installieren neuer Komponenten</span><span class="sxs-lookup"><span data-stu-id="3501e-124">Installing New Components</span></span>](installing-new-components.md)
</dt> <dt>

[<span data-ttu-id="3501e-125">Verschieben von Komponenten</span><span class="sxs-lookup"><span data-stu-id="3501e-125">Moving Components</span></span>](moving-components.md)
</dt> <dt>

[<span data-ttu-id="3501e-126">Entfernen einer Komponente aus einer COM+-Anwendung</span><span class="sxs-lookup"><span data-stu-id="3501e-126">Removing a Component from a COM+ Application</span></span>](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



