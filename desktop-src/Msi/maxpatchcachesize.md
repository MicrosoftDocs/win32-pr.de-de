---
description: Wenn diese pro-Computer-System Richtlinie auf einen Wert größer als 0 festgelegt ist, speichert Windows Installer ältere Versionen von Dateien in einem Cache, wenn ein Patch auf eine Anwendung angewendet wird.
ms.assetid: 986cd521-6907-420d-a2e9-5e0da0069834
title: Maxpatchcachesize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8d9930f4a52d3ea0126a19d4dfadae359321f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485262"
---
# <a name="maxpatchcachesize"></a><span data-ttu-id="654f9-103">Maxpatchcachesize</span><span class="sxs-lookup"><span data-stu-id="654f9-103">MaxPatchCacheSize</span></span>

<span data-ttu-id="654f9-104">Wenn diese pro-Computer- [System Richtlinie](system-policy.md) auf einen Wert größer als 0 festgelegt ist, speichert Windows Installer ältere Versionen von Dateien in einem Cache, wenn ein Patch auf eine Anwendung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="654f9-104">If this per-machine [system policy](system-policy.md) is set to a value greater than 0, Windows Installer saves older versions of files in a cache when a patch is applied to an application.</span></span> <span data-ttu-id="654f9-105">Das Caching kann die Leistung zukünftiger Installationen erhöhen, die andernfalls die alten Dateien aus einer ursprünglichen Anwendungs Quelle abrufen müssen.</span><span class="sxs-lookup"><span data-stu-id="654f9-105">Caching can increase the performance of future installations that otherwise need to obtain the old files from a original application source.</span></span>

<span data-ttu-id="654f9-106">Der Wert der maxpatchcachesize-Richtlinie ist der maximale Prozentsatz des Speicherplatzes, den das Installationsprogramm für den Cache Alter Dateien verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="654f9-106">The value of the MaxPatchCacheSize policy is the maximum percentage of disk space that the installer can use for the cache of old files.</span></span> <span data-ttu-id="654f9-107">Der Wert 20 gibt z. b. an, dass nicht mehr als 20% verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="654f9-107">For example, a value of 20 specifies no more than 20% be used.</span></span> <span data-ttu-id="654f9-108">Wenn die Gesamtgröße des Caches den angegebenen Prozentsatz des Speicherplatzes erreicht, werden keine zusätzlichen Dateien im Cache gespeichert.</span><span class="sxs-lookup"><span data-stu-id="654f9-108">If the total size of the cache reaches the specified percentage of disk space, no additional files are saved to the cache.</span></span> <span data-ttu-id="654f9-109">Die Richtlinie wirkt sich nicht auf Dateien aus, die bereits gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="654f9-109">The policy does not affect files that have already been saved.</span></span>

<span data-ttu-id="654f9-110">Wenn der Wert der maxpatchcachesize-Richtlinie auf 0 festgelegt ist, werden keine weiteren Dateien gespeichert.</span><span class="sxs-lookup"><span data-stu-id="654f9-110">If the value of the MaxPatchCacheSize policy is set to 0, no additional files are saved.</span></span>

<span data-ttu-id="654f9-111">Wenn die maxpatchcachesize-Richtlinie nicht festgelegt ist, ist der Standardwert 10, und es können maximal 10% des Speicherplatzes zum Speichern alter Dateien verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="654f9-111">If the MaxPatchCacheSize policy is not set, the default value is 10 and a maximum of 10% of the disk space can be used to save old files.</span></span>

## <a name="registry-key"></a><span data-ttu-id="654f9-112">Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="654f9-112">Registry Key</span></span>

<span data-ttu-id="654f9-113">**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="654f9-113">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="654f9-114">Datentyp</span><span class="sxs-lookup"><span data-stu-id="654f9-114">Data Type</span></span>

<span data-ttu-id="654f9-115">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="654f9-115">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="654f9-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="654f9-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="654f9-117">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="654f9-117">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



