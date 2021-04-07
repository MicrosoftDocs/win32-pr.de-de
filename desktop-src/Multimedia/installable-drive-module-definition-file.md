---
title: Installier bares Laufwerk Module-Definition Datei
description: Installier bares Laufwerk Module-Definition Datei
ms.assetid: d8d8d32e-18ac-47a5-a923-48b94b75e11d
keywords:
- installierbare Treiber, Modul Definitions Dateien
- installierbare Treiber, DEF-Dateien
- ninstallable Drivers, driverproc-Funktion
- Driverproc-Funktion
- Modul Definitions Dateien
- DEF-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 700931c91bfb3c17a36a1e3a1bbc4833097b4b38
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038879"
---
# <a name="installable-drive-module-definition-file"></a><span data-ttu-id="ecf51-109">Installier bares Laufwerk Module-Definition Datei</span><span class="sxs-lookup"><span data-stu-id="ecf51-109">Installable Drive Module-Definition File</span></span>

<span data-ttu-id="ecf51-110">Die Modul Definition (. DEF) die Datei eines installierbaren Treibers benennt den Treiber, exportiert die [driverproc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) -Funktion und definiert eine Treiber Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="ecf51-110">The module-definition (.DEF) file of an installable driver names the driver, exports the [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) function, and defines a driver description.</span></span> <span data-ttu-id="ecf51-111">Das folgende Beispiel zeigt eine typische Modul Definitionsdatei für einen installierbaren Treiber:</span><span class="sxs-lookup"><span data-stu-id="ecf51-111">The following example shows a typical module-definition file for an installable driver:</span></span>


```C++
LIBRARY OSCI 
DESCRIPTION 'FREQ,AMPL:Oscilloscope frequency and amplitude drivers.'
EXPORTS
    DriverProc
 
```



<span data-ttu-id="ecf51-112">Einige Installationsanwendungen können den Treiber öffnen und die Beschreibungs Zeile abrufen, die bei der Installation des Treibers verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ecf51-112">Some installation applications may open the driver and retrieve the description line to use when installing the driver.</span></span> <span data-ttu-id="ecf51-113">Um mit diesen Installationsanwendungen kompatibel zu bleiben, sollte die Beschreibungs Zeile folgendes Format aufweisen:</span><span class="sxs-lookup"><span data-stu-id="ecf51-113">To remain compatible with these installation applications, the description line should have this form:</span></span>

<span data-ttu-id="ecf51-114">**Beschreibungs**  *Alias* \[ ,*Alias* \] ... **:* \* \* Text*</span><span class="sxs-lookup"><span data-stu-id="ecf51-114">**DESCRIPTION**  *alias*\[,*alias*\]...\**:\*\*\*text*</span></span>

<span data-ttu-id="ecf51-115">Der *Alias* gibt einen eindeutigen Namen für den Treiber an, der von Anwendungen zum Öffnen des Treibers verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ecf51-115">The *alias* specifies a unique name for the driver that applications can use to open the driver.</span></span> <span data-ttu-id="ecf51-116">Der Alias fungiert auch als Wertname, der dem Treiber in der Registrierung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ecf51-116">The alias also serves as the value name associated with the driver in the registry.</span></span> <span data-ttu-id="ecf51-117">Mehrere Aliase werden durch Kommas getrennt.</span><span class="sxs-lookup"><span data-stu-id="ecf51-117">Multiple aliases are separated by commas.</span></span> <span data-ttu-id="ecf51-118">Der *Text* beschreibt den Zweck des Treibers.</span><span class="sxs-lookup"><span data-stu-id="ecf51-118">The *text* describes the purpose of the driver.</span></span>

 

 