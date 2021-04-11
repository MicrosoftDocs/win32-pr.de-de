---
title: Vorbereiten der Entwicklungsumgebung
description: Vorbereiten der Entwicklungsumgebung
ms.assetid: 5a3fd27e-ec8f-41eb-9d31-86d6d9f70862
ms.topic: article
ms.date: 10/03/2019
ms.openlocfilehash: ec42509ea81efce4bb17365d3bf08d36c2a4f415
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314931"
---
# <a name="prepare-your-development-environment"></a><span data-ttu-id="665b6-103">Vorbereiten der Entwicklungsumgebung</span><span class="sxs-lookup"><span data-stu-id="665b6-103">Prepare Your Development Environment</span></span>

<span data-ttu-id="665b6-104">Wenn Sie ein Windows-Programm in C oder C++ schreiben möchten, müssen Sie das Microsoft Windows Software Development Kit (SDK) oder Microsoft Visual Studio installieren.</span><span class="sxs-lookup"><span data-stu-id="665b6-104">To write a Windows program in C or C++, you must install the Microsoft Windows Software Development Kit (SDK) or Microsoft Visual Studio.</span></span> <span data-ttu-id="665b6-105">Die Windows SDK enthält die Header und Bibliotheken, die erforderlich sind, um Ihre Anwendung zu kompilieren und zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="665b6-105">The Windows SDK contains the headers and libraries necessary to compile and link your application.</span></span> <span data-ttu-id="665b6-106">Die Windows SDK enthält auch Befehlszeilen Tools zum Entwickeln von Windows-Anwendungen, einschließlich Visual C++ Compiler und Linker.</span><span class="sxs-lookup"><span data-stu-id="665b6-106">The Windows SDK also contains command-line tools for building Windows applications, including the Visual C++ compiler and linker.</span></span> <span data-ttu-id="665b6-107">Obwohl Sie Windows-Programme mit den Befehlszeilen Tools kompilieren und erstellen können, empfiehlt es sich, Microsoft Visual Studio zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="665b6-107">Although you can compile and build Windows programs with the command-line tools, we recommend using Microsoft Visual Studio.</span></span> <span data-ttu-id="665b6-108">Sie können einen kostenlosen Download von Visual Studio Community oder kostenlose Testversionen von Visual Studio [hier](https://visualstudio.microsoft.com/downloads/)herunterladen.</span><span class="sxs-lookup"><span data-stu-id="665b6-108">You can download a free download of Visual Studio Community or free trials of other versions of Visual Studio [here](https://visualstudio.microsoft.com/downloads/).</span></span>

<span data-ttu-id="665b6-109">Jede Version des Windows SDK ist für die aktuelle Version von Windows und für mehrere frühere Versionen vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="665b6-109">Each release of the Windows SDK targets the latest version of Windows as well as several previous versions.</span></span> <span data-ttu-id="665b6-110">In den Anmerkungen zu dieser Version werden die unterstützten Plattformen aufgeführt. Wenn Sie jedoch keine Anwendung für eine frühere Windows-Version verwalten, sollten Sie die neueste Version der Windows SDK installieren.</span><span class="sxs-lookup"><span data-stu-id="665b6-110">The release notes list the specific platforms that are supported, but unless you are maintaining an application for a very old version of Windows, you should install the latest release of the Windows SDK.</span></span> <span data-ttu-id="665b6-111">Sie können den neuesten Windows SDK [hier](https://developer.microsoft.com/windows/downloads/windows-10-sdk)herunterladen.</span><span class="sxs-lookup"><span data-stu-id="665b6-111">You can download the latest Windows SDK [here](https://developer.microsoft.com/windows/downloads/windows-10-sdk).</span></span>

<span data-ttu-id="665b6-112">Der Windows SDK unterstützt die Entwicklung von 32-Bit-und 64-Bit-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="665b6-112">The Windows SDK supports development of both 32-bit and 64-bit applications.</span></span> <span data-ttu-id="665b6-113">Die Windows-APIs sind so konzipiert, dass der gleiche Code ohne Änderungen für 32-Bit oder 64-Bit kompiliert werden kann.</span><span class="sxs-lookup"><span data-stu-id="665b6-113">The Windows APIs are designed so that the same code can compile for 32-bit or 64-bit without changes.</span></span>

> [!Note]  
> <span data-ttu-id="665b6-114">Der Windows SDK unterstützt die Entwicklung von Hardware Treibern nicht, und in dieser Serie wird die Treiberentwicklung nicht erörtert.</span><span class="sxs-lookup"><span data-stu-id="665b6-114">The Windows SDK does not support hardware driver development, and this series will not discuss driver development.</span></span> <span data-ttu-id="665b6-115">Informationen zum Schreiben eines Hardware Treibers finden Sie unter [Getting Started with Windows Drivers](/windows-hardware/drivers/gettingstarted/).</span><span class="sxs-lookup"><span data-stu-id="665b6-115">For information about writing a hardware driver, see [Getting Started with Windows Drivers](/windows-hardware/drivers/gettingstarted/).</span></span>

## <a name="next"></a><span data-ttu-id="665b6-116">Nächste</span><span class="sxs-lookup"><span data-stu-id="665b6-116">Next</span></span>

[<span data-ttu-id="665b6-117">Windows-Codierungs Konventionen</span><span class="sxs-lookup"><span data-stu-id="665b6-117">Windows Coding Conventions</span></span>](windows-coding-conventions.md)

## <a name="related-topics"></a><span data-ttu-id="665b6-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="665b6-118">Related topics</span></span>

* [<span data-ttu-id="665b6-119">Herunterladen von Visual Studio</span><span class="sxs-lookup"><span data-stu-id="665b6-119">Download Visual Studio</span></span>](https://visualstudio.microsoft.com/downloads/)
* [<span data-ttu-id="665b6-120">Download Windows SDK</span><span class="sxs-lookup"><span data-stu-id="665b6-120">Download Windows SDK</span></span>](https://developer.microsoft.com/windows/downloads/windows-10-sdk)