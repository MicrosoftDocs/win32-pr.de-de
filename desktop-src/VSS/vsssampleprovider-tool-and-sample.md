---
description: Zeigt, wie die VSS-Schnittstellen zum Erstellen eines VSS-Hardware Anbieters verwendet werden.
ms.assetid: 4d3c3f3c-22d2-4246-afef-aee2a0bd52d6
title: Vsssampleprovider-Tool und-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1fceaa65b851e5469a3e82323da92d8bde0651a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345729"
---
# <a name="vsssampleprovider-tool-and-sample"></a><span data-ttu-id="6bc99-103">Vsssampleprovider-Tool und-Beispiel</span><span class="sxs-lookup"><span data-stu-id="6bc99-103">VssSampleProvider Tool and Sample</span></span>

<span data-ttu-id="6bc99-104">Zeigt, wie die VSS- [Schnittstellen](volume-shadow-copy-api-interfaces.md) zum Erstellen eines VSS-Hardware Anbieters verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6bc99-104">Shows how to use the VSS [interfaces](volume-shadow-copy-api-interfaces.md) to create a VSS hardware provider.</span></span>

> [!Note]  
> <span data-ttu-id="6bc99-105">Das vsssampleprovider-Tool und-Beispiel sind im Microsoft Windows Software Development Kit (SDK) enthalten.</span><span class="sxs-lookup"><span data-stu-id="6bc99-105">The VssSampleProvider tool and sample are included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6bc99-106">Sie können den Windows SDK aus dem [Windows Software Development Kit (SDK) für Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk)herunterladen.</span><span class="sxs-lookup"><span data-stu-id="6bc99-106">You can download the Windows SDK from [Windows Software Development Kit (SDK) for Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk).</span></span>

 

<span data-ttu-id="6bc99-107">In der Windows SDK-Installation befindet sich das Tool vsssampleprovider in `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (für 64-Bit-Windows) und `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (für 32-Bit-Windows).</span><span class="sxs-lookup"><span data-stu-id="6bc99-107">In the Windows SDK installation, the VssSampleProvider tool can be found in `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (for 64-bit Windows) and `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (for 32-bit Windows).</span></span>

> [!Note]  
> <span data-ttu-id="6bc99-108">Hardware Anbieter werden nur auf Windows Server-Betriebssystemen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6bc99-108">Hardware providers are only supported on Windows Server operating systems.</span></span> <span data-ttu-id="6bc99-109">Unter einem Windows-Client Betriebssystem können Sie das vsssampleprovider-Beispiel kompilieren, aber Sie können es nicht als Hardware Anbieter registrieren.</span><span class="sxs-lookup"><span data-stu-id="6bc99-109">On a Windows Client operating system, you can compile the VssSampleProvider sample, but you can't register it as a hardware provider.</span></span>

 

<span data-ttu-id="6bc99-110">Das Tool vsssampleprovider besteht aus den folgenden Dateien:</span><span class="sxs-lookup"><span data-stu-id="6bc99-110">The VssSampleProvider tool consists of the following files:</span></span>

-   <span data-ttu-id="6bc99-111">Virtualstorage.sys</span><span class="sxs-lookup"><span data-stu-id="6bc99-111">Virtualstorage.sys</span></span>
-   <span data-ttu-id="6bc99-112">Vstorcontrol.exe</span><span class="sxs-lookup"><span data-stu-id="6bc99-112">Vstorcontrol.exe</span></span>
-   <span data-ttu-id="6bc99-113">Vssampleprovider.dll</span><span class="sxs-lookup"><span data-stu-id="6bc99-113">Vssampleprovider.dll</span></span>
-   <span data-ttu-id="6bc99-114">Vstorinterface.dll</span><span class="sxs-lookup"><span data-stu-id="6bc99-114">Vstorinterface.dll</span></span>

<span data-ttu-id="6bc99-115">Das vsssampleprovider-Beispiel enthält die folgenden Installations-und deinstalstallations Skripts:</span><span class="sxs-lookup"><span data-stu-id="6bc99-115">The VssSampleProvider sample includes the following installation and uninstallation scripts:</span></span>

-   <span data-ttu-id="6bc99-116">Install-SampleProvider. cmd</span><span class="sxs-lookup"><span data-stu-id="6bc99-116">Install-sampleprovider.cmd</span></span>
-   <span data-ttu-id="6bc99-117">Uninstall-SampleProvider. cmd</span><span class="sxs-lookup"><span data-stu-id="6bc99-117">Uninstall-sampleprovider.cmd</span></span>
-   <span data-ttu-id="6bc99-118">\_app.vbs registrieren</span><span class="sxs-lookup"><span data-stu-id="6bc99-118">Register\_app.vbs</span></span>

<span data-ttu-id="6bc99-119">**So installieren und verwenden Sie das vsssampleprovider-Beispiel**</span><span class="sxs-lookup"><span data-stu-id="6bc99-119">**To install and use the VssSampleProvider sample**</span></span>

