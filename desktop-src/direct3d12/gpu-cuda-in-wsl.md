---
title: Aktivieren von NVIDIA CUDA in WSL 2
description: Aktivieren der NVIDIA CUDA Preview im Windows-Subsystem für Linux
ms.topic: article
ms.date: 06/17/2020
ms.openlocfilehash: ea5b460d4b4c71417f8ac9969f58bcebf6d10af9
ms.sourcegitcommit: 85acfd5afdcd30c81e3d2b375e813957f9830e9f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/03/2020
ms.locfileid: "106338693"
---
# <a name="enable-nvidia-cuda-in-wsl-2"></a><span data-ttu-id="890c2-103">Aktivieren von NVIDIA CUDA in WSL 2</span><span class="sxs-lookup"><span data-stu-id="890c2-103">Enable NVIDIA CUDA in WSL 2</span></span>

<span data-ttu-id="890c2-104">Das Windows Insider SDK unterstützt die Ausführung vorhandener ml-Tools, Bibliotheken und beliebter Frameworks, die NVIDIA CUDA für die GPU-Hardwarebeschleunigung innerhalb einer WSL 2-Instanz verwenden.</span><span class="sxs-lookup"><span data-stu-id="890c2-104">The Windows Insider SDK supports running existing ML tools, libraries, and popular frameworks that use NVIDIA CUDA for GPU hardware acceleration inside a WSL 2 instance.</span></span> <span data-ttu-id="890c2-105">Dies umfasst pytorch und tensorflow sowie alle docker-und NVIDIA Container Toolkit-Unterstützung, die in einer nativen Linux-Umgebung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="890c2-105">This includes PyTorch and TensorFlow as well as all the Docker and NVIDIA Container Toolkit support available in a native Linux environment.</span></span> 

> [!NOTE]
> <span data-ttu-id="890c2-106">Die folgenden Features sind in vorab Versionen von Windows 10 verfügbar und unterliegen Änderungen.</span><span class="sxs-lookup"><span data-stu-id="890c2-106">The following features are available in prerelease versions of Windows 10, and are subject to change.</span></span>

## <a name="install-the-latest-windows-insider-dev-channel-build"></a><span data-ttu-id="890c2-107">Installieren Sie den neuesten Windows Insider dev-kanalbuild.</span><span class="sxs-lookup"><span data-stu-id="890c2-107">Install the latest Windows Insider Dev Channel build</span></span> 

