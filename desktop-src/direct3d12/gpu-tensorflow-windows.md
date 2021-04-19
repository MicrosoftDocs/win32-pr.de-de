---
title: Tensorflow mit directml unter Windows
description: Aktivieren von tensorflow mit directml direkt unter Windows
ms.topic: article
ms.date: 06/17/2020
ms.openlocfilehash: 665ba456d59f09f27a435135468cf71cb6f6f014
ms.sourcegitcommit: 8f3fb56ebad4615389dec5c74d965dec84ad4123
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/22/2020
ms.locfileid: "106341917"
---
# <a name="enable-tensorflow-with-directml-on-windows"></a><span data-ttu-id="4adb1-103">Aktivieren von TensorFlow mit DirectML unter Windows</span><span class="sxs-lookup"><span data-stu-id="4adb1-103">Enable TensorFlow with DirectML on Windows</span></span>

<span data-ttu-id="4adb1-104">Diese Vorschau bietet Schülern und Einsteiger die Möglichkeit, mit dem Paket "tensorflow mit directml" Ihr Wissen im ml-Raum auf der vorhandenen Hardware zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="4adb1-104">This preview provides students and beginners a way to start building their knowledge in the ML space on their existing hardware by using the the TensorFlow with DirectML package.</span></span> <span data-ttu-id="4adb1-105">Nach der Einrichtung können Benutzer mit dem [tensorflow-tutorialmodell](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) oder [unseren directml-Beispielen](https://github.com/microsoft/DirectML)beginnen.</span><span class="sxs-lookup"><span data-stu-id="4adb1-105">Once set up, users can start with the [TensorFlow tutorial models](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) or [our DirectML samples](https://github.com/microsoft/DirectML).</span></span> 

> [!NOTE]
> <span data-ttu-id="4adb1-106">Das folgende Feature befindet sich in der Vorschau Phase und unterliegt Änderungen.</span><span class="sxs-lookup"><span data-stu-id="4adb1-106">The following feature is in preview, and are subject to change.</span></span>

## <a name="check-your-version-of-windows"></a><span data-ttu-id="4adb1-107">Überprüfen Sie Ihre Windows-Version.</span><span class="sxs-lookup"><span data-stu-id="4adb1-107">Check your version of Windows</span></span> 

<span data-ttu-id="4adb1-108">Das tensorflow-Paket mit directml auf System eigenem Windows funktioniert ab Windows 10, Version 1709 (Build 16299 oder höher).</span><span class="sxs-lookup"><span data-stu-id="4adb1-108">The TensorFlow with DirectML package on native Windows works starting with Windows 10 Version 1709 (Build 16299 or higher).</span></span> <span data-ttu-id="4adb1-109">Sie können die Buildversionsnummer überprüfen, indem Sie `winver` den Befehl " **Ausführen** " (Windows-Taste + R) ausführen.</span><span class="sxs-lookup"><span data-stu-id="4adb1-109">You can check your build version number by running `winver` via the **Run** command (Windows logo key + R).</span></span>

## <a name="check-for-gpu-driver-updates"></a><span data-ttu-id="4adb1-110">Auf GPU-Treiber Updates überprüfen</span><span class="sxs-lookup"><span data-stu-id="4adb1-110">Check for GPU driver updates</span></span> 

<span data-ttu-id="4adb1-111">Stellen Sie sicher, dass Sie den aktuellen GPU-Treiber installiert haben.</span><span class="sxs-lookup"><span data-stu-id="4adb1-111">Ensure you have the latest GPU driver installed.</span></span> <span data-ttu-id="4adb1-112">Wählen Sie im **Windows Update** Abschnitt der App "Einstellungen" die Option **nach Updates suchen** aus.</span><span class="sxs-lookup"><span data-stu-id="4adb1-112">Select **Check for updates** in the **Windows Update** section of the Settings app.</span></span>

## <a name="set-up-the-tensorflow-with-directml-preview"></a><span data-ttu-id="4adb1-113">Einrichten von tensorflow mit directml (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="4adb1-113">Set up the TensorFlow with DirectML preview</span></span> 

<span data-ttu-id="4adb1-114">Es wird empfohlen, in Windows eine virtuelle python-Umgebung einzurichten.</span><span class="sxs-lookup"><span data-stu-id="4adb1-114">We recommend setting up a virtual Python environment inside Windows.</span></span> <span data-ttu-id="4adb1-115">Es gibt viele Tools, die Sie verwenden können, um eine virtuelle python-Umgebung einzurichten – für diese Anweisungen verwenden wir [den minikonda von Anaconda](https://docs.conda.io/en/latest/miniconda.html).</span><span class="sxs-lookup"><span data-stu-id="4adb1-115">There are many tools you can use to setup a virtual Python environment — for these instructions, we'll use [Anaconda’s Miniconda](https://docs.conda.io/en/latest/miniconda.html).</span></span> <span data-ttu-id="4adb1-116">Der Rest dieses Setups setzt voraus, dass Sie eine miniconfiguration-Umgebung verwenden.</span><span class="sxs-lookup"><span data-stu-id="4adb1-116">The rest of this setup assumes you use a miniconda environment.</span></span> 

### <a name="set-up-python-environment"></a><span data-ttu-id="4adb1-117">Einrichten der python-Umgebung</span><span class="sxs-lookup"><span data-stu-id="4adb1-117">Set up Python environment</span></span> 

<span data-ttu-id="4adb1-118">Laden Sie den [miniconfiguration-Windows Installer](https://docs.conda.io/en/latest/miniconda.html#windows-installers) auf Ihrem System herunter, und installieren Sie ihn.</span><span class="sxs-lookup"><span data-stu-id="4adb1-118">Download and install the [Miniconda Windows installer](https://docs.conda.io/en/latest/miniconda.html#windows-installers) on your system.</span></span> <span data-ttu-id="4adb1-119">Es gibt [zusätzliche Anleitungen für das Setup](https://conda.io/projects/conda/en/latest/user-guide/install/windows.html) auf dem Standort von Anaconda.</span><span class="sxs-lookup"><span data-stu-id="4adb1-119">There is [additional guidance for setup](https://conda.io/projects/conda/en/latest/user-guide/install/windows.html) on Anaconda’s site.</span></span> <span data-ttu-id="4adb1-120">Nachdem Mini-da installiert wurde, erstellen Sie eine Umgebung mithilfe von Python mit dem Namen **directml** und aktivieren Sie mithilfe der folgenden Befehle.</span><span class="sxs-lookup"><span data-stu-id="4adb1-120">Once Miniconda is installed, create an environment using Python named **directml** and activate it through the following commands.</span></span> 

> [!NOTE]
> <span data-ttu-id="4adb1-121">In den folgenden Befehlen wird Python 3,6 verwendet.</span><span class="sxs-lookup"><span data-stu-id="4adb1-121">In the commands below, we use Python 3.6.</span></span> <span data-ttu-id="4adb1-122">Das tensorflow-directml-Paket funktioniert jedoch in einer python-Umgebung 3,5, 3,6 oder 3,7.</span><span class="sxs-lookup"><span data-stu-id="4adb1-122">However, the tensorflow-directml package works in a Python 3.5, 3.6 or 3.7 environment.</span></span> 

```
conda create --name directml python=3.6 

conda activate directml 
```

### <a name="install-the-tensorflow-with-directml-package"></a><span data-ttu-id="4adb1-123">Installieren des tensorflow mit dem directml-Paket</span><span class="sxs-lookup"><span data-stu-id="4adb1-123">Install the Tensorflow with DirectML package</span></span> 

<span data-ttu-id="4adb1-124">Installieren Sie das Paket von tensorflow mithilfe eines directml-Back-Ends über PIP, indem Sie den folgenden Befehl ausführen.</span><span class="sxs-lookup"><span data-stu-id="4adb1-124">Install the package of TensorFlow with a DirectML backend through pip by running the following command.</span></span>

> [!NOTE]
> <span data-ttu-id="4adb1-125">Das tensorflow-directml-Paket unterstützt nur tensorflow 1,15.</span><span class="sxs-lookup"><span data-stu-id="4adb1-125">The tensorflow-directml package only supports TensorFlow 1.15.</span></span> 

```
pip install tensorflow-directml
```

<span data-ttu-id="4adb1-126">Nachdem Sie das tensorflow-directml-Paket installiert haben, können Sie überprüfen, ob es ordnungsgemäß ausgeführt wird, indem Sie zwei Tensoren hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4adb1-126">Once you’ve installed the tensorflow-directml package, you can verify that it runs correctly by adding two tensors.</span></span> <span data-ttu-id="4adb1-127">Kopieren Sie die folgenden Zeilen in eine interaktive python-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="4adb1-127">Copy the following lines into an interactive Python session.</span></span> 

```
import tensorflow.compat.v1 as tf 

tf.enable_eager_execution(tf.ConfigProto(log_device_placement=True)) 

print(tf.add([1.0, 2.0], [3.0, 4.0])) 
```

<span data-ttu-id="4adb1-128">Es sollte eine Ausgabe ähnlich der folgenden angezeigt werden, bei der der Add-Operator auf dem DML-Gerät abgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="4adb1-128">You should see output similar to the following, with the add operator placed on the DML device.</span></span> 

```
2020-06-15 11:27:18.235973: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:45] DirectML device enumeration: found 1 compatible adapters. 

2020-06-15 11:27:18.240065: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:32] DirectML: creating device on adapter 0 (AMD Radeon VII) 

2020-06-15 11:27:18.323949: I tensorflow/stream_executor/platform/default/dso_loader.cc:60] Successfully opened dynamic library DirectMLba106a7c621ea741d2159d8708ee581c11918380.dll 

2020-06-15 11:27:18.337830: I tensorflow/core/common_runtime/eager/execute.cc:571] Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0 

tf.Tensor([4. 6.], shape=(2,), dtype=float32) 
```

## <a name="tensorflow-with-directml-samples-and-feedback"></a><span data-ttu-id="4adb1-129">Tensorflow mit directml-Beispielen und Feedback</span><span class="sxs-lookup"><span data-stu-id="4adb1-129">Tensorflow with DirectML samples and feedback</span></span> 

<span data-ttu-id="4adb1-130">Nun können Sie mehr über das ml-Training erfahren.</span><span class="sxs-lookup"><span data-stu-id="4adb1-130">Now you’re ready to start learning more about ML training.</span></span> <span data-ttu-id="4adb1-131">Sehen Sie sich die [tensorflow-Tutorials](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) oder [unsere Beispiele](https://github.com/microsoft/DirectML)an.</span><span class="sxs-lookup"><span data-stu-id="4adb1-131">Check out the [TensorFlow tutorials](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) or [our samples](https://github.com/microsoft/DirectML).</span></span> <span data-ttu-id="4adb1-132">Wir haben diesen Inhalt als Validierung für dieses erste Vorschau Paket von tensorflow mit einem directml-Back-End verwendet.</span><span class="sxs-lookup"><span data-stu-id="4adb1-132">We used this content as validation for this initial preview package of TensorFlow with a DirectML backend.</span></span> 

<span data-ttu-id="4adb1-133">Wenn Sie Probleme haben oder Feedback zum tensorflow mit dem directml-Paket haben, stellen Sie eine [Verbindung mit unserem Team her](https://github.com/microsoft/DirectML/issues).</span><span class="sxs-lookup"><span data-stu-id="4adb1-133">If you run into issues or have feedback on the TensorFlow with DirectML package, please [connect with our team here](https://github.com/microsoft/DirectML/issues).</span></span> 
