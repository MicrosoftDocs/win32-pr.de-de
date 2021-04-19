---
description: Beim WMI-Steuerelement handelt es sich um ein MMC-Snap-in in der Systemsteuerung, das verwendet wird, um die WMI-Namespace Sicherheit manuell auf einem lokalen Computer festzulegen. Sie können auch den Standard Namespace für die Skripterstellung festlegen.
ms.assetid: 87c23919-c482-4278-b005-894a8ac21da4
ms.tgt_platform: multiple
title: Festlegen der Namespace Sicherheit mit dem WMI-Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8e8b6ed7c45b6b0d107f7f4e4b92f31f504900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351098"
---
# <a name="setting-namespace-security-with-the-wmi-control"></a><span data-ttu-id="8ea1d-104">Festlegen der Namespace Sicherheit mit dem WMI-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="8ea1d-104">Setting Namespace Security with the WMI Control</span></span>

<span data-ttu-id="8ea1d-105">Beim WMI-Steuerelement handelt es sich um ein MMC-Snap-in in der **Systemsteuerung** , das verwendet wird, um die WMI-Namespace Sicherheit manuell auf einem lokalen Computer festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8ea1d-105">The WMI Control is an MMC snap-in located in the **Control Panel** and is used to set WMI namespace security manually on a local computer.</span></span> <span data-ttu-id="8ea1d-106">Sie können auch den Standard Namespace für die Skripterstellung festlegen.</span><span class="sxs-lookup"><span data-stu-id="8ea1d-106">You can also set the default namespace for scripting.</span></span>


<span data-ttu-id="8ea1d-107">Im folgenden Verfahren wird beschrieben, wie Sie das WMI-Steuerelement finden.</span><span class="sxs-lookup"><span data-stu-id="8ea1d-107">The following procedure describes how to locate the WMI Control.</span></span>

<span data-ttu-id="8ea1d-108">**So suchen Sie das WMI-Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="8ea1d-108">**To locate the WMI control**</span></span>

1.  <span data-ttu-id="8ea1d-109">Doppelklicken Sie in der **Systemsteuerung** auf **Verwaltung**.</span><span class="sxs-lookup"><span data-stu-id="8ea1d-109">In the **Control Panel**, double-click **Administrative Tools**.</span></span>
2.  <span data-ttu-id="8ea1d-110">Doppelklicken Sie im Fenster **Verwaltung** auf **Computerverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="8ea1d-110">In the **Administrative Tools** window, double-click **Computer Management**.</span></span>
3.  <span data-ttu-id="8ea1d-111">Erweitern Sie im Fenster **Computer Verwaltung** die Struktur **Dienste und Anwendungen** , und doppelklicken Sie auf das **WMI-Steuer** Element.</span><span class="sxs-lookup"><span data-stu-id="8ea1d-111">In the **Computer Management** window, expand the **Services and Applications** tree and double-click the **WMI Control**.</span></span>
4.  <span data-ttu-id="8ea1d-112">Klicken Sie mit der rechten Maustaste auf das Symbol **WMI-Steuerung** , und wählen Sie **Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="8ea1d-112">Right-click the **WMI Control** icon and select **Properties**.</span></span>

<span data-ttu-id="8ea1d-113">Im folgenden Verfahren wird beschrieben, wie Sie das WMI-Steuerelement verwenden, um die Sicherheit für einen Namespace als Vorlage einzurichten. Anschließend können Sie die Sicherheitseinstellungen Programm gesteuert abrufen, um die Sicherheit für andere Namespaces festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8ea1d-113">The following procedure describes how to use the WMI control to set up the security for a namespace as a template, then programmatically obtain the security settings to set security for other namespaces.</span></span>

<span data-ttu-id="8ea1d-114">**So legen Sie die Namespace Sicherheit mit dem WMI-Steuerelement fest**</span><span class="sxs-lookup"><span data-stu-id="8ea1d-114">**To set namespace security with the WMI control**</span></span>

