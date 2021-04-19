---
description: In Windows Vista haben Leistungsindikatoren eine neue Architektur (Version 2,0) zum Bereitstellen von Indikator Daten implementiert.
ms.assetid: c17eda2f-3cf8-40d6-8be6-c1ce190d1a26
title: Bereitstellen von gegen Daten
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: ed5aa4cc505baab9e15d3f69c3fb466712eddbfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360538"
---
# <a name="providing-counter-data"></a><span data-ttu-id="e2275-103">Bereitstellen von gegen Daten</span><span class="sxs-lookup"><span data-stu-id="e2275-103">Providing Counter Data</span></span>

<span data-ttu-id="e2275-104">Software Komponenten, die Daten über Windows-Leistungsindikatoren veröffentlichen, werden als Leistungsdaten Anbieter bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e2275-104">Software components that publish data via Windows Performance Counters are called performance data providers.</span></span>

<span data-ttu-id="e2275-105">Windows unterstützt zwei Arten von Leistungsdaten Anbietern.</span><span class="sxs-lookup"><span data-stu-id="e2275-105">Windows supports two kinds of performance data providers.</span></span> <span data-ttu-id="e2275-106">Legacy-Leistungsdaten Anbieter (**v1-Anbieter**) werden mithilfe eines implementiert. INI-Datei und eine Leistungs-DLL.</span><span class="sxs-lookup"><span data-stu-id="e2275-106">Legacy performance data providers (**V1 providers**) are implemented using an .INI file and a performance DLL.</span></span> <span data-ttu-id="e2275-107">Moderne Leistungsdaten Anbieter (**v2-Anbieter**) verwenden. MAN (XML-Manifest) und die Leistungs Anbieter-APIs.</span><span class="sxs-lookup"><span data-stu-id="e2275-107">Modern performance data providers (**V2 providers**) use a .MAN (XML manifest) and the performance counter provider APIs.</span></span>

## <a name="manifests"></a><span data-ttu-id="e2275-108">Manifeste</span><span class="sxs-lookup"><span data-stu-id="e2275-108">Manifests</span></span>

<span data-ttu-id="e2275-109">Von modernen Leistungsdaten Anbietern wird ein verwendet. Man (XML-Manifest) zum Definieren der Leistungsdaten und zum Verwalten von Daten im Kontext des Anbieters.</span><span class="sxs-lookup"><span data-stu-id="e2275-109">Modern performance data providers use a .MAN (XML manifest) to define the counter data and use performance counter provider APIs to manage data within the context of the provider.</span></span>

<span data-ttu-id="e2275-110">Anbieter, die mit einem Manifest und Leistungs Anbieter-APIs implementiert werden, werden häufig als **v2-Anbieter** bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e2275-110">Providers implemented using a manifest and performance counter provider APIs are often called **V2 providers**.</span></span>

<span data-ttu-id="e2275-111">Windows unterstützt Benutzermodus v2-Anbieter unter Windows Vista oder höher.</span><span class="sxs-lookup"><span data-stu-id="e2275-111">Windows supports user-mode V2 providers on Windows Vista or later.</span></span> <span data-ttu-id="e2275-112">Details zum Benutzermodus finden Sie unter [Bereitstellen von Counter-Daten mit Version 2,0](providing-counter-data-using-version-2-0.md).</span><span class="sxs-lookup"><span data-stu-id="e2275-112">For user-mode details, see [Providing Counter Data Using Version 2.0](providing-counter-data-using-version-2-0.md).</span></span>

<span data-ttu-id="e2275-113">Windows unterstützt Kernel Modus-v2-Anbieter unter Windows 7 oder höher.</span><span class="sxs-lookup"><span data-stu-id="e2275-113">Windows supports kernel-mode V2 providers on Windows 7 or later.</span></span> <span data-ttu-id="e2275-114">Details zum Kernel Modus finden Sie unter [Kernel Mode Performance Monitoring](/windows-hardware/drivers/devtest/kernel-mode-performance-monitoring).</span><span class="sxs-lookup"><span data-stu-id="e2275-114">For kernel-mode details, see [Kernel Mode Performance Monitoring](/windows-hardware/drivers/devtest/kernel-mode-performance-monitoring).</span></span>

## <a name="performance-dll-deprecated"></a><span data-ttu-id="e2275-115">Leistungs-DLL (veraltet)</span><span class="sxs-lookup"><span data-stu-id="e2275-115">Performance DLL (deprecated)</span></span>

<span data-ttu-id="e2275-116">In der Legacy-Leistungs Leistungs Dienst-Architektur implementierten Anbieter eine Leistungs-DLL, die im Prozess des Consumers ausgeführt wurde, um die Leistungsdaten zu sammeln und bereitzustellen, als Sie von einem Consumer angefordert wurden.</span><span class="sxs-lookup"><span data-stu-id="e2275-116">In the legacy performance counter architecture, providers implemented a performance DLL to that ran in the consumer's process to collect and provide the counter data when a consumer requested it.</span></span> <span data-ttu-id="e2275-117">Der Anbieter hat eine Initialisierung verwendet (. INI) Datei-und Registrierungseinträge zum Definieren der Zähler und zum Konfigurieren der Leistungs-DLL.</span><span class="sxs-lookup"><span data-stu-id="e2275-117">The provider used an initialization (.INI) file and registry entries to define the counters and to configure the performance DLL.</span></span>

<span data-ttu-id="e2275-118">Anbieter, die mit einem implementiert werden. Die INI-Datei und eine Leistungs-DLL werden oft als **v1-Anbieter** bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e2275-118">Providers implemented using an .INI file and a performance DLL are often called **V1 providers**.</span></span>

> [!CAUTION]
> <span data-ttu-id="e2275-119">Obwohl Sie weiterhin eine Leistungs-DLL zur Bereitstellung von Leistungsdaten verwenden können, ist diese Architektur aufgrund erheblicher Leistungs-und Zuverlässigkeits Beschränkungen veraltet.</span><span class="sxs-lookup"><span data-stu-id="e2275-119">Although you can still use a performance DLL to provide counter data, this architecture is deprecated due to significant performance and reliability limitations.</span></span> <span data-ttu-id="e2275-120">Außerdem sind v1-Anbieter oft schwieriger zu implementieren, da Sie eine separate dll versenden müssen, die im Prozess des Consumers ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="e2275-120">In addition, V1 providers are often harder to implement since they require shipping a separate DLL that must run in the consumer's process.</span></span>

<span data-ttu-id="e2275-121">Weitere Informationen finden [Sie unter Bereitstellen von Leistungsdaten mithilfe einer Leistungs-DLL](providing-counter-data-using-a-performance-dll.md).</span><span class="sxs-lookup"><span data-stu-id="e2275-121">For details, see [Providing Counter Data Using a Performance DLL](providing-counter-data-using-a-performance-dll.md).</span></span>
