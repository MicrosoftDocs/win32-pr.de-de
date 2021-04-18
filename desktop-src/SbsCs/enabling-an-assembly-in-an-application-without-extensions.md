---
description: Wenn die Anwendung keine dll, Erweiterung, kein Plug-in oder Systemsteuerung hostet, können Sie die in diesem Abschnitt beschriebene Methode verwenden, um eine Assembly für Ihre Anwendung zu aktivieren.
ms.assetid: d043ec1b-ac31-45fb-9232-eec42aef4ac3
title: Aktivieren einer Assembly in einer Anwendung ohne Erweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a1bbcfe510f5a3cdbce323f01cb9342ce236c7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352341"
---
# <a name="enabling-an-assembly-in-an-application-without-extensions"></a><span data-ttu-id="70923-103">Aktivieren einer Assembly in einer Anwendung ohne Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="70923-103">Enabling an Assembly in an Application Without Extensions</span></span>

<span data-ttu-id="70923-104">Wenn die Anwendung keine dll, Erweiterung, kein Plug-in oder Systemsteuerung hostet, können Sie die in diesem Abschnitt beschriebene Methode verwenden, um eine Assembly für Ihre Anwendung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="70923-104">If your application does not host a DLL, extension, plug-in, or control panel, you can use the method described in this section to enable an assembly for your application.</span></span> <span data-ttu-id="70923-105">Weitere Informationen zum Hinzufügen einer Assembly zu Anwendungen mit Erweiterungen finden Sie unter [Aktivieren einer Assembly in einer Anwendung, die eine DLL, Erweiterung oder Systemsteuerung gehostet](enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel.md).</span><span class="sxs-lookup"><span data-stu-id="70923-105">For more information about adding an assembly to applications with extensions, see [Enabling an Assembly in an Application Hosting a DLL, Extension, or Control Panel](enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel.md).</span></span>

<span data-ttu-id="70923-106">**So aktivieren Sie eine Assembly in einer Anwendung ohne gehostete Komponenten**</span><span class="sxs-lookup"><span data-stu-id="70923-106">**To enable an assembly in an application without any hosted components**</span></span>

1.  <span data-ttu-id="70923-107">Erstellen Sie ein Manifest, das die Abhängigkeit von der Anwendung oder Erweiterung in der Assembly beschreibt.</span><span class="sxs-lookup"><span data-stu-id="70923-107">Author a manifest that describes the dependence of the application or extension on the assembly.</span></span>

    <span data-ttu-id="70923-108">Beispielsweise kann das Manifest für "yourapplication" erstellt werden, indem das folgende Beispiel Manifest kopiert und die richtigen Werte für **assemblyIdentity**, **ProcessorArchitecture** und **Description** ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="70923-108">For example, the manifest for "YourApplication" can be created by copying the following sample manifest and substituting correct values for **assemblyIdentity**, **processorArchitecture**, and **description**.</span></span> <span data-ttu-id="70923-109">Legen Sie den Wert von **ProcessorArchitecture** auf x86 fest, wenn Sie auf einer 32-Bit-Plattform aufbauen, und auf ia64, wenn Sie auf einer 64-Bit-Plattform aufbauen.</span><span class="sxs-lookup"><span data-stu-id="70923-109">Set the value of **processorArchitecture** to x86 if building on a 32-bit platform, and to ia64 if building on a 64-bit platform.</span></span> <span data-ttu-id="70923-110">Das **Description** -Element enthält eine options Beschreibung der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="70923-110">The **description** element contains an option description of the application.</span></span> <span data-ttu-id="70923-111">Weitere Informationen zum Manifest-Format finden Sie unter [Anwendungs Manifeste](application-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="70923-111">For more information about the manifest format, see [application manifests](application-manifests.md).</span></span>

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

2.  <span data-ttu-id="70923-112">Fügen Sie das Manifest der Anwendung als Ressource in der binären ausführbaren Header Datei der Anwendung hinzu.</span><span class="sxs-lookup"><span data-stu-id="70923-112">Add the manifest to the application as a resource in the application's binary executable header file.</span></span> <span data-ttu-id="70923-113">Es wird nicht empfohlen, das Manifest als externe Manifest-Datei der Anwendung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="70923-113">It is not recommended that you add the manifest to the application as an external manifest file.</span></span>

    <span data-ttu-id="70923-114">Um das Manifest als Ressource hinzuzufügen, erstellen Sie eine Ressource in der Anwendung des Typs RT \_ Manifest ID 1.</span><span class="sxs-lookup"><span data-stu-id="70923-114">To add the manifest as a resource, create a resource in the application of type RT\_MANIFEST id 1.</span></span> <span data-ttu-id="70923-115">Wenn der Name der Anwendung beispielsweise yourapp lautet, sollte die Header Datei der Anwendung Folgendes enthalten:</span><span class="sxs-lookup"><span data-stu-id="70923-115">For example, if the application's name is YourApp, the application's header file should contain the following:</span></span>

    ``` syntax
    #define MANIFEST_RESOURCE_ID 1
    MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.manifest"
    ```

    <span data-ttu-id="70923-116">Wenn Sie das Manifest stattdessen als externe Manifest-Datei hinzufügen, stellen Sie sicher, dass die-Installation die Manifest-Datei in den Ordner kopiert, der die ausführbare Datei der Anwendung enthält.</span><span class="sxs-lookup"><span data-stu-id="70923-116">If you instead add the manifest as an external manifest file, be sure that the installation copies the manifest file into the folder containing the application's executable file.</span></span>

3.  <span data-ttu-id="70923-117">Testen Sie, um sicherzustellen, dass von der Anwendung verwendete Assemblys in der Anwendung ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="70923-117">Test to ensure that assemblies used by the application work correctly in the application.</span></span>

 

 



