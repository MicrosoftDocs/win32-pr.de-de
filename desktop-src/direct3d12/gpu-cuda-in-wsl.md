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
# <a name="enable-nvidia-cuda-in-wsl-2"></a>Aktivieren von NVIDIA CUDA in WSL 2

Das Windows Insider SDK unterstützt die Ausführung vorhandener ml-Tools, Bibliotheken und beliebter Frameworks, die NVIDIA CUDA für die GPU-Hardwarebeschleunigung innerhalb einer WSL 2-Instanz verwenden. Dies umfasst pytorch und tensorflow sowie alle docker-und NVIDIA Container Toolkit-Unterstützung, die in einer nativen Linux-Umgebung verfügbar ist. 

> [!NOTE]
> Die folgenden Features sind in vorab Versionen von Windows 10 verfügbar und unterliegen Änderungen.

## <a name="install-the-latest-windows-insider-dev-channel-build"></a>Installieren Sie den neuesten Windows Insider dev-kanalbuild. 

Um diese Vorschauversion verwenden zu können, müssen Sie sich [für das Windows Insider-Programm registrieren](https://insider.windows.com/getting-started/#register). Befolgen Sie anschließend die folgenden [Instuktionen](https://insider.windows.com/getting-started/#install) , um den neuesten Insider-Build zu installieren. Wenn Sie Ihre Einstellungen auswählen, stellen Sie sicher, dass Sie den Entwicklungs [Kanal](/windows-insider/flight-hub/#active-development-builds-of-windows-10)auswählen. 

Für diese Vorschau benötigen Sie Build 20150 oder höher. Sie können die Buildversionsnummer überprüfen, indem Sie `winver` den Befehl " **Ausführen** " (Windows-Taste + R) ausführen.

## <a name="install-the-preview-gpu-driver"></a>Installieren des Vorschau-GPU-Treibers 

Herunterladen und Installieren des [NVIDIA CUDA-fähigen Treibers für WSL für](https://developer.nvidia.com/cuda/wsl) die Verwendung mit Ihren vorhandenen CUDA ml-Workflows. 

## <a name="set-up-wsl-2-for-the-preview"></a>Einrichten von WSL 2 für die Vorschauversion 

Nachdem Sie den obigen Treiber installiert haben, stellen Sie sicher, dass Sie [WSL 2 aktivieren](/windows/wsl/install-win10) und [eine auf glibc basierende Verteilung](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (z. b. Ubuntu oder Debian) installieren. Stellen Sie sicher, dass Sie über den neuesten Kernel verfügen, indem Sie im **Windows Update** Abschnitt der App "Einstellungen" auf " **Updates suchen" klicken** 

> [!NOTE]
> Stellen Sie sicher, **dass Sie Updates für andere Microsoft-Produkte erhalten, wenn Sie Windows aktiviert aktualisieren** . Sie finden ihn unter " **Erweiterte Optionen** " im Abschnitt " **Windows Update** " der App "Einstellungen". 

Für diese Vorschau benötigen Sie eine Kernel Version von 4.19.121 oder höher. Sie können die Versionsnummer überprüfen, indem Sie den folgenden Befehl in PowerShell ausführen. 

```powershell
wsl cat /proc/version
```

Nun können Sie Ihre vorhandenen Linux-Workflows über [NVIDIA docker](https://github.com/NVIDIA/nvidia-docker)oder durch die Installation von [pytorch](https://pytorch.org/get-started/locally/) oder [tensorflow](https://www.tensorflow.org/install/gpu) in WSL 2 verwenden. Weitere Informationen zum Einrichten von Informationen finden Sie im [Benutzerhandbuch zu NVIDIA-CUDA auf WSL](https://docs.nvidia.com/cuda/wsl-user-guide/index.html).

Teilen Sie uns Feedback zur NVIDIA-Unterstützung über das [Communityforum für CUDA auf WSL mit](https://forums.developer.nvidia.com/c/accelerated-computing/cuda/cuda-on-windows-subsystem-for-linux-wsl-2/303).
