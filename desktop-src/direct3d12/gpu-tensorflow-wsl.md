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
# <a name="enable-tensorflow-with-directml-in-wsl-2"></a>Aktivieren von TensorFlow mit DirectML in WSL 2

Diese Vorschau bietet Schülern und Einsteiger eine Möglichkeit, mit der Verwendung des tensorflow mit directml-Paket wissen im ml-Speicherplatz auf der vorhandenen Hardware zu entwickeln. Nach der Einrichtung können Benutzer mit dem [tensorflow-tutorialmodell](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) oder unseren [directml-Beispielen](https://github.com/microsoft/DirectML)beginnen. 

> [!NOTE]
> Die folgenden Features sind in vorab Versionen von Windows 10 verfügbar und unterliegen Änderungen.

## <a name="install-the-latest-windows-insider-dev-channel-build"></a>Installieren Sie den neuesten Windows Insider dev-kanalbuild. 

Um diese Vorschauversion verwenden zu können, müssen Sie sich [für das Windows Insider-Programm registrieren](https://insider.windows.com/getting-started/#register). Befolgen Sie anschließend die folgenden [Instuktionen](https://insider.windows.com/getting-started/#install) , um den neuesten Insider-Build zu installieren. Wenn Sie Ihre Einstellungen auswählen, stellen Sie sicher, dass Sie den Entwicklungs [Kanal](/windows-insider/flight-hub/#active-development-builds-of-windows-10)auswählen. 

Für diese Vorschau benötigen Sie Build 20150 oder höher. Sie können die Buildversionsnummer überprüfen, indem Sie `winver` den Befehl " **Ausführen** " (Windows-Taste + R) ausführen.

## <a name="install-the-preview-gpu-driver"></a>Installieren des Vorschau-GPU-Treibers 

Vor der Installation des tensorflow mit dem directml-Paket in WSL 2 müssen Sie Treiber von Ihrem GPU-Hardware Anbieter installieren. Diese Treiber ermöglichen es Windows GPU, mit WSL 2 zu arbeiten.

### <a name="amd"></a>AMD 

[Laden Sie den AMD-Vorschau Treiber von seiner Website herunter und installieren Sie](https://www.amd.com/en/support/kb/release-notes/rn-rad-win-wsl-support) ihn. Dieser Vorschau Treiber unterstützt die folgende Hardware: 

* AMD Radeon™ RX-Serie und Radeon™ VII-Grafiken. 
* AMD Radeon™ Grafik der Pro-Serie. 
* AMD ryzen™ und ryzen™ pro-Prozessoren mit Radeon™ Vega-Grafiken. 
* AMD ryzen™ und ryzen™ pro Mobile-Prozessoren mit Radeon™ Vega-Grafiken. 

Eine umfassende Liste der kompatiblen AMD-Produkte finden Sie in den Anmerkungen zu dieser Version. 

### <a name="intel"></a>Intel 

[Laden Sie den Intel-Vorschau Treiber](https://downloadcenter.intel.com/download/29526) für die Verwendung mit directml von Ihrer Website herunter, und installieren Sie ihn. 

### <a name="nvidia"></a>NVIDIA 

[Laden Sie den NVIDIA-Vorschau Treiber](https://developer.nvidia.com/cuda/wsl/download) für die Verwendung mit directml von der Website herunter, und installieren Sie ihn. Weitere Informationen finden Sie auf [der Seite zu NVIDIA-GPU auf dem Windows-Subsystem für Linux (WSL)](https://developer.nvidia.com/cuda/wsl) .

## <a name="set-up-the-tensorflow-with-directml-preview"></a>Einrichten von tensorflow mit directml (Vorschau) 

### <a name="install-wsl-2"></a>Installieren von WSL 2 

Nachdem Sie den obigen Treiber installiert haben, stellen Sie sicher, dass Sie [WSL 2 aktivieren](/windows/wsl/install-win10) und [eine auf glibc basierende Verteilung](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (z. b. Ubuntu oder Debian) installieren. Für unsere Tests haben wir Ubuntu verwendet. Stellen Sie sicher, dass Sie über den neuesten Kernel verfügen, indem Sie im **Windows Update** Abschnitt der App "Einstellungen" auf " **Updates suchen" klicken** 

> [!NOTE]
> Stellen Sie sicher, dass Sie über die **Empfangs Updates für andere Microsoft-Produkte verfügen, wenn Sie Windows aktiviert aktualisieren** . Sie finden ihn unter " **Erweiterte Optionen** " im Abschnitt " **Windows Update** " der App "Einstellungen". 

Für diese Vorschau benötigen Sie eine Kernel Version von 4.19.121 oder höher. Sie können die Versionsnummer überprüfen, indem Sie den folgenden Befehl in PowerShell ausführen. 

```
wsl cat /proc/version
```

### <a name="set-up-python-environment"></a>Einrichten der python-Umgebung 

Es wird empfohlen, eine virtuelle python-Umgebung in ihrer WSL 2-Instanz einzurichten. Es gibt viele Tools, die Sie verwenden können, um eine virtuelle python-Umgebung einzurichten – für diese Anweisungen verwenden wir [den minikonda von Anaconda](https://docs.conda.io/en/latest/miniconda.html). Der Rest dieses Setups setzt voraus, dass Sie eine miniconfiguration-Umgebung verwenden. 

Installieren Sie minikonda, indem Sie die [Anweisungen auf der Website von Anaconda](https://conda.io/projects/conda/en/latest/user-guide/install/index.html)befolgen, oder indem Sie die folgenden Befehle in WSL ausführen. 

```
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh 
bash Miniconda3-latest-Linux-x86_64.sh 
```

Nachdem miniconfiguration in WSL installiert wurde, erstellen Sie eine Umgebung mithilfe von Python mit dem Namen "directml", und aktivieren Sie Sie mithilfe der folgenden Befehle. 

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

2020-06-15 11:27:18.323949: I tensorflow/stream_executor/platform/default/dso_loader.cc:60] Successfully opened dynamic library libdirectml.so.ba106a7c621ea741d21598708ee581c11918380 

2020-06-15 11:27:18.337830: I tensorflow/core/common_runtime/eager/execute.cc:571] Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0 

tf.Tensor([4. 6.], shape=(2,), dtype=float32) 
```

## <a name="tensorflow-with-directml-samples-and-feedback"></a>Tensorflow mit directml-Beispielen und Feedback 

Nun können Sie mehr über das ml-Training erfahren. Sehen Sie sich die [tensorflow-Tutorials](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) oder [unsere Beispiele](https://github.com/microsoft/DirectML)an. Wir haben diesen Inhalt als Validierung für dieses erste Vorschau Paket von tensorflow mit directml verwendet. 

Wenn Sie Probleme haben oder Feedback zum tensorflow mit dem directml-Paket haben, stellen Sie eine [Verbindung mit unserem Team her](https://github.com/microsoft/DirectML/issues).