1.  <span data-ttu-id="6bc99-120">Navigieren Sie zum Verzeichnis `Program Files (x86)\Windows Kits\8.0\bin\`.</span><span class="sxs-lookup"><span data-stu-id="6bc99-120">Navigate to the `Program Files (x86)\Windows Kits\8.0\bin\` directory.</span></span> <span data-ttu-id="6bc99-121">Dieses Verzeichnis enthält virtualstoragevss.sys und vstorcontrol.exe.</span><span class="sxs-lookup"><span data-stu-id="6bc99-121">This directory contains virtualstoragevss.sys and vstorcontrol.exe.</span></span>
2.  <span data-ttu-id="6bc99-122">Öffnen Sie ein Eingabe Aufforderungs Fenster im angegebenen Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="6bc99-122">Open a command prompt window in the specified directory.</span></span>
3.  <span data-ttu-id="6bc99-123">Geben Sie zum Installieren des virtuellen Speicher Treibers im Eingabe Aufforderungs Fenster den folgenden Befehl ein:</span><span class="sxs-lookup"><span data-stu-id="6bc99-123">To install the virtual storage driver, in the command prompt window, type the following command:</span></span>

    ```cmd
    vstorcontrol.exe install
    ```

    

4.  <span data-ttu-id="6bc99-124">Geben Sie zum Installieren des VSS-Beispiel Anbieters im Eingabe Aufforderungs Fenster den folgenden Befehl ein:</span><span class="sxs-lookup"><span data-stu-id="6bc99-124">To install the VSS sample provider, in the command prompt window, type the following command:</span></span>

    ```cmd
    install-sampleprovider.cmd
    ```

    

5.  <span data-ttu-id="6bc99-125">Gehen Sie folgendermaßen vor, um eine virtuelle LUN zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6bc99-125">To create a virtual LUN, do the following.</span></span>

    1.  <span data-ttu-id="6bc99-126">Geben Sie im Fenster der Eingabeaufforderung folgenden Befehl ein:</span><span class="sxs-lookup"><span data-stu-id="6bc99-126">In the command prompt window, type the following command:</span></span>

        ```cmd
        vstorcontrol.exe create fixeddisk -
        newimage C:\disk1.image -size 20M -storid "VSS Sample HW Provider"
        ```

        

        <span data-ttu-id="6bc99-127">Dieser Befehl erstellt eine virtuelle LUN, deren Speicher Bezeichner **VSS-Beispiel-HW-Anbieter** ist.</span><span class="sxs-lookup"><span data-stu-id="6bc99-127">This command creates a virtual LUN whose storage identifier is **VSS Sample HW Provider**.</span></span> <span data-ttu-id="6bc99-128">Um zusätzliche virtuelle LUNs zu erstellen, wiederholen Sie diesen Schritt.</span><span class="sxs-lookup"><span data-stu-id="6bc99-128">To create additional virtual LUNs, repeat this step.</span></span>

        <span data-ttu-id="6bc99-129">Der VSS-Beispiel Anbieter erkennt eine LUN nur, wenn der **VSS-Beispiel-HW-Anbieter** Teil des Speicher Bezeichners ist.</span><span class="sxs-lookup"><span data-stu-id="6bc99-129">The VSS sample provider recognizes a LUN only if **VSS Sample HW Provider** is a part of the storage identifier.</span></span> <span data-ttu-id="6bc99-130">Weitere Informationen zur Speicher Kennung finden Sie im folgenden Blogbeitrag.</span><span class="sxs-lookup"><span data-stu-id="6bc99-130">For more information about the storage identifier, see the following blog post.</span></span>

        [<span data-ttu-id="6bc99-131">LUN-Resync mit DiskShadow und virtuellem Speicher</span><span class="sxs-lookup"><span data-stu-id="6bc99-131">LUN - Resync with Diskshadow and Virtual Storage</span></span>](https://blogs.msdn.microsoft.com/b/himanshu_kale/archive/2009/06/02/lun-resync-with-diskshadow-virtual-storage.aspx)

    2.  <span data-ttu-id="6bc99-132">Verwenden Sie im Eingabe Aufforderungs Fenster diskpart.exe, um den virtuellen Datenträger zu formatieren, und weisen Sie ihm einen Laufwerk Buchstaben zu.</span><span class="sxs-lookup"><span data-stu-id="6bc99-132">In the command prompt window, use diskpart.exe to format the virtual disk and assign a drive letter to it.</span></span>

        <span data-ttu-id="6bc99-133">Hier ist ein Beispielskript, das an der DiskPart-Eingabeaufforderung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6bc99-133">Here is a sample script to run at the diskpart command prompt.</span></span>

        ```cmd
        Select disk 
        Create partition primary size=<size>
        Format FS=NTFS quick
        Assign Letter=<letter>
        Exit
        ```

        

6.  <span data-ttu-id="6bc99-134">Geben Sie zum Ausführen des Beispiel Anbieters im Eingabe Aufforderungs Fenster den folgenden Befehl ein:</span><span class="sxs-lookup"><span data-stu-id="6bc99-134">To run the sample provider, in the command prompt window, type the following command:</span></span>

    ```cmd
    Run vshadow.exe -p -nw <drive>
    ```

    

    <span data-ttu-id="6bc99-135">*<drive>* stellt den Laufwerk Buchstaben der virtuellen LUN dar.</span><span class="sxs-lookup"><span data-stu-id="6bc99-135">*<drive>* represents the drive letter of the virtual LUN.</span></span>

7.  <span data-ttu-id="6bc99-136">Um den VSS-Beispiel Anbieter zu deinstallieren, geben Sie im Eingabe Aufforderungs Fenster den folgenden Befehl ein:</span><span class="sxs-lookup"><span data-stu-id="6bc99-136">To uninstall the VSS sample provider, in the command prompt window, type the following command:</span></span>

    ```cmd
    uninstall-sampleprovider.cmd
    ```

    

8.  <span data-ttu-id="6bc99-137">Um den virtuellen Speicher Treiber zu deinstallieren, geben Sie im Eingabe Aufforderungs Fenster den folgenden Befehl ein:</span><span class="sxs-lookup"><span data-stu-id="6bc99-137">To uninstall the virtual storage driver, in the command prompt window, type the following command:</span></span>

    ```cmd
    vstorcontrol.exe uninstall
    ```

    

 

 



