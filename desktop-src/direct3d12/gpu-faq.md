---
title: 'GPU-Beschleunigung in WSL – Häufig gestellte Fragen '
description: Häufig gestellte Fragen zur GPU-Beschleunigung im Windows-Subsystem für Linux
ms.topic: article
ms.date: 09/28/2020
ms.openlocfilehash: 7c55a8c06bd2b62c670cbf532bc3aa65ddd919d7
ms.sourcegitcommit: f58718691e8b989650108b8c70aaa471d17bf3aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "106338101"
---
# <a name="faq"></a><span data-ttu-id="4f385-103">Häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="4f385-103">FAQ</span></span>

### <a name="how-do-i-enable-directml-acceleration"></a><span data-ttu-id="4f385-104">Gewusst wie aktivieren Sie die directml-Beschleunigung?</span><span class="sxs-lookup"><span data-stu-id="4f385-104">How do I enable DirectML acceleration?</span></span> 

 
<span data-ttu-id="4f385-105">Das directml-Gerät ist standardmäßig aktiviert, sofern eine entsprechende DirectX 12-GPU verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="4f385-105">The DirectML device is enabled by default, assuming you have an appropriate DirectX 12 GPU available.</span></span> <span data-ttu-id="4f385-106">Tensorflow-Vorgänge werden dem directml-Gerät nach Möglichkeit automatisch zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="4f385-106">TensorFlow operations will automatically be assigned to the DirectML device if possible.</span></span> 

<span data-ttu-id="4f385-107">Wenn Sie Probleme haben, festzustellen, ob Ihr Modell mithilfe von directml-Beschleunigung ausgeführt wird, können Sie `tf.debugging.set_log_device_placement(True)` als erste Anweisung ihres Programms einfügen, und tensorflow druckt Informationen zur Geräte Platzierung in der Konsole.</span><span class="sxs-lookup"><span data-stu-id="4f385-107">If you're having trouble determining whether your model is running using DirectML acceleration or not, you can put `tf.debugging.set_log_device_placement(True)` as the first statement of your program and TensorFlow will print device placement information to the console.</span></span>

### <a name="how-do-i-control-device-placement-of-specific-operations"></a><span data-ttu-id="4f385-108">Gewusst wie Steuern Sie die Platzierung bestimmter Vorgänge durch das Gerät?</span><span class="sxs-lookup"><span data-stu-id="4f385-108">How do I control device placement of specific operations?</span></span> 
 

