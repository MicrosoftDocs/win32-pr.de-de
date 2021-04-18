---
title: GPU-Beschleunigung in WSL
description: Direct Machine Learning (directml) ermöglicht GPU-accelleration im Windows-Subsystem für Linux.
ms.topic: article
ms.date: 06/17/2020
ms.openlocfilehash: 217a1763c0030a856e10a822cbd9f2642480c056
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338291"
---
# <a name="gpu-accelerated-ml-training"></a>GPU-beschleunigtes ml-Training

![Grafik zu Windows ML](images/winml-graphic.png)

In dieser Dokumentation wird beschrieben, was derzeit von der GPU Accelerated Machine Learning-Schulungs Vorschau (ml Accelerated Machine Learning, ml) für das [Windows-Subsystem für Linux](/windows/wsl/about) (WSL) und Native Windows unterstützt wird.  

Diese Vorschau unterstützt sowohl professionelle als auch Anfänger Szenarien. Unten finden Sie Verweise auf schrittweise Anleitungen zum Einrichten Ihres Systems in Abhängigkeit von Ihrem Know-how in ml, GPU-Anbieter und der Software Bibliothek, die Sie verwenden möchten. 

> [!NOTE]
> Die folgenden Features befinden sich in der Vorschau Phase und unterliegen Änderungen.


## <a name="professionals"></a>Tätige

Wenn Sie ein professioneller Daten Analyst sind, der täglich eine native Linux-Umgebung für die Entwicklung und das Experimentieren mit einer internen Schleife verwendet und Sie über eine NVIDIA-GPU verfügen, empfiehlt es sich, die [NVIDIA CUDA Preview in WSL 2 einzurichten.](gpu-cuda-in-wsl.md)

## <a name="students-and-beginners"></a>Studenten und Anfänger 

Wenn Sie ein Student oder ein Anfänger sind, der mit der Erstellung Ihres Wissens in den ml-Raum beginnt, empfiehlt es sich, das tensorflow mit dem directml-Back-End-Paket einzurichten. Dieses Paket beschleunigt derzeit Workflows auf AMD-und Intel-GPUs. Die Unterstützung für NVIDIA-GPUs ist in Kürze verfügbar. 

Wenn Sie mit einer nativen Linux-Umgebung vertraut sind, die mit ml-Workflows beginnt, empfiehlt es sich, das [tensorflow-Paket mit dem directml-Paket in WSL 2](gpu-tensorflow-wsl.md)zu starten. 

Für diejenigen, die mit den ersten Schritten mit ml-Workflows vertraut sind, empfiehlt es sich, das [tensorflow-Paket mit dem directml-Paket in](gpu-tensorflow-windows.md)systemeigenen Fenstern einzurichten. 

## <a name="next-steps"></a>Nächste Schritte

* [Aktivieren Sie NVIDIA CUDA Preview in WSL 2](gpu-cuda-in-wsl.md).
* [Aktivieren Sie tensorflow mit directml-Paket in WSL 2](gpu-tensorflow-wsl.md).
* [Aktivieren Sie tensorflow mit directml-Paket auf](gpu-tensorflow-windows.md)System eigenem Windows.