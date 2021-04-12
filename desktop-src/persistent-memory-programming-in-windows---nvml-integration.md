---
description: Die Technologie für persistente Speicher (PM) bietet Zugriff auf bytebene auf nicht flüchtige Medien und reduziert gleichzeitig die Latenz beim Speichern oder Abrufen von Daten.
ms.assetid: 68BF6074-09CB-4D6E-8BFD-FBA297391286
title: Persistente Speicher Programmierung in Windows-nvml-Integration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c9f033963a8fecded8943eb053781d05a78d568
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218111"
---
# <a name="persistent-memory-programming-in-windows---nvml-integration"></a><span data-ttu-id="2930b-103">Persistente Speicher Programmierung in Windows-nvml-Integration</span><span class="sxs-lookup"><span data-stu-id="2930b-103">Persistent Memory Programming in Windows - NVML Integration</span></span>

<span data-ttu-id="2930b-104">Die Technologie für persistente Speicher (PM) bietet Zugriff auf bytebene auf nicht flüchtige Medien und reduziert gleichzeitig die Latenz beim Speichern oder Abrufen von Daten.</span><span class="sxs-lookup"><span data-stu-id="2930b-104">Persistent memory (PM) technology provides byte-level access to non-volatile media while also reducing the latency of storing or retrieving data significantly.</span></span> <span data-ttu-id="2930b-105">Es wird eine neue Ebene zwischen dem Arbeitsspeicher des Systems und dem herkömmlichen Speicher erstellt.</span><span class="sxs-lookup"><span data-stu-id="2930b-105">It creates a new tier between a system’s memory and traditional storage.</span></span> <span data-ttu-id="2930b-106">Jedes Programm, das von einem persistenten Medium abhängig ist oder mit diesem skaliert werden kann, kann von pm profitieren.</span><span class="sxs-lookup"><span data-stu-id="2930b-106">Any program that is dependent on or scales with quick writes to a persistent medium can benefit from PM.</span></span>

<span data-ttu-id="2930b-107">In diesem Artikel wird erläutert, wie die nicht flüchtige Speicher Bibliothek (nvml) zur einfachen Verwendung in ein Visual Studio-Projekt integriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="2930b-107">The purpose of this article is to outline how the non-volatile memory library (NVML) can be integrated into a Visual Studio project for easy use.</span></span>

> [!Note]  
> <span data-ttu-id="2930b-108">Persistenter Speicher wird manchmal auch als Speicher Klassen Speicher (SCM) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="2930b-108">Persistent Memory is sometimes also referred to as Storage Class Memory (SCM).</span></span>

 

## <a name="pm-and-nvml"></a><span data-ttu-id="2930b-109">PM und nvml</span><span class="sxs-lookup"><span data-stu-id="2930b-109">PM and NVML</span></span>

<span data-ttu-id="2930b-110">Die erste Unterstützung für permanenten Speicher wurde in Windows Server 2016 und Windows 10 Anniversary Update (1607) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2930b-110">First support for persistent memory was introduced in Windows Server 2016 and the Windows 10 Anniversary Update (1607).</span></span> <span data-ttu-id="2930b-111">Eine kurze Übersicht finden Sie in den folgenden beiden channel9-Videos:</span><span class="sxs-lookup"><span data-stu-id="2930b-111">For a quick overview, check out these two Channel9 videos:</span></span>

