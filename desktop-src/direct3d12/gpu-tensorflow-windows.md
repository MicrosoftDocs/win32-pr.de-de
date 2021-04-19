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
# <a name="enable-tensorflow-with-directml-on-windows"></a>Aktivieren von TensorFlow mit DirectML unter Windows

Diese Vorschau bietet Schülern und Einsteiger die Möglichkeit, mit dem Paket "tensorflow mit directml" Ihr Wissen im ml-Raum auf der vorhandenen Hardware zu entwickeln. Nach der Einrichtung können Benutzer mit dem [tensorflow-tutorialmodell](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) oder [unseren directml-Beispielen](https://github.com/microsoft/DirectML)beginnen. 

> [!NOTE]
> Das folgende Feature befindet sich in der Vorschau Phase und unterliegt Änderungen.

## <a name="check-your-version-of-windows"></a>Überprüfen Sie Ihre Windows-Version. 

Das tensorflow-Paket mit directml auf System eigenem Windows funktioniert ab Windows 10, Version 1709 (Build 16299 oder höher). Sie können die Buildversionsnummer überprüfen, indem Sie `winver` den Befehl " **Ausführen** " (Windows-Taste + R) ausführen.

## <a name="check-for-gpu-driver-updates"></a>Auf GPU-Treiber Updates überprüfen 

Stellen Sie sicher, dass Sie den aktuellen GPU-Treiber installiert haben. Wählen Sie im **Windows Update** Abschnitt der App "Einstellungen" die Option **nach Updates suchen** aus.

## <a name="set-up-the-tensorflow-with-directml-preview"></a>Einrichten von tensorflow mit directml (Vorschau) 

Es wird empfohlen, in Windows eine virtuelle python-Umgebung einzurichten. Es gibt viele Tools, die Sie verwenden können, um eine virtuelle python-Umgebung einzurichten – für diese Anweisungen verwenden wir [den minikonda von Anaconda](https://docs.conda.io/en/latest/miniconda.html). Der Rest dieses Setups setzt voraus, dass Sie eine miniconfiguration-Umgebung verwenden. 

### <a name="set-up-python-environment"></a>Einrichten der python-Umgebung 

Laden Sie den [miniconfiguration-Windows Installer](https://docs.conda.io/en/latest/miniconda.html#windows-installers) auf Ihrem System herunter, und installieren Sie ihn. Es gibt [zusätzliche Anleitungen für das Setup](https://conda.io/projects/conda/en/latest/user-guide/install/windows.html) auf dem Standort von Anaconda. Nachdem Mini-da installiert wurde, erstellen Sie eine Umgebung mithilfe von Python mit dem Namen **directml** und aktivieren Sie mithilfe der folgenden Befehle. 

> [!NOTE]
> In den folgenden Befehlen wird Python 3,6 verwendet. Das tensorflow-directml-Paket funktioniert jedoch in einer python-Umgebung 3,5, 3,6 oder 3,7. 

```
conda create --name directml python=3.6 

conda activate directml 
```

### <a name="install-the-tensorflow-with-directml-package"></a>Installieren des tensorflow mit dem directml-Paket 

Installieren Sie das Paket von tensorflow mithilfe eines directml-Back-Ends über PIP, indem Sie den folgenden Befehl ausführen.

> [!NOTE]
> Das tensorflow-directml-Paket unterstützt nur tensorflow 1,15. 

```
pip install tensorflow-directml
```

Nachdem Sie das tensorflow-directml-Paket installiert haben, können Sie überprüfen, ob es ordnungsgemäß ausgeführt wird, indem Sie zwei Tensoren hinzufügen. Kopieren Sie die folgenden Zeilen in eine interaktive python-Sitzung. 

```
import tensorflow.compat.v1 as tf 

tf.enable_eager_execution(tf.ConfigProto(log_device_placement=True)) 

print(tf.add([1.0, 2.0], [3.0, 4.0])) 
```

Es sollte eine Ausgabe ähnlich der folgenden angezeigt werden, bei der der Add-Operator auf dem DML-Gerät abgelegt wird. 

```
2020-06-15 11:27:18.235973: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:45] DirectML device enumeration: found 1 compatible adapters. 

2020-06-15 11:27:18.240065: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:32] DirectML: creating device on adapter 0 (AMD Radeon VII) 

2020-06-15 11:27:18.323949: I tensorflow/stream_executor/platform/default/dso_loader.cc:60] Successfully opened dynamic library DirectMLba106a7c621ea741d2159d8708ee581c11918380.dll 

2020-06-15 11:27:18.337830: I tensorflow/core/common_runtime/eager/execute.cc:571] Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0 

tf.Tensor([4. 6.], shape=(2,), dtype=float32) 
```

## <a name="tensorflow-with-directml-samples-and-feedback"></a>Tensorflow mit directml-Beispielen und Feedback 

Nun können Sie mehr über das ml-Training erfahren. Sehen Sie sich die [tensorflow-Tutorials](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) oder [unsere Beispiele](https://github.com/microsoft/DirectML)an. Wir haben diesen Inhalt als Validierung für dieses erste Vorschau Paket von tensorflow mit einem directml-Back-End verwendet. 

Wenn Sie Probleme haben oder Feedback zum tensorflow mit dem directml-Paket haben, stellen Sie eine [Verbindung mit unserem Team her](https://github.com/microsoft/DirectML/issues). 
