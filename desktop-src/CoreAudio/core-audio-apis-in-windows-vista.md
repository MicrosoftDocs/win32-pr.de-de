---
description: Kernaudioapis
ms.assetid: 87ca9a31-1bc8-47ea-be00-40159d30e189
title: Kernaudioapis
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 83488233240121ba2edcfd677484df67a452e479
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2021
ms.locfileid: "106353780"
---
# <a name="core-audio-apis"></a><span data-ttu-id="1d54a-103">Kernaudioapis</span><span class="sxs-lookup"><span data-stu-id="1d54a-103">Core Audio APIs</span></span>

> [!NOTE]
> <span data-ttu-id="1d54a-104">Codebeispiele finden Sie unter [SDK-Beispiele, die die Kerndatei-APIs verwenden](/windows/win32/coreaudio/sdk-samples-that-use-the-core-audio-apis).</span><span class="sxs-lookup"><span data-stu-id="1d54a-104">For code examples, see [SDK samples that use the core audio APIs](/windows/win32/coreaudio/sdk-samples-that-use-the-core-audio-apis).</span></span>

<span data-ttu-id="1d54a-105">Diese Dokumentation enthält Informationen zu Kern-APIs (Application Programming Interface) der Microsoft Windows-Betriebssystem Familie.</span><span class="sxs-lookup"><span data-stu-id="1d54a-105">This documentation provides information about core audio application programming interfaces (APIs) for the Microsoft Windows family of operating systems.</span></span> <span data-ttu-id="1d54a-106">Es enthält Richtlinien für Softwareentwickler, die in der Entwicklung von Anwendungen, die die Kerncode-APIs in Windows Vista verwenden, befolgt werden.</span><span class="sxs-lookup"><span data-stu-id="1d54a-106">It provides guidelines for software developers to follow in developing applications that use the core audio APIs in Windows Vista.</span></span> <span data-ttu-id="1d54a-107">Diese APIs waren in Windows Vista neu und in früheren Versionen von Windows nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1d54a-107">These APIs were new in Windows Vista and are not available in earlier versions of Windows.</span></span>

<span data-ttu-id="1d54a-108">Mit den Kerncode-APIs können Audioanwendungen auf audioendpunktgeräte wie z. b. Kopfhörer und Mikrofon zugreifen.</span><span class="sxs-lookup"><span data-stu-id="1d54a-108">The core audio APIs provide the means for audio applications to access audio endpoint devices such as headphones and microphones.</span></span> <span data-ttu-id="1d54a-109">Die kernaudio-APIs dienen als Grundlage für Audio-APIs auf höherer Ebene, wie z. b. Microsoft DirectSound und die Windows Multimedia **wavexxx** -Funktionen.</span><span class="sxs-lookup"><span data-stu-id="1d54a-109">The core audio APIs serve as the foundation for higher-level audio APIs such as Microsoft DirectSound and the Windows multimedia **waveXxx** functions.</span></span> <span data-ttu-id="1d54a-110">Die meisten Anwendungen kommunizieren mit den APIs auf höherer Ebene, aber einige Anwendungen mit speziellen Anforderungen müssen möglicherweise direkt mit den Kerncode-APIs kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="1d54a-110">Most applications communicate with the higher-level APIs, but some applications with special requirements might need to communicate directly with the core audio APIs.</span></span>

<span data-ttu-id="1d54a-111">Ab Windows 7 wurden die vorhandenen APIs verbessert, und es wurden neue APIs hinzugefügt, um neue Szenarien zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="1d54a-111">Starting with Windows 7, the existing APIs have been improved and new APIs have been added to support new scenarios.</span></span> <span data-ttu-id="1d54a-112">Die Stream-und Sitzungsverwaltungs-APIs wurden verbessert, sodass die Anwendung jetzt die erweiterte Steuerung der Audiositzung aufzählen kann.</span><span class="sxs-lookup"><span data-stu-id="1d54a-112">The stream and session management APIs have been improved so that the application can now enumerate and get extended control over the audio session.</span></span> <span data-ttu-id="1d54a-113">Mithilfe der neuen APIs kann die Anwendung eine benutzerdefinierte Datenstrom Dämpfung implementieren.</span><span class="sxs-lookup"><span data-stu-id="1d54a-113">By using the new APIs, the application can implement a custom stream attenuation experience.</span></span> <span data-ttu-id="1d54a-114">Neue gerätebezogene APIs ermöglichen den Zugriff auf die Treiber Eigenschaften der Endpunkt Geräte.</span><span class="sxs-lookup"><span data-stu-id="1d54a-114">New device-related APIs provide access to the driver properties of the endpoint devices.</span></span>

<span data-ttu-id="1d54a-115">Diese Dokumentation enthält die folgenden Abschnitte.</span><span class="sxs-lookup"><span data-stu-id="1d54a-115">This documentation includes the following sections.</span></span>

| <span data-ttu-id="1d54a-116">`Section`</span><span class="sxs-lookup"><span data-stu-id="1d54a-116">Section</span></span>                                                                    | <span data-ttu-id="1d54a-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1d54a-117">Description</span></span>                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="1d54a-118">Informationen zu den Windows Core-audioapis</span><span class="sxs-lookup"><span data-stu-id="1d54a-118">About the Windows Core Audio APIs</span></span>](about-the-windows-core-audio-apis.md) | <span data-ttu-id="1d54a-119">Bietet eine Übersicht über die Windows Core-audioapis und beschreibt grundlegende Konzepte.</span><span class="sxs-lookup"><span data-stu-id="1d54a-119">Provides an overview of the Windows core audio APIs and describes basic concepts.</span></span> |
| [<span data-ttu-id="1d54a-120">Programmierhandbuch</span><span class="sxs-lookup"><span data-stu-id="1d54a-120">Programming Guide</span></span>](programming-guide.md)                                 | <span data-ttu-id="1d54a-121">Beschreibt die wichtigsten Features der kernaudioapis und deren Verwendung.</span><span class="sxs-lookup"><span data-stu-id="1d54a-121">Describes the key features of the core audio APIs and how to use them.</span></span>            |
| [<span data-ttu-id="1d54a-122">Programmierverzeichnis</span><span class="sxs-lookup"><span data-stu-id="1d54a-122">Programming Reference</span></span>](programming-reference.md)                         | <span data-ttu-id="1d54a-123">Bietet C++-Referenzinformationen für die Kerndatei-APIs.</span><span class="sxs-lookup"><span data-stu-id="1d54a-123">Provides C++ reference information for the core audio APIs.</span></span>                       |

## <a name="related-topics"></a><span data-ttu-id="1d54a-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1d54a-124">Related topics</span></span>

<span data-ttu-id="1d54a-125">[Medientechnologien für Windows](/previous-versions/bg125389(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="1d54a-125">[Media Technologies for Windows](/previous-versions/bg125389(v=msdn.10))</span></span>

[<span data-ttu-id="1d54a-126">SDK-Beispiele für die Verwendung der kernaudioapis</span><span class="sxs-lookup"><span data-stu-id="1d54a-126">SDK samples that use the core audio APIs</span></span>](/windows/win32/coreaudio/sdk-samples-that-use-the-core-audio-apis)
