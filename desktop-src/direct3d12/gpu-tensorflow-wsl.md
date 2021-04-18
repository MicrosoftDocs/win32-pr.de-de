---
title: Tensorflow mit directml auf WSL 2
description: Aktivieren von tensorflow mit directml im Windows-Subsystem für Linux
ms.topic: article
ms.date: 06/17/2020
ms.openlocfilehash: bfd776013e417760d52134d697439be60c5a1ae8
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "106340947"
---
# <a name="enable-tensorflow-with-directml-in-wsl-2"></a><span data-ttu-id="4f0a3-103">Aktivieren von TensorFlow mit DirectML in WSL 2</span><span class="sxs-lookup"><span data-stu-id="4f0a3-103">Enable TensorFlow with DirectML in WSL 2</span></span>

<span data-ttu-id="4f0a3-104">Diese Vorschau bietet Schülern und Einsteiger eine Möglichkeit, mit der Verwendung des tensorflow mit directml-Paket wissen im ml-Speicherplatz auf der vorhandenen Hardware zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-104">This preview provides students and beginners a way to start building knowledge in the ML space on their existing hardware by using the TensorFlow with DirectML package.</span></span> <span data-ttu-id="4f0a3-105">Nach der Einrichtung können Benutzer mit dem [tensorflow-tutorialmodell](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) oder unseren [directml-Beispielen](https://github.com/microsoft/DirectML)beginnen.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-105">Once set up, users can start with the [TensorFlow tutorial models](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) or our [DirectML samples](https://github.com/microsoft/DirectML).</span></span> 

> [!NOTE]
> <span data-ttu-id="4f0a3-106">Die folgenden Features sind in vorab Versionen von Windows 10 verfügbar und unterliegen Änderungen.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-106">The following features are available in prerelease versions of Windows 10, and are subject to change.</span></span>

## <a name="install-the-latest-windows-insider-dev-channel-build"></a><span data-ttu-id="4f0a3-107">Installieren Sie den neuesten Windows Insider dev-kanalbuild.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-107">Install the latest Windows Insider Dev Channel build</span></span> 

<span data-ttu-id="4f0a3-108">Um diese Vorschauversion verwenden zu können, müssen Sie sich [für das Windows Insider-Programm registrieren](https://insider.windows.com/getting-started/#register).</span><span class="sxs-lookup"><span data-stu-id="4f0a3-108">To use this preview, you'll need to [register for the Windows Insider Program](https://insider.windows.com/getting-started/#register).</span></span> <span data-ttu-id="4f0a3-109">Befolgen Sie anschließend die folgenden [Instuktionen](https://insider.windows.com/getting-started/#install) , um den neuesten Insider-Build zu installieren.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-109">Once you do, follow [these instuctions](https://insider.windows.com/getting-started/#install) to install the latest insider build.</span></span> <span data-ttu-id="4f0a3-110">Wenn Sie Ihre Einstellungen auswählen, stellen Sie sicher, dass Sie den Entwicklungs [Kanal](/windows-insider/flight-hub/#active-development-builds-of-windows-10)auswählen.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-110">When choosing your settings, ensure you're selecting the [Dev Channel](/windows-insider/flight-hub/#active-development-builds-of-windows-10).</span></span> 

<span data-ttu-id="4f0a3-111">Für diese Vorschau benötigen Sie Build 20150 oder höher.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-111">For this preview, you need Build 20150 or higher.</span></span> <span data-ttu-id="4f0a3-112">Sie können die Buildversionsnummer überprüfen, indem Sie `winver` den Befehl " **Ausführen** " (Windows-Taste + R) ausführen.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-112">You can check your build version number by running `winver` via the **Run** command (Windows logo key + R).</span></span>

## <a name="install-the-preview-gpu-driver"></a><span data-ttu-id="4f0a3-113">Installieren des Vorschau-GPU-Treibers</span><span class="sxs-lookup"><span data-stu-id="4f0a3-113">Install the preview GPU driver</span></span> 

<span data-ttu-id="4f0a3-114">Vor der Installation des tensorflow mit dem directml-Paket in WSL 2 müssen Sie Treiber von Ihrem GPU-Hardware Anbieter installieren.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-114">Before installing the TensorFlow with DirectML package inside WSL 2, you need to install drivers from your GPU hardware vendor.</span></span> <span data-ttu-id="4f0a3-115">Diese Treiber ermöglichen es Windows GPU, mit WSL 2 zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-115">These drivers enable the Windows GPU to work with WSL 2.</span></span>

### <a name="amd"></a><span data-ttu-id="4f0a3-116">AMD</span><span class="sxs-lookup"><span data-stu-id="4f0a3-116">AMD</span></span> 

<span data-ttu-id="4f0a3-117">[Laden Sie den AMD-Vorschau Treiber von seiner Website herunter und installieren Sie](https://www.amd.com/en/support/kb/release-notes/rn-rad-win-wsl-support) ihn.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-117">[Download and install AMD’s preview driver](https://www.amd.com/en/support/kb/release-notes/rn-rad-win-wsl-support) from their website.</span></span> <span data-ttu-id="4f0a3-118">Dieser Vorschau Treiber unterstützt die folgende Hardware:</span><span class="sxs-lookup"><span data-stu-id="4f0a3-118">This preview driver supports the following hardware:</span></span> 

* <span data-ttu-id="4f0a3-119">AMD Radeon™ RX-Serie und Radeon™ VII-Grafiken.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-119">AMD Radeon™ RX series and Radeon™ VII graphics.</span></span> 
* <span data-ttu-id="4f0a3-120">AMD Radeon™ Grafik der Pro-Serie.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-120">AMD Radeon™ Pro series graphics.</span></span> 
* <span data-ttu-id="4f0a3-121">AMD ryzen™ und ryzen™ pro-Prozessoren mit Radeon™ Vega-Grafiken.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-121">AMD Ryzen™ and Ryzen™ PRO Processors with Radeon™ Vega graphics.</span></span> 
* <span data-ttu-id="4f0a3-122">AMD ryzen™ und ryzen™ pro Mobile-Prozessoren mit Radeon™ Vega-Grafiken.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-122">AMD Ryzen™ and Ryzen™ PRO Mobile Processors with Radeon™ Vega graphics.</span></span> 

<span data-ttu-id="4f0a3-123">Eine umfassende Liste der kompatiblen AMD-Produkte finden Sie in den Anmerkungen zu dieser Version.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-123">For a complete list of compatible AMD products, please refer to the AMD Release Notes.</span></span> 

### <a name="intel"></a><span data-ttu-id="4f0a3-124">Intel</span><span class="sxs-lookup"><span data-stu-id="4f0a3-124">Intel</span></span> 

<span data-ttu-id="4f0a3-125">[Laden Sie den Intel-Vorschau Treiber](https://downloadcenter.intel.com/download/29526) für die Verwendung mit directml von Ihrer Website herunter, und installieren Sie ihn.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-125">[Download and install Intel’s preview driver](https://downloadcenter.intel.com/download/29526) to use with DirectML from their website.</span></span> 

### <a name="nvidia"></a><span data-ttu-id="4f0a3-126">NVIDIA</span><span class="sxs-lookup"><span data-stu-id="4f0a3-126">NVIDIA</span></span> 

<span data-ttu-id="4f0a3-127">[Laden Sie den NVIDIA-Vorschau Treiber](https://developer.nvidia.com/cuda/wsl/download) für die Verwendung mit directml von der Website herunter, und installieren Sie ihn.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-127">[Download and install NVIDIA's preview driver](https://developer.nvidia.com/cuda/wsl/download) to use with DirectML from their website.</span></span> <span data-ttu-id="4f0a3-128">Weitere Informationen finden Sie auf [der Seite zu NVIDIA-GPU auf dem Windows-Subsystem für Linux (WSL)](https://developer.nvidia.com/cuda/wsl) .</span><span class="sxs-lookup"><span data-stu-id="4f0a3-128">For more information, see [NVIDIA's GPU in Windows Subsystem for Linux (WSL)](https://developer.nvidia.com/cuda/wsl) page.</span></span>

## <a name="set-up-the-tensorflow-with-directml-preview"></a><span data-ttu-id="4f0a3-129">Einrichten von tensorflow mit directml (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="4f0a3-129">Set up the TensorFlow with DirectML preview</span></span> 

### <a name="install-wsl-2"></a><span data-ttu-id="4f0a3-130">Installieren von WSL 2</span><span class="sxs-lookup"><span data-stu-id="4f0a3-130">Install WSL 2</span></span> 

<span data-ttu-id="4f0a3-131">Nachdem Sie den obigen Treiber installiert haben, stellen Sie sicher, dass Sie [WSL 2 aktivieren](/windows/wsl/install-win10) und [eine auf glibc basierende Verteilung](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (z. b. Ubuntu oder Debian) installieren.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-131">Once you've installed the above driver, ensure you [enable WSL 2](/windows/wsl/install-win10) and [install a glibc-based distribution](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (like Ubuntu or Debian).</span></span> <span data-ttu-id="4f0a3-132">Für unsere Tests haben wir Ubuntu verwendet.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-132">For our testing, we used Ubuntu.</span></span> <span data-ttu-id="4f0a3-133">Stellen Sie sicher, dass Sie über den neuesten Kernel verfügen, indem Sie im **Windows Update** Abschnitt der App "Einstellungen" auf " **Updates suchen" klicken**</span><span class="sxs-lookup"><span data-stu-id="4f0a3-133">Ensure you have the latest kernel by selecting **Check for updates** in the **Windows Update** section of the Settings app.</span></span> 

> [!NOTE]
> <span data-ttu-id="4f0a3-134">Stellen Sie sicher, dass Sie über die **Empfangs Updates für andere Microsoft-Produkte verfügen, wenn Sie Windows aktiviert aktualisieren** .</span><span class="sxs-lookup"><span data-stu-id="4f0a3-134">Ensure you have the **Receive updates for other Microsoft products when you update Windows** enabled.</span></span> <span data-ttu-id="4f0a3-135">Sie finden ihn unter " **Erweiterte Optionen** " im Abschnitt " **Windows Update** " der App "Einstellungen".</span><span class="sxs-lookup"><span data-stu-id="4f0a3-135">You can find it in **Advanced options** within the **Windows Update** section of the Settings app.</span></span> 

<span data-ttu-id="4f0a3-136">Für diese Vorschau benötigen Sie eine Kernel Version von 4.19.121 oder höher.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-136">For this preview, you need a kernel version of 4.19.121 or higher.</span></span> <span data-ttu-id="4f0a3-137">Sie können die Versionsnummer überprüfen, indem Sie den folgenden Befehl in PowerShell ausführen.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-137">You can check the version number by running the following command in PowerShell.</span></span> 

```
wsl cat /proc/version
```

### <a name="set-up-python-environment"></a><span data-ttu-id="4f0a3-138">Einrichten der python-Umgebung</span><span class="sxs-lookup"><span data-stu-id="4f0a3-138">Set up Python environment</span></span> 

<span data-ttu-id="4f0a3-139">Es wird empfohlen, eine virtuelle python-Umgebung in ihrer WSL 2-Instanz einzurichten.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-139">We recommend setting up a virtual Python environment inside your WSL 2 instance.</span></span> <span data-ttu-id="4f0a3-140">Es gibt viele Tools, die Sie verwenden können, um eine virtuelle python-Umgebung einzurichten – für diese Anweisungen verwenden wir [den minikonda von Anaconda](https://docs.conda.io/en/latest/miniconda.html).</span><span class="sxs-lookup"><span data-stu-id="4f0a3-140">There are many tools you can use to setup a virtual Python environment — for these instructions, we'll use [Anaconda’s Miniconda](https://docs.conda.io/en/latest/miniconda.html).</span></span> <span data-ttu-id="4f0a3-141">Der Rest dieses Setups setzt voraus, dass Sie eine miniconfiguration-Umgebung verwenden.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-141">The rest of this setup assumes you use a miniconda environment.</span></span> 

<span data-ttu-id="4f0a3-142">Installieren Sie minikonda, indem Sie die [Anweisungen auf der Website von Anaconda](https://conda.io/projects/conda/en/latest/user-guide/install/index.html)befolgen, oder indem Sie die folgenden Befehle in WSL ausführen.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-142">Install Miniconda by following the [guidance on Anaconda’s site](https://conda.io/projects/conda/en/latest/user-guide/install/index.html), or by running the following commands in WSL.</span></span> 

```
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh 
bash Miniconda3-latest-Linux-x86_64.sh 
```

<span data-ttu-id="4f0a3-143">Nachdem miniconfiguration in WSL installiert wurde, erstellen Sie eine Umgebung mithilfe von Python mit dem Namen "directml", und aktivieren Sie Sie mithilfe der folgenden Befehle.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-143">Once Miniconda is installed in WSL, create an environment using Python named “directml” and activate it through the following commands.</span></span> 

> [!NOTE]
> <span data-ttu-id="4f0a3-144">In den folgenden Befehlen wird Python 3,6 verwendet.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-144">In the commands below, we use Python 3.6.</span></span> <span data-ttu-id="4f0a3-145">Das tensorflow-directml-Paket funktioniert jedoch in einer python-Umgebung 3,5, 3,6 oder 3,7.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-145">However, the tensorflow-directml package works in a Python 3.5, 3.6 or 3.7 environment.</span></span> 

```
conda create --name directml python=3.6 

conda activate directml 
```

### <a name="install-the-tensorflow-with-directml-package"></a><span data-ttu-id="4f0a3-146">Installieren des tensorflow mit dem directml-Paket</span><span class="sxs-lookup"><span data-stu-id="4f0a3-146">Install the Tensorflow with DirectML package</span></span> 

<span data-ttu-id="4f0a3-147">Installieren Sie das Paket von tensorflow mithilfe eines directml-Back-Ends über PIP, indem Sie den folgenden Befehl ausführen.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-147">Install the package of TensorFlow with a DirectML backend through pip by running the following command.</span></span>

> [!NOTE]
> <span data-ttu-id="4f0a3-148">Das tensorflow-directml-Paket unterstützt nur tensorflow 1,15.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-148">The tensorflow-directml package only supports TensorFlow 1.15.</span></span> 

```
pip install tensorflow-directml
```

<span data-ttu-id="4f0a3-149">Nachdem Sie das tensorflow-directml-Paket installiert haben, können Sie überprüfen, ob es ordnungsgemäß ausgeführt wird, indem Sie zwei Tensoren hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-149">Once you’ve installed the tensorflow-directml package, you can verify that it runs correctly by adding two tensors.</span></span> <span data-ttu-id="4f0a3-150">Kopieren Sie die folgenden Zeilen in eine interaktive python-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-150">Copy the following lines into an interactive Python session.</span></span> 

```
import tensorflow.compat.v1 as tf 

tf.enable_eager_execution(tf.ConfigProto(log_device_placement=True)) 

print(tf.add([1.0, 2.0], [3.0, 4.0])) 
```

<span data-ttu-id="4f0a3-151">Es sollte eine Ausgabe ähnlich der folgenden angezeigt werden, bei der der Add-Operator auf dem DML-Gerät abgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-151">You should see output similar to the following, with the add operator placed on the DML device.</span></span> 

```
2020-06-15 11:27:18.235973: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:45] DirectML device enumeration: found 1 compatible adapters. 

2020-06-15 11:27:18.240065: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:32] DirectML: creating device on adapter 0 (AMD Radeon VII) 

2020-06-15 11:27:18.323949: I tensorflow/stream_executor/platform/default/dso_loader.cc:60] Successfully opened dynamic library libdirectml.so.ba106a7c621ea741d21598708ee581c11918380 

2020-06-15 11:27:18.337830: I tensorflow/core/common_runtime/eager/execute.cc:571] Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0 

tf.Tensor([4. 6.], shape=(2,), dtype=float32) 
```

## <a name="tensorflow-with-directml-samples-and-feedback"></a><span data-ttu-id="4f0a3-152">Tensorflow mit directml-Beispielen und Feedback</span><span class="sxs-lookup"><span data-stu-id="4f0a3-152">Tensorflow with DirectML samples and feedback</span></span> 

<span data-ttu-id="4f0a3-153">Nun können Sie mehr über das ml-Training erfahren.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-153">Now you’re ready to start learning more about ML training.</span></span> <span data-ttu-id="4f0a3-154">Sehen Sie sich die [tensorflow-Tutorials](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) oder [unsere Beispiele](https://github.com/microsoft/DirectML)an.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-154">Check out the [TensorFlow tutorials](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) or [our samples](https://github.com/microsoft/DirectML).</span></span> <span data-ttu-id="4f0a3-155">Wir haben diesen Inhalt als Validierung für dieses erste Vorschau Paket von tensorflow mit directml verwendet.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-155">We used this content as validation for this initial preview package of TensorFlow with DirectML.</span></span> 

<span data-ttu-id="4f0a3-156">Wenn Sie Probleme haben oder Feedback zum tensorflow mit dem directml-Paket haben, stellen Sie eine [Verbindung mit unserem Team her](https://github.com/microsoft/DirectML/issues).</span><span class="sxs-lookup"><span data-stu-id="4f0a3-156">If you run into issues or have feedback on the TensorFlow with DirectML package, please [connect with our team here](https://github.com/microsoft/DirectML/issues).</span></span>
