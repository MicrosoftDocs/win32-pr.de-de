---
description: Wenn Ihre Anwendung eine Drittanbieter-DLL, Erweiterung, ein Plug-in oder eine Systemsteuerung hostet, können Sie eine Assembly in der Anwendung&8212 aktivieren, \# ohne diese Assembly auch für die gehosteten Komponenten aktivieren zu müssen.
ms.assetid: 832957ca-82fc-4600-b469-512621dde921
title: Aktivieren einer Assembly in einer Anwendung, die eine DLL, Erweiterung oder Systemsteuerung gehostet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b04dd19b18c2cdce4783be47333b9afe53dd1ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357813"
---
# <a name="enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel"></a><span data-ttu-id="7e07d-103">Aktivieren einer Assembly in einer Anwendung, die eine DLL, Erweiterung oder Systemsteuerung gehostet</span><span class="sxs-lookup"><span data-stu-id="7e07d-103">Enabling an Assembly in an Application Hosting a DLL, Extension, or Control Panel</span></span>

<span data-ttu-id="7e07d-104">Wenn Ihre Anwendung eine Drittanbieter-DLL, Erweiterung, ein Plug-in oder eine Systemsteuerung hostet, empfiehlt es sich, eine Assembly in Ihrer Anwendung zu aktivieren – ohne diese Assembly für die gehosteten Komponenten aktivieren zu müssen.</span><span class="sxs-lookup"><span data-stu-id="7e07d-104">If your application hosts a third-party DLL, extension, plug-in, or control panel, you may want to enable an assembly in your application—without also enabling this assembly for the hosted components.</span></span> <span data-ttu-id="7e07d-105">Dies kann der Fall sein, wenn eine gehostete Komponente Codeänderungen erfordert, um die Assembly zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7e07d-105">This can be the case when a hosted component requires code changes to use the assembly.</span></span> <span data-ttu-id="7e07d-106">Als Anwendungsentwickler können Sie möglicherweise keine Änderungen an diesen Komponenten von Drittanbietern vornehmen.</span><span class="sxs-lookup"><span data-stu-id="7e07d-106">As the application developer, you may be unable to make changes to these third-party components.</span></span> <span data-ttu-id="7e07d-107">In diesem Fall sollten Sie das in diesem Abschnitt beschriebene Verfahren befolgen, damit Ihre Anwendung die Assembly verwenden kann, ohne dass sich dies auf die gehosteten Komponenten auswirkt.</span><span class="sxs-lookup"><span data-stu-id="7e07d-107">In this case, you should follow the procedure described in this section so that your application can use the assembly without affecting the hosted components.</span></span>

-   <span data-ttu-id="7e07d-108">Um eine Assembly in einer Anwendung ohne Auswirkungen auf gehostete DLLs, Erweiterungen, Plug-ins oder Steuerelemente zu aktivieren, sollte ein Manifest, das die Abhängigkeit der Anwendung von der Assembly beschreibt, in der Anwendung als Ressource enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="7e07d-108">To enable an assembly in an application without affecting any hosted DLLs, extensions, plug-ins, or control panels, a manifest that describes the application's dependence on the assembly should be included in the application as a resource.</span></span> <span data-ttu-id="7e07d-109">Die gehosteten Komponenten, die nicht mit der Assembly aktiviert werden, sollten keine Manifeste einschließen, in denen diese Abhängigkeit beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="7e07d-109">The hosted components that are not being enabled with the assembly should not include manifests describing this dependency.</span></span>
-   <span data-ttu-id="7e07d-110">Um eine Assembly in einer Anwendung und ihren gehosteten DLLs, Erweiterungen, Plug-ins oder Steuerelementen zu aktivieren, schließen Sie Manifeste als Ressourcen in die Anwendung und die zugehörigen gehosteten Komponenten ein.</span><span class="sxs-lookup"><span data-stu-id="7e07d-110">To enable an assembly in an application and its hosted DLLs, extensions, plug-ins, or control panels, include manifests as resources in both the application and its hosted components.</span></span> <span data-ttu-id="7e07d-111">Die in der Anwendung und in den gehosteten Komponenten enthaltenen Manifeste sollten jeweils eine Abhängigkeit von der Assembly beschreiben.</span><span class="sxs-lookup"><span data-stu-id="7e07d-111">The manifests included in the application and in the hosted components should each describe a dependence on the assembly.</span></span> <span data-ttu-id="7e07d-112">In der Regel fügt der Anwendungsentwickler der Anwendung ein Manifest hinzu, und der Entwickler der gehosteten Komponente fügt der dll, Erweiterung, dem Plug-in oder der Systemsteuerung ein Manifest hinzu.</span><span class="sxs-lookup"><span data-stu-id="7e07d-112">Typically, the application developer adds a manifest to the application and the hosted component developer adds a manifest to the DLL, extension, plug-in, or control panel.</span></span>

