---
description: WMI registriert die Ansichts Anbieter-DLL während des WMI-Installationsvorgangs automatisch. Allerdings müssen Sie den Ansichts Anbieter für jeden Namespace, der Ansichts Klassen enthalten soll, bei WMI registrieren.
ms.assetid: 62db8cdc-0bbf-4784-bfc4-6fd5cb53368a
ms.tgt_platform: multiple
title: Der Ansichts Anbieter wird registriert.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 530a701d3ffc39523b1b3432dd2d94a3da256605
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352739"
---
# <a name="registering-the-view-provider"></a><span data-ttu-id="ffe59-104">Der Ansichts Anbieter wird registriert.</span><span class="sxs-lookup"><span data-stu-id="ffe59-104">Registering the View Provider</span></span>

<span data-ttu-id="ffe59-105">WMI registriert die Ansichts Anbieter-DLL während des WMI-Installationsvorgangs automatisch.</span><span class="sxs-lookup"><span data-stu-id="ffe59-105">WMI automatically registers the View Provider DLL during the WMI installation process.</span></span> <span data-ttu-id="ffe59-106">Allerdings müssen Sie den Ansichts Anbieter für jeden Namespace, der Ansichts Klassen enthalten soll, bei WMI registrieren.</span><span class="sxs-lookup"><span data-stu-id="ffe59-106">However, you still need to register the View Provider with WMI for each namespace that will contain view classes.</span></span>

<span data-ttu-id="ffe59-107">Im folgenden Verfahren wird beschrieben, wie der Ansichts Anbieter registriert wird.</span><span class="sxs-lookup"><span data-stu-id="ffe59-107">The following procedure describes how to register the View Provider.</span></span>

<span data-ttu-id="ffe59-108">**So registrieren Sie den Ansichts Anbieter**</span><span class="sxs-lookup"><span data-stu-id="ffe59-108">**To register the View Provider**</span></span>

1.  <span data-ttu-id="ffe59-109">Erstellen Sie eine Instanz der [**\_ \_ Win32Provider**](--win32provider.md) -Klasse, um die Implementierung des Ansichts Anbieters zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="ffe59-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class to describe the implementation of the View Provider.</span></span>

    <span data-ttu-id="ffe59-110">Die [**\_ \_ Win32Provider**](--win32provider.md) -Instanz beschreibt den Namen des Anbieters und dessen Klassen Bezeichner (CLSID) sowie die Standard Sicherheitseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="ffe59-110">The [**\_\_Win32Provider**](--win32provider.md) instance describes the name of the provider and its class identifier (CLSID), as well as the default security settings.</span></span>

    <span data-ttu-id="ffe59-111">Im folgenden Codebeispiel wird eine Implementierung von [**\_ \_ Win32Provider**](--win32provider.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ffe59-111">The following code example describes an implementation of [**\_\_Win32Provider**](--win32provider.md).</span></span>

    ``` syntax
    instance of __Win32Provider as $DataProv
    {
        Name = "MS_VIEW_INSTANCE_PROVIDER";
        ClsId = "{AA70DDF4-E11C-11D1-ABB0-00C04FD9159E}";
        ImpersonationLevel = 1;
        PerUserInitialization = "True";
        
    };
    ```

2.  <span data-ttu-id="ffe59-112">Erstellen Sie eine Instanz der [**\_ \_ instanceproviderregistration**](--instanceproviderregistration.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="ffe59-112">Create an instance of the [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) class.</span></span>

    <span data-ttu-id="ffe59-113">Im folgenden Codebeispiel wird gezeigt, wie eine Instanz der **\_ \_ instanceproviderregistration** -Klasse erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ffe59-113">The following code example shows how to create an instance of the **\_\_InstanceProviderRegistration** class.</span></span>

    ``` syntax
    instance of __InstanceProviderRegistration
    {
        Provider = $DataProv;
        SupportsPut = True;
        SupportsGet = True;
        SupportsDelete = True;
        SupportsEnumeration = True;
        QuerySupportLevels = {"WQL:UnarySelect"};
    };
    ```

3.  <span data-ttu-id="ffe59-114">Erstellen Sie eine Instanz der [**\_ \_ methodproviderregistration**](--methodproviderregistration.md) -Klasse, wenn Sie die Unterstützung von Methoden der Union-Ansichts Klasse benötigen.</span><span class="sxs-lookup"><span data-stu-id="ffe59-114">Create an instance of the [**\_\_MethodProviderRegistration**](--methodproviderregistration.md) class if you want to have your union view class support methods.</span></span>

    <span data-ttu-id="ffe59-115">Im folgenden Codebeispiel wird gezeigt, wie eine Instanz der **\_ \_ methodproviderregistration** -Klasse erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ffe59-115">The following code example shows how to create an instance of the **\_\_MethodProviderRegistration** class.</span></span>

    ``` syntax
    instance of __MethodProviderRegistration
    {
        Provider = $DataProv;
    };
    ```

4.  <span data-ttu-id="ffe59-116">Kompilieren Sie den MOF-Code mit dem MOF-[Compiler ("](mofcomp.md)MOF") oder der [**imuscompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ffe59-116">Compile your MOF code using the MOF compiler ([mofcomp](mofcomp.md)) or the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface.</span></span>

    <span data-ttu-id="ffe59-117">Wenn Sie das zuvor aufgeführte MOF-Codebeispiel in einer Datei namens viewtest. MOF speichern, verwenden Sie den Befehl "mufcomp", um den MOF-Code in den Ziel Namespace zu laden.</span><span class="sxs-lookup"><span data-stu-id="ffe59-117">If you save the previously listed MOF code example into a file named Viewtest.mof, use the Mofcomp command to load the MOF code into the target namespace.</span></span> <span data-ttu-id="ffe59-118">*NamespacePath* ist der Namespace, in dem Sie die Ansichts Klasseninstanz erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="ffe59-118">*NamespacePath* is the namespace in which you wish to create the view class instance.</span></span>

    <span data-ttu-id="ffe59-119">Geben Sie den folgenden Befehl an einer Eingabeaufforderung ein, um den MOF-Code in den Ziel Namespace zu laden.</span><span class="sxs-lookup"><span data-stu-id="ffe59-119">Type the following command at a command prompt to load the MOF code into the target namespace.</span></span>

    ``` syntax
    Mofcomp /N:<NamespacePath> Viewtest.mof
    ```

    <span data-ttu-id="ffe59-120">Weitere Informationen finden Sie unter [Kompilieren von MOF-Dateien](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="ffe59-120">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="ffe59-121">Weitere Informationen finden Sie unter [Registrieren eines Anbieters](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ffe59-121">For more information, see [Registering a Provider](registering-a-provider.md).</span></span>

 

 