<span data-ttu-id="890c2-108">Um diese Vorschauversion verwenden zu können, müssen Sie sich [für das Windows Insider-Programm registrieren](https://insider.windows.com/getting-started/#register).</span><span class="sxs-lookup"><span data-stu-id="890c2-108">To use this preview, you'll need to [register for the Windows Insider Program](https://insider.windows.com/getting-started/#register).</span></span> <span data-ttu-id="890c2-109">Befolgen Sie anschließend die folgenden [Instuktionen](https://insider.windows.com/getting-started/#install) , um den neuesten Insider-Build zu installieren.</span><span class="sxs-lookup"><span data-stu-id="890c2-109">Once you do, follow [these instuctions](https://insider.windows.com/getting-started/#install) to install the latest Insider build.</span></span> <span data-ttu-id="890c2-110">Wenn Sie Ihre Einstellungen auswählen, stellen Sie sicher, dass Sie den Entwicklungs [Kanal](/windows-insider/flight-hub/#active-development-builds-of-windows-10)auswählen.</span><span class="sxs-lookup"><span data-stu-id="890c2-110">When choosing your settings, ensure you're selecting the [Dev Channel](/windows-insider/flight-hub/#active-development-builds-of-windows-10).</span></span> 

<span data-ttu-id="890c2-111">Für diese Vorschau benötigen Sie Build 20150 oder höher.</span><span class="sxs-lookup"><span data-stu-id="890c2-111">For this preview, you need Build 20150 or higher.</span></span> <span data-ttu-id="890c2-112">Sie können die Buildversionsnummer überprüfen, indem Sie `winver` den Befehl " **Ausführen** " (Windows-Taste + R) ausführen.</span><span class="sxs-lookup"><span data-stu-id="890c2-112">You can check your build version number by running `winver` via the **Run** command (Windows logo key + R).</span></span>

## <a name="install-the-preview-gpu-driver"></a><span data-ttu-id="890c2-113">Installieren des Vorschau-GPU-Treibers</span><span class="sxs-lookup"><span data-stu-id="890c2-113">Install the preview GPU driver</span></span> 

<span data-ttu-id="890c2-114">Herunterladen und Installieren des [NVIDIA CUDA-fähigen Treibers für WSL für](https://developer.nvidia.com/cuda/wsl) die Verwendung mit Ihren vorhandenen CUDA ml-Workflows.</span><span class="sxs-lookup"><span data-stu-id="890c2-114">Download and install the [NVIDIA CUDA-enabled driver for WSL](https://developer.nvidia.com/cuda/wsl) to use with your existing CUDA ML workflows.</span></span> 

## <a name="set-up-wsl-2-for-the-preview"></a><span data-ttu-id="890c2-115">Einrichten von WSL 2 für die Vorschauversion</span><span class="sxs-lookup"><span data-stu-id="890c2-115">Set up WSL 2 for the preview</span></span> 

<span data-ttu-id="890c2-116">Nachdem Sie den obigen Treiber installiert haben, stellen Sie sicher, dass Sie [WSL 2 aktivieren](/windows/wsl/install-win10) und [eine auf glibc basierende Verteilung](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (z. b. Ubuntu oder Debian) installieren.</span><span class="sxs-lookup"><span data-stu-id="890c2-116">Once you've installed the above driver, ensure you [enable WSL 2](/windows/wsl/install-win10) and [install a glibc-based distribution](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (such as Ubuntu or Debian).</span></span> <span data-ttu-id="890c2-117">Stellen Sie sicher, dass Sie über den neuesten Kernel verfügen, indem Sie im **Windows Update** Abschnitt der App "Einstellungen" auf " **Updates suchen" klicken**</span><span class="sxs-lookup"><span data-stu-id="890c2-117">Ensure you have the latest kernel by selecting **Check for updates** in the **Windows Update** section of the Settings app.</span></span> 

> [!NOTE]
> <span data-ttu-id="890c2-118">Stellen Sie sicher, **dass Sie Updates für andere Microsoft-Produkte erhalten, wenn Sie Windows aktiviert aktualisieren** .</span><span class="sxs-lookup"><span data-stu-id="890c2-118">Ensure you have **Receive updates for other Microsoft products when you update Windows** enabled.</span></span> <span data-ttu-id="890c2-119">Sie finden ihn unter " **Erweiterte Optionen** " im Abschnitt " **Windows Update** " der App "Einstellungen".</span><span class="sxs-lookup"><span data-stu-id="890c2-119">You can find it in **Advanced options** within the **Windows Update** section of the Settings app.</span></span> 

<span data-ttu-id="890c2-120">Für diese Vorschau benötigen Sie eine Kernel Version von 4.19.121 oder höher.</span><span class="sxs-lookup"><span data-stu-id="890c2-120">For this preview, you need a kernel version of 4.19.121 or higher.</span></span> <span data-ttu-id="890c2-121">Sie können die Versionsnummer überprüfen, indem Sie den folgenden Befehl in PowerShell ausführen.</span><span class="sxs-lookup"><span data-stu-id="890c2-121">You can check the version number by running the following command in PowerShell.</span></span> 

```powershell
wsl cat /proc/version
```

<span data-ttu-id="890c2-122">Nun können Sie Ihre vorhandenen Linux-Workflows über [NVIDIA docker](https://github.com/NVIDIA/nvidia-docker)oder durch die Installation von [pytorch](https://pytorch.org/get-started/locally/) oder [tensorflow](https://www.tensorflow.org/install/gpu) in WSL 2 verwenden.</span><span class="sxs-lookup"><span data-stu-id="890c2-122">Now you can start using your exisiting Linux workflows through [NVIDIA Docker](https://github.com/NVIDIA/nvidia-docker), or by installing [PyTorch](https://pytorch.org/get-started/locally/) or [TensorFlow](https://www.tensorflow.org/install/gpu) inside WSL 2.</span></span> <span data-ttu-id="890c2-123">Weitere Informationen zum Einrichten von Informationen finden Sie im [Benutzerhandbuch zu NVIDIA-CUDA auf WSL](https://docs.nvidia.com/cuda/wsl-user-guide/index.html).</span><span class="sxs-lookup"><span data-stu-id="890c2-123">More information on getting set up is captured in [NVIDIA's CUDA on WSL User Guide](https://docs.nvidia.com/cuda/wsl-user-guide/index.html).</span></span>

<span data-ttu-id="890c2-124">Teilen Sie uns Feedback zur NVIDIA-Unterstützung über das [Communityforum für CUDA auf WSL mit](https://forums.developer.nvidia.com/c/accelerated-computing/cuda/cuda-on-windows-subsystem-for-linux-wsl-2/303).</span><span class="sxs-lookup"><span data-stu-id="890c2-124">Share feedback on NVIDIA's support via their [Community forum for CUDA on WSL](https://forums.developer.nvidia.com/c/accelerated-computing/cuda/cuda-on-windows-subsystem-for-linux-wsl-2/303).</span></span>