1.  <span data-ttu-id="8ea1d-115">Erstellen Sie einen neuen Namespace mit dem MOF-Code (Managed Object Format).</span><span class="sxs-lookup"><span data-stu-id="8ea1d-115">Create a new namespace by using Managed Object Format (MOF) code.</span></span>
2.  <span data-ttu-id="8ea1d-116">Führen Sie das WMI-Steuerelement aus, um die Sicherheit für den neuen Namespace festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8ea1d-116">Run the WMI Control to set the security on the new namespace.</span></span> <span data-ttu-id="8ea1d-117">Klicken Sie im **Startmenü** auf **Ausführen** , und geben Sie **Wmimgmt. msc** ein, oder untersuchen Sie [das WMI-Steuer](#)Element.</span><span class="sxs-lookup"><span data-stu-id="8ea1d-117">On the **Start** menu, click **Run** and type **wmimgmt.msc** or see [Locating the WMI Control](#).</span></span>
3.  <span data-ttu-id="8ea1d-118">Klicken Sie im **WMI-Steuerungs** Bereich mit der rechten Maustaste auf **WMI-Steuerung**, wählen Sie **Eigenschaften** aus, und wählen Sie dann die Registerkarte **Sicherheit** aus.</span><span class="sxs-lookup"><span data-stu-id="8ea1d-118">In the **WMI Control** pane, right-click **WMI Control**, choose **Properties**, and then select the **Security** tab.</span></span>
4.  <span data-ttu-id="8ea1d-119">Navigieren Sie zum neuen Namespace, klicken Sie auf **Sicherheit**, und konfigurieren Sie dann Gruppen und Berechtigungen für den Namespace.</span><span class="sxs-lookup"><span data-stu-id="8ea1d-119">Navigate to the new namespace, click **Security**, and then configure groups and permissions for the namespace.</span></span>

<span data-ttu-id="8ea1d-120">Sie können auch Windows-Verwaltungsinstrumentation Command-Line ([WMIC](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754534(v=ws.11))) verwenden, um die Namespace Sicherheit festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8ea1d-120">You can also use Windows Management Instrumentation Command-Line ([WMIC](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754534(v=ws.11))) to set namespace security.</span></span> <span data-ttu-id="8ea1d-121">Weitere Informationen finden Sie unter [**WMIC**](wmic.md).</span><span class="sxs-lookup"><span data-stu-id="8ea1d-121">For more information, see [**wmic**](wmic.md).</span></span>

## <a name="setting-the-default-namespace-for-scripts"></a><span data-ttu-id="8ea1d-122">Festlegen des Standard Namespace für Skripts</span><span class="sxs-lookup"><span data-stu-id="8ea1d-122">Setting the Default Namespace for Scripts</span></span>

<span data-ttu-id="8ea1d-123">Wenn ein Skript beim Herstellen einer Verbindung mit WMI nicht explizit eine Verbindung mit einem Namespace herstellt, verwendet WMI den Standard Namespace, der in diesem Steuerelement angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="8ea1d-123">If a script does not connect explicitly to a namespace when connecting to WMI, then WMI uses the default namespace specified in this control.</span></span> <span data-ttu-id="8ea1d-124">Der Standardwert ist auch wie folgt im Registrierungs Eintrag zu finden:</span><span class="sxs-lookup"><span data-stu-id="8ea1d-124">The default is also found in the registry entry as follows:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         WBEM
            Scripting
               Default
                  Namespace
```

<span data-ttu-id="8ea1d-125">Da der Standard Namespace leicht geändert werden kann, entweder mit diesem Steuerelement oder Programm gesteuert durch Aufrufen von Methoden von [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), geben Sie den Namespace an, wenn Sie eine Verbindung mit WMI herstellen, indem Sie entweder über den [Moniker](constructing-a-moniker-string.md) oder Aufrufe an " [**Swap. ConnectServer**](swbemlocator-connectserver.md)" eine Verbindung mit WMI</span><span class="sxs-lookup"><span data-stu-id="8ea1d-125">Because the default namespace is easy to change, either with this control or programmatically by calling methods of [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), specify the namespace when connecting to WMI either through the [moniker](constructing-a-moniker-string.md) or calls to [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md).</span></span> <span data-ttu-id="8ea1d-126">Weitere Informationen finden Sie unter [Erstellen eines WMI-Skripts](creating-a-wmi-script.md) .</span><span class="sxs-lookup"><span data-stu-id="8ea1d-126">For more information, see [Creating a WMI Script](creating-a-wmi-script.md)</span></span>

<span data-ttu-id="8ea1d-127">**So legen Sie den Standard Namespace für Skripts fest**</span><span class="sxs-lookup"><span data-stu-id="8ea1d-127">**To set the default namespace for scripts**</span></span>

1.  <span data-ttu-id="8ea1d-128">Wählen Sie im Fenster **Eigenschaften von WMI-Steuerung** die Registerkarte **erweitert** aus.</span><span class="sxs-lookup"><span data-stu-id="8ea1d-128">In the **WMI Control Properties** window, choose the **Advanced** tab.</span></span>
2.  <span data-ttu-id="8ea1d-129">Klicken Sie auf die Schaltfläche **ändern** , und wählen Sie den Namespace aus, um die Standardeinstellung</span><span class="sxs-lookup"><span data-stu-id="8ea1d-129">Click the **Change** button and select the namespace to make the default.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ea1d-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8ea1d-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ea1d-131">Festlegen von Namespace-Sicherheits Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="8ea1d-131">Setting Namespace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> </dl>

 

 
