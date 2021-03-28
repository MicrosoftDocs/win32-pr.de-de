---
title: Gerätetreiber Informationen
description: Gerätetreiber und-Module sind insofern ähnlich, als beide auf PE-Dateien basieren.
ms.assetid: 4f4ec15b-5592-4fe3-b754-fda25ab24159
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0735e791b8c6e1fc7434decc7ac71ccb5c1c469e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036586"
---
# <a name="device-driver-information"></a><span data-ttu-id="e83fd-103">Gerätetreiber Informationen</span><span class="sxs-lookup"><span data-stu-id="e83fd-103">Device Driver Information</span></span>

<span data-ttu-id="e83fd-104">Gerätetreiber und-Module sind insofern ähnlich, als beide auf PE-Dateien basieren.</span><span class="sxs-lookup"><span data-stu-id="e83fd-104">Device drivers and modules are similar in that they are both based on PE files.</span></span> <span data-ttu-id="e83fd-105">Obwohl jeder Prozess über eine eigene private Liste geladener Module verfügt, verfügen Gerätetreiber über Module, die für das System Global sind.</span><span class="sxs-lookup"><span data-stu-id="e83fd-105">However, while each process has its own private list of loaded modules, device drivers have modules that are global to the system.</span></span> <span data-ttu-id="e83fd-106">Daher verfügt PSAPI über bestimmte Funktionen zum Abrufen der Liste der Gerätetreiber und ihrer Namen.</span><span class="sxs-lookup"><span data-stu-id="e83fd-106">Therefore, PSAPI has specific functions for obtaining the list of device drivers and their names.</span></span>

<span data-ttu-id="e83fd-107">Sie können die Lade Adresse für jeden Gerätetreiber abrufen, indem Sie die [**enumdevicedrivers**](/windows/desktop/api/Psapi/nf-psapi-enumdevicedrivers) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e83fd-107">You can retrieve the load address for each device driver by calling the [**EnumDeviceDrivers**](/windows/desktop/api/Psapi/nf-psapi-enumdevicedrivers) function.</span></span> <span data-ttu-id="e83fd-108">Diese Funktion füllt ein Array von **LPVOID** -Werten mit den Lade Adressen aller Gerätetreiber im System.</span><span class="sxs-lookup"><span data-stu-id="e83fd-108">This function fills an array of **LPVOID** values with the load addresses of all device drivers in the system.</span></span>

<span data-ttu-id="e83fd-109">Die [**getdevicedriverbasename**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverbasenamea) -Funktion nimmt eine Treiber Lade Adresse als Eingabe an und füllt einen Puffer mit dem Basisnamen des Treibers (z. b. Win32k.sys) aus.</span><span class="sxs-lookup"><span data-stu-id="e83fd-109">The [**GetDeviceDriverBaseName**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverbasenamea) function takes a driver load address as input and fills in a buffer with the base name of the driver (for example, Win32k.sys).</span></span> <span data-ttu-id="e83fd-110">Die zugehörige Funktion [**getdevicedriverfilename**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverfilenamea)übernimmt dieselben Parameter und gibt den Pfad zum Gerätetreiber zurück (z. b. C: \\ Windows \\ system32 \\Win32k.sys).</span><span class="sxs-lookup"><span data-stu-id="e83fd-110">A related function, [**GetDeviceDriverFileName**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverfilenamea), takes the same parameters and returns the path to the device driver (for example, C:\\Windows\\System32\\Win32k.sys).</span></span>

 

 




