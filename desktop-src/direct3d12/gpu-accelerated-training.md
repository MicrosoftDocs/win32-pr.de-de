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
# <a name="gpu-accelerated-ml-training"></a><span data-ttu-id="60dd7-103">GPU-beschleunigtes ml-Training</span><span class="sxs-lookup"><span data-stu-id="60dd7-103">GPU accelerated ML training</span></span>

![Grafik zu Windows ML](images/winml-graphic.png)

<span data-ttu-id="60dd7-105">In dieser Dokumentation wird beschrieben, was derzeit von der GPU Accelerated Machine Learning-Schulungs Vorschau (ml Accelerated Machine Learning, ml) für das [Windows-Subsystem für Linux](/windows/wsl/about) (WSL) und Native Windows unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="60dd7-105">This documentation covers what is currently supported by the GPU accelerated machine learning (ML) training preview for the [Windows Subsystem for Linux](/windows/wsl/about) (WSL) and native Windows.</span></span>  

<span data-ttu-id="60dd7-106">Diese Vorschau unterstützt sowohl professionelle als auch Anfänger Szenarien.</span><span class="sxs-lookup"><span data-stu-id="60dd7-106">This preview supports both professional and beginner scenarios.</span></span> <span data-ttu-id="60dd7-107">Unten finden Sie Verweise auf schrittweise Anleitungen zum Einrichten Ihres Systems in Abhängigkeit von Ihrem Know-how in ml, GPU-Anbieter und der Software Bibliothek, die Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="60dd7-107">Below you will find pointers to step-by-step guides on how to get your system setup depending on your level of expertise in ML, GPU vendor, and the software library you intend to use.</span></span> 

> [!NOTE]
> <span data-ttu-id="60dd7-108">Die folgenden Features befinden sich in der Vorschau Phase und unterliegen Änderungen.</span><span class="sxs-lookup"><span data-stu-id="60dd7-108">The following features are in preview, and are subject to change.</span></span>


## <a name="professionals"></a><span data-ttu-id="60dd7-109">Tätige</span><span class="sxs-lookup"><span data-stu-id="60dd7-109">Professionals</span></span>

<span data-ttu-id="60dd7-110">Wenn Sie ein professioneller Daten Analyst sind, der täglich eine native Linux-Umgebung für die Entwicklung und das Experimentieren mit einer internen Schleife verwendet und Sie über eine NVIDIA-GPU verfügen, empfiehlt es sich, die [NVIDIA CUDA Preview in WSL 2 einzurichten.](gpu-cuda-in-wsl.md)</span><span class="sxs-lookup"><span data-stu-id="60dd7-110">If you’re a professional data scientist that uses a native Linux environment day-to-day for inner-loop ML development and experimentation, and you have an NVIDIA GPU, we recommend setting up the [NVIDIA CUDA preview in WSL 2.](gpu-cuda-in-wsl.md)</span></span>

## <a name="students-and-beginners"></a><span data-ttu-id="60dd7-111">Studenten und Anfänger</span><span class="sxs-lookup"><span data-stu-id="60dd7-111">Students and beginners</span></span> 

<span data-ttu-id="60dd7-112">Wenn Sie ein Student oder ein Anfänger sind, der mit der Erstellung Ihres Wissens in den ml-Raum beginnt, empfiehlt es sich, das tensorflow mit dem directml-Back-End-Paket einzurichten.</span><span class="sxs-lookup"><span data-stu-id="60dd7-112">If you’re a student or beginner looking to start building your knowledge in the ML space, we recommend setting up the TensorFlow with DirectML backend package.</span></span> <span data-ttu-id="60dd7-113">Dieses Paket beschleunigt derzeit Workflows auf AMD-und Intel-GPUs.</span><span class="sxs-lookup"><span data-stu-id="60dd7-113">This package currently accelerates workflows on AMD and Intel GPUs.</span></span> <span data-ttu-id="60dd7-114">Die Unterstützung für NVIDIA-GPUs ist in Kürze verfügbar.</span><span class="sxs-lookup"><span data-stu-id="60dd7-114">Support for NVIDIA GPUs is coming soon.</span></span> 

<span data-ttu-id="60dd7-115">Wenn Sie mit einer nativen Linux-Umgebung vertraut sind, die mit ml-Workflows beginnt, empfiehlt es sich, das [tensorflow-Paket mit dem directml-Paket in WSL 2](gpu-tensorflow-wsl.md)zu starten.</span><span class="sxs-lookup"><span data-stu-id="60dd7-115">For those more familiar with a native Linux environment that are getting started with ML workflows, we recommend running the [TensorFlow with DirectML package inside WSL 2](gpu-tensorflow-wsl.md).</span></span> 

<span data-ttu-id="60dd7-116">Für diejenigen, die mit den ersten Schritten mit ml-Workflows vertraut sind, empfiehlt es sich, das [tensorflow-Paket mit dem directml-Paket in](gpu-tensorflow-windows.md)systemeigenen Fenstern einzurichten.</span><span class="sxs-lookup"><span data-stu-id="60dd7-116">For those more familiar with Windows that are getting started with ML workflows, we recommend setting up the [TensorFlow with DirectML package on native Windows](gpu-tensorflow-windows.md).</span></span> 

## <a name="next-steps"></a><span data-ttu-id="60dd7-117">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="60dd7-117">Next steps</span></span>

* <span data-ttu-id="60dd7-118">[Aktivieren Sie NVIDIA CUDA Preview in WSL 2](gpu-cuda-in-wsl.md).</span><span class="sxs-lookup"><span data-stu-id="60dd7-118">[Enable NVIDIA CUDA preview in WSL 2](gpu-cuda-in-wsl.md).</span></span>
* <span data-ttu-id="60dd7-119">[Aktivieren Sie tensorflow mit directml-Paket in WSL 2](gpu-tensorflow-wsl.md).</span><span class="sxs-lookup"><span data-stu-id="60dd7-119">[Enable TensorFlow with DirectML package inside WSL 2](gpu-tensorflow-wsl.md).</span></span>
* <span data-ttu-id="60dd7-120">[Aktivieren Sie tensorflow mit directml-Paket auf](gpu-tensorflow-windows.md)System eigenem Windows.</span><span class="sxs-lookup"><span data-stu-id="60dd7-120">[Enable TensorFlow with DirectML package on native Windows](gpu-tensorflow-windows.md).</span></span>