-   <span data-ttu-id="2930b-112">[Using Non-volatile Memory (NVDIMM-N) as Block Storage in Windows Server 2016 (Verwenden von permanentem Speicher [NVDIMM-N] als Blockspeicher in Windows Server 2016)](https://channel9.msdn.com/Events/Build/2016/P466)</span><span class="sxs-lookup"><span data-stu-id="2930b-112">[Using Non-volatile Memory (NVDIMM-N) as Block Storage in Windows Server 2016](https://channel9.msdn.com/Events/Build/2016/P466)</span></span>
-   <span data-ttu-id="2930b-113">[Using Non-volatile Memory (NVDIMM-N) as Byte-Addressable Storage in Windows Server 2016 (Verwenden von permanentem Speicher [NVDIMM-N] als byteadressierbaren Speicher in Windows Server 2016)](https://channel9.msdn.com/Events/Build/2016/P470)</span><span class="sxs-lookup"><span data-stu-id="2930b-113">[Using Non-volatile Memory (NVDIMM-N) as Byte-Addressable Storage in Windows Server 2016](https://channel9.msdn.com/Events/Build/2016/P470)</span></span>

<span data-ttu-id="2930b-114">Damit Entwickler die Vorteile der persistenten Speicher Angebote nutzen können, hat Microsoft auch zu den Bemühungen beigetragen, die nicht flüchtige Speicher Bibliothek (nvml) in Windows zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2930b-114">To help developers take advantage of the benefits persistent memory offers, Microsoft has also contributed to the efforts of bringing the non-volatile memory library (NVML) to Windows.</span></span> <span data-ttu-id="2930b-115">Diese Bibliothek bietet verschiedene Tools, mit denen Anwendungen persistente Speicher fähig werden.</span><span class="sxs-lookup"><span data-stu-id="2930b-115">This library provides various tools to make applications persistent-memory aware.</span></span> <span data-ttu-id="2930b-116">Sie enthält z. b. Code, mit dem Sie problemlos einen PM-fähigen Schlüssel-Wert-Speicher für extrem schnelle Suche und Speicher erstellen können.</span><span class="sxs-lookup"><span data-stu-id="2930b-116">For example, it contains code that lets you easily create a PM-aware key-value store for extremely fast look-ups and stores.</span></span> <span data-ttu-id="2930b-117">Weitere Informationen zu nvml, einschließlich Beispielen, finden Sie in der [NVM-Bibliothek](https://pmem.io/nvml/).</span><span class="sxs-lookup"><span data-stu-id="2930b-117">You can find more information on NVML, including samples, at [NVM Library](https://pmem.io/nvml/).</span></span>

## <a name="integrating-nvml-into-a-visual-studio-project"></a><span data-ttu-id="2930b-118">Integrieren von nvml in ein Visual Studio-Projekt</span><span class="sxs-lookup"><span data-stu-id="2930b-118">Integrating NVML into a Visual Studio Project</span></span>

1. <span data-ttu-id="2930b-119">Herunterladen der nvml-Bibliotheksdateien und-Header</span><span class="sxs-lookup"><span data-stu-id="2930b-119">Download NVML library files and headers</span></span>

-   <span data-ttu-id="2930b-120">Nvml wird auf GitHub verwaltet.</span><span class="sxs-lookup"><span data-stu-id="2930b-120">NVML is maintained on GitHub.</span></span> <span data-ttu-id="2930b-121">Sie können entweder die Quelle selbst kompilieren oder nur kompilierte Binärdateien direkt von hier herunterladen: [nvml Version 1,2-Windows Technical Preview](https://github.com/pmem/pmdk/releases/tag/1.2%2Bwtp1).</span><span class="sxs-lookup"><span data-stu-id="2930b-121">You can either compile the source yourself, or just download compiled binaries directly from here: [NVML Version 1.2 - Windows Technical Preview](https://github.com/pmem/pmdk/releases/tag/1.2%2Bwtp1).</span></span>

2. <span data-ttu-id="2930b-122">Platzieren Sie die Bibliotheksdateien und Header in einem Verzeichnis Ihrer Wahl, z. b.: "c: \\ nvml \\ lib" und "c: \\ nvml \\ Inc".</span><span class="sxs-lookup"><span data-stu-id="2930b-122">Place the library files and headers in a directory of your choosing, for example: “C:\\NVML\\lib” and “C:\\NVML\\inc” respectively.</span></span>

3. <span data-ttu-id="2930b-123">Konfigurieren Sie das Projekt wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2930b-123">Configure your project as follows:</span></span>

-   <span data-ttu-id="2930b-124">Öffnen Sie das Visual Studio-Projekt, und klicken Sie in der Projektmappen-Explorer mit der rechten Maustaste auf den Namen Ihres Projekts.</span><span class="sxs-lookup"><span data-stu-id="2930b-124">Open your visual studio project and in the “Solution Explorer” right-click on your project’s name.</span></span>
-   <span data-ttu-id="2930b-125">Öffnen Sie den Einstellungsbereich des Projekts am unteren Rand des resultierenden Popup Fensters.</span><span class="sxs-lookup"><span data-stu-id="2930b-125">Open the project’s setting pane at the bottom of the resulting pop-up.</span></span>
-   <span data-ttu-id="2930b-126">Navigieren Sie zu "Konfigurations Eigenschaften-> C/C++", und fügen Sie den Ordner, in dem Sie den Header (C: \\ nvml \\ Inc) gespeichert haben, dem Feld "Zusätzliche Includeverzeichnisse" hinzu.</span><span class="sxs-lookup"><span data-stu-id="2930b-126">Navigate to “Configuration Properties -> C/C++” and add the folder in which you stored the header (C:\\NVML\\inc) to the “Additional Include Directories” field.</span></span>
-   <span data-ttu-id="2930b-127">Navigieren Sie als nächstes zu "Konfigurations Eigenschaften-> Linker", und fügen Sie den Ordner, in dem Sie die Bibliothek (C: \\ nvml \\ lib) gespeichert haben, in das Feld "zusätzliche Bibliotheks Verzeichnisse" ein.</span><span class="sxs-lookup"><span data-stu-id="2930b-127">Next, navigate to “Configuration Properties -> Linker” and add the folder in which you stored the library (C:\\NVML\\lib) to the “Additional Library Directories” field</span></span>

4. <span data-ttu-id="2930b-128">Stellen Sie als nächstes sicher, dass Sie das Projekt für Windows Server 2016 oder Windows 10 Anniversary Update als Ziel festlegen:</span><span class="sxs-lookup"><span data-stu-id="2930b-128">Next, make sure you target the project for Windows Server 2016 or Windows 10 Anniversary Update:</span></span>

-   <span data-ttu-id="2930b-129">Navigieren Sie zu "Konfigurations Eigenschaften-> Allgemein", und legen Sie das Feld "Ziel Platt Form Version" auf "10.0.14393.0" und</span><span class="sxs-lookup"><span data-stu-id="2930b-129">Navigate to “Configuration Properties -> General” and set the “Target Platform Version” field to “10.0.14393.0” and</span></span>
-   <span data-ttu-id="2930b-130">Navigieren Sie zu "Konfigurations Eigenschaften-> C/C++", und fügen Sie \_ \_ \_ dem Feld "Preprocessor" den Wert "ntddi Version = ntddi WIN10 RS1;" hinzu.</span><span class="sxs-lookup"><span data-stu-id="2930b-130">Navigate to “Configuration Properties -> C/C++” and add “NTDDI\_VERSION=NTDDI\_WIN10\_RS1;” to the “Preprocessor” field.</span></span>

5. <span data-ttu-id="2930b-131">Schließen Sie die Header in Ihren Code ein, und verknüpfen Sie die erforderlichen Bibliotheken.</span><span class="sxs-lookup"><span data-stu-id="2930b-131">Include the headers in your code and link to the required libraries</span></span>

-   <span data-ttu-id="2930b-132">An diesem Punkt können Sie einfach die Header Dateien, die Sie in Ihrem Code verwenden möchten, wie alle anderen Header Dateien einschließen.</span><span class="sxs-lookup"><span data-stu-id="2930b-132">At this point, you can simply include the header files you are looking to use in your code like any other header files.</span></span> <span data-ttu-id="2930b-133">Verwenden Sie beispielsweise, um libpmem zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="2930b-133">For example, to use libpmem:</span></span>
    -   <span data-ttu-id="2930b-134">Fügen Sie " \# include <libpmem. h>" und</span><span class="sxs-lookup"><span data-stu-id="2930b-134">add "\#include <libpmem.h>" and</span></span>
    -   <span data-ttu-id="2930b-135">Fügen Sie "libpmem. lib" zu "Konfigurations Eigenschaften-> Linker-> Eingabe > zusätzliche Abhängigkeiten" hinzu.</span><span class="sxs-lookup"><span data-stu-id="2930b-135">add "libpmem.lib" to "Configuration Properties -> Linker -> Input -> Additional Dependencies"</span></span>

<span data-ttu-id="2930b-136">An diesem Punkt können Sie die Funktionen der Bibliothek direkt im Code aufzurufen und Sie nutzen.</span><span class="sxs-lookup"><span data-stu-id="2930b-136">At this point you are ready to call the library’s functions directly in your code and take advantage of them.</span></span>

 

 