<span data-ttu-id="4f385-109">Wie bei jedem anderen Gerät (siehe [tensorflow-Handbuch: Verwenden von GPU](https://www.tensorflow.org/guide/gpu)) können Sie mit `tf.device()` Steuern, auf welchem Gerät ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4f385-109">As with any other device (see [TensorFlow Guide: Use a GPU](https://www.tensorflow.org/guide/gpu)), you can use `tf.device()` to control which device to run on.</span></span> 
 

<span data-ttu-id="4f385-110">Die Geräte Zeichenfolge der directml ist `'DML'` .</span><span class="sxs-lookup"><span data-stu-id="4f385-110">The DirectML device string is `'DML'`.</span></span> 


```python 

import tensorflow as tf 

tf.debugging.set_log_device_placement(True) 

tf.enable_eager_execution() 

 

# Explicitly place tensors on the DirectML device 

with tf.device('/DML:0'): 

  a = tf.constant([1.0, 2.0, 3.0]) 

  b = tf.constant([4.0, 5.0, 6.0]) 

 

c = tf.add(a, b) 

print(c) 

``` 


``` 

Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0 

tf.Tensor([5. 7. 9.], shape=(3,), dtype=float32) 

```

### <a name="i-have-multiple-gpus-how-do-i-select-which-one-is-used-by-directml"></a><span data-ttu-id="4f385-111">Ich verfüge über mehrere GPUs.</span><span class="sxs-lookup"><span data-stu-id="4f385-111">I have multiple GPUs.</span></span> <span data-ttu-id="4f385-112">Gewusst wie auswählen, welche von directml verwendet wird?</span><span class="sxs-lookup"><span data-stu-id="4f385-112">How do I select which one is used by DirectML?</span></span>

<span data-ttu-id="4f385-113">Es gibt verschiedene Möglichkeiten, dies zu tun, je nachdem, ob Sie die Prozess weite oder pro Sitzung (oder beides) steuern möchten.</span><span class="sxs-lookup"><span data-stu-id="4f385-113">There are a couple of different ways to do this, depending on whether you want to control it process-wide or per-session (or both).</span></span>

<span data-ttu-id="4f385-114">Wenn Sie steuern möchten, welche Geräte für tensorflow-Prozess weit sichtbar sind, verwenden Sie die- `DML_VISIBLE_DEVICES` Umgebungsvariable.</span><span class="sxs-lookup"><span data-stu-id="4f385-114">If you want to control which devices are visible to TensorFlow process-wide, use the `DML_VISIBLE_DEVICES` environment variable.</span></span> <span data-ttu-id="4f385-115">Wenn Sie die Anwendung pro Sitzung steuern möchten, verwenden Sie `tf.GPUOptions.visible_device_list` .</span><span class="sxs-lookup"><span data-stu-id="4f385-115">If you want to control it on a per-session basis, use `tf.GPUOptions.visible_device_list`.</span></span>

### <a name="how-do-i-use-the-dml_visible_devices-environment-variable-to-control-which-gpus-get-used-by-directml"></a><span data-ttu-id="4f385-116">Gewusst wie die `DML_VISIBLE_DEVICES` Umgebungsvariable verwenden, um zu steuern, welche GPU (s) von directml verwendet werden?</span><span class="sxs-lookup"><span data-stu-id="4f385-116">How do I use the `DML_VISIBLE_DEVICES` environment variable to control which GPU(s) get used by DirectML?</span></span>

<span data-ttu-id="4f385-117">Tensorflow mit directml unterstützt eine `DML_VISIBLE_DEVICES` Umgebungsvariable, die eine durch Trennzeichen getrennte Liste von Geräte-IDs (auch als "Adapter Indizes" bezeichnet) annimmt. Wenn diese Einstellung festgelegt ist, werden nur die Geräte-IDs in dieser Liste für den Prozess weiten tensorflow sichtbar.</span><span class="sxs-lookup"><span data-stu-id="4f385-117">TensorFlow with DirectML supports a `DML_VISIBLE_DEVICES` environment variable, which takes the form of a comma-separated list of device IDs (also known as "adapter indices".) When set, only the device IDs in that list will be visible to TensorFlow process-wide.</span></span> <span data-ttu-id="4f385-118">Geräte `DML_VISIBLE_DEVICES` , die mithilfe von ausgeschlossen wurden, werden nicht in der Liste der für tensorflow verfügbaren physischen Geräte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4f385-118">Devices excluded using `DML_VISIBLE_DEVICES` will not appear in the list of physical devices available to TensorFlow.</span></span>

```python
import tensorflow as tf
tf.debugging.set_log_device_placement(True)
tf.enable_eager_execution()

a = tf.constant([1.])
b = tf.constant([2.])
c = tf.add(a, b)
print(c)
```

<span data-ttu-id="4f385-119">Hier sehen Sie eine Beispielausgabe **ohne** `DML_VISIBLE_DEVICES` Set:</span><span class="sxs-lookup"><span data-stu-id="4f385-119">Here is example output **without** `DML_VISIBLE_DEVICES` set:</span></span>

```
DirectML device enumeration: found 2 compatible adapters.
DirectML: creating device on adapter 0 (NVIDIA TITAN V)
DirectML: creating device on adapter 1 (AMD Radeon RX 5700 XT)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

<span data-ttu-id="4f385-120">Mit `DML_VISIBLE_DEVICES="1"` :</span><span class="sxs-lookup"><span data-stu-id="4f385-120">With `DML_VISIBLE_DEVICES="1"`:</span></span>

```
DirectML device enumeration: found 1 compatible adapters.
DirectML: creating device on adapter 0 (AMD Radeon RX 5700 XT)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

<span data-ttu-id="4f385-121">Beachten Sie Folgendes: Wenn Sie die sichtbaren Geräte auf Index 1 beschränken (AMD Radeon RX 5700 XT), weist tensorflow nun diesem Gerät die ID 0 zu und legt sie als Standard fest.</span><span class="sxs-lookup"><span data-stu-id="4f385-121">Note that by restricting the visible devices to only index 1 (AMD Radeon RX 5700 XT), TensorFlow now assigns an ID of 0 to this device, and makes it the default.</span></span>

<span data-ttu-id="4f385-122">Sie können Geräte auch mit dieser Umgebungsvariablen neu anordnen.</span><span class="sxs-lookup"><span data-stu-id="4f385-122">You may also re-order devices using this environment variable.</span></span> <span data-ttu-id="4f385-123">Legen Sie beispielsweise Folgendes fest `DML_VISIBLE_DEVICES="1,0"` :</span><span class="sxs-lookup"><span data-stu-id="4f385-123">For example, setting `DML_VISIBLE_DEVICES="1,0"`:</span></span>

```
DirectML device enumeration: found 2 compatible adapters.
DirectML: creating device on adapter 0 (AMD Radeon RX 5700 XT)
DirectML: creating device on adapter 1 (NVIDIA TITAN V)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

<span data-ttu-id="4f385-124">Beachten Sie, dass die beiden GPUs (NVIDIA Titan V und AMD Radeon RX 5700 XT) nun die Orte gewechselt haben.</span><span class="sxs-lookup"><span data-stu-id="4f385-124">Notice that the two GPUs (NVIDIA TITAN V and AMD Radeon RX 5700 XT) have now switched places.</span></span>

<span data-ttu-id="4f385-125">Um zu verhindern, dass bestimmte Geräte sichtbar sind, können Sie in der durch Trennzeichen getrennten Liste eine ungültige ID (z. b. `-1` ) angeben.</span><span class="sxs-lookup"><span data-stu-id="4f385-125">To prevent specific devices from being visible, you can supply an invalid ID (e.g. `-1`) in the comma-separated list.</span></span> <span data-ttu-id="4f385-126">Alle Geräte-IDs nach dem ungültigen Eintrag werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="4f385-126">All device IDs after the invalid entry are ignored.</span></span> <span data-ttu-id="4f385-127">Dies kann auch verwendet werden, um die directml-Beschleunigung vollständig zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="4f385-127">You can also use this to disable DirectML acceleration altogether.</span></span>

<span data-ttu-id="4f385-128">`DML_VISIBLE_DEVICES="-1"`:</span><span class="sxs-lookup"><span data-stu-id="4f385-128">`DML_VISIBLE_DEVICES="-1"`:</span></span>

```
DirectML device enumeration: found 0 compatible adapters.
Executing op Add in device /job:localhost/replica:0/task:0/device:CPU:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

### <a name="how-do-i-use-the-visible_device_list-session-option-to-control-which-gpus-directml-uses-to-run-the-session"></a><span data-ttu-id="4f385-129">Gewusst wie mit der `visible_device_list` Sitzungs Option steuern, welche GPU (s)-directml zum Ausführen der Sitzung verwendet wird?</span><span class="sxs-lookup"><span data-stu-id="4f385-129">How do I use the `visible_device_list` session option to control which GPU(s) DirectML uses to run the session?</span></span>

<span data-ttu-id="4f385-130">Ähnlich wie bei `DML_VISIBLE_DEVICES` können Sie auch eine ähnliche Zeichenfolge festlegen, um sichtbare Geräte auf Sitzungs Ebene zu steuern.</span><span class="sxs-lookup"><span data-stu-id="4f385-130">Similar to `DML_VISIBLE_DEVICES`, you can also set a similar string to control visible devices at a session level.</span></span> <span data-ttu-id="4f385-131">Das- `visible_device_list` Attribut ist für die-Klasse verfügbar, `GPUOptions` Wenn Sie Ihre tensorflow-Sitzung erstellen.</span><span class="sxs-lookup"><span data-stu-id="4f385-131">The `visible_device_list` attribute is available on the `GPUOptions` class when creating your TensorFlow session.</span></span>

```python
import tensorflow as tf

a = tf.constant([1.])
b = tf.constant([2.])
c = tf.add(a, b)

gpu_config = tf.GPUOptions()
gpu_config.visible_device_list = "1"

session = tf.Session(config=tf.ConfigProto(gpu_options=gpu_config))
print(session.run(c))
```

```
DirectML device enumeration: found 2 compatible adapters.
DirectML: creating device on adapter 1 (AMD Radeon RX 5700 XT)
[3.]
```

<span data-ttu-id="4f385-132">Weitere Informationen finden Sie in der [API-Referenz zu tensorflow gpuoptions](https://www.tensorflow.org/versions/r1.15/api_docs/python/tf/GPUOptions#visible_device_list) .</span><span class="sxs-lookup"><span data-stu-id="4f385-132">You can read the [TensorFlow GPUOptions API reference](https://www.tensorflow.org/versions/r1.15/api_docs/python/tf/GPUOptions#visible_device_list) for more details.</span></span>