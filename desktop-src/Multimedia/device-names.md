---
title: Gerätenamen
description: Gerätenamen
ms.assetid: 0ba06439-cc33-43e1-a094-09bcc5e2f6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e516f7f8eed338067dc373f8509f46598e198c71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471765"
---
# <a name="device-names"></a><span data-ttu-id="092d5-103">Gerätenamen</span><span class="sxs-lookup"><span data-stu-id="092d5-103">Device Names</span></span>

<span data-ttu-id="092d5-104">Für jeden Gerätetyp gibt es möglicherweise mehrere MCI-Treiber, die den Befehlssatz gemeinsam nutzen, aber unterschiedlichen Datenformaten arbeiten.</span><span class="sxs-lookup"><span data-stu-id="092d5-104">For each device type, there might be several MCI drivers that share the command set but operate on different data formats.</span></span> <span data-ttu-id="092d5-105">Zum eindeutigen Identifizieren eines MCI-Treibers verwendet MCI *Gerätenamen*.</span><span class="sxs-lookup"><span data-stu-id="092d5-105">To uniquely identify an MCI driver, MCI uses *device names*.</span></span>

<span data-ttu-id="092d5-106">Gerätenamen werden entweder im \[ MCI- \] Abschnitt der SYSTEM.INI Datei oder im entsprechenden Teil der Registrierung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="092d5-106">Device names are identified either in the \[mci\] section of the SYSTEM.INI file or in the appropriate part of the registry.</span></span> <span data-ttu-id="092d5-107">Diese Informationen identifizieren alle MCI-Treiber für Windows.</span><span class="sxs-lookup"><span data-stu-id="092d5-107">This information identifies all MCI drivers to Windows.</span></span> <span data-ttu-id="092d5-108">Die Einträge im \[ MCI- \] Abschnitt verwenden die folgende Form:</span><span class="sxs-lookup"><span data-stu-id="092d5-108">The entries in the \[mci\] section use the following form:</span></span>

<span data-ttu-id="092d5-109">*Geräte \_ Namen*  =  *Treiber \_ Dateiname. Erweiterung*</span><span class="sxs-lookup"><span data-stu-id="092d5-109">*device\_name* = *driver\_filename.extension*</span></span>

<span data-ttu-id="092d5-110">Das folgende Beispiel zeigt einen typischen \[ MCI- \] Abschnitt aus SYSTEM.INI:</span><span class="sxs-lookup"><span data-stu-id="092d5-110">The following example shows a typical \[mci\] section from SYSTEM.INI:</span></span>


```C++
[mci]
cdaudio=mcicda.drv 
sequencer=mciseq.drv 
waveaudio=mciwave.drv 
avivideo=mciavi.drv
```



<span data-ttu-id="092d5-111">Wenn ein MCI-Treiber mit einem Gerätenamen installiert wird, der bereits in SYSTEM.INI oder der Registrierung vorhanden ist, fügt das System eine ganze Zahl an den Gerätenamen des neuen Treibers an und erstellt dabei einen eindeutigen Gerätenamen.</span><span class="sxs-lookup"><span data-stu-id="092d5-111">If an MCI driver is installed using a device name that already exists in SYSTEM.INI or the registry, the system appends an integer to the device name of the new driver, creating a unique device name.</span></span> <span data-ttu-id="092d5-112">Im vorherigen Beispiel würde ein zusätzlicher Treiber, der mit dem Gerätenamen "CDAudio" installiert wird, dem Gerätenamen "cdaudio1" zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="092d5-112">In the preceding example, an additional driver installed using the "cdaudio" device name would be assigned the device name "cdaudio1".</span></span>

 

 




