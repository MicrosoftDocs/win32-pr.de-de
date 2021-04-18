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
# <a name="faq"></a>Häufig gestellte Fragen

### <a name="how-do-i-enable-directml-acceleration"></a>Gewusst wie aktivieren Sie die directml-Beschleunigung? 

 
Das directml-Gerät ist standardmäßig aktiviert, sofern eine entsprechende DirectX 12-GPU verfügbar ist. Tensorflow-Vorgänge werden dem directml-Gerät nach Möglichkeit automatisch zugewiesen. 

Wenn Sie Probleme haben, festzustellen, ob Ihr Modell mithilfe von directml-Beschleunigung ausgeführt wird, können Sie `tf.debugging.set_log_device_placement(True)` als erste Anweisung ihres Programms einfügen, und tensorflow druckt Informationen zur Geräte Platzierung in der Konsole.

### <a name="how-do-i-control-device-placement-of-specific-operations"></a>Gewusst wie Steuern Sie die Platzierung bestimmter Vorgänge durch das Gerät? 
 

Wie bei jedem anderen Gerät (siehe [tensorflow-Handbuch: Verwenden von GPU](https://www.tensorflow.org/guide/gpu)) können Sie mit `tf.device()` Steuern, auf welchem Gerät ausgeführt werden soll. 
 

Die Geräte Zeichenfolge der directml ist `'DML'` . 


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

### <a name="i-have-multiple-gpus-how-do-i-select-which-one-is-used-by-directml"></a>Ich verfüge über mehrere GPUs. Gewusst wie auswählen, welche von directml verwendet wird?

Es gibt verschiedene Möglichkeiten, dies zu tun, je nachdem, ob Sie die Prozess weite oder pro Sitzung (oder beides) steuern möchten.

Wenn Sie steuern möchten, welche Geräte für tensorflow-Prozess weit sichtbar sind, verwenden Sie die- `DML_VISIBLE_DEVICES` Umgebungsvariable. Wenn Sie die Anwendung pro Sitzung steuern möchten, verwenden Sie `tf.GPUOptions.visible_device_list` .

### <a name="how-do-i-use-the-dml_visible_devices-environment-variable-to-control-which-gpus-get-used-by-directml"></a>Gewusst wie die `DML_VISIBLE_DEVICES` Umgebungsvariable verwenden, um zu steuern, welche GPU (s) von directml verwendet werden?

Tensorflow mit directml unterstützt eine `DML_VISIBLE_DEVICES` Umgebungsvariable, die eine durch Trennzeichen getrennte Liste von Geräte-IDs (auch als "Adapter Indizes" bezeichnet) annimmt. Wenn diese Einstellung festgelegt ist, werden nur die Geräte-IDs in dieser Liste für den Prozess weiten tensorflow sichtbar. Geräte `DML_VISIBLE_DEVICES` , die mithilfe von ausgeschlossen wurden, werden nicht in der Liste der für tensorflow verfügbaren physischen Geräte angezeigt.

```python
import tensorflow as tf
tf.debugging.set_log_device_placement(True)
tf.enable_eager_execution()

a = tf.constant([1.])
b = tf.constant([2.])
c = tf.add(a, b)
print(c)
```

Hier sehen Sie eine Beispielausgabe **ohne** `DML_VISIBLE_DEVICES` Set:

```
DirectML device enumeration: found 2 compatible adapters.
DirectML: creating device on adapter 0 (NVIDIA TITAN V)
DirectML: creating device on adapter 1 (AMD Radeon RX 5700 XT)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

Mit `DML_VISIBLE_DEVICES="1"` :

```
DirectML device enumeration: found 1 compatible adapters.
DirectML: creating device on adapter 0 (AMD Radeon RX 5700 XT)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

Beachten Sie Folgendes: Wenn Sie die sichtbaren Geräte auf Index 1 beschränken (AMD Radeon RX 5700 XT), weist tensorflow nun diesem Gerät die ID 0 zu und legt sie als Standard fest.

Sie können Geräte auch mit dieser Umgebungsvariablen neu anordnen. Legen Sie beispielsweise Folgendes fest `DML_VISIBLE_DEVICES="1,0"` :

```
DirectML device enumeration: found 2 compatible adapters.
DirectML: creating device on adapter 0 (AMD Radeon RX 5700 XT)
DirectML: creating device on adapter 1 (NVIDIA TITAN V)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

Beachten Sie, dass die beiden GPUs (NVIDIA Titan V und AMD Radeon RX 5700 XT) nun die Orte gewechselt haben.

Um zu verhindern, dass bestimmte Geräte sichtbar sind, können Sie in der durch Trennzeichen getrennten Liste eine ungültige ID (z. b. `-1` ) angeben. Alle Geräte-IDs nach dem ungültigen Eintrag werden ignoriert. Dies kann auch verwendet werden, um die directml-Beschleunigung vollständig zu deaktivieren.

`DML_VISIBLE_DEVICES="-1"`:

```
DirectML device enumeration: found 0 compatible adapters.
Executing op Add in device /job:localhost/replica:0/task:0/device:CPU:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

### <a name="how-do-i-use-the-visible_device_list-session-option-to-control-which-gpus-directml-uses-to-run-the-session"></a>Gewusst wie mit der `visible_device_list` Sitzungs Option steuern, welche GPU (s)-directml zum Ausführen der Sitzung verwendet wird?

Ähnlich wie bei `DML_VISIBLE_DEVICES` können Sie auch eine ähnliche Zeichenfolge festlegen, um sichtbare Geräte auf Sitzungs Ebene zu steuern. Das- `visible_device_list` Attribut ist für die-Klasse verfügbar, `GPUOptions` Wenn Sie Ihre tensorflow-Sitzung erstellen.

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

Weitere Informationen finden Sie in der [API-Referenz zu tensorflow gpuoptions](https://www.tensorflow.org/versions/r1.15/api_docs/python/tf/GPUOptions#visible_device_list) .