<span data-ttu-id="7e07d-113">Die folgende Methode kann verwendet werden, um einer Anwendung oder einer gehosteten Komponente, bei der es sich um eine DLL, Erweiterung, ein Plug-in oder eine Systemsteuerung handelt, ein Manifest hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="7e07d-113">The following method can be used to add a manifest to an application or a hosted component that is a DLL, extension, plug-in, or control panel.</span></span>

<span data-ttu-id="7e07d-114">**Zum Aktivieren einer Assembly in einer Anwendung oder einer gehosteten Komponente.**</span><span class="sxs-lookup"><span data-stu-id="7e07d-114">**To enable an assembly in an application or hosted component.**</span></span>

1.  <span data-ttu-id="7e07d-115">Erstellen Sie ein Manifest, das die Abhängigkeit von der Anwendung oder Erweiterung in der Assembly beschreibt.</span><span class="sxs-lookup"><span data-stu-id="7e07d-115">Author a manifest that describes the dependence of the application or extension on the assembly.</span></span>

    <span data-ttu-id="7e07d-116">Beispielsweise kann das Manifest für "yourapplication" erstellt werden, indem das folgende Beispiel Manifest kopiert und die richtigen Werte für **assemblyIdentity**, **ProcessorArchitecture** und **Description** ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="7e07d-116">For example, the manifest for "YourApplication" can be created by copying the following sample manifest and substituting correct values for **assemblyIdentity**, **processorArchitecture**, and **description**.</span></span> <span data-ttu-id="7e07d-117">Legen Sie den Wert von **ProcessorArchitecture** auf x86 fest, wenn Sie auf einer 32-Bit-Plattform aufbauen, und auf ia64, wenn Sie auf einer 64-Bit-Plattform aufbauen.</span><span class="sxs-lookup"><span data-stu-id="7e07d-117">Set the value of **processorArchitecture** to x86 if building on a 32-bit platform and to ia64 if building on a 64-bit platform.</span></span> <span data-ttu-id="7e07d-118">Das **Description** -Element enthält eine options Beschreibung der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="7e07d-118">The **description** element contains an option description of the application.</span></span> <span data-ttu-id="7e07d-119">Weitere Informationen zum Manifest-Format finden Sie unter [Anwendungs Manifeste](application-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="7e07d-119">For more information about the manifest format, see [application manifests](application-manifests.md).</span></span>

    ``` syntax
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="x86"
        name="YourCompanyName.YourDivision.YourApp"
        type="win32"
    />
    <description>Your app description here</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Proseware.Research.SampleAssembly"
                version="6.0.0.0"
                processorArchitecture="X86"
                publicKeyToken="0000000000000000"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

2.  <span data-ttu-id="7e07d-120">Erstellen Sie eine Ressource in der Anwendung oder Erweiterung des Typs RT \_ Manifest ID 2.</span><span class="sxs-lookup"><span data-stu-id="7e07d-120">Create a resource in the application or extension of type RT\_MANIFEST id 2.</span></span>

    <span data-ttu-id="7e07d-121">Wenn der Name der Anwendung beispielsweise yourapp lautet, sollte die Anwendung Folgendes enthalten:</span><span class="sxs-lookup"><span data-stu-id="7e07d-121">For example, if the application's name is YourApp, the application should contain the following:</span></span>

    ``` syntax
    #define MANIFEST_RESOURCE_ID 2
    MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.manifest"
    ```

3.  <span data-ttu-id="7e07d-122">Kompilieren Sie die Anwendung mit dem Flag "-disolations \_ \_ fähig", oder fügen Sie diese Anweisung vor der \# include-Anweisung "Windows. h" ein.</span><span class="sxs-lookup"><span data-stu-id="7e07d-122">Compile the application with the -DISOLATION\_AWARE\_ENABLED flag, or insert this statement before the \#include "Windows.h" statement.</span></span> <span data-ttu-id="7e07d-123">Im Fall einer Anwendung mit mehreren Modulen ist das Flag-disolations- \_ \_ fähig aktiviert für alle Module erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7e07d-123">In the case of an application with multiple modules, the -DISOLATION\_AWARE\_ENABLED flag is required on all modules.</span></span>

    ``` syntax
    #define ISOLATION_AWARE_ENABLED 1
    ```

4.  <span data-ttu-id="7e07d-124">Testen Sie, um sicherzustellen, dass die von der Anwendung verwendeten Assemblys in der Anwendung und der gehosteten Komponente ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="7e07d-124">Test to ensure that assemblies that are used by the application work correctly in the application and hosted component.</span></span>

<span data-ttu-id="7e07d-125">Weitere Informationen zum Hinzufügen einer Assembly zu Anwendungen ohne Erweiterungen finden Sie unter [Aktivieren einer Assembly in einer Anwendung ohne Erweiterungen](enabling-an-assembly-in-an-application-without-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="7e07d-125">For more information about adding an assembly to applications without extensions, see [Enabling an Assembly in an Application Without Extensions](enabling-an-assembly-in-an-application-without-extensions.md).</span></span>

 

